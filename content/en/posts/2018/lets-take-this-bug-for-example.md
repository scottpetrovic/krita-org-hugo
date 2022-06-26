---
title: "Let's take this bug, for example..."
date: "2018-09-18"
---

Krita's [2018 fund raiser is all about fixing bugs!](https://krita.org) And we're fixing bugs already. So, let's take a non-technical look at a bug Dmitry fixed yesterday. This is the bug: "[key sequence ctrl+w ambiguous with photoshop compatible bindings set](https://bugs.kde.org/show_bug.cgi?id=398729)" And [this is the fix.](https://phabricator.kde.org/R37:f2f2be209d8d40a5e7df97f6d259e14818355a4c)

So, we actually both started looking at the bug at the same time, me being Boudewijn. The issue is, if you use a custom keyboard shortcut scheme that includes a shortcut definition for "close current image", then a popup would show, saying that the shortcut is ambiguous:

[![](/images/posts/2018/ambiguous.png)](/images/posts/2018/ambiguous.png)

The popup doesn't tell where the ambiguous definition _is..._ Only that there is an ambiguous definition. Hm... Almost everything that does something in Krita that is triggered by a shortcut is an [_action._](http://doc.qt.io/qt-5/qaction.html) And deep down, Qt keeps track of all actions, and all shortcuts, but we cannot access that list.

So we went through Krita's source code. The action for closing an image was really created only once, inside Krita's code. And, another bug, Krita doesn't by default assign a shortcut to this action. The default shortcut should be CTRL+W on Linux and Windows, and COMMAND+W on macOS.

Curiously enough, the photoshop-compatible shortcut definitions did assign that shortcut. So, if you'd [select that scheme](https://docs.krita.org/en/reference_manual/preferences/shortcut_settings.html), a shortcut _would_ be set.

Even curiouser, if you don't select one of those profiles, so Krita doesn't set a shortcut, the default ctrl+w/command+w shortcut would _still work_.

Now, that can mean only one thing: Krita's close-image action is a dummy. It never gets used. Somewhere else, another close-image action is created, but that doesn't happen inside Krita.

So, Dmitry started digging into Qt's source code. Parts of Qt are rather old, and the module that makes it possible to show multiple subwindows inside a big window is part of that old code.

/\*!
    \\internal
\*/
void QMdiSubWindowPrivate::createSystemMenu()
{
...
    addToSystemMenu(CloseAction, QMdiSubWindow::tr("&Close"), SLOT(close()));
...
    actions\[CloseAction\]->setShortcuts(QKeySequence::Close);
....
}
#endif

Ah! That's where another action is created, and a shortcut allocated. Completely outside our control. This bug, which was reported only two days ago, must have been in Krita since version 2.9! So, what we do now is to make sure that the Krita's own close-image action's shortcut gets triggered. We do that by making sure Qt's action only can get triggered if the subwindow's menu is open.

    /\*\*
     \* Qt has a weirdness, it has hardcoded shortcuts added to an action
     \* in the window menu. We need to reset the shortcuts for that menu
     \* to nothing, otherwise the shortcuts cannot be made configurable.
     \*
     \* See: https://bugs.kde.org/show_bug.cgi?id=352205
     \*      https://bugs.kde.org/show_bug.cgi?id=375524
     \*      https://bugs.kde.org/show_bug.cgi?id=398729
     \*/
    QMdiSubWindow \*subWindow = d->mdiArea->currentSubWindow();
    if (subWindow) {
        QMenu \*menu = subWindow->systemMenu();
        if (menu) {
            Q_FOREACH (QAction \*action, menu->actions()) {
                action->setShortcut(QKeySequence());
            }
        }
    }

That means, for every subwindow we've got, we grab the menu. For every entry in the menu, we remove the shortcut. That means that our global Krita close-window shortcut always fires, and that people can select a different shortcut, if they want to.

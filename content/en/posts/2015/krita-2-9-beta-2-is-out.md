---
title: "Krita 2.9 Beta 2 is Out!"
date: "2015-01-15"
---

Everyone has been working their fingers to the bone to get Krita 2.9 in tip-top shape. For Beta 2, there was a large focus on squishing bugs, fixing crashes, as well as finding memory leaks. There are way too many changes to include everything in the release notes, so here are some highlights from the past month (as well as some fresh builds to get your hands on!)

[![krita_texture_bg](/images/posts/2015/krita_texture_bg-1024x564.jpg)](/images/posts/2015/krita_texture_bg.jpg)

(Krita 2.9 beta 2, with a textured window background. Illustrations by [David Revoy](http://www.patreon.com/davidrevoy)).

**Boudewijn Rempt**

- Fixes and improvements with how actions and shortcuts are managed. This will help fix a lot of shortcut conflicts that existed in the past. Actions and functionality are smarter now as well. This means that buttons and menu items will be disabled/enabled when they are not available. (eg. You cannot change the canvas size if there is no documents open).
- add drag and drop when there are no documents open
- make the background configurable with a color or image (located in Settings > Configure Krita)
- fixed a lot of multiple document bugs
- rename "hairy" brush engine to "bristle" brush engine
- add "flatten" action to layer context menu
- PDF export - landscape and portrait now work correctly
- initial tool when loaded is freehand brush
- don't show menu icons unless you are using KDE
- added a lot of presets for color profiles from Elle Stone
- fix handling of locked dockers behaves better when changing workspaces
- make it possible to convert images using 'krita --export bla.png --export-filename bla.jpg'
- fix crash when mergine a multi-selection of layers that includes a group layer
- Removed the selection brush; use the global selection mask and the regular brush tools instead
- Make krita open new images in the current window
- On Linux: use colord to get the system monitor profile, and make the system monitor profiles work in a multi-monitor setup
- Fix the layout of the filter and filter layer dialogs.
- Make it possible to use different OpenColorIO settings for each canvas
- Improve startup speed on all platforms

**Jouni Pentikainen**

- Mirror axis tools now follow the rotation of the canvas
- fix rotation in brush preview

**Wolthera van Hövell tot Westerflier**

- fixed loading assistants
- fixed toggling of painting assistants
- improve how the color slider widget is used
- resource bundle fixes with paint operations, loading tags, and double loading resources
- prevent loading corrupt resource bundles (added MD5 Checksums)
- fix lockup with perspective assistants
- improve the color smudge brush engine so it doesn't darken too much
- lots of fixes for working with resource bundles

**Sven Langkamp**

-  bug fixes when selecting shapes
- fixed some computer systems that weren't loading preset bundles correctly
- fixed color selector crashes when no document open
- fix switching between landscape and portrait orientation
- lots of fixes with handling multiple open images and the dockers

**Lukas Tvrdy (G'MIC)**

- update gmic to version 1.6.0.3
- enable interactive filters like [colorize \[interactive\]](http://www.davidrevoy.com/article240/gmic-line-art-colorization)
- implement progress reporting when applying filter
- if gmic script fails, inform user about the error message
- fixed lost filtering when you select filter and click ok

**Dmitry Kazakov**

- fixed a bunch of multi-document specific issues
- fixes when selecting colors with the advanced color selector
- brush sizes are back to having 2 decimals to prevent issues
- fixed a few bugs related to the crop tool with properties and resetting
- fixed saving split alpha mask
- fixed a lot of bugs in the dirty presets feature
- fixed mirror tool working with shapes like circles and rectangles
- fix shaky lines on 32-bit systems when using canvas rotation
- fixes to the cage transform tool
- Improve handles for the transform tool
- fixes to the opacity slider
- fixes to the tablet handling (make working with vector shapes with the tablet possible again)
- make the liquify tool handle build-up/wash mode properly

**Timothee Giet**

- new color smudge presets

**Stefano Bonicatti**

- Fix a bunch memory leaks and double deletions
- Fix crash when adding drop shadow effect
- Fix crash when closing a document while moving the stylus
- Fix the opengl canvas for some (notably AMD drivers). More fixes coming up!

**Scott Petrovic (UI)**

- updated layout for resource manager
- mirror tools have updated UI
- G'MIC has been moved to filters in the menu
- Resource manager has moved to settings
- "Size Canvas to Size of Current Layer" is renamed to "Trim to Current Layer" and "Size Canvas to Size of Selection" is renamed to "Trim to Selection"

 **André Wöbbeking**

- Lots of warnings fixed that only show up with clang, quite a few of which unconvered real bugs.

**Friedrich W. H. Kossebau**

- Fix thumbnailing for .kra and .ora files

 **Rishabh Saxena**

- Add a shortcut to toggle the assistants on and off

**Thorsten Zachmann**

- Fix pasting text in a multi-line text shape

**Downloads**

There are still  [222 bugs](https://bugs.kde.org/buglist.cgi?bug_severity=critical&bug_severity=grave&bug_severity=major&bug_severity=crash&bug_severity=normal&bug_severity=minor&bug_status=UNCONFIRMED&bug_status=CONFIRMED&bug_status=ASSIGNED&bug_status=REOPENED&list_id=1167792&product=krita&query_format=advanced) at the moment, but quite a lot are rather minor. Lots and lots and lots of thanks to all the beta testers who have been sending in report after report!

For Linux users, [Krita Lime](https://launchpad.net/~dimula73/+archive/ubuntu/krita) has been updated. Remember that launchpad is very strict about the versions of Ubuntu it supports. So the update is only available for 14.04 and up.

OpenSUSE users can use the new OBS repositories created by Leinir:

- [http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_13.1/](http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_13.1/)
- [http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_13.2/](http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_13.2/)
- [http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_Factory/](http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_Factory/)

Windows users can choose between an installer and the zip file. You can unzip the zip file anywhere and start Krita by executing bin/krita.exe. The Surface Pro 3 tablet offset issue has been fixed! We only have 64 bits Windows builds at the moment, we’re working on fixing a problem with the 32 bits build.

- [http://files.kde.org/krita/windows/krita_x64_2.8.91.0.zip](http://files.kde.org/krita/windows/krita_x64_2.8.91.0.zip)
- [http://files.kde.org/krita/windows/krita_x64_2.8.91.0.msi](http://files.kde.org/krita/windows/krita_x64_2.8.91.0.msi)

OSX users can open the dmg and copy krita.app where they want. Note that OSX still is _not_ supported. There are OSX-specific bugs and some features are missing.

- [http://files.kde.org/krita/osx/krita-2.8.91.1.dmg](http://files.kde.org/krita/osx/krita-2.8.91.1.dmg)

There will be a third beta, and afterwards -- the release!

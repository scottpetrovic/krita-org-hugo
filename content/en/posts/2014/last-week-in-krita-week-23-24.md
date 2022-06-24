---
title: "Last week in Krita — week 23 & 24"
date: "2014-06-18"
---

Even with the effort of designing, launching and running the kickstarterwe haven’t stopped developing!

In the last two weeks, besides the coding work on the git repositories, Boudewijn has made available a hefty number of testing builds for the windows community. This builds brings up the latest novelties and features developed in the master branch. Note, however, not all feature sets are finished and it is not recommended for production use. [Get the bleeding edge build](http://forum.kde.org/viewtopic.php?f=281&t=121434&start=15#p313091)

In other development: The community is slowly building a new site for Krita. Planning and designing has been done mainly through the forums. Still in the early stages of develop, which consists of mock ups and concept designs, the project is shaping up for a brilliant future for this website. [Join the forums!](http://forum.kde.org/viewforum.php?f=136) and take part in the community!

It’s time to review this last two weeks commited hard work.

## This week’s new features:

This was a busy period, Boudewijn worked pretty hard to improve the file saving dialog behavior. This is much more difficult than it sounds since every system uses a different file open/save dialog each one working slightly different, because of the differences the implementation needs to take into account how each one asks and gives back data. The changes should make the dialog behave as expected on all systems.

Dmitry in particular, aside from the many bugs fixed, enhanced the stroke smoothing options adding a scaling factor to the weight option. This allows the weighted smoothing to behave exactly the same at different zoom levels.

### New features:

- Improvements to the clone tool. (Boudewijn Rempt)
- Scalable Distance option in Weighted Smoothing. (Dmitry Kazakov)
- Make it possible to zoom in all resource selectors, like brushes, presets, gradients (Sven Langkamp)
- Make the grabbing area for Transform Tool handles twice lager than the handles themselves. (Dmitry Kazakov)
- Add image sizes and textures for games. (Boudewijn Rempt and Paul Geraskin)
- Restore the new view action to the view menu. (Boudewijn Rempt)
- Add Y + mouse click + movement shortcut for Exposure correction. (Dmitry Kazakov)
- Add shortcuts to switch between painting blending modes. (Boudewijn Rempt)

![Gamma and exposure new cursors](/images/posts/2014/w23-gamma_exp-cursor.jpg)

## General bugfixes and features

- FIX [#334933](https://bugs.kde.org/show_bug.cgi?id=334933): Make the grabbing area for Transform Tool handles twice lager than the handles themselves. (Dmitry Kazakov)
- FIX [#335834](https://bugs.kde.org/show_bug.cgi?id=335834): Added a Scalable Distance option to Weighted Smoothing. (Dmitry Kazakov)
- FIX [#335647](https://bugs.kde.org/show_bug.cgi?id=335647): Fix painting checkers on openGL mode. (Dmitry Kazakov)
- FIX [#335649](https://bugs.kde.org/show_bug.cgi?id=335649): Fix hiding the brush outline when the cursor is outside the canvas. (Dmitry Kazakov)
- FIX [#335660](https://bugs.kde.org/show_bug.cgi?id=335660): Use flake/always as activation id for a Krita tools. (Sven Langkamp)
- FIX [#335746](https://bugs.kde.org/show_bug.cgi?id=335746): Floating message block input under Gnome. (Boudewijn Rempt)
- FIX [#335745](https://bugs.kde.org/show_bug.cgi?id=335745): Hide Pseudo Infinite canvas decoration when in Wraparound mode. (Dmitry Kazakov)
- FIX [#335670](https://bugs.kde.org/show_bug.cgi?id=335670): Artistic Color Selector lightstrip display non working when floating. (Boudewijn Rempt)
- FIX [#331358](https://bugs.kde.org/show_bug.cgi?id=331358): Fix artifacts when rotation stylus sensor is activated. (Dmitry Kazakov)
- FIX [#332773](https://bugs.kde.org/show_bug.cgi?id=332773): Add option to disable touch capabilities of the Wacom tablets on canvas only mode. To activate, in kritarc, please add disableTouchOnCanvas=true. (Dmitry Kazakov)
- FIX [#335048](https://bugs.kde.org/show_bug.cgi?id=335048): Rename stable category to Brush engines. (Sven Langkamp)
- Created new cursors for Exposure/Gamma gestures. (David Revoy)
- Fix "Move layer into group" icon design. (Timothée Giet)
- Fix file dialog filter types and use native dialogs when possible. (Boudewijn Rempt)
- Tweak mirror axes display and default position of move handles. (Arjen Hiemstra)

### Clone tool improvements

Clone tool has change now makes it possible to clone from one layer to a different one. This works as follows:

- \[CTRL + CLICK\] FIRST Time: Define source layer and source area to clone. You can change layer after this to clone to a different layer
- \[CTRL + CLICK\]: Adjusts, changes source coordinates. Note that source clone layer remains the same.
- \[CTRL + ALT + CLICK\]: Change source layer and source area to clone.

### Layer blending modes shortcuts

Following [Photoshop default shortcuts for blending modes](http://helpx.adobe.com/en/photoshop/using/default-keyboard-shortcuts.html#keys_for_blending_modes) developers added the same shortcuts to Krita for painting blending modes. this is awesome as there is no loose in focus during painting sessions just to change brush blending mode.

To promote the use of the new added shortcuts here is a list for you. [![Painting blending mode shortcuts](/images/posts/2014/w23-blend-short-med_web.jpg)](/images/posts/2014/w23-blending-shortcuts_768.jpg)

### File dialogs

File dialogs were reworked to work and behave as the user expects, Boudewijn worked amongst other things to ensure dialogs remember the last used directory and to ensure the correct format output on any system. It’s no longer necessary to select the desired format from the list, it’s enough to write the extension after naming the file for Krita to know exactly what format you want to save the file to. Many other enhancements and tweaks were also necessary to make it possible to work with native dialogs on the main systems: KDE, GNOME and Windows.

## krita gemini and sketch

Krita Gemini and Krita sketch received much love to make it run smoothly and consistent in all systems, most changes were in the underlying code to optimize and prepare the code for better development. Some changes to note:

- Use the desktop dialog for opening images from the welcome screen. (Arjen Hiemstra)
- Fix colouring of the layer controls and tweak them to look good. (Arjen Hiemstra)
- Properly disable warnings about floating messages. (Arjen Hiemstra)
- Add duplicate/clear layer buttons to the Layer panel. (Arjen Hiemstra)
- Add a clear and clone method to LayerModel. (Arjen Hiemstra)
- Enable floating messages for Gemini and disable them properly for sketch. (Arjen Hiemstra)
- Fix the save page and reduce the number of errors/warnings. (Arjen Hiemstra)

## Code optimization and cleanup

The ever going process of optimization continues with a huge amount of developer commits. The process might not look like much when reading the git logs, but renaming, moving and getting rid of old naming schemes, paves the way for bigger changes. I couldn’t list them all as I list all else since you will probably get bored, but let’s just say they did a lot of housekeeping this past two weeks.

## Kickstarter

We're over 50% funded now for the basic goal of having Dmitry another work for six months on Krita. But it's time to put in some sprinting to get to the stretch goals! Help Krita by spreading the word:

[![](/images/posts/2014/kickstarter-29-front-ban.png)](http://krita.org/kickstarter.php)

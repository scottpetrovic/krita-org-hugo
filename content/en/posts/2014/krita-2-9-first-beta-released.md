---
title: "Krita 2.9: First Beta Released!"
date: "2014-12-14"
categories: 
  - "development-builds"
tags: 
  - "krita-2-9"
---

Last week, the first preparations for the next Krita release started with the creation of the first Krita 2.9 beta release: Krita 2.9 Beta 1. This means that we've stopped adding new features to the codebase, and are now focusing on making Krita 2.9 as stable as possible.

We've come a long way since March, when we released Krita 2.8! Thanks to the enthusiastic support of many, many users, here and on kickstarter, Krita 2.9 has a huge set of cool new features, improvements and refinements.

Here's a short list to wet your appetite -- a full intro to all new features will be presented when we present the final 2.9 release. That's expected to happen in January, by the way.

- Interface:
    
    - Krita can now open more than one image in a singe window, and the same image in more than one window. You can choose between sub windows and tabs in the preferences.
    
    - You can now organize the favorite presets in the pop-up palette using tags.
    - You can also increase the amount of brushes available in the pop-up palette at a time in preferences.
    - You can select more than one layer at a time and delete, move or drag and drop them in the layer docker.
    - New options for the cursor, including one to show a dot at the center of the brush outline.
    - The thumbnails for resources like brushes, gradients or patterns are resizable by using ctrl+scrollwheel over them.
    - Editing gradients have been improved.
    - You can now choose between giving the first layer a default color and giving the image a non-transparent background.
    - You can create palette files inside Krita.
    - The compositions docker stores the collapsed state, you can update compositions and control which compositions you export.
    - A new type of gradients: selection-shape based gradients was added.
- Layers, Selections and Masks
    - A new mask type was added: non-destructive transformation masks.
    - Many new ways to convert between layers and masks.
    - The rendering of vector graphics at various image resolution settings was fixed.
    - It's now possible to edit the alpha channel separately.
    - You can split a layer into several layers, one for each color on the layer, which is useful together with G'Mic's recolorize\[comics\] feature for coloring artwork.
    - You can isolate a layer by using the shortcut alt-select.
    - You can edit selections directly as if it were a black and white image.
- Brushes and painting:
    - The anti-aliasing quality of thin lines has been improved greatly.
    - The smudge brush was improved.
    - The Flow option has finally been separated from opacity.
    - Steps in the undo history can now be merged.
    - The brush preset system was extended to make it possible to keep changes to a certain preset during a session, instead of resetting to the original preset on every brush preset switch.
    - You can lock the size of the brush when switching between paint and erase mode, or have a separate size for each mode.
    - New painting assistants for working with vanishing points and rulers.
    - the line tool will use all sensors now! Rotation, speed, tilt, etc.
    - There's a sticky key available for accessing the straight line tool from the freehand brush (V).
    - a delayed-stroke based stabilizer option was added for stroke smoothing
    - the weighted smoothing and stabilizer have a 'delay' option now, which allows you to create a dead area around your cursor for extra sharp corners.
    - a scalable distance option was added to the weighted stroke smoothing, so now the weight is relative to the zoom.
- The transform tool has been enormously extended:
    - Perspective transformation was added
    - Liquify transformation was added
    - Cage transformation was added (and is super-fast, too)
    - Selecting multiple nodes in the cage and warp tools is now possible. You can resize, rotate and move a whole section at once.
- Color selectors:
    - A new color selector with accurate sliders, for every color model, was added
    - HSY' and HSI color models are supported in both the new slider docker, the MyPaint shade selector, and the advanced color selector. You can even customise the weights for the HSY' calculation.
    - All color selectors are now color managed, and also work when you paint in HDR mode.
    - You can paint in HDR mode now, with the LUT docker and OCIO.
    - There are sticky keys for gamma and exposure with HDR painting.
- Filters:
    - The G'Mic plugin (controls filters) was updated to the latest version of G'Mic. On-canvas and miniature preview was added.
    - A posterize filter was added.
    - Index-colors filter was added, which is very useful in the HD-pixel art painting technique.
- Files:
    - Some improvements to the PSD import/export filter: resource blocks are round-tripped, all but four PSD blending modes are now supported, Krita can now load some CS6 PSD files, PSD layer groups are loaded, support for 16 bit multi-layer files is improved, Krita vector layers are saved (as raster layers) to PSD.
    - The OpenEXR filter can now load and save single-channel grayscale EXR files, and was fixed for loading images with very small alpha values, and images with zero alpha but non-zero color values
    - Support for raw
    - Saving 16 bit grayscale images to tiff, jpeg and ppm now works
    - support for r16 and r8 heightmap files were added

Missing in 2.9 are Photoshop layer styles and PSD layer masks: we're working hard on those, but they aren't done yet. All the scaffolding is done, and most of the drop shadow effect, except the integration, is in the rendering process... We're working to have them ready by the end of January. The animation tool has been disabled for refactoring. In Beta 1, Sketch and Gemini have been disabled.

### Downloads

There are still  [234 bugs](https://bugs.kde.org/buglist.cgi?bug_severity=critical&bug_severity=grave&bug_severity=major&bug_severity=crash&bug_severity=normal&bug_severity=minor&bug_status=UNCONFIRMED&bug_status=CONFIRMED&bug_status=ASSIGNED&bug_status=REOPENED&list_id=1167792&product=krita&query_format=advanced) at the moment, some of which might cause dataloss, so users are recommended to use the beta builds for testing, not for critical work!

For Linux users, Krita Lime will be updated on Monday. Remember that launchpad is very strict about the versions of Ubuntu it supports. So the update is only available for 14.04 and up.

OpenSUSE users can use the new OBS repositories created by Leinir:

- [http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_13.1/](http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_13.1/)
- [http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_13.2/](http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_13.2/)
- [http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_Factory/](http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_Factory/)

Windows users can choose between an installer and the zip file. You can unzip the zip file anywhere and start Krita by executing bin/krita.exe. The Surface Pro 3 tablet offset issue has been fixed! We only have 64 bits Windows builds at the moment, we're working on fixing a problem with the 32 bits build.

- [http://files.kde.org/krita/windows/krita_x64_2.8.90.1.zip](http://files.kde.org/krita/windows/krita_x64_2.8.90.1.zip)
- [http://files.kde.org/krita/windows/krita_x64_2.8.90.1.msi](http://files.kde.org/krita/windows/krita_x64_2.8.90.1.msi)

OSX users can open the dmg and copy krita.app where they want. Note that OSX still is _not_ supported. There are OSX-specific bugs and some features are missing.

- [http://files.kde.org/krita/osx/krita-2.8.80.1.dmg](http://files.kde.org/krita/osx/krita-2.8.80.1.dmg)

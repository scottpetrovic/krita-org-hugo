---
title: "New Features in Krita 2.4"
date: "2011-09-14"
---

Krita had about 1400 commits during the 2.4 development lifecycle which took about eight months. Of course, there's lots of cool work which likely won't be in 2.4, but in a later release, like Matus Talcik's opencl filter plugin or Torio Mishi's animation plugin.

Here's a non-exhaustive list of significant changes:

- new colorengine plugin that uses lcms2: this is preferred for performance and stability reasons and we urge all distributions to compile krita against lcms2.(Cyrille Berger and Boudewijn Rempt)
- a history docker showing the undo/redo history (Matus Talcik)
- the filter api has been refactored to make it easier to create new filter plugins (Cyrille Berger and Dmitry Kazakov)
- MyPaint brush engine support (experimental, will probably not be in the final release) (Sven Langkamp)
- New color sources (pattern, gradient, random) for brushes (Cyrille Berger, Silvio Heinrich)
- improved convolution filters (Jose Luis Vergara)
- new smudge+paint brush engine (Silvio Heinrich)
- make krita work much better with large images (Boudewijn Rempt)
- New blending modes (Arcus Tangent, Gamma Light, Gamma Dark, Geometric Mean, Vivid Light, Pin Light, Grain Merge", "Grain Extract", "Hard Mix", "Copy Red/Green/Blue/Opacy", Additive-Substractive, improved divide, Soft Light, Hard Light, Atop, HSY, HSV, HSL, HSI, dissolve and Overlay) (Silvio Heinrich)
- made the burnd, dodge and color burn blend modes compatible with Photoshop (Silvio Heinrich)
- create an experimental multihand-tool which allows the user to paint with several brushes at the same time (Lukas Tvrdy)
- add a workspaces features: you can save named configurations of dockers for different purposes (Sven Langkamp)
- add symmetry, mirror and translate mode for painting (Lukas Tvrdy)
- add a channel selection docker (Sven Langkamp)
- add new sensors and make it possible to influence a brush parameter with more than one sensor (like pressure, random, tilt and so on) (Cyrille Berger)
- improve canvas rotation (Silvio Heinrich)
- Fix embedding of icc profile data in JPG and PNG files (Cyrille Berger)
- Fix brush preset data when editing a .kpp brush preset file in Krita (Cyrille Berger)
- Add support for DNG and Panasonic RAW2 raw image files (Cyrille Berger, Sven Langkamp)
- Make it possible to select different layers in different views (Sven Langkamp)
- Improve the tiles backend to make projection updating faster (Dmitry Kazakov)
- Improve scaling gui when using the transform tool (Marc Pegon)
- Improve handling of layerbox when using a tablet (Dmitry Kazakov and Jose Luis Vergara)
- Add an opacity setting to brush presets
- Improve smoothing of the freehand tool (Geoffry Song)
- Make it possible to remove painting assistants (Geoffry Song)
- New feature: split an image in a set of rectangles (Srikanth Tiyyagura)
- Make painting obey channel locks
- Improve compatibility with GIMP's XCF file format (import only) (Silvio Heinrich, Lukas Tvrdy)
- Improve painting speed with the default autobrush (Geoffry Song)
- the sketch brush no supports density, line width and offset scale sensors.
- Integrate Get Hot New Stuff with Krita's resource management for brushes, presets, patterns and gradients (Srikanth Tiyyagura)
- Add hexadecimal input to the specific color selector (Sven Langkamp)
- Load blending modes defined in OpenRaster (Boudewijn Rempt)
- Make it possible to load single-layer PSD images (may not be in the 2.4 release) (Siddharth Sharma)
- Add opacity, size and flow sliders to the toolbar (Sven Langkamp and Silvio Heinrich)
- The line tool now supports pressure and tilt (Lukas Tvrdy)
- Add keyboard shortcut for changing luminosity of the active color (darker: K, lighter: L) (Lukas Tvrdy)
- Configurable "Show just the canvas" mode (Boudewijn Rempt)
- Improved selected color preview in the advanced color selector (Adam Celarek)
- Add simple support for BMP, GIF, XPM and XBM formats. (Boudewijn Rempt)
- Add preset management to the preset editor popup (Jose Luis Vergara)
- Improve the preset editor in many ways (Sven Langkamp, Jose Luis Vergara, Silvio Heinrich, Cyrille Berger, Lukas Tvrdy)
- Fix margins in export to PDF (Sven Langkamp)
- Add a "save incremental" option which saves your work with an auto-incrementing suffix (Jose Luis Vergara)
- Use brush presets in the right-click popup palette (Sven Langkamp)
- Add Nepomuk and GIMP-xml-based tagging to all Krita resources (Srikanth Tiyyagura)
- Make it possible to disable and enable the on-canvas preview of filters (Sven Langkamp)
- Make it possible to add a new ICC profile from Krita instead of copying it to certain directories (Boudewijn Rempt)
- Fix a problem where switching tools would make Krita, especially selecting colors, slower and slower (Boudewijn Rempt)
- Smooth out the canvas zooming in non-opengl mode (Boudewijn Rempt)
- New mode for the Text brush: it now can spray the letters of the text, one letter per dab.    (Lukas Tvrdy)
- New feature: the Image Docker, which makes it easy to create and browse sets of reference images (Silvio Heinrich)
- New color selector based on the color wheel. Picking the three color dimensions (hue, saturation, lightness) separated from each other with this color selector should be more convenient. (Silvio Heinrich)
- Implement drag & drop between Krita and other applications, like Dolphin, Gimp, Gwenview, Firefox and so on, and more advanded drag & drop between instances of Krita. (Boudewijn Rempt)
- New Text Tool: this places the text tool that creates artistic text vector objecs where users who come from Photoshop expect it. (Sven Langkamp)
- Improve brush outline mode (Sven Langkamp)
- Add a splash screen to Krita (Boudewijn Rempt)
- Make it possible to add, remove and hide resources (Srikanth Tiyyagura)
- New implementation for the curve brush with curvy, recurvy and smooth effects (Lukas Tvrdy)
- Add taskset docker (Sven Langkamp)

Uncategorized, unsorted -- just showing you what we've been doing to make your life with Krita better!

---
title: "Krita 2.8 Beta 2 Released"
date: "2014-01-18"
---

This week, we made a lot of progress on the road towards the 2.8 release of Krita, which is expected around the end of this month. There are still a number of bugs that we really want to address, of course, but Krita is getting very polished and stable now!

![](/images/posts/2014/krita-28b2.png)

Important changes since the first beta, released in December are:

- 19 crash fixes
- Lovely new splash screen by Tyson Tan
- The fill tool uses 75% less memory
- The color palettes have been updated refined
- New icon for the magic wand/contiguous selection tool
- Support for non-zero fill rule in the experiment brush (thanks to David Gowers)
- New icons by Jens Reuterberg, David Revoy and Vasco Basque
- Fix Krita Gemini to find the QML files correctly on Linux
- Improved out-of-memory handling
- Fix the cursor when pressing CTRL to pick colors
- Fix the cursor outline when hovering
- Don't show an error when the autosave fails because the user is still painting
- When pressing backspace/shift backspace to fill a whole layer with the foreground or background color, disregard the global opacity setting
- Don't show garbage on the canvas when moving a rotated canvas around when OpenGL is disabled
- Synchronize the color selectors with each other
- New, more precise cursors by David Revoy
- Fix calculation of the shape's insets when it has Miter joining
- Fix the initial size of the window
- Fix the color smudge brush in dulling mode
- Fix double cropping of the image when using the infinite-canvas feature
- Make the text tool create a vector layer
- Correctly initialize the mouse-pressure feature for the hairy brush
- Save the Color As Mask setting to brush presets
- Fix saving a single layer image where the layer is larger than the image
- Fix the pixelize filter
- Improve the desaturate filter and add two new types of desaturation
- Many fixes to the shade selector
- Show the selection outline when loading a selection from file
- Fix the high quality scaling on some ATI cards. Patch by Paul Geraskin.
- Fix performance issues caused by the overview docker
- Updated brush presets
- Fix the transform tool to not process locked layers
- Make the crop tool handle the shift modifier to lock the aspect ratio
- Add Qt plugins to load ORA and KRA files. This allows these file types to be shown in the reference images docker
- Smoother thumbnails for KRA files
- Many fixes to tablet and stylus handling and add preliminary support for evdev-based tablets
- Fix the Lut docker to use the right OCIO display
- Fix the COPY blending mode to handle the alpha channel correctly
- Fix loading hatching brush presets
- Fix the scaling and reloading of file-backed layers
- Fix the channel docker getting confused when converting the image a new colorspace
- Add a third brush option slider to the toolbar
- Show newly created tags in the context menus for adding tags
- Fix a deadlock when editing nodes. Thanks to Anton Saraev for the patch!
- When opening the favourites palette with a keyboard shortcut, show it under the cursor position
- Fix saving and loading the color-dodge blending mode in ORA files
- Added a menu entry to open the file manager in the resources folder
- Fix the autbrush size calculation

For Windows, there are new builds:

- [http://heap.kogmbh.net/downloads/krita\_x86\_2.7.9.5.msi](http://heap.kogmbh.net/downloads/krita_x86_2.7.9.5.msi)
- [http://heap.kogmbh.net/downloads/krita\_x64\_2.7.9.5.msi](http://heap.kogmbh.net/downloads/krita_x64_2.7.9.5.msi)

A build for Windows XP will follow.

Especially on Windows, we have many important improvements:

- The x64 build now installs by default into the right folder
- If the x86 version is started on a 64 bits windows a warning is displayed
- The installer now allows custom install locations
- The swapper now works on Windows, which means that crashes due to being out-of-memory shouldn't happen anymore
- The X86 build is much more stable -- there was an interesting problem there with our memory management. We allowed 50% of the main memory of the system to be used for tiles. However, 32 bits Windows has a 2GB limit per process. If you've got 4GB of memory in your system, Krita would use the full 2GB for tiles, leaving no memory for the rest of Krita.
- Fix the size and position of the window correctly
- Fix the mapping of tablet buttons

There are some known regressions that will be fixed before the final release

- On Intel GPU's with OpenGL enabled, canvas-only mode only works if you disable hiding the titlebar
- Using the color-to-alpha filter when painting is broken

Upcoming fixes include improved gaussian blur and unsharp mask filters.

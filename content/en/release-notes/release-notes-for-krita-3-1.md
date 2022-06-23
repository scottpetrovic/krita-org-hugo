---
title: "Release Notes for Krita 3.1"
date: "2016-10-03"
---

# Release Notes for Krita 3.1

A quick video overview of all of the major features and fixes that are being shaipped with Krita 3.1.

{{< youtube 0eHNll7lPKk >}}

### Full Support for OSX

![krita_texture_bg](/images/pages/krita3osx.jpg)

Julian Thijssen's Google Summer of code project for 2016 gives us the power to run openGL on OSX! This was the biggest blocker for full OSX support! OpenGL is a special type of code that allows us to use your graphics card for operations like rotating, zooming and panning the canvas. Graphics cards are typically super good at this, meaning it makes the canvas really fast, no matter what kind of image you have before you. Apple devices are super picky about which version of OpenGL they can run, so Julian had to rewrite a part of QT to upgrade it all to openGL 3, ensuring our OSX users can finally enjoy Krita without bizare glitches when navigating!

### Render Animation

\[video width="720" height="571" mp4="https://krita.org/wp-content/uploads/2016/10/animation-challenge.mp4"\]\[/video\]

Finally, you can now export your animations to the following animation formats: animated GIF, MP4, MKV, OGG, giving a range of small sized files for your favourite blogging site to high quality formats to show off on your favourite video sharing site! This requires the ffmpeg library. [See instructions on on how to set this up here](https://docs.krita.org/Render_Animation)!

### Animation Curves and Opacity

![krita_texture_bg](/images/pages/krita_animation_3_0_2.gif)

Jouni Pentikäinen Google Summer of code project has been merged as well! Its biggest feature is the ground work laid for automated tweening of properties. There is now a animation curves docker to allow making opacity tweens, and we hope to allow transformation mask tweens in the future! [Documentation here.](https://docs.krita.org/Animation_Curves) But that is not all! Other raster like layers like filter layers, fill layers, transparency masks and filter masks can now have their raster content animated, allowing for raster animating transparency or a filter effect! Furthermore, you can now color code frames, which can be used to mark the most important frames in an animation, so you can find them back more easily.

### New Internal Color Picker

![krita_texture_bg](/images/pages/16-bit-color.png)

Thanks to Wolthera's Google Summer of Code work, Krita now has a new internal color selector for selecting wide-gamut values! This means that you can finally break free from the limited gamut of your screen(sRGB) and use wide gamut spaces. Other features include easy access to the palette and the ability to type in HDR values in floating space without any extra toggles and buttons. You can access this new dialog from the current color patch in the toolbar. Furthermore, the pop-up palette will also grant access to this new selector, if you enable it by adding the popuppalette/usevisualcolorselector=true line to the kritarc configuration file. The other color selector dockers are untouched for now, but hopefully they'll be able to be extended in the same way soon!

### New Quick Brush Engine

<iframe src="https://www.youtube.com/embed/Ao7-aEcwoN0" width="560" height="315" frameborder="0" allowfullscreen="allowfullscreen"></iframe>

In the ever continuing quest for speed on big documents, we developed the quick brush engine! One of the ways how a brush engine can be super slow is due to all the extra options available. Removing those and changing the way how we calculate brushes, gives a sharp edged, extremely simple but super fast brush that doesn't require openGL 3.1 but can tackle high resolution canvases with ease! [See documentation...](https://docs.krita.org/Quick_Brush)

### Stop-Based Gradient Editor

![krita_texture_bg](/images/pages/stop-based-gradients.png)

Sven Langkamp brought us a secret suprise in the form of a stop-based gradient editor! Krita's segment based gradient editor is based on Gimp's model, but the stopbased format is far more common and easier to understand! [See the docs on how to use it.](https://docs.krita.org/Managing_Gradients)

### Lazy Brush/Colorize Mask

The lazy/brush colorize mask feature is technically complete, but it's too slow to be useful in practice. We need a different algorithm... But if you want to play with it, you can enable it by adding the following line to your kritarc configuration file:

**disableColorizeMaskFeature=false**

### Other New Features

- Create a stroke around your selection (https://docs.krita.org/Stroke\_Selection)
- Halftone filter added. Find it in the main menu: Filters > Artistic.
- add a new Eraser Switch Opacity feature, similar to the Eraser Switch Size one.
- new layer from visible option in layer menu
- OSX: add quicklook plugin
- Added support for loading Scribus XML palettes.

### Fixes/Changes

- Fixed loading the templates
- brush resize slow-down fixed
- fixes when creating and saving custom shortcuts
- Fixes with stabilizer including finishing line segments and bent lines
- Auto-saving while working is more stable. Fixed race condition while saving.
- Do not install the majority of extra ICC profiles. This helps Krita's startup speed a lot
- fix transform handles from resizing while doing transforms (349666)
- All shortcuts can be configurable now before a document is open
- Fix for a crash when saving a document after adding a text shape
- ORA: convert the projection for the mergedimage when necessary
- History docker right-click options have been moved to a button since right-clicking wasn't working
- Escape key gets out of of picking a color on the screen
- fix crash when copying an animation keyframe to frame zero
- Fix exporting images on the command line
- OCIO: fix filling in values if a config is loaded
- BUG: 372171 Save show-in-timeline not depending on the animated status of the layer
- fix crash when moving filter masks
- added a "demo" brush tag
- removed a help button that didn't do anything in the preferences
- Disable transform tool on vector layers. This cannot be done and created issues
- fix crash is second window with a view into the first window is closed
- fix crash when creating a new document
- Fill painter tool can now fill 8-bit color on a 16-bit device
- Updated the transform tool options icons
- BUG:372110 Fix hiding Tool Options widgets when a new window is created
- fix crash when filter layer needs to create a LAB color space for filtering (368648)
- fix potential memory leak in the popup action
- fix crash when using the filter brush
- Show a message box when saving fails because the target directory does not exist
- Prevent rulers from flashing on and off with a new document
- BUG:372545 Fix isotropic spacing when working on a mirrored canvas
- BUG: 372171 - Mark image as modified when the user changes frame rate or animation range
- BUG:373205 Disable the quick-group actions if the active node is a mask
- assistants combobox is now ordered by name
- BUG: 373077 Select the mimetype of split images by default to the mimetype of the current image
- BUG:372613 Fix the out-of-gamut warning color configuration
- BUG:373342 Correctly save the visibility of a vector layer
- CCBUG:373077 Image split: show error dialogs only once
- fix potential crash when using the scratchpad
- BUG:373267 Always save the merged image as 8 bit sRGB, no profile. This improves the compatibility with other applications
- Remove tags assocated with bundles when needed
- disabled the spriter plugin for now as it is having issues
- Fix layout of monitor profiles by using a QFormLayout
- D3525: Fix floating point Lab color space values
- BUG:373334 Fix installing proifles with complex filenames
- Splash screen loading progress text is more accurate
- fix regression when using the hatching and sketch brush engines
- fix crash with LUT docker not managing pointers well (368764)
- fix sobel filter to display correctly
- BUG:372893 Fix painting of the sliderspinbox
- BUG:366289, 369451 - Fix Tilt-elevation to work with rotated/mirrored canvas
- Disabled the big brother plugin
- fix clone brush from copy/paste error
- fixed isue with the brush editor not updating correctly (T3578)
- fix crash using "Create Copy from Current Image" (351106)
- fix clipping issue with auto brush (367804)
- UI fix for the transform tool options
- Updated zoom menu icons
- fix potential crash when closing the window
- unify colors on all SVG icons
- fix drag and drop crash with clone layer (20405)
- fix memory leak when Cumulative undo is turned on (365992)
- fix tablet no pressure bug when closing the brush editor (369114)
- fix crash when changing the canvas type while showing the pop up palette
- fixed saving thumbnails when auto-saving
- Don't crash when using split layer in another language
- PgUp/PgDown fix when moving around layer masks
- fixed brush property Color: Mix doesnt work right with the default colorspace in 16 Bits (369882)

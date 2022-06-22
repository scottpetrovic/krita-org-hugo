---
title: "Krita 4.2 Release Notes"
date: "2018-08-22"
---

# Krita 4.2 Release Notes

Krita 4.2 has been [released on May 29th, 2019](/item/krita-4-2-0-is-out/). While the core team focused on stability and performance, this release also includes many new features and the performance work and the work on handling palettes done during the 2018 Google Summer of Code. Join us for the ride!

{{< youtube ZbnQn6h5q0g >}}

## Updated Tablet Support for Windows, Linux and macOS

We finally managed to bring together the code we wrote for supporting tablets on Windows (both Wintab as Windows Ink), Linux and macOS with the existing code in our development platform, Qt. This has improved support for multi-monitor setups, more tablets are supported and a host of bugs with tablets have been resolved. This was a huge amount of work!

**Note: we needed to patch Qt to make all of this work. [The patches have been upstreamed](https://phabricator.kde.org/T10838) but might not yet be integrated by your linux distribution. Until that happens, you might need to use the Linux AppImage instead of Krita as built by your distribution.**

## HDR Painting

{{< youtube Uy_22vFu1R0 >}}

HDR Animation created in Krita by Agata Cacko

{{< youtube V_0ocw1H3vs >}}

Krita at CES2019

Krita has been able to work with HDR images since 2005, but it's now possible to view your HDR image in HDR, on supported hardware. You can now not only save your HDR image in .kra or OpenEXR files, but also extended PNG. With the right version of FFMPEG you can even create animations in HDR! Having the correct computer setup for this can be rather complicated, so head to the documentation to see what is involved. _HDR display is only available on Windows 10_. If you have HDR enabled, the Small Color Selector Docker has an extra "nits" slider that allows you to change the brightness of a specfic color.

- Feature - [https://docs.krita.org/en/reference\_manual/hdr\_display.html](https://docs.krita.org/en/reference_manual/hdr_display.html)
- Background Knowledge - [https://docs.krita.org/en/general\_concepts/colors/scene\_linear\_painting.html](https://docs.krita.org/en/general_concepts/colors/scene_linear_painting.html)

![](/images/pages/intel-logo.png) This work was possible through cooperating with Intel. The work also involved helping these HDR changes get pushed into the development framework Krita uses, Qt. This can allow other applications to take advantange of these features.

## Improved brush speed performance with vectorization and lock-free programming

![](/images/pages/avx_cgauss_60.gif)

![](/images/pages/lockless.png)

Two of our 2018 Google Summer of Code students sped up Krita with programming techniques called lock-free hashmap for managing the pixel data (Andrey Kamakin) and GPU vectorization  (Ivan Yossi). The lock-free hashmap should improve Krita's speed with multithreading, the chart shows the performance gains based off your CPU core count. Vectorization for the Gaussian and Soft-brush tips optimizes Krita by taking advantage of your processor's ability to do similar calculations really quickly, the gif above showing the speed difference for the gaussian brush tip.

The left axis on the graph is time in milliseconds. You can see the painting operations go from 1.5 seconds down to about 1 second with the lock-free hashmap. The blue line shows how Krita previously worked.

## Improved Color Palette Docker

![](/images/pages/color-palette-improvements.png) An improved color palette from one of our Google Summer of Code students for 2018 -- Michael Zhou. It is more stable as well as some of the following changes:

1. Instead of an entry-based docker, a rows and column based docker.
2. It can hold empty entries, which is useful for organizing.
3. Stable drag and dropping of colors.
4. Easy adding in entries by clicking them in the docker.
5. Right-clicking removes an entry.
6. Palettes can be put into the KRA file.
7. You can press the folder icon to open a palette editing dialog where you can set a palette to be stored in the document or resource-folder.

## Animation Python API

{{< youtube VsYGtPXgJIg >}}

Control and create customized workflows that deal with animations.

- Move to a specific frame
- Set the frame rate
- Set start and end frame playback length

A couple plugins have already been created that are using some of these functions. There was also another fix to the Node/Layer API where the "scaleNode" call was passing the wrong parameter

**Animator Video Reference and importer** - [https://github.com/scottpetrovic/animator-video-reference](https://github.com/scottpetrovic/animator-video-reference) **Sprite Sheet manager** - [https://github.com/Falano/kritaSpritesheetManager](https://github.com/Falano/kritaSpritesheetManager)

## Configure File backups

![](/images/pages/4-2-file-backup-options.png) Options to control how your backups are done. You can even control if you want your backup files to be stored in a different location. These settings are found in the "Configure Krita" main menu under the General section.

If you have very large files and are have issues saving, you can enable the Zip64 options.

## Color Gamut Masking

![](/images/pages/4-2-gamut-mask.png)

A new color gamut docker where you can limit your colors shown. New contributor Anna Medonosova has added this. This feature is available with the artistic color selector and the circle advanced color docker displays. Note: The default triangle selector doesn't allow this feature.

You can also rotate the gamut mask by using the slider. Create new masks and edit existing ones through the Gamut Mask docker. You can disable the mask with the selector icon at the top as shown to the left of the rotation slider.

## News about Krita

![](/images/pages/news-widget-splash-screen-2.png) A news widget has been added to the startup screen that allows Krita to fetch the latest news coming from krita.org. Now, if there's something interesting, like a new release, you'll be in the front row! Clicking on a news item will take you to the web page. This is off by default, so you will need to turn it on. Special thanks goes out to Alvin Wong on getting the OpenSSL library included to make this work.

## Improved Artistic Color Selector

![](/images/pages/improved-artistic-color-selector.png) More options and cleaned up Artistic Color Selector. There is now a "continuous mode" (infinity symbol) that allows you to remove the stepping with certain attributes. Additional options for new gamut masking. Anna Medonosova has added this great feature.

## Undo operations with move tool

![](/images/pages/undo-move-feature.gif) Move tool operations are now part part of the undo history. This means you can undo multiple moves in a row while you are using the move tool.

## Move and transform selections

{{< youtube gWv--Do9L0E >}}

Easily move, rotate, or transform the selection by itself. You can even edit the anchor points with how the selection is made to do things like rounding corners.

## Improve display of memory usage

![](/images/pages/image.png) Give a better indication when your computer is running out of memory. This can be useful as well when making an animation and you won't have enough memory to actually render it. This bar already exists in the status bar, but should help warn people better.

## Overview Docker improvements

![](/images/pages/4-2-rotate-flip.png) Rotate and mirror canvas quickly from the docker. The Overview docker now also better preserves the aspect ratio and doesn't stretch when some layers are hidden.

## Resize layer thumbnails

\[video width="344" height="502" mp4="https://krita.org/wp-content/uploads/2018/08/resize-thumbnail.mp4"\]\[/video\]

There is a new slider on the layers docker that allows you to resize the layer thumbnails to see them larger. The size is saved for when you return back to Krita the next time.

## Multibrush improvements

![](/images/pages/4-2-multi-brush-preview.png) Better preview when showing multiple axes.

There is also a new "Copy Translate" mode. This allows you to specify multiple cursors on the screen to paint or draw with at the same time. This is accessed and used through the Tool options like the other modes.

## Painting mask performance improvement

\[video width="1378" height="825" webm="https://krita.org/wp-content/uploads/2019/05/painting\_selection\_mask.webm"\]\[/video\]

You can create a selection with your normal brushes using the Global Selection option. This has previously been a slow area until now. They are now significantly faster. A small workflow change was made as well. If you show the Global Selection mask with no selection, everything will be selected by default.

## Improvement to Select Opaque

\[video width="1378" height="825" webm="https://krita.org/wp-content/uploads/2019/05/select\_opque\_improvements.webm"\]\[/video\]

Ctrl + clicking a layer's thumbnail in the layer docker makes a selection of the layers content. This is the same as the right click option Select Opaque. There are also new methods for making layer selections. "Select Opaque" has been renamed to "Select Opaque (replace)" now to account for the new functions.

- Ctrl+click = replace selection
- Ctrl+shift+click = add selection
- Ctrl+alt+click = subtract selection
- Ctrl+shift+alt+click = intersect selection

## Sharpness Changes

[![](/images/pages/sharpness_in_motion.gif)](https://krita.org/wp-content/uploads/2019/05/sharpness_in_motion.gif)

The sharpness option, which sets a threshold filter on the current brushtip now allows controlling this threshold with pressure, making it easy to create bristle like brushes from any with the pixel brush.

## Flow/Opacity Changes

[![](/images/pages/flow_opacity_adapt_flow_preset.gif)](https://krita.org/wp-content/uploads/2019/05/flow_opacity_adapt_flow_preset.gif)

Flow and Opacity now interact more like in other programs. The above gif shows how to adapt a brush which uses the new behaviour to go back to the old behaviour. The new behaviour should make it a lot easier to make delicate strokes. For now you can still go back to using the old behaviour globally by going to Configure Krita → General → Tools → Flow Mode

## Clone Brush - Reset Origin

\[video width="1000" height="640" webm="https://krita.org/wp-content/uploads/2019/05/clone\_brush-v2.webm"\]\[/video\]

A new option was added to the clone brush that allows you to reset the origin after every brush stroke.

## Simplex Noise Generator

\[video width="1000" height="640" webm="https://krita.org/wp-content/uploads/2019/05/fill\_simplex\_noise.webm"\]\[/video\]

Add ability to dynamically add noise to your document. There are also options to make the noise tileable.

## New Blend modes

\[video width="480" height="720" webm="https://krita.org/wp-content/uploads/2019/05/blend\_modes.webm"\]\[/video\]

New categories of the blend modes were added to create interesting effects.

## Other Changes and bug fixes

- Fix: Allow changing layer name to set document as modified (bug 380437)
- Fix: Allow undoing when changing layer names ([bug 380437](https://bugs.kde.org/show_bug.cgi?id=380437))
- Fix: Update the undo limit if we change it
- Fix: Handling of modified document notification in sub-window mode ([bug 386488](https://bugs.kde.org/show_bug.cgi?id=386488))
- Fix: Fix when holding right-click over layer's color settings ([bug 392815](https://bugs.kde.org/show_bug.cgi?id=392815))
- Fix: Do not show language switch warning when going back to the default ([bug 362961](https://bugs.kde.org/show_bug.cgi?id=362961))
- Fix: Gradient map color mapping issues ([bug 388976](https://bugs.kde.org/show_bug.cgi?id=388976))
- Fix: Layout improvements and showing levels for histogram filter ([bug 376048](https://bugs.kde.org/show_bug.cgi?id=376048))
- Improvement: Add warning when adding shape to clone layer ([bug 406730](https://bugs.kde.org/show_bug.cgi?id=406730))
- Usability: Make default background for text editor white for readability
- Fix: Activation of FFTW convolution worker ([bug 407062](https://bugs.kde.org/show_bug.cgi?id=407062))
- Fix: Crash in halftone filter ([bug 407045](https://bugs.kde.org/show_bug.cgi?id=407045))
- Fix: remove notification for unused keyboard short for wrap-around ([bug 407119](https://bugs.kde.org/show_bug.cgi?id=407119))
- Fix: Safe assert triggered while drawing ([bug 404552](https://bugs.kde.org/show_bug.cgi?id=404552))
- Improvement: Warn artists if they try to render an animated GIF with over 50 FPS ([bug 403873](https://bugs.kde.org/show_bug.cgi?id=403873))
- Improvement: Handle calculation better for grayscale images in high bit depth ([bug 405693](https://bugs.kde.org/show_bug.cgi?id=405693))
- Usability: Make tabs and table headers and text translatable ([bug 406943](https://bugs.kde.org/show_bug.cgi?id=406943), [bug 406944](https://bugs.kde.org/show_bug.cgi?id=406944))
- Improvement: Make zoom mode persistent when moving across screens
- Fix: Exporting animation frames into EXR format ([bug 406830](https://bugs.kde.org/show_bug.cgi?id=406830))
- Improvement: Load broken TGA files that have bad alpha data ([bug 354791](https://bugs.kde.org/show_bug.cgi?id=354791))
- Python: Allow selecting boundary limits on export ([bug 404615](https://bugs.kde.org/show_bug.cgi?id=404615))
- Fix: Unable to set minimal shade selector ([bug 368587](https://bugs.kde.org/show_bug.cgi?id=368587))
- Improvement: Add pixel snap mode for canvas ([bug 390952](https://bugs.kde.org/show_bug.cgi?id=390952))
- Fix: Load pre-Krita 4.0 transform masks ([bug 396815](https://bugs.kde.org/show_bug.cgi?id=396815))
- Fix: TIFF export filter flatten images with group layers ([bug 404204](https://bugs.kde.org/show_bug.cgi?id=404204))
- Fix: Do not activate already running app instance when exporting image sequence
- Fix: Memory leak with GIFs when saving and line length ([bug 404160](https://bugs.kde.org/show_bug.cgi?id=404160))
- Improvement: Better calculate SVG document size and loading omitted commands ([bug 406124](https://bugs.kde.org/show_bug.cgi?id=406124))
- Usability: Hide pattern fill option in vector tools until it is fully implemented
- Fix: Artifacts when saving vector layers as PNG ([bug 404976](https://bugs.kde.org/show_bug.cgi?id=404976))
- Fix: Crash when merging back split alpha function
- Fix: Address sanitizer (ASAN) crash when creating a guide ([bug 405732](https://bugs.kde.org/show_bug.cgi?id=405732))
- Fix: Hard to select color in vector objects ([bug 404975](https://bugs.kde.org/show_bug.cgi?id=404975))
- Fix: Undo merging a layer that is cloned ([bug 397836](https://bugs.kde.org/show_bug.cgi?id=397836))
- Improvement: Add fractional DPI scaling (found in settings)
- Improvement: Allow clone brush to have an option to reset origin after every stroke
- Fix: Canvas input cursor updates when it has no input focus ([bug 369305](https://bugs.kde.org/show_bug.cgi?id=369305))
- Fix: Hiccups when using wheel on Wacom's tablet ([bug 381452](https://bugs.kde.org/show_bug.cgi?id=381452))
- Fix: Clone brush should use the last layer the source was placed on ([bug 401919](https://bugs.kde.org/show_bug.cgi?id=401919))
- Fix: Tilt elevation curve corrections ([bug 399846](https://bugs.kde.org/show_bug.cgi?id=399846))
- Fix: Do not focus on tag search line edit in the show event ([bug 404131](https://bugs.kde.org/show_bug.cgi?id=404131))
- Usability: Only show layer styles contour and texture when Bevel and Emboss is checked ([bug 396015](https://bugs.kde.org/show_bug.cgi?id=396015))
- Python: Comics plugin improvements to file saving and creating documents
- Fix: Pop-up palette color fix when changing themes
- Usability: Improve control point size for brush editor curves ([bug 406233](https://bugs.kde.org/show_bug.cgi?id=406233))
- Feature: Add option in settings to disable AVX optimizations on Windows ([bug 406209](https://bugs.kde.org/show_bug.cgi?id=406209))
- Fix: Make font size consistent ([bug 406386](https://bugs.kde.org/show_bug.cgi?id=406386))
- Fix: Unable to select new view item with OSX long path names ([bug 403639](https://bugs.kde.org/show_bug.cgi?id=403639))
- Usability: Theme change fixes for overview docker, rulers, and subwindows
- Fix: Memory leak caused by converting function
- Fix: Wrong position of the merged layer ([bug 405686](https://bugs.kde.org/show_bug.cgi?id=405686))
- Fix: Right clicking on popup-palette color selector hides it ([bug 402990](https://bugs.kde.org/show_bug.cgi?id=402990))
- Fix: rulers showing pixels no matter what unit ([bug 406181](https://bugs.kde.org/show_bug.cgi?id=406181))
- Fix: Crash in Split Alpha function ([bug 406241](https://bugs.kde.org/show_bug.cgi?id=406241))
- Fix: wrong bounding box on gradient map ([bug 406234](https://bugs.kde.org/show_bug.cgi?id=406234))
- Fix: page orientation switch in new dialog ([bug 374493](https://bugs.kde.org/show_bug.cgi?id=374493))
- Improvement: Do a better job when finding ffmpeg for flatpak ([bug 405146](https://bugs.kde.org/show_bug.cgi?id=405146))
- Improvement: Do a better job when calculating nearest neighbor filters ([bug 401788](https://bugs.kde.org/show_bug.cgi?id=401788))
- Usability: Improve contrast with checkboxes on pen settings and brush favorites
- Fix: Allow group layers to be transformed and improve logic for layers that cannot be transformed ([bug 406036](https://bugs.kde.org/show_bug.cgi?id=406036))
- Fix: Background color being lost after merging ([bug 405230](https://bugs.kde.org/show_bug.cgi?id=405230))
- Improvement: Remember last used directory for shortcut import/export ([bug 368360](https://bugs.kde.org/show_bug.cgi?id=368360))
- Improvement: Improve canvas refresh rate when moving vector objects ([bug 403340](https://bugs.kde.org/show_bug.cgi?id=403340), [bug 405698](https://bugs.kde.org/show_bug.cgi?id=405698))
- Improvement: Intel OpenGL detection for newer drivers
- Fix crash on quick brush engine because of calculations ([bug 404179](https://bugs.kde.org/show_bug.cgi?id=404179))
- Fix: splash screen on some high DPI screens
- Improvement: Move color filters on onion skin out of combo box for easier toggling
- Usability: Improve contrast with checkboxes on brush settings, pen sensors, and blending modes ([bug 404190](https://bugs.kde.org/show_bug.cgi?id=404190))
- Fix: hangup when starting painting too quickly after changing opacity ([bug 405879](https://bugs.kde.org/show_bug.cgi?id=405879))
- Fix: Data loss when adding multiple hold frames through right-click menu (bug 404246)
- Fix: Copy correct image cache when cloning a layer ([bug 387698](https://bugs.kde.org/show_bug.cgi?id=387698))
- Fix: Only show Intel graphics card warning on Windows
- Text: changed "Launch Bug Report Wizard" to "Submit Bug Report" from main menu ([bug 406152](https://bugs.kde.org/show_bug.cgi?id=406152))
- Usability: Add tooltip to eraser button in toolbar
- Fix activation of isolate mode when merging layers down ([bug 295981](https://bugs.kde.org/show_bug.cgi?id=295981))
- Improvement: Add ability for shape brushes to use patterns for filling
- Fix: Transform tool crash on layers with pass-through mode
- Improvement: Add more information like HighDPI and language to usage logger
- Fix: Make sure a masked painter knows about outlines ([bug 404963](https://bugs.kde.org/show_bug.cgi?id=404963))
- Fix: Make sure polyline takes into account the no-stroke setting
- Feature: Add ability to export animation to PNG sequence using commandline
- Fix: Better handle loading recent files ([bug 405364](https://bugs.kde.org/show_bug.cgi?id=405364))
- Improvement: Better show/hide progress bars when loading an unsupported image ([bug 402625](https://bugs.kde.org/show_bug.cgi?id=402625))
- Feature: Add mirroring capability for Quick brush ([bug 372636](https://bugs.kde.org/show_bug.cgi?id=372636))
- Usability: Add a second row to pop-up palette presets if the number gets above 20 so they are easier to see
- Fix: Color smudge might not have an image for tip ([bug 405336](https://bugs.kde.org/show_bug.cgi?id=405336))
- Fix: Prevent crash with mirror manager decorations
- Fix: When no outline is selected, outline doesn't use brush width ([bug 398509](https://bugs.kde.org/show_bug.cgi?id=398509))
- Fix: Low pixel size limit in Scale to New Size dialog
- Feature: Simplex Noise Generator can now be used from a fill layer
- Usability: Make disabled icons in animation docker semi-transparent to be like other disabled icons
- Fix: creating vector shapes with pattern fills ([bug 405037](https://bugs.kde.org/show_bug.cgi?id=405037))
- Fix: minimum animation cell grid size on windows
- Fix: conversion errors in Scale new image dialog ([bug 400177](https://bugs.kde.org/show_bug.cgi?id=400177))
- Improve UI for Arrange docker to make it easier to understand ([bug 399984](https://bugs.kde.org/show_bug.cgi?id=399984), [bug 394084](https://bugs.kde.org/show_bug.cgi?id=394084))
- Fix: Only load a thumbnail for a recent file that still exists ([bug 401939](https://bugs.kde.org/show_bug.cgi?id=401939))
- Improve angle selection on layer effects ([bug 372169](https://bugs.kde.org/show_bug.cgi?id=372169))
- Fix: Restore broken fonts ([bug 402092](https://bugs.kde.org/show_bug.cgi?id=402092))
- Add a few new options for fill type when creating new documents
- Fix: Remove the default shortcut for text tool. We just don't have any good available keys left ([bug 402270](https://bugs.kde.org/show_bug.cgi?id=402270))
- Improve animation export dialog: Add warning when dimensions are not divisible by 2 for MP4 and MKV. Make sure the default dialog uses the encoder config for the format
- Fix opening templates from the command line ([bug 402342](https://bugs.kde.org/show_bug.cgi?id=402342))
- Inserting a layer when on a group layer adds it above the layer, not inside it now (bug 399103)
- Feature: Advanced Color Selector - Add option to hide the color selector in the configure menu ([bug 337328](https://bugs.kde.org/show_bug.cgi?id=337328))
- Remove old Karbon gradient files that weren't being used
- Fix: Restore the UI after crashing in canvas only mode ([bug 402710](https://bugs.kde.org/show_bug.cgi?id=402710))
- Fix: Added safe assert to prevent Krita from crashing when a toolbar gets accidentally enabled
- Improvement: Add more information to the bug reporter with memory, CPU cores, and swap location
- Usability: Update the layer box to better to support RTL languages
- Feature: Add Python plugin importer to make importing plugins easier
- Improvement: Add direction choice for the Image Split feature
- Fix: Actions on Move Tool only being executed after changing current node in move tool ([bug 403048](https://bugs.kde.org/show_bug.cgi?id=403048))
- Fix: Python API. Fix crash when trying to access projection pixel data on transform mask ([bug 402382](https://bugs.kde.org/show_bug.cgi?id=402382))
- Fix: Return colorspace of projection before returning the colorspace of the node ([bug 402382](https://bugs.kde.org/show_bug.cgi?id=402382))
- Improvement: Enable automatic docstring generation for python ([commit e7fe83c9](https://phabricator.kde.org/R37:e7fe83c9210d4302dabd7c6e81c1c35dec912db2))
- Fix: Loading KRA files with image names starting with a "/" symbol
- Fix: Enabling the selection mode shortcuts ([bug 403587](https://bugs.kde.org/show_bug.cgi?id=403587))
- Improvement: Generator Layers. Added real-time preview when changing layer properties
- Improvement: Polygonal Selection: Add ability to undo these operations
- Fix: File layers: Use the mergedimage preview when opening ORA or KRA files
- Improvement: Transform Tool: Added Granularity to tool options
- Back-end: Update Qt programming framework to Qt 5.12
- Improvement: Update GMIC filters plugin to version 2.4.5
- Back-end: Update PDF library (Poppler) to version 0.74.0
- Back-end: Update Python API libraries (PyQt and SIP) to version 5.12
- Improvement: Added new blending modes: Reflect, Glow, Freeze, Heat, Glow-Heat, Heat-Glow, Reflect-Freeze, Freeze-Reflect, Heat-Glow & Freeze-Reflect Hybrid
- Fix: Save mirror tool state to KRA file ([bug 339515](https://bugs.kde.org/show_bug.cgi?id=339515))
- Usability: Make it easier to select lower values for stabilizer sliders
- Fix: Saving reference images z-order ([bug 403974](https://bugs.kde.org/show_bug.cgi?id=403974))
- Fix: Disable use of Always Use Template in the New File Window ([bug 399796](https://bugs.kde.org/show_bug.cgi?id=399796))
- Fix: Be the top handler of applications on some Linux distributions ([bug 337272](https://bugs.kde.org/show_bug.cgi?id=337272))
- Usability: Add a tooltip to the composition docker
- Fix: Bug where mirroring canvas would get out of sync with the main menu action
- Fix: Check if animation config exists before accessing its contents ([bug 404521](https://bugs.kde.org/show_bug.cgi?id=404521))

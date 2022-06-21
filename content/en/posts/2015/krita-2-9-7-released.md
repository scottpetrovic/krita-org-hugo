---
title: "Krita 2.9.7 Released!"
date: "2015-09-02"
categories: 
  - "officialrelease"
---

Two months of bug fixing, feature implementing, Google-Summer-of-Code-sweating, it's time for a new release! Krita 2.9.7 is special, because it's the last 2.9 release that will have new features. We'll be releasing regular bug fix releases, but from now on, all feature development focuses on Krita 3.0. But 2.9.7 is packed! There are new features, a host of bug fixes, the Windows builds have been updated with OpenEXR 2.2. New icons give Krita a fresh new look, updated brushes improve performance, memory handling is improved... Let's first look at some highlights:

## New Features:

### Tangent Normal Brush Engine

As is traditional, in September, we release the first Google Summer of Code results. Wolthera's Tangent Normal Brush engine has already been merged!

[![tangenttiltbrush](../images/tangenttiltbrush.png)](https://krita.org/wp-content/uploads/2015/08/tangenttiltbrush.png)[![phongbum1](../images/phongbum1.png)](https://krita.org/wp-content/uploads/2015/08/phongbum1.png)

It's a specialized feature, for drawing normal maps, as used in 3d engines and games. Check out the introduction video:

https://www.youtube.com/watch?v=qiX60EWyMF8

There were four parts to the project:

- [The Tangent Normal Brush Engine](https://userbase.kde.org/Krita/Manual/BrushEngines/TangentNormalBrush). (You need a tilt-enabled tablet stylus to use it!)
- The bumpmap filter now accepts normal map input
- A whole new Normalize filter
- And a new cursor option: the Tilt Cursor

### Fresh New Icons

We've got a whole new, carefully assembled icon set. All icons are tuned so they work equally well with light and dark themes. And it's now also possible to choose the size of the icons in the toolbox.

[![toolbox](../images/toolbox.png)](https://krita.org/wp-content/uploads/2015/08/toolbox.png)

If you've got a high-dpi screen, make them big, if you're on a netbook, make them small! All it takes is a right-click on the toolbox.

[![resize-icons](../images/resize-icons.gif)](https://krita.org/wp-content/uploads/2015/09/resize-icons.gif)

And to round out the improvements to the toolbox, the tooltips now show the keyboard shortcuts you can use to activate a tool and you can show and hide the toolbox from the docker menu.

### Improvements to the Wrap-around mode

Everyone who does seamless textures loves Krita's unique wraparound mode. And now we've fixed two limitations, and you can not just pick colors from anywhere, not just the original central image, but also fill from anywhere!

[![pickcolorwraparound](../images/pickcolorwraparound.png)](https://krita.org/wp-content/uploads/2015/08/pickcolorwraparound.png)

### New Color Space Selector

Wolthera also added a new dialog for picking the color profile: The Color Profile browser. if you just want to draw without worries, Krita's default will work for you, of course. But if are curious, or want to go deeper into color management, or have advanced needs then this browser dialog gives you all the details you need to make an informed choice!

[![colorspacebrowser](../images/colorspacebrowser.png)](https://krita.org/wp-content/uploads/2015/08/colorspacebrowser.png) Krita ships with a large set of carefully tuned ICC profiles created by [Elle Stone](http://ninedegreesbelow.com/). Her extensive notes on when one might prefer to use one or the other are included in the new color profile browser.

### Compatibility with the rest of the world

We improved compatibility with Gimp: Krita can now load group layers, load XCF v3 files and finally load XCF files on Windows, too. Photoshop PSD support always gets attention. We made it possible to load bit/channel CMYK and Grayscale images, ZIP compressed PSD files and improved saving images with a single layer that has transparency to PSD.

### Right-click to undo last path point

You can now right-click in the middle of creating a path to undo the last point. [![right-click-delete](../images/right-click-delete.gif)](https://krita.org/wp-content/uploads/2015/09/right-click-delete.gif)

### More things...

- The freehand tools' Stabilizer mode has a new 'Scalable smoothness' feature.
- You can now merge down Selection Masks
- We already had shortcuts to fill your layer or selection with the foreground or background color or the current pattern at 100% opacity. If you press Shift in addition to the shortcut, the currently set painting opacity will be used.
- We improved the assistants. You can now use the Shift key to add horizontal snapping to the handles of the straight-line assistants. The same shortcut will snap the third handle of the ellipse assistant to provide perfect circles.
- Another assistant improvement:  there is now a checkbox to assistant snapping that will make the snapping happen to only the first snapped-to-assistant. This removes snapping issues on infinite assistants while keeping the ability to snap to chained assistants while the checkbox is unticked.
- Several brushes were replaced with optimized versions: Basic\_tip\_default, Basic\_tip\_soft, Basic\_wet, Block\_basic, Block\_bristles, Block\_tilt, Ink\_brush\_25, Ink\_gpen\_10, Ink\_gpen\_25 now are much more responsive.
- There is a new and mathematically robust normal map combination blending mode.
- Slow down cursor outline updates for randomized brushes: when painting with a brush with fuzzy rotation, the outline looked really noisy before, now it's smoother and easier to look at.
- You can now convert any selection into a vector shape!
- We already had a trim image to layer size option, but we added the converse: Trim to Image Size for if your layers are bigger than your image. (Which is easily managed with moving, rotating and so on).
- The dodge and burn filter got optimized
- Fixes to the Merge Layer functionality: you can use Ctrl+E to merge multiple selected layers, you can merge multiple selected layers with layer styles and merging of clone layers together with their sources will no longer break Krita.
- The Color to Alpha filter now works correctly  with 16 bits floating point per channel color models.
- We added a few more new shortcuts: scale image to new size using CTRL+ALT+I,  resize canvas with CTRL+ALT+C, create group kayer is CTRL+G, and feather selection = SHIFT+F6.

## Fixed Bugs:

We resolved more than 150 bugs for this release. Here's a highlight of the most important bug fixes! Some important fixes have to do with loading bundles. This is now more robust, but you might have problems with older bundle files. We also redesigned the Clone and Stamp brush creation dialogs. Look for the buttons in the predefined brush-tip tab of the brush editor. There are also performance optimizations, memory leak fixes and more:

1.  BUG: 351599 Fix abr (photoshop) brush loading
2. BUG:343615 Remember the toolbar visibility state when switching to canvas-only
3. BUG:338839 Do not let the wheel zoom if there are modifiers pressed
4. BUG:347500 Fix active layer activation mask
5. Remove misleading error message after saving fails
6. BUG 350289 : Prevent Krita from loading incomplete assistant.
7. BUG:350960 Add ctrl-shift-s as default shortcut for "Save As" on Windows.
8. Fix the Bristle brush presets
9. Fix use normal map checkbox in the bumpmap filter UI.
10. Fix loading the system-set monitor profile when using colord
11. When converting between linear light sRGB and gamma corrected sRGB, automatically uncheck the "Optimize" checkbox in the colorspace conversion dialog.
12. BUG:351488 Do not share textures when that's not possible. This fixes showing the same image in two windows on two differently profiled monitors.
13. BUG:351488 Update the display profile when moving screens. Now Krita will check whether you moved your window to another monitor, and if it detects you did that, recalculate the color correction if needed.
14. Update the display profile after changing the settings -- you no longer need to restart Krita after changing the color management settings.
15. BUG:351664 Disable the layerbox if there is no open image, fixing a crash that could happen if you right-clicked on the layerbox before opening an image.
16. BUG:351548 Make the transform tool work with Pass Through group layers
17. BUG:351560 Make sure a default KoColor is black and transparent (fixes the default color settings for color fill layers)
18. Lots of memory leak fixes
19. BUG:351497 Blacklist "photoshop":DateCreated" when saving. Photoshop adds a broken metadata line to JPG images that gave trouble when saving an image that contained a JPG created in Photoshop as a layer to Krita's native file format.
20. Ask for a profile when loading 16 bits PNG images, since Krita assumes linear light is default for 16 bits per channel RGB images.
21. Improve the performance of most color correction filters
22. BUG:350498 Work around encoding issues in kzip: images with a Japanese name now load correctly again.
23. BUG:348099 Better error messages when exporting to PNG.
24. BUG:349571 Disable the opacity setting for the shape brush. It hasn't worked for about six years now.
25. Improve the Image Recovery dialog by added some explanations.
26. BUG:321361 Load resources from nested directories
27. Do not use a huge amount of memory to save the pre-rendered image to OpenRaster or KRA files.
28. BUG:351298 Fix saving CMYK JPEG's correctly and do not crash saving 16 bit CMYK to JPEG
29. BUG:351195 Fix slowdown when activating "Isolate Layer" mode
30. Fix loading of selection masks
31. BUG:345560 Don't add the files you select when creating a File Layer  to the recent files list.
32. BUG:351224 Fix crash when activating Pass-through mode for a group with transparency mask
33. BUG:347798 Don't truncate fractional brush sizes on eraser switch
34. Don't add new layers to a locked group layer
35. Transform invisible layers if they are part of the group
36. BUG:345619 Allow Drag & Drop of masks
37. Fix the Fill Layer dialog to show the correct options
38. BUG:344490 Make the luma options in the color selector settings translatable.
39. BUG:351193 Don't hang when isolating a layer during a stroke
40. BUG:349621 Palette docker: Avoid showing a horizontal scrollbar
41. Many fixes and a UI redesign for the Stamp and Clipboard brush creation dialogs
42. BUG:351185 Make it possible to select layers in a pass-through group using the R shortcut.
43. Don't stop loading a bundle when a wrong manifest entry is found
44. BUG:349333 fix inherit alpha on fill layers
45. BUG:351005 Don't crash on closing krita if the filter manager is open
46. BUG:347285: Open the Krita Manual on F1 on all platforms
47. BUG: 341899 Workaround for Surface Pro 3 Eraser
48. BUG:350588 Fix a crash when the PSD file type is not recognized by the system
49. BUG:350280 Fix a hangup when pressing 'v' and 'b' in the brush tool simultaneously
50. BUG:350280 Fix  crash in the line tool.
51. BUG:350507 Fix crash when loading a transform mask with a non-affine transform

### Download

- Linux:
    - Distributions are expected to create packages for their bleeding edge repositories.
    - Ubuntu and derivatives can use Krita Lime, as usual: [https://launchpad.net/~dimula73/+archive/ubuntu/krita](https://launchpad.net/%7Edimula73/+archive/ubuntu/krita).
    - OpenSUSE users can use the KDE:Extra repo: [http://download.opensuse.org/repositories/KDE:/Extra/](http://download.opensuse.org/repositories/KDE:/Extra/) or Leinir’s OBS repositories which have Krita built with support for Vc (which makes painting faster):
        - [http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE\_13.1/](http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_13.1/)
        - [http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE\_13.2/](http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_13.2/)
        - [http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE\_Factory/](http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_Factory/)
- Windows and OSX
    - The [download page](https://krita.org/download/krita-desktop/ "Krita Desktop") has been updated, so check out the new builds. If you don’t want to use the MSI installer, go to [files.kde.org](http://files.kde.org/krita) for the portable zip-file based version of Krita for Windows.
    - You can also get the latest version of [Krita on Steam](http://store.steampowered.com/app/280680), using the "Desktop29″ option in the Beta channel! Steam users get updates automatically.

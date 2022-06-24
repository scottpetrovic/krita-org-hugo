---
title: "Krita 4.4.2 Released"
date: "2021-01-19"
categories: 
  - "officialrelease"
---

Today, the Krita team has released Krita 4.4.2. With over 300 changes, this is mainly a bugfix release, though some key new features, too!

## New Features

### Mesh Gradients

Sharaf Zaman's Google Summer of Code project has landed in this release! Compatible with Inkscape, Krita now provides the second independent implementation of SVG Mesh Gradients. Mesh gradients are used on vector objects and can deliver really natural looking results:

[![Mesh Gradients](/images/posts/2021/Handles-meshgradient-1024x554.png)](/images/posts/2020/Handles-meshgradient.png) Mesh Gradients

### Mesh Transform

[![Image showing how useful mesh transforms can be](/images/posts/2021/krita_4_4_2_mesh_gradients.png)](/images/posts/2020/krita_4_4_2_mesh_gradients.png) Mesh transforms will greatly speed up your concept by allowing complex transformations, such as the half-rounded grate on this window!

But the gradients are not the only mesh related feature! This release also sees the first iteration of the mesh-transform. Like the gradient mesh, the mesh transform consists of bezier patches that can be individually shaped to create precise transforms, especially useful for rounded objects. Not shown in the above screenshot: you can optionally show the handles of each bezier curve making up the mesh for even more precision and control!

We're still tweaking this one, but currently the shortcuts are the following:

1. Mesh node: - click+drag --- move node
2. Border node: - click+drag --- move node - shift+click+drag --- move whole row/column - ctrl+alt+click+drag --- split/slide row/column - ctrl+alt+click+drag-away --- remove split
3. Control point: - click+drag --- change control point symmetrically - shift+click+drag --- change control point non-symmetrically; this action will create angular texture artifacts
4. Node or Control: - ctrl+click --- select multiple nodes
5. Patch area: - click+drag --- free patch deform - shift+click+drag --- move whole mesh
6. Empty area outside mesh: - click+drag --- rotate mesh or selection - ctrl+click+drag --- scale mesh or selection - shift+click+drag --- move mesh or selection

### Gradient Fill Layer and new Gradient Editor

[![Showing the gradient fill layer and the new gradient editor.](/images/posts/2021/krita_4_4_2_new_gradient_editor_and_fill_layer.png)](/images/posts/2020/krita_4_4_2_new_gradient_editor_and_fill_layer.png) The gradient fill layer and the new gradient editor in action.

Deif Lou added a new gradient fill layer type, this one will make it easy to quickly create a variety of gradients non-destructively. With it, he also made an important usability fix: Gradients in Krita could be either segment type, or stop type, with different features each, and different editors each. That could get quite annoying if you were working on a gradient, but you realized you had the wrong type! This is now fixed, as both gradient types can now be edited by the same editor, which also converts between the two.

### Improved Halftone Filter

Deif Lou also created a new halftone filter. The old filter was slow and could not be used as a filter mask, and could only show dots.

[![Our splash screen as filtered by the half tone filter](/images/posts/2021/krita_4_4_2_halftone_filter.png)](/images/posts/2020/krita_4_4_2_halftone_filter.png) The new halftone filter can do per-channel filtering, useful for vintag effects and maybe even printing!

The new filter can handle being applied as filter layer, per-channel filtering, and the pattern itself can be generated with any of the fill layer options, giving endless combinations.

### Updated macOS integration plugins

Amyspark improved the quicklook plugin by adding thumbnailing support (needs macOS 10.15 or higher) and added metadata support for Spotlight.

### A Paste Shape Style Action

A small feature that allows you to only paste the style of the copied vector shape onto other selected vector shapes. This feature can be found under the edit menu, or assigned a shortcut in the shortcut settings.

### A Toolbar Button for Wraparound Mode

Originally, we had a shortcut, W, that enabled Krita's Wraparound mode, one of the features Adobe copied this year for the next release of Photoshop.

[![](/images/posts/2021/wrap-around-mode.jpg)](/images/posts/2014/wrap-around-mode.jpg)

But too many people pressed the shortcut by accident and were then confused and thought Krita had gone crazy... So we removed the shortcut, but now nobody could find it anymore. That's why in this release, we have added a button to the toolbar that activates wraparound:

[![](/images/posts/2021/wraparound_button.png)](/images/posts/2020/wraparound_button.png)Please don't press it by accident!

### New brushes

There are also six new brushes by Ramon Miranda, meant to show off the new RGBA brush tip feature:

[![](/images/posts/2021/rgba_brushes.png)](/images/posts/2020/rgba_brushes.png)

### HiDPI Support

![This image shows the difference between the old popup palette and the new one on 4k display with 200% UI scaling. Note that it also shows a new button and custom UI text.](/images/posts/2021/popup_palette_comparison.png) Agata Cacko improved HiDPI rendering ([BUG:411118](https://bugs.kde.org/show_bug.cgi?id=411118)) of

- Pixelart previews
- Reference images
- Comic manager pages
- Image thumbnails in the last documents docker
- Recent documents thumbnails
- The Popup palette
- Clipboard content in the new image dialog
- The Color selectors
- Gamut masks
- Brush preset icon in the Brush preset editor
- Layer thumbnails and icons
- Resource choosers
- Bundle icons

## Bug Fixes

### File Handling

- Files with names starting with a number are now autosaved correctly
- Make it possible to load EXR files with non-ascii characters in the path
- Disable making the background black for a semi-transparent EXR file ([BUG:427720](https://bugs.kde.org/show_bug.cgi?id=427720))

### Painting

- The PressureIn sensor now works correctly in combination with the Hue color expression ([BUG:426234](https://bugs.kde.org/show_bug.cgi?id=426234))
- The speed smoothing algorithm no longer creates blobby lines ([BUG:363364](https://bugs.kde.org/show_bug.cgi?id=363364), [375360](https://bugs.kde.org/show_bug.cgi?id=375360))
- The colorsmudge brush now blends when there is a selection active ([BUG:423851](https://bugs.kde.org/show_bug.cgi?id=423851))
- The brush outline no longer snaps when switching between two images with a different zoom level ([BUG:427094](https://bugs.kde.org/show_bug.cgi?id=427094))

### Animation

Most animation work is going in the master branch, which will become Krita 5.0.

- Onion skins are hidden when playing an animation ([BUG:426246](https://bugs.kde.org/show_bug.cgi?id=426246))
- Warn the user when they are trying to run the ffmpeg download archive, instead of unpacking it
- Fix converting an animated transparency mask to a paint layer ([BUG:419223](https://bugs.kde.org/show_bug.cgi?id=419223))

### Usability

- The default shortcuts for changing the mode in the selection tools have been removed: they are replaced by ctrl/shift/alt modifiers. The actions still exist, so you can configure single-key shortcuts in Krita's shorcut settings dialog.
- The magnetic selection tool now has buttons to confirm or discard a selection
- An issue where moving a selection would jump was fixed ([BUG:426949](https://bugs.kde.org/show_bug.cgi?id=426949))
- A Fit to Height zoom shortcut was added, patch by Jonathan Colman ([BUG:410929](https://bugs.kde.org/show_bug.cgi?id=410929))
- The screentone generator's defaults were improved
- File layers that are dragged and dropped now have a proper name (patch by Jonathan Colman) ([BUG:427235](https://bugs.kde.org/show_bug.cgi?id=427235))
- The popup palette now has a clear color history button (patch by Emilio Del Castillo)
- The report bug dialog now provides the system information and usage logs in an easy to copy/paste manner
- Blacklisted resources that contain a \\ in the filename were ignored ([BUG:421575](https://bugs.kde.org/show_bug.cgi?id=421575))
- Displays are shown by name in the color management settings page ([BUG:412943](https://bugs.kde.org/show_bug.cgi?id=412943))
- Fix showing custom icons for user-defined templates (patch by Evan Thompson) ([BUG:395894](https://bugs.kde.org/show_bug.cgi?id=395894))
- The fill layer dialog and seexpr widgets were polished
- The x/y position spin boxes in the move tool options were fixed ([BUG:420329](https://bugs.kde.org/show_bug.cgi?id=420329), [423452](https://bugs.kde.org/show_bug.cgi?id=423452))
- Add default letter spacing for the text shape (patch by Lucid Sunlight)
- Add support for user-installed color schemes (patch by Daniel)
- All dialogs and message boxes are now correctly parented to the main window (patch by Daniel)
- Make it possible to export groups as merged layers (patch by Dmitrij Antsevich)
- Fix kerning handling in the text editor (patch by Lucid Sunlight)
- Add support for color opacity in the text editor (patch by Lucid Sunlight) ([BUG:342303](https://bugs.kde.org/show_bug.cgi?id=342303))
- Fix cropping the transform mask when moving the masked layer
- Improve switching between SVG source and rich text editor (patch by Lucid Sunlight) ([BUG:424213](https://bugs.kde.org/show_bug.cgi?id=424213))
- Fix issues with the brush outline getting stuck when the brush size is smaller than 0 ([BUG:427751](https://bugs.kde.org/show_bug.cgi?id=427751))
- Improve the Python plugin importer so action files get imported correctly. (Patch by Rebecca Breu) ([BUG:429262](https://bugs.kde.org/show_bug.cgi?id=429262))
- Fix tearing of patterns when scrolling in the resource chooser.
- The rectangle and ellipse tool now have default shortcuts: Shift+R and Shift+J, respectively
- Allow the Select Similar Color selection tool to pick from a set of layers, make work correctly with image bounds and handle transparent layers correctly. ([BUG:428441](https://bugs.kde.org/show_bug.cgi?id=428441))
- Fix the isometric grid so it is drawn correctly
- The outline selection tool was renamed to freehand selection tool ([BUG:425894](https://bugs.kde.org/show_bug.cgi?id=425894))

### Filters

- The bundled g'mic plugin is updated to 2.9.2 which contains a correct Boost-Fade filter (BUG:412617)
- The gradient map filter was improved and made faster (patch by Deif Lou)

### Stability and Performance

- Fix a lot of memory leaks
- Improve performance by removing a bottleneck when transforming internal colors to and from QColor
- Fix a race condition in the Comics Manager plugin ([BUG:426701](https://bugs.kde.org/show_bug.cgi?id=426701))
- Fix the fill layers updating too many times
- Fix random crashes when changing screentone fill layer parameters ([BUG:428014](https://bugs.kde.org/show_bug.cgi?id=428014))
- Fix a crash in the Square Gradient strategy (patch by Deif Lou)
- Fix a crash when converting SVG source to rich text or back (patch by Lucid Sunlight)
- Fix an assert when trying to liquify transform an empty layer ([BUG:428685](https://bugs.kde.org/show_bug.cgi?id=428685))
- Fix an assert when creating a new layer from the visible layers while the active layer is hidden ([BUG:428683](https://bugs.kde.org/show_bug.cgi?id=428683))
- Make the Select Similar selection tool multithreaded.

### MacOS

- On macOS, the Delete key (which is actually backspace) now deletes a selection. ([BUG:425370](https://bugs.kde.org/show_bug.cgi?id=425370))

### Android

- It's now possible to open files from external sources, like a file manager, google drive or a download manager on Android
- Add mimetype and pathpatter for .kra files
- Make Krita a SingleTask application: this means that opening a file of a type supported by Krita will work properly even if Krita is already running.
- Fix possible corruption when saving .kra or .ora files
- Fix a crash on closing Krita ([BUG:426092](https://bugs.kde.org/show_bug.cgi?id=426092))
- Fix "also save as KRA" ([BUG:424612](https://bugs.kde.org/show_bug.cgi?id=424612))
- Handle mouse buttons state and touch events properly
- Make resaving with different mime type work on Android ([BUG:429056](https://bugs.kde.org/show_bug.cgi?id=429056))
- Make the theme background black for chromeos: this used to be pink, which looked ugly when resizing a window.
- Fix flickering tiles when OpenGL is enabled ([BUG:424347](https://bugs.kde.org/show_bug.cgi?id=424347))

## Download

### Windows

If you're using the portable zip files, just open the zip file in Explorer and drag the folder somewhere convenient, then double-click on the krita icon in the folder. This will not impact an installed version of Krita, though it will share your settings and custom resources with your regular installed version of Krita. For reporting crashes, also get the debug symbols folder.

- 64 bits Windows Installer: [krita-x64-4.4.2-setup.exe](https://download.kde.org/stable/krita/4.4.2/krita-x64-4.4.2-setup.exe)
- Portable 64 bits Windows: [krita-x64-4.4.2.zip](https://download.kde.org/stable/krita/4.4.2/krita-x64-4.4.2.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.4.2/krita-x64-4.4.2-dbg.zip)

- 32 bits Windows Installer: [krita-x86-4.4.2-setup.exe](https://download.kde.org/stable/krita/4.4.2/krita-x86-4.4.2-setup.exe)
- Portable 32 bits Windows: [krita-x86-4.4.2.zip](https://download.kde.org/stable/krita/4.4.2/krita-x86-4.4.2.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.4.2/krita-x86-4.4.2-dbg.zip)

### Linux

- 64 bits Linux: [krita-4.4.2-x86\_64.appimage](https://download.kde.org/stable/krita/4.4.2/krita-4.4.2-x86_64.appimage)
- 64 bits Linux [G'Mic-Qt plugin appimage](https://download.kde.org/stable/krita/4.4.2/gmic_krita_qt-x86_64.appimage)

(If, for some reason, Firefox thinks it needs to load this as text: to download, right-click on the link.)

### OSX

- OSX disk image: [krita-4.4.2.dmg](https://download.kde.org/stable/krita/4.4.2/krita-4.4.2.dmg)

Note: the gmic-qt is not available on OSX.

### Android

This time, the Android releases are made from the release tarball, so there are translations. We consider Krita on ChromeOS and Android still **_beta_**. There are many things that don't work and other things that are impossible without a real keyboard.

- [64 bits Intel CPU APK](https://download.kde.org/stable/krita/4.4.2/krita_build_apk-release-x86_64-release.apk)
- [32 bits Intel CPU APK](https://download.kde.org/stable/krita/4.4.2/krita_build_apk-release-x86-release.apk)
- [64 bits Arm CPU APK](https://download.kde.org/stable/krita/4.4.2/krita_build_apk-release-arm64_v8a-release.apk)
- [32 bits Arm CPU APK](https://download.kde.org/stable/krita/4.4.2/krita_build_apk-release-armeabi_v7a-release.apk)

### Source code

- [krita-4.4.2.tar.gz](https://download.kde.org/stable/krita/4.4.2/krita-4.4.2.tar.gz)
- [krita-4.4.2.tar.xz](https://download.kde.org/stable/krita/4.4.2/krita-4.4.2.tar.xz)

### md5sum

For all downloads:

- [md5sum.txt](https://download.kde.org/stable/krita/4.4.2/md5sum.txt)

### Key

The Linux appimage and the source .tar.gz and .tar.xz tarballs are signed. You can retrieve the public key with gpg: "gpg –recv-key 7468332F". The signatures are [here](https://download.kde.org/stable/krita/4.4.2/) (filenames ending in .sig).

## Support Krita

Krita is a free and open source project. Please consider supporting the project with [donations](/support-us/donations/) or by [buying training videos!](/support-us/shop) With your support, we can keep the core team working on Krita full-time.

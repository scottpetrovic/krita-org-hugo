---
title: "Krita 4.2.8 Released"
date: "2019-11-27"
categories: 
  - "officialrelease"
---

The Krita team is pleased to announce another bug fix release of Krita 4.2: Krita 4.2.8.  Part of Krita's core team is now working on rewriting the way Krita loads and saves resources like brushes or gradients. This is a big task that takes up a lot of time, so there are fewer bug fixes in this release than there were for 4.2.7. Still, there has been a lot of work done on vector shapes, the transform tool and, especially, saving on Windows.

Windows usually only writes out saved files to the actual disk when it feels like it. So if you'd cut the power to your computer before Windows did that, you might get corrupted files. With 1,500,000 distinct Windows 10 users of Krita in the past month, chances are good for that happening (just like there are people who work exclusively with unnamed autosave files -- don't do that!), so we now try to force Windows to write files to disk after saving. This does make saving slower on Windows, but the added security should be worth it.

The autoprecision setting in the brush preset editor has been rewritten as well, which should result in better performance and nicer lines, too.

Here's the full list of fixes:

- Fix the sliders in the performance settings page. [BUG:414092](https://bugs.kde.org/show_bug.cgi?id=414092)
- Fix the color space of the onion skin cache. [BUG:407251](https://bugs.kde.org/show_bug.cgi?id=407251)
- Fix transforming layers that have onion skins enabled. [BUG:408152](https://bugs.kde.org/show_bug.cgi?id=408152)
- Also save the preferences when closing the preferences dialog with the titlebar close button
- Fix a bug in the polygon tool that adds an extra point. [BUG:411059](https://bugs.kde.org/show_bug.cgi?id=411059)
- Save the last used export settings. [BUG:409044](https://bugs.kde.org/show_bug.cgi?id=409044)
- Prevent a crash on macOS when closing a dialog that opened the system color dialog. [BUG:413922](https://bugs.kde.org/show_bug.cgi?id=413922)
- Fix an issue on macOS where the native file dialogs would not return a filename. [BUG:413241](https://bugs.kde.org/show_bug.cgi?id=413241)
- Make it possible to save the "All" tag as the current tag. [BUG:409748](https://bugs.kde.org/show_bug.cgi?id=409748)
- Show the correct blending mode in the brush preset editor. [BUG:410136](https://bugs.kde.org/show_bug.cgi?id=410136)
- Fix saving color profiles that are not sRGB to PNG files
- Make the transform tool work correctly with the selection mask's overlay
- Fix a crash when editing the global selection mask. [BUG:412747](https://bugs.kde.org/show_bug.cgi?id=412747)
- Remove the "Show Decorations" option from the transform tool. [BUG:413573](https://bugs.kde.org/show_bug.cgi?id=413573)
- Remove the CSV export filter (it hasn't worked for ages)
- Fix slowdown in the Warp transform tool. [BUG:413157](https://bugs.kde.org/show_bug.cgi?id=413157)
- Fix possible data loss when pressing the escape key multiple times. [BUG:412561](https://bugs.kde.org/show_bug.cgi?id=412561)
- Fix a crash when opening an image with a clone layer when instant preview is active. [BUG:412278](https://bugs.kde.org/show_bug.cgi?id=412278)
- Fix a crash when editing vector shapes. [BUG:413932](https://bugs.kde.org/show_bug.cgi?id=413932)
- Fix visibility of Reference Layer and Global Selection Mask in Timeline. [BUG:412905](https://bugs.kde.org/show_bug.cgi?id=412905)
- Fix random crashes when converting image color space. [BUG:410776](https://bugs.kde.org/show_bug.cgi?id=410776)
- Rewrite the "auto precision" option in the brush preset editor. [BUG:413085](https://bugs.kde.org/show_bug.cgi?id=413085)
- Fix legacy convolution filters on images with non-transparent background. [BUG:411159](https://bugs.kde.org/show_bug.cgi?id=411159)
- Fix an assert when force-autosaving the image right during the stroke. [BUG:412835](https://bugs.kde.org/show_bug.cgi?id=412835)
- Fix crash when using Contionous Selection tool with Feather option. [BUG:412622](https://bugs.kde.org/show_bug.cgi?id=412622)
- Fix an issue where temporary files were created in the folder above the current folder.
- Improve the rendering of the transform tool handles while actually making a transformation
- Use the actual mimetype instead of the extension to identify files when creating thumbnails for the recent files display
- Improve the logging to detect whether Krita has closed improperly
- Fix exporting compositions from the compositions docker. [BUG:412953](https://bugs.kde.org/show_bug.cgi?id=412953), [BUG:412470](https://bugs.kde.org/show_bug.cgi?id=412470)
- Fix Color Adjustment Curves not processing. [BUG:412491](https://bugs.kde.org/show_bug.cgi?id=412491)
- Fix artifacts on layers with colorize mask \*and\* disabled layer styles
- Make Separate Channels work. [BUG:336694](https://bugs.kde.org/show_bug.cgi?id=336694), [BUG:412624](https://bugs.kde.org/show_bug.cgi?id=412624)
- Make it possible to create vector shapes on images that are bigger than QImage's limits. [BUG:408936](https://bugs.kde.org/show_bug.cgi?id=408936)
- Disable adjustmentlayer support on the raindrop filter. [BUG:412522](https://bugs.kde.org/show_bug.cgi?id=412522)
- Make it possible to use .kra files as file layers. [BUG:412549](https://bugs.kde.org/show_bug.cgi?id=412549)
- Fix Crop tool loosing aspect ratio on move. [BUG:343586](https://bugs.kde.org/show_bug.cgi?id=343586)
- Fix Rec2020 display format. [BUG:410918](https://bugs.kde.org/show_bug.cgi?id=410918)
- Improve error messages when loading and saving fails.
- Fix jumping of vector shapes when resizing them
- Add hi-res input events for pan, zoom and rotate. [BUG:409460](https://bugs.kde.org/show_bug.cgi?id=409460)
- Fix crash when using Pencil Tool with a tablet. [BUG:412530](https://bugs.kde.org/show_bug.cgi?id=412530)
- Always ask Windows to synchronize the file systems after saving a file from Krita.
- Fix wrong aspect ratio on loading SVG files. [BUG:407425](https://bugs.kde.org/show_bug.cgi?id=407425)

## Download

### Windows

For the beta, you should only only use the portable zip files. Just open the zip file in Explorer and drag the folder somewhere convenient, then double-click on the krita icon in the folder. This will not impact an installed version of Krita, though it will share your settings and custom resources with your regular installed version of Krita. For reporting crashes, also get the debug symbols folder.

- 64 bits Windows Installer: [krita-x64-4.2.8-setup.exe](https://download.kde.org/stable/krita/4.2.8/krita-x64-4.2.8-setup.exe)
- Portable 64 bits Windows: [krita-x64-4.2.8.zip](https://download.kde.org/stable/krita/4.2.8/krita-x64-4.2.8.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.2.8/krita-x64-4.2.8-dbg.zip)

- 32 bits Windows Installer: [krita-x86-4.2.80-setup.exe](https://download.kde.org/stable/krita/4.2.8/krita-x86-4.2.8-setup.exe)
- Portable 32 bits Windows: [krita-x86-4.2.8.zip](https://download.kde.org/stable/krita/4.2.8/krita-x86-4.2.8.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.2.8/krita-x86-4.2.8-dbg.zip)

### Linux

- 64 bits Linux: [krita-4.2.8-x86\_64.appimage](https://download.kde.org/stable/krita/4.2.8/krita-4.2.8-x86_64.appimage)
- 64 bits Linux [G'Mic-Qt plugin appimage](https://download.kde.org/stable/krita/4.2.8/gmic_krita_qt-x86_64.appimage)

(If, for some reason, Firefox thinks it needs to load this as text: to download, right-click on the link.)

### OSX

- OSX disk image: [krita-4.2.8.dmg](https://download.kde.org/stable/krita/4.2.8/krita-4.2.8.dmg)

Note: the gmic-qt is not available on OSX.

### Source code

- [krita-4.2.8.2.tar.gz](https://download.kde.org/stable/krita/4.2.8/krita-4.2.8.2.tar.gz)
- [krita-4.2.8.2.tar.xz](https://download.kde.org/stable/krita/4.2.8/krita-4.2.8.2.tar.xz)

### md5sum

For all downloads:

- [md5sum.txt](https://download.kde.org/stable/krita/4.2.8/md5sum.txt)

### Key

The Linux appimage and the source .tar.gz and .tar.xz tarballs are signed. You can retrieve the public key over https here: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8). The signatures are [here](https://download.kde.org/stable/krita/4.2.8/) (filenames ending in .sig).

## Support Krita

Krita is a free and open source project. Please consider supporting the project with [donations](https://krita.org/en/support-us/donations/) or by [buying training videos!](https://krita.org/en/support-us/shop) With your support, we can keep the core team working on Krita full-time.

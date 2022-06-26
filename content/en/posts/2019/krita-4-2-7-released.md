---
title: "Krita 4.2.7 Released"
date: "2019-10-03"
categories: 
  - "officialrelease"
---

Today, we're releasing the sixth bug fix release of Krita 4.2. As discussed in our development update, we intend to release a few more monthly 4.2 bug fix releases before releasing Krita 4.3. There are a lot of bug fixes!

And to celebrate the release, we have a new video by Ramon Miranda which comes with a very nice present: a [free new bundle of six sketching brush presets](https://files.kde.org/krita/extras/RM_Sketch_V1.bundle)!

{{< youtube HtBzzXulIr0 >}}

### Bugs Fixed in 4.2.7

- Improve the layout and functionality of the color selector dialog and make it perform much better. ([BUG:381529](https://bugs.kde.org/show_bug.cgi?id=381529)). Patches by Mathias Wein.
- Do not crash when trying to merge an invisible group layer ([BUG:411124](https://bugs.kde.org/show_bug.cgi?id=411124))
- Make it possible to save group layers to file layers even if they are empty ([BUG:411101](https://bugs.kde.org/show_bug.cgi?id=411101))
- Make the initial location of the OCIO profile selector sensible
- Fix possible crashes when a broken file ends up in the Recent Documents List ([BUG:411416](https://bugs.kde.org/show_bug.cgi?id=411416))
- Use locale-based formatting of numbers in the measure tool and other places. Patch by Karl Ove Lufthammer.
- Make HTML markup in the Search Field tooltips work. Patch by Karl Ove Lufthammer.
- Fix a crash when moving multiple vector shapes ([BUG:409872](https://bugs.kde.org/show_bug.cgi?id=409872))
- Fix the sort order of images imported as frames if they are not numbered with prefix 0's ([BUG:375885](https://bugs.kde.org/show_bug.cgi?id=375885))
- Make it possible again to run the Python Scripting Debugger on Linux (BUG:410807) Patch by Rebecca Breu.
- Cache ICC profiles when loading layers: this speeds up loading images with thousands of layers ([BUG:411532](https://bugs.kde.org/show_bug.cgi?id=411532))
- Fix file layer and comics manager page updating on Windows ([BUG:410409](https://bugs.kde.org/show_bug.cgi?id=410409), [BUG:389544](https://bugs.kde.org/show_bug.cgi?id=389544))
- Use LittleCMS' copy alpha channel flag to speed up color transformations
- Fix outline move mode ([BUG:411057](https://bugs.kde.org/show_bug.cgi?id=411057))
- Fix a hang in the text shape if an UTF-8 Line Break character is used ([BUG:410402](https://bugs.kde.org/show_bug.cgi?id=410402))
- Fix a random crash if there is not enough space in the swapfile location for AMD Ryzen 3500 CPU's ([BUG:411081](https://bugs.kde.org/show_bug.cgi?id=411081))
- Fix checking whether the swapfile location is actually writable on Windows ([BUG:411129](https://bugs.kde.org/show_bug.cgi?id=411129), [BUG:411081](https://bugs.kde.org/show_bug.cgi?id=411081))
- Fix another random crash when painting ([BUG:411280](https://bugs.kde.org/show_bug.cgi?id=411280))
- Fix artifacts when moving control points of a path shape ([BUG:411334](https://bugs.kde.org/show_bug.cgi?id=411334))
- Fix a crash when cropping a particular image ([BUG:411536](https://bugs.kde.org/show_bug.cgi?id=411536))
- Fix move action in the bezier selection tool ([BUG:398294](https://bugs.kde.org/show_bug.cgi?id=398294))
- Fix artifacts in Gaussian Blur on transparent layers ([BUG:411719](https://bugs.kde.org/show_bug.cgi?id=411719))
- Fix a crash when the Liquify Transform is started too quickly ([BUG:411703](https://bugs.kde.org/show_bug.cgi?id=411703))
- Fix a bad memory leak in the jpeg converter ([BUG:410864](https://bugs.kde.org/show_bug.cgi?id=410864))
- Fix a crash when loading a JPEG image with a broken color profile ([BUG:410864](https://bugs.kde.org/show_bug.cgi?id=410864))
- Fix problems when zooming with a touchpad ([BUG:410940](https://bugs.kde.org/show_bug.cgi?id=410940))
- Fix issues when using the calculation capabilities of the specific color selector's spin boxes ([BUG:409818](https://bugs.kde.org/show_bug.cgi?id=409818)). Patch by Jasper Hartog
- Make sure all layers are shown in the animation timeline by default
- Fix a crash when the colorize tool is active on closing Krita
- Fix a crash when converting a colorspace with OCIO enabled ([BUG:411045](https://bugs.kde.org/show_bug.cgi?id=411045))
- Fix the Strength parameter not being used in Rotation - Fuzzy Dab ([BUG:376179](https://bugs.kde.org/show_bug.cgi?id=376179))
- Fix a crash when using the mouse wheel while an image is opening
- Re-add error messages lost when refactoring the error messages for loading images
- Do not crash if libjpeg encounters any kind of error ([BUG:364350](https://bugs.kde.org/show_bug.cgi?id=364350))
- Fix presets with random offset of texture being marked dirty all the time ([BUG:406427](https://bugs.kde.org/show_bug.cgi?id=406427))
- Fix curves changing randomly with sensors with Use Same Curve enabled ([BUG:383909](https://bugs.kde.org/show_bug.cgi?id=383909))
- Add a simple progress bar when saving .kra files
- Ensure that the temporary folder isn't suggested as a save-location as this can result in lost work.
- Make sure toolbars don't get enabled after editing the toolbar buttons ([BUG:402679](https://bugs.kde.org/show_bug.cgi?id=402679))
- Do not crash when loading a tiled TIFF file with planar color data. ([BUG:407171](https://bugs.kde.org/show_bug.cgi?id=407171))
- Fix freezes when changing some brush properties or curves ([BUG:410158](https://bugs.kde.org/show_bug.cgi?id=410158))
- Fix wrong borders in the Edge Detection and Height To Normal Map Filters ([BUG:411922](https://bugs.kde.org/show_bug.cgi?id=411922))
- Fix outline of Group Layers in Move Tool and Transform Tool ([BUG:392717](https://bugs.kde.org/show_bug.cgi?id=392717))
- Fix preview of shape layers in Transform Tool and Move Tool ([BUG:392717](https://bugs.kde.org/show_bug.cgi?id=392717))
- Raise the maximum FPS limit to 300 fps from 100 fps
- Do not allow clone layers from pass-through group layers ([BUG:409949](https://bugs.kde.org/show_bug.cgi?id=409949))
- Fix the color of a selected shape being synchronized with the color selectors ([BUG:381784](https://bugs.kde.org/show_bug.cgi?id=381784))
- Fix updating the current shape color when doing undo/redo ([BUG:404975](https://bugs.kde.org/show_bug.cgi?id=404975))
- Fix the broken TestKisSwatchGroup test ([BUG:410387](https://bugs.kde.org/show_bug.cgi?id=410387)) Patch by Krysztof Kurek.
- Make the splash render pixel-perfect on fractionally scaled displays. Patch by Guo Yunhe.
- Fix a crash in Feather Selection, Wavelets, Blur and Edge Detection ([BUG:412057](https://bugs.kde.org/show_bug.cgi?id=412057))
- Include reference images in the screen color picker ([BUG:411816](https://bugs.kde.org/show_bug.cgi?id=411816)) Patch by Matthias Wein.
- Clean up the SVG files used for icons and license the SVG files properly. Patch by Raghavendra Kamath.
- Fix updating the assistants when moving the handles. Patch by Matthias Wein.
- Fix a bad memory corruption error color handling. Patch by Matthias Wein.

## Download

### Windows

- 64 bits Windows: [krita-x64-4.2.7.1-setup.exe](https://download.kde.org/stable/krita/4.2.7.1/krita-x64-4.2.7.1-setup.exe)
- Portable 64 bits Windows: [krita-x64-4.2.7.1.zip](https://download.kde.org/stable/krita/4.2.7.1/krita-x64-4.2.7.1.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.2.7.1/krita-x64-4.2.7.1-dbg.zip)

- 32 bits Windows: [krita-x86-4.2.7.1-setup.exe](https://download.kde.org/stable/krita/4.2.7.1/krita-x86-4.2.7.1-setup.exe)
- Portable 32 bits Windows: [krita-x86-4.2.7.1.zip](https://download.kde.org/stable/krita/4.2.7.1/krita-x86-4.2.7.1.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.2.7.1/krita-x86-4.2.7.1-dbg.zip)

### Linux

- 64 bits Linux: [krita-4.2.7.1b-x86_64.appimage](https://download.kde.org/stable/krita/4.2.7.1/krita-4.2.7.1-x86_64.appimage)
- 64 bits Linux [G'Mic-Qt plugin appimage](https://download.kde.org/stable/krita/4.2.7.1/gmic_krita_qt-x86_64.appimage).

(If, for some reason, Firefox thinks it needs to load this as text: to download, right-click on the link.)

### OSX

- OSX disk image: [krita-4.2.7.1.dmg](https://download.kde.org/stable/krita/4.2.7.1/b/krita-4.2.7.1.dmg)

Note: the gmic-qt is not available on OSX.

### Source code

Note: Linux distributions building Krita against Qt 5.13 have to be aware that a regression in Qt crashes Krita on exit. There's a workaround for that, but that was not ready for this release.

- [krita-4.2.7.1.tar.gz](https://download.kde.org/stable/krita/4.2.7.1/krita-4.2.7.1.tar.gz)
- [krita-4.2.7.1.tar.xz](https://download.kde.org/stable/krita/4.2.7.1/krita-4.2.7.1.tar.xz)

### md5sum

For all downloads:

- [md5sum.txt](https://download.kde.org/stable/krita/4.2.7.1/md5sum.txt)

## Support Krita

Krita is a free and open source project. Please consider supporting the project with [donations](/support-us/donations/) or by [buying training videos or the artbook!](/support-us/shop) With your support, we can keep the core team working on Krita full-time.

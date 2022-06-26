---
title: "Krita 4.1.5 Released"
date: "2018-10-11"
categories: 
  - "news"
  - "officialrelease"
---

Coming hot on the heels of Krita 4.1.3, which had an unfortunate accident to the TIFF plugin, we're releasing Krita 4.1.5 today! There's a lot more than just that fix, though, since we're currently celebrating the last week of the Krita Fundraiser by having a _very_ productive development sprint in Deventer, the Netherlands.

[![](/images/posts/2018/2018-fundraiser-hero2.png)](https://krita.org)

There are some nice highlights as well, like much improved support for scaling on hi-dpi or retina screens. But here's a full list of more than fifty fixes:

- Associate Krita with .ico files
- Auto-update the device pixel ration when changing screens
- Disable autoscrolling for the pan tool
- Disable drag & drop in the recent documents list [BUG:399397](https://bugs.kde.org/show_bug.cgi?id=399397)
- Disable zoom-in/out actions when editing text in rich-text mode [BUG:399157](https://bugs.kde.org/show_bug.cgi?id=399157)
- Do not add template files to recent documents list [BUG:398877](https://bugs.kde.org/show_bug.cgi?id=398877)
- Do not allow creating masks on locked layers. [BUG:399145](https://bugs.kde.org/show_bug.cgi?id=399145)
- Do not close the settings dialog when pressing enter while searching for a shortcut [BUG:399116](https://bugs.kde.org/show_bug.cgi?id=399116)
- Fill polyline shapes if some fill style was selected [BUG:399135](https://bugs.kde.org/show_bug.cgi?id=399135)
- Fix Tangent Normal paintop to work with 16 and 32 bit floating point images [BUG:398826](https://bugs.kde.org/show_bug.cgi?id=398826)
- Fix a blending issue with the color picker when picking a color for the first time [BUG:394399](http://394399)
- Fix a problem with namespaces when loading SVG
- Fix an assert when right-clicking the animation timeline [BUG:399435](https://bugs.kde.org/show_bug.cgi?id=399435)
- Fix autohiding the color selector popup
- Fix canvas scaling in hidpi mode [BUG:360541](https://bugs.kde.org/show_bug.cgi?id=360541)
- Fix deleting canvas input settings shortcuts [BUG:385662](https://bugs.kde.org/show_bug.cgi?id=385662)
- Fix loading multiline text with extra mark-up [BUG:399227](https://bugs.kde.org/show_bug.cgi?id=399227)
- Fix loading of special unicode whitespace characters [BUG:392710](https://bugs.kde.org/show_bug.cgi?id=392710)
- Fix loading the alpha channel from Photoshop TIFF files [BUG:376950](https://bugs.kde.org/show_bug.cgi?id=376950)
- Fix missing shortcut from Fill Tool tooltip. [BUG:399111](https://bugs.kde.org/show_bug.cgi?id=399111)
- Fix projection update after undoing create layer [BUG:399575](https://bugs.kde.org/show_bug.cgi?id=399575)
- Fix saving layer lock, alpha lock and alpha inheritance. [BUG:399513](https://bugs.kde.org/show_bug.cgi?id=399513)
- Fix saving the location of audio source files in .kra files
- Fix selections and transform tool overlay when Mirror Axis is active [BUG:395222](https://bugs.kde.org/show_bug.cgi?id=395222)
- Fix setting active session after creating a new one
- Fix showing the color selector popup in hover mode
- Fix the ctrl-w close window shortcut on Windows [BUG:399339](https://bugs.kde.org/show_bug.cgi?id=399339)
- Fix the overview docker [BUG:396922](https://bugs.kde.org/show_bug.cgi?id=396922), [BUG:384033](https://bugs.kde.org/show_bug.cgi?id=384033)
- Fix the shift-I color selector shortcut
- Fix unsuccessful restoring of a session blocking Krita from closing [BUG:399203](https://bugs.kde.org/show_bug.cgi?id=399203)
- Import SVG files as vector layers instead of pixel layers [BUG:399166](https://bugs.kde.org/show_bug.cgi?id=399166)
- Improve spacing between canvas input setting categories
- Make Krita merge layers correctly if the order of selecting layers is not top-down. [BUG:399146](https://bugs.kde.org/show_bug.cgi?id=399146)
- Make it possible to select the SVG text tool text has been moved inside an hidden group and then made visible again [BUG:395412](https://bugs.kde.org/show_bug.cgi?id=395412)
- Make the color picker pick the alpha channel value correctly. [BUG:399169](https://bugs.kde.org/show_bug.cgi?id=399169)
- Prevent opening filter dialogs on non-editable layers. [BUG:398915](https://bugs.kde.org/show_bug.cgi?id=398915)
- Reset the brush preset selection docker on creating a new document [BUG:399340](https://bugs.kde.org/show_bug.cgi?id=399340)
- Support fractional display scaling factors
- Update color history after fill [BUG:379199](https://bugs.kde.org/show_bug.cgi?id=379199)

## Download

### Windows

Note for Windows users: if you encounter crashes, please follow [these instructions](https://docs.krita.org/en/reference_manual/dr_minw_debugger.html#dr-minw) to use the debug symbols so we can figure out where Krita crashes.

- 64 bits Windows: [krita-x64-4.1.5-setup.exe](https://download.kde.org/stable/krita/4.1.5/krita-x64-4.1.5-setup.exe)
- Portable 64 bits Windows: [krita-x64-4.1.5.zip](https://download.kde.org/stable/krita/4.1.5/krita-x64-4.1.5.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.1.5/krita-x64-4.1.5-dbg.zip)

- 32 bits Windows: [krita-x86-4.1.5-setup.exe](https://download.kde.org/stable/krita/4.1.5/krita-x86-4.1.5-setup.exe)
- Portable 32 bits Windows: [krita-x86-4.1.5.zip](https://download.kde.org/stable/krita/4.1.5/krita-x86-4.1.5.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.1.5/krita-x86-4.1.5-dbg.zip)

### Linux

- 64 bits Linux: [krita-4.1.5-x86_64.appimage](https://download.kde.org/stable/krita/4.1.5/krita-4.1.5-x86_64.appimage)
- 64 bits Linux [G'Mic-Qt plugin appimage](https://download.kde.org/stable/krita/4.1.5/gmic_krita_qt-x86_64.appimage).

(If, for some reason, Firefox thinks it needs to load this as text: to download, right-click on the link.)

When it is updated, you can also use the [Krita Lime PPA](https://launchpad.net/%7Ekritalime/+archive/ubuntu/ppa) to install Krita 4.1.5 on Ubuntu and derivatives. We are working on an updated snap.

### OSX

- OSX disk image: [krita-4.1.5.1.dmg](https://download.kde.org/stable/krita/4.1.5/krita-4.1.5.1.dmg)

Note: the touch docker, gmic-qt and python plugins are not available on OSX.

### Source code

- Source code: [krita-4.1.5.tar.gz](https://download.kde.org/stable/krita/4.1.5/krita-4.1.5.tar.gz)

### md5sum

For all downloads:

- [md5sum.txt](https://download.kde.org/stable/krita/4.1.5/md5sum.txt)

### Key

The Linux appimage and the source tarball are signed. You can retrieve the public key over https here: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8). The signatures are [here](http://download.kde.org/stable/krita/4.1.5/) (filenames ending in .sig).

## Support Krita

Krita is a free and open source project. Please consider supporting the project with [donations](/support-us/donations/) or by [buying training videos or the artbook!](/support-us/shop) With your support, we can keep the core team working on Krita full-time.

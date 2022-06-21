---
title: "Krita 4.1.1 Released"
date: "2018-07-18"
categories: 
  - "news"
  - "officialrelease"
---

Today we're releasing Krita 4.1.1, the first bug fix release for Krita 4.1.0.

- Fix loading PyKrita when using PyQt 5.11 (patch by Antonio Rojas, thanks!) ([BUG:396381](https://bugs.kde.org/show_bug.cgi?id=396381))
- Fix possible crashes with vector objects ([BUG:396145](https://bugs.kde.org/show_bug.cgi?id=396145))
- Fix an issue when resizing pixel brushes in the brush editor ([BUG:396136](https://bugs.kde.org/show_bug.cgi?id=396136))
- Fix loading the system language on macOS if more than one language is enabled in macOS
- Don't show the unimplemented color picker button in the vector object tool properties docker ([BUG:389525](https://bugs.kde.org/show_bug.cgi?id=389525))
- Fix activation of the autosave time after a modify, save, modify cycle ([BUG:393266](https://bugs.kde.org/show_bug.cgi?id=393266))
- Fix out-of-range lookups in the cross-channel curve filter ([BUG:396244](https://bugs.kde.org/show_bug.cgi?id=396244))
- Fix an assert when pressing PageUp into the reference images layer
- Avoid a crash when merging layers in isolated mode ([BUG:395981](https://bugs.kde.org/show_bug.cgi?id=395981))
- Fix loading files with a transformation mask that uses the box transformation filter ([BUG:395979](https://bugs.kde.org/show_bug.cgi?id=395979))
- Fix activating the transform tool if the Box transformation filter was selected ([BUG:395979](https://bugs.kde.org/show_bug.cgi?id=395979))
- Warn the user when using an unsupported version of Windows
- Fix a crash when hiding the last visible channel ([BUG:395301](https://bugs.kde.org/show_bug.cgi?id=395301))
- Make it possible to load non-conforming GPL palettes like https://lospec.com/palette-list/endesga-16
- Simplify display of the warp transformation grid
- Re-add the Invert Selection menu entry ([BUG:395764](https://bugs.kde.org/show_bug.cgi?id=395764))
- Use KFormat to show formatted numbers (Patch by Pino Toscano, thanks!)
- Hide the color sliders config page
- Don't pick colors from fully transparent reference images ([BUG:396358](https://bugs.kde.org/show_bug.cgi?id=396358))
- Fix a crash when embedding a reference image
- Fix some problems when saving and loading reference images ([BUG:396143](https://bugs.kde.org/show_bug.cgi?id=396143))
- Fix the color picker tool not working on reference images ([BUG:396144](https://bugs.kde.org/show_bug.cgi?id=396144))
- Extend the panning range to include any reference images

## Download

### Windows

Note for Windows users: if you encounter crashes, please follow [these instructions](https://docs.krita.org/en/reference_manual/dr_minw_debugger.html#dr-minw) to use the debug symbols so we can figure out where Krita crashes.

- 64 bits Windows: [krita-x64-4.1.1-setup.exe](https://download.kde.org/stable/krita/4.1.1/krita-x64-4.1.1-setup.exe)
- Portable 64 bits Windows: [krita-x64-4.1.1.zip](https://download.kde.org/stable/krita/4.1.1/krita-x64-4.1.1.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.1.1/krita-x64-4.1.1-dbg.zip)

- 32 bits Windows: [krita-x86-4.1.1-setup.exe](https://download.kde.org/stable/krita/4.1.1/krita-x86-4.1.1-setup.exe)
- Portable 32 bits Windows: [krita-x86-4.1.1.zip](https://download.kde.org/stable/krita/4.1.1/krita-x86-4.1.1.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.1.1/krita-x86-4.1.1-dbg.zip)

### Linux

- 64 bits Linux: [krita-4.1.1-x86\_64.appimage](https://download.kde.org/stable/krita/4.1.1/krita-4.1.1-x86_64.appimage)
- 64 bits Linux [G'Mic-Qt plugin appimage](https://download.kde.org/stable/krita/4.1.1/gmic_krita_qt-x86_64.appimage).

(If, for some reason, Firefox thinks it needs to load this as text: to download, right-click on the link.)

When it is updated, you can also use the [Krita Lime PPA](https://launchpad.net/%7Ekritalime/+archive/ubuntu/ppa) to install Krita 4.1.1 on Ubuntu and derivatives. We are working on an updated snap.

### OSX

- OSX disk image: [krita-4.1.1.dmg](https://download.kde.org/stable/krita/4.1.1/krita-4.1.1.dmg)

Note: the touch docker, gmic-qt and python plugins are not available on OSX.

### Source code

- Source code: [krita-4.1.1.tar.gz](https://download.kde.org/stable/krita/4.1.1/krita-4.1.1.tar.gz)

### md5sum

For all downloads:

- [md5sum.txt](https://download.kde.org/stable/krita/4.1.1/md5sum.txt)

### Key

The Linux appimage and the source tarball are signed. You can retrieve the public key over https here: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8). The signatures are [here](http://download.kde.org/stable/krita/4.1.1/) (filenames ending in .sig).

## Support Krita

Krita is a free and open source project. Please consider supporting the project with [donations](/support-us/donations/) or by [buying training videos or the artbook!](/support-us/shop) With your support, we can keep the core team working on Krita full-time.

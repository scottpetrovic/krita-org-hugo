---
title: "Krita 3.2.0: We Have a Release Candidate!"
date: "2017-08-07"
---

After last week's rollercoaster ride (if you haven't seen it, check the [news,](/item/krita-foundation-in-trouble/) then the [update](/item/krita-foundation-update/)!), it was hard to get back into making releases and writing code. Yet, here is the release candidate for Krita 3.2.0. Fixes since the second beta include:

- Some cleanups when handling OpenGL
- Show a clearer error when loading the wintab32.dll file fails on Windows
- Fix a regression where bezier tools couldn't close the curve and couldn't create a second curve
- Fixes for working with multiple windows in subwindow mode where one of the documents is set to "stays on top"
- Fix resetting the Level of Detail cache when changing the visibility of a layer: this fixes an issue where after changing the visibility of a layer, the color picker would pick from an older version of the layer.
- Save the last used folder in the Reference Images Docker
- Don't create nested autosave documents.
- Add recognizing uc-logic tablets on Linux
- Improve the stabilizer
- Improve the communication between Krita and the gmic-qt plugin
- Fix progress reporting after the gmic-qt filter returns
- Fix loading a custom brush preset that uses the text brush
- Update the new brush preset set

### Download

#### Windows

Note for Windows users: if you encounter crashes, please follow [these instructions](https://docs.krita.org/Dr._Mingw_debugger) to use the debug symbols so we can figure out where Krita crashes.

- 32 bits Windows: [krita-3.2.0-rc.1-x86-setup.exe](https://download.kde.org/unstable/krita/3.2.0-rc.1/krita-3.2.0-rc.1-x86-setup.exe)
- Portable 32 bits Windows: [krita-3.2.0-rc.1-x86.zip](https://download.kde.org/unstable/krita/3.2.0-rc.1/krita-3.2.0-rc.1-x86.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/unstable/krita/3.2.0-rc.1/krita-3.2.0-rc.1-x86-dbg.zip)

- 64 bits Windows: [krita-3.2.0-rc.1-x64-setup.exe](https://download.kde.org/unstable/krita/3.2.0-rc.1/krita-3.2.0-rc.1-x64-setup.exe)
- Portable 64 bits Windows: [krita-3.2.0-rc.1-x64.zip](https://download.kde.org/unstable/krita/3.2.0-rc.1/krita-3.2.0-rc.1-x64.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/unstable/krita/3.2.0-rc.1/krita-3.2.0-rc.1-x64-dbg.zip)

- Explorer Shell extension: [kritashellex-1.2.4.0-setup.exe](https://download.kde.org/stable/krita/KritaShellExtension-v1.2.4-setup.exe)

#### Linux

- - 64 bits Linux: [krita-3.2.0-rc.1-x86_64.appimage](https://download.kde.org/unstable/krita/3.2.0-rc.1/krita-3.2.0-rc.1-x86_64.appimage)

(If, for some reason, Firefox thinks it needs to load this as text: to download, right-click on the link.)

When it is updated, you can also use the [Krita Lime PPA](https://launchpad.net/%7Ekritalime/+archive/ubuntu/ppa) to install Krita 3.2.0-rc.1 on Ubuntu and derivatives.

#### OSX

- OSX disk image: [krita-3.2.0-rc.1.dmg](https://download.kde.org/unstable/krita/3.2.0-rc.1/krita-3.2.0-rc.1.dmg)

### Source code

- Source code: [krita-3.2.0-rc.1.tar.gz](https://download.kde.org/unstable/krita/3.2.0-rc.1/krita-3.2.0-rc.1.tar.gz)

#### md5sums

For all downloads:

- [md5sums.txt](https://download.kde.org/unstable/krita/3.2.0-rc.1/md5sums.txt)

#### Key

The Linux appimage and the source tarball are signed. You can retrieve the public key over https here: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8). The signatures are [here](http://download.kde.org/unstable/krita/3.2.0-rc.1/).

#### Support Krita

Krita is a free and open source project. Please consider supporting the project with [donations](/support-us/donations/) or by [buying training videos or the artbook!](/support-us/shop) With your support, we can keep the core team working on Krita full-time.

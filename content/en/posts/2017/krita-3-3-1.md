---
title: "Krita 3.3.1"
date: "2017-10-11"
---

Today we are releasing Krita 3.3.1, a bugfix release for Krita 3.3.0. This release fixes two important regressions:

- Krita would crash if you would restart Krita after closing Krita with the reference images docker set to floating
- Krita 3.3.0 could not read .kra backup files or .kra files that were unzipped, then zipped up manually.

Additionally, there are the following fixes and improvements:

- Fix a crash when creating a swap file on OSX (Bernhard Liebl).
- Merge down does not remove locked layers anymore (Nikita Smirnov)
- Various performance improvements, especially for macOS (Bernhard Liebl)
- Improve the look and feel of dragging and dropping layers (Bernhard Liebl)
- Improve the tooltips in the brush preset selector (Bernhard Liebl)
- Fix a memory leak in the color selectors (Boudewijn Rempt)
- Fix rotation and tilt when using the Windows Ink api (Alvin Wong)
- Don't allow the fill tool to be used on group layers (Boudewijn Rempt)
- Add brightness and contrast sliders for textured brushes (Rad)
- Add paste-at-cursor (Dmitry Kazakov)
- Improve performance of the cpu canvas (Alvin Wong)
- Fix a crash on closing Krita when there is something on the clipboard (Dmitry Kazakov)
- Add a button to open a file layer's image in Krita (Wolthera van Hövell tot Westerflier)

### Download

#### Windows

Note for Windows users: if you encounter crashes, please follow [these instructions](https://docs.krita.org/Dr._Mingw_debugger) to use the debug symbols so we can figure out where Krita crashes.

- 64 bits Windows: [krita-3.3.1-x64-setup.exe](https://download.kde.org/stable/krita/3.3.1/krita-3.3.1-x64-setup.exe)
- Portable 64 bits Windows: [krita-3.3.1-x64.zip](https://download.kde.org/stable/krita/3.3.1/krita-3.3.1-x64.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/3.3.1/krita-3.3.1-x64-dbg.zip)

- 32 bits Windows: [krita-3.3.1-x86-setup.exe](https://download.kde.org/stable/krita/3.3.1/krita-3.3.1-x86-setup.exe)
- Portable 32 bits Windows: [krita-3.3.1-x86.zip](https://download.kde.org/stable/krita/3.3.1/krita-3.3.1-x86.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/3.3.1/krita-3.3.1-x86-dbg.zip)

- Explorer Shell extension: [kritashellex-1.2.4.0-setup.exe](https://download.kde.org/stable/krita/KritaShellExtension-v1.2.4-setup.exe)

#### Linux

- 64 bits Linux: [krita-3.3.1-x86_64.appimage](https://download.kde.org/stable/krita/3.3.1/krita-3.3.1-x86_64.appimage)

(If, for some reason, Firefox thinks it needs to load this as text: to download, right-click on the link.)

When it is updated, you can also use the [Krita Lime PPA](https://launchpad.net/%7Ekritalime/+archive/ubuntu/ppa) to install Krita 3.3.1 on Ubuntu and derivatives. There is also an updated snap.

#### OSX

- OSX disk image: [krita-3.3.1.dmg](https://download.kde.org/stable/krita/3.3.1/krita-3.3.1.dmg)

Note: the gmic-qt and pdf plugins are not available on OSX.

### Source code

- Source code: [krita-3.3.1.tar.gz](https://download.kde.org/stable/krita/3.3.1/krita-3.3.1.tar.gz)

#### md5sums

For all downloads:

- [md5sums.txt](https://download.kde.org/stable/krita/3.3.1/md5sums.txt)

#### Key

The Linux appimage and the source tarball are signed. You can retrieve the public key over https here: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8). The signatures are [here](http://download.kde.org/stable/krita/3.3.1/).

#### Support Krita

Krita is a free and open source project. Please consider supporting the project with [donations](/support-us/donations/) or by [buying training videos or the artbook!](/support-us/shop) With your support, we can keep the core team working on Krita full-time.

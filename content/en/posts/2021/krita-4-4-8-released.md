---
title: "Krita 4.4.8 Released"
date: "2021-08-25"
categories: 
  - "news"
  - "officialrelease"
---

This is strictly a bug fix release. There are two changes: we fixed an issue with saving a .kra file with an embedded palette, which was broken leading to dataloss, and, for Windows, support for fractional HiDPI display scaling is now disabled by default.

## Download

### Windows

If you're using the portable zip files, just open the zip file in Explorer and drag the folder somewhere convenient, then double-click on the krita icon in the folder. This will not impact an installed version of Krita, though it will share your settings and custom resources with your regular installed version of Krita. For reporting crashes, also get the debug symbols folder.

Note that we are not making 32 bits Windows builds anymore.

- 64 bits Windows Installer: [krita-x64-4.4.8-setup.exe](https://download.kde.org/stable/krita/4.4.8/krita-x64-4.4.8-setup.exe)
- Portable 64 bits Windows: [krita-x64-4.4.8.zip](https://download.kde.org/stable/krita/4.4.8/krita-x64-4.4.8.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.4.8/krita-x64-4.4.8-dbg.zip)

### Linux

- 64 bits Linux: [krita-4.4.8-x86\_64.appimage](https://download.kde.org/stable/krita/4.4.8/krita-4.4.8-x86_64.appimage)
- 64 bits Linux [G'Mic-Qt plugin appimage](https://download.kde.org/stable/krita/4.4.8/gmic_krita_qt-x86_64.appimage)

(If, for some reason, Firefox thinks it needs to load this as text: to download, right-click on the link.)

### macOS

Note: if you use macOS Sierra or High Sierra, please [check this video](https://www.youtube.com/watch?v=3py0kgq95Hk) to learn how to enable starting developer-signed binaries, instead of just Apple Store binaries.

- macOS disk image: [krita-4.4.8.dmg](https://download.kde.org/stable/krita/4.4.8/krita-4.4.8.dmg)

Note: the gmic-qt is not available on macOS.

### Android

It was not possible to build Krita 4.4.8 for Android at this point, because the build system was changed to make the Krita 5.0 beta 1 build possible.

### Source code

- [krita-4.4.8.tar.gz](https://download.kde.org/stable/krita/4.4.8/krita-4.4.8.tar.gz)
- [krita-4.4.8.tar.xz](https://download.kde.org/stable/krita/4.4.8/krita-4.4.8.tar.xz)

### md5sum

For all downloads:

- [md5sum.txt](https://download.kde.org/stable/krita/4.4.8/md5sum.txt)

### Key

The Linux appimage and the source .tar.gz and .tar.xz tarballs are signed. The signatures are [here](https://download.kde.org/stable/krita/4.4.8/) (filenames ending in .sig). You can retrieve the public key [here](https://files.kde.org/krita/4DA79EDA231C852B).

## Support Krita

Krita is a free and open source project. Please consider supporting the project with [donations](https://fund.krita.org) or by [buying training videos!](/shop/) With your support, we can keep the core team working on Krita full-time.

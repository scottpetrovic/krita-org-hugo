---
title: "Krita 4.2.0 Beta Released"
date: "2019-05-16"
categories: 
  - "development-builds"
---

We're still on track to release Krita 4.2.0 this month! Compared to the [alpha release](/item/krita-4-2-0-alpha-released/), we fixed over thirty issues. This release also has a fresh splash screen by Tyson Tan and restores Python support to the Linux AppImage. The Linux AppImage does not have support for sound, the macOS build does not have support for G'Mic.

[![](/images/posts/2019/electrichearts_20190316_kiki_a_sm-1.png)](/images/posts/2019/electrichearts_20190316_kiki_a_sm-1.png)

**Warning**: Linux users should be careful with distribution packages. We have a [host of patches for Qt queued up](https://phabricator.kde.org/T10838), some of which are important for distributions to carry until the patches are merged and released in a new version of Qt.

## Download

### Windows

Note for Windows users: if you encounter crashes, please follow [these instructions](https://docs.krita.org/en/reference_manual/dr_minw_debugger.html#dr-minw) to use the debug symbols so we can figure out where Krita crashes.

- 64 bits Windows: [krita-x64-4.2.0-beta2-setup.exe](https://download.kde.org/unstable/krita/4.2.0-beta2/krita-x64-4.2.0-beta2-setup.exe)
- Portable 64 bits Windows: [krita-x64-4.2.0-beta2.zip](https://download.kde.org/unstable/krita/4.2.0-beta2/krita-x64-4.2.0-beta2.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/unstable/krita/4.2.0-beta2/krita-x64-4.2.0-beta2-dbg.zip)

- 32 bits Windows: [krita-x86-4.2.0-beta2-setup.exe](https://download.kde.org/unstable/krita/4.2.0-beta2/krita-x86-4.2.0-beta2-setup.exe)
- Portable 32 bits Windows: [krita-x86-4.2.0-beta2.zip](https://download.kde.org/unstable/krita/4.2.0-beta2/krita-x86-4.2.0-beta2.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/unstable/krita/4.2.0-beta2/krita-x86-4.2.0-beta2-dbg.zip)

### Linux

- 64 bits Linux: [krita-4.2.0-beta-x86\_64.appimage](https://download.kde.org/unstable/krita/4.2.0-beta2/krita-4.2.0-beta-x86_64.appimage)
- 64 bits Linux [G'Mic-Qt plugin appimage](https://download.kde.org/unstable/krita/4.2.0-beta2/gmic_krita_qt-x86_64.appimage).

(If, for some reason, Firefox thinks it needs to load this as text: to download, right-click on the link.)

### OSX

- OSX disk image: [krita-4.2.0-beta2.dmg](https://download.kde.org/unstable/krita/4.2.0-beta2/krita-4.2.0-beta2.dmg)

Note: the touch docker, gmic-qt and python plugins are not available on OSX.

### Source code

- [krita-4.2.0-beta2.tar.gz](https://download.kde.org/unstable/krita/4.2.0-beta2/krita-4.2.0-beta2.tar.gz)
- [krita-4.2.0-beta2.tar.xz](https://download.kde.org/unstable/krita/4.2.0-beta2/krita-4.2.0-beta2.tar.xz)

### md5sum

For all downloads:

- [md5sum.txt](https://download.kde.org/unstable/krita/4.2.0-beta2/md5sum.txt)

### Key

The Linux appimage and the source tarball are signed. You can retrieve the public key over https here: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8). The signatures are [here](http://download.kde.org/unstable/krita/4.2.0-beta2/) (filenames ending in .sig).

## Support Krita

Krita is a free and open source project. Please consider supporting the project with [donations](/support-us/donations/) or by [buying training videos or the artbook!](/support-us/shop) With your support, we can keep the core team working on Krita full-time.

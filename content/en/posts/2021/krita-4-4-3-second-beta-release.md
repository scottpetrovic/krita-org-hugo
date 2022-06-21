---
title: "Krita 4.4.3: Second Beta Release"
date: "2021-03-12"
categories: 
  - "development-builds"
  - "news"
---

We're releasing the second beta for Krita 4.4.3 today. This version only fixes regressions found in the first beta, but it still needs testing!

- Thanks to Jonathan Wakely, Krita 4.4.3 beta 2 now can be compiled with GCC 11.
- Fixed: a crash when showing the popup palette on Linux if the display was set to 125% ([BUG:431944](https://bugs.kde.org/show_bug.cgi?id=431944))
- Fixed: tiling artefacts in the oilpaint filter
- Fixed an issue showing that there are updates available in the welcome screen when the latest version was already running
- If the image name no longer fits the tab, the right-hand side is elided, instead of the middle
- Fixed: using shortcuts with special keys on non-US layouts ([BUG:430479](https://bugs.kde.org/show_bug.cgi?id=430479))

## Download

### Windows

If you're using the portable zip files, just open the zip file in Explorer and drag the folder somewhere convenient, then double-click on the krita icon in the folder. This will not impact an installed version of Krita, though it will share your settings and custom resources with your regular installed version of Krita. For reporting crashes, also get the debug symbols folder.

- 64 bits Windows Installer: [krita-x64-4.4.3-beta2-setup.exe](https://download.kde.org/unstable/krita/4.4.3-beta2/krita-x64-4.4.3-beta2-setup.exe)
- Portable 64 bits Windows: [krita-x64-4.4.3-beta2.zip](https://download.kde.org/unstable/krita/4.4.3-beta2/krita-x64-4.4.3-beta2.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/unstable/krita/4.4.3-beta2/krita-x64-4.4.3-beta2-dbg.zip)

- 32 bits Windows Installer: [krita-x86-4.4.3-beta2-setup.exe](https://download.kde.org/unstable/krita/4.4.3-beta2/krita-x86-4.4.3-beta2-setup.exe)
- Portable 32 bits Windows: [krita-x86-4.4.3-beta2.zip](https://download.kde.org/unstable/krita/4.4.3-beta2/krita-x86-4.4.3-beta2.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/unstable/krita/4.4.3-beta2/krita-x86-4.4.3-beta2-dbg.zip)

### Linux

- 64 bits Linux: [krita-4.4.3-beta2-x86\_64.appimage](https://download.kde.org/unstable/krita/4.4.3-beta2/krita-4.4.3-beta2-x86_64.appimage)
- 64 bits Linux [G'Mic-Qt plugin appimage](https://download.kde.org/unstable/krita/4.4.3-beta2/gmic_krita_qt-x86_64.appimage)

(If, for some reason, Firefox thinks it needs to load this as text: to download, right-click on the link.)

### OSX

- OSX disk image: [krita-4.4.3-beta2.dmg](https://download.kde.org/unstable/krita/4.4.3-beta2/krita-4.4.3-beta2.dmg)

Note: the gmic-qt plugin is not yet available on OSX.

### Android

This time, the Android releases are made from the release tarball, so there are translations. We consider Krita on ChromeOS and Android still **_beta_**. There are many things that don't work and other things that are impossible without a real keyboard.

- [64 bits Intel CPU APK](https://download.kde.org/unstable/krita/4.4.3-beta2/krita_x86_64_apk-4.4.3-beta2.apk)
- [32 bits Intel CPU APK](https://download.kde.org/unstable/krita/4.4.3-beta2/krita_x86_apk-4.4.3-beta2.apk)
- [64 bits Arm CPU APK](https://download.kde.org/unstable/krita/4.4.3-beta2/krita_arm64-v8a_apk-4.4.3-beta2.apk)
- [32 bits Arm CPU APK](https://download.kde.org/unstable/krita/4.4.3-beta2/krita_armeabi-v7a_apk-4.4.3-beta2.apk)

### Source code

- [krita-4.4.3-beta2.tar.gz](https://download.kde.org/unstable/krita/4.4.3-beta2/krita-4.4.3-beta2.tar.gz)
- [krita-4.4.3-beta2.tar.xz](https://download.kde.org/unstable/krita/4.4.3-beta2/krita-4.4.3-beta2.tar.xz)

### md5sum

For all downloads:

- [md5sum.txt](https://download.kde.org/unstable/krita/4.4.3-beta2/md5sum.txt)

### Key

The Linux appimages and the source .tar.gz and .tar.xz tarballs are signed. You can retrieve the public key with gpg: "gpg --recv-key 7468332F". The signatures are [here](https://download.kde.org/unstable/krita/4.4.3-beta2/) (filenames ending in .sig).

## Support Krita

Krita is a free and open source project. Please consider supporting the project with [donations](/support-us/donations/) or by [buying training videos!](/support-us/shop) With your support, we can keep the core team working on Krita full-time.

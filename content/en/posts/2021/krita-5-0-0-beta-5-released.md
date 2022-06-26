---
title: "Krita 5.0.0 beta 5 released"
date: "2021-12-03"
categories: 
  - "development-builds"
  - "news"
---

Following the botched macOS build yesterday, we're releasing Krita 5.0.0 beta 5. Beta 4 didn't happen: while it was building, Dmitry Kazakov fixed an issue which we really wanted tested right away.

![](/images/posts/2021/2021-11-16_kiki-piggy-bank_krita5.png) Krita is a free and open source project. Please consider supporting the project with [donations](https://fund.krita.org) or by [buying training videos!](/shop/) With your support, we can keep the core team working on Krita full-time.

This release has the following fixes since beta 3

- The macOS build works again...
- Fix an issue with the resource selector where the wrong resource would be selected
- Only save color palettes if they are modified
- Fix the line height of text shapes being too large
- Fix the size of text in text shapes compared to Krita 4
- Remove the obsolete shortcut for the brightness/contrast filter
- Create MSIX packages of Krita on the binary builder
- Fix wrong animation for preset save dialog
- Fix loading resources from bundles if newer versions of the resource are deleted from the resource folder
- Fix the color model of group layers
- Fix issues with soft proofing
- Fix brush presets that use the gradient map mode

## Download

### Windows

If you're using the portable zip files, just open the zip file in Explorer and drag the folder somewhere convenient, then double-click on the krita icon in the folder. This will not impact an installed version of Krita, though it will share your settings and custom resources with your regular installed version of Krita. For reporting crashes, also get the debug symbols folder.

Note that we are not making 32 bits Windows builds anymore.

- 64 bits Windows Installer: [krita-x64-5.0.0-beta5-setup.exe](https://download.kde.org/unstable/krita/5.0.0-beta5/krita-x64-5.0.0-beta5-setup.exe)
- Portable 64 bits Windows: [krita-x64-5.0.0-beta5.zip](https://download.kde.org/unstable/krita/5.0.0-beta5/krita-x64-5.0.0-beta5.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/unstable/krita/5.0.0-beta5/krita-x64-5.0.0-beta5-dbg.zip)

### Linux

- 64 bits Linux: [krita-5.0.0-beta5-x86_64.appimage](https://download.kde.org/unstable/krita/5.0.0-beta5/krita-5.0.0-beta5-x86_64.appimage)

The separate gmic-qt appimage is no longer needed.

(If, for some reason, Firefox thinks it needs to load this as text: to download, right-click on the link.)

### macOS

Note: if you use macOS Sierra or High Sierra, please [check this video](https://www.youtube.com/watch?v=3py0kgq95Hk) to learn how to enable starting developer-signed binaries, instead of just Apple Store binaries.

- macOS disk image: [krita-5.0.0-beta5.dmg](https://download.kde.org/unstable/krita/5.0.0-beta5/krita-5.0.0-beta5.dmg)

### Android

The Android releases are made from the release tarball, so there are translations. We consider Krita on ChromeOS and Android still **_beta_**. There are many things that don't work and other things that are impossible without a real keyboard.

- [64 bits Intel CPU APK](https://download.kde.org/unstable/krita/5.0.0-beta5/krita-x86_64-5.0.0-beta5-release-signed.apk)
- [32 bits Intel CPU APK](https://download.kde.org/unstable/krita/5.0.0-beta5/krita-x86-5.0.0-beta5-release-signed.apk)
- [64 bits Arm CPU APK](https://download.kde.org/unstable/krita/5.0.0-beta5/krita-arm64-v8a-5.0.0-beta5-release-signed.apk)
- [32 bits Arm CPU APK](https://download.kde.org/unstable/krita/5.0.0-beta5/krita-armeabi-v7a-5.0.0-beta5-release-signed.apk)

### Source code

- [krita-5.0.0-beta5.tar.gz](https://download.kde.org/unstable/krita/5.0.0-beta5/krita-5.0.0-beta5.tar.gz)
- [krita-5.0.0-beta5.tar.xz](https://download.kde.org/unstable/krita/5.0.0-beta5/krita-5.0.0-beta5.tar.xz)

### md5sum

For all downloads:

- [md5sum.txt](https://download.kde.org/unstable/krita/5.0.0-beta5/md5sum.txt)

### Key

The Linux appimage and the source .tar.gz and .tar.xz tarballs are signed. You can retrieve the public key [here](https://files.kde.org/krita/4DA79EDA231C852B). The signatures are [here](https://download.kde.org/unstable/krita/5.0.0-beta5/) (filenames ending in .sig).

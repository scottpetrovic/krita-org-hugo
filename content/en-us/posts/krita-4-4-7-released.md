---
title: "Krita 4.4.7 Released"
date: "2021-08-07"
categories: 
  - "officialrelease"
---

This is strictly a bug fix release. The most important reason for this release is a fix for a performance regression in Krita 4.4.5. There are a few other fixes:

- Fix a crash on exit with certain versions of Qt and PyQt
- Fix moving selection with the magnetic selection tool ([BUG:433633](https://bugs.kde.org/show_bug.cgi?id=433633))
- Fix crashes in the magnetic selection tool when deleting nodes ([BUG:439896](https://bugs.kde.org/show_bug.cgi?id=439896))
- Fix an assert when converting the image color space from Python ([BUG:437980](https://bugs.kde.org/show_bug.cgi?id=437980))
- Fix a crash when closing a gamut mask document ([BUG:438914](https://bugs.kde.org/show_bug.cgi?id=438914))
- Fix drag and drop of clone layers between images ([BUG:414699](https://bugs.kde.org/show_bug.cgi?id=414699))
- Fix crash when saving the image with trimming enabled ([BUG:437626](https://bugs.kde.org/show_bug.cgi?id=437626))

## Download

Note: there is no Krita 4.4.6, that version number was created only for the release on the Epic store.

### Windows

If you're using the portable zip files, just open the zip file in Explorer and drag the folder somewhere convenient, then double-click on the krita icon in the folder. This will not impact an installed version of Krita, though it will share your settings and custom resources with your regular installed version of Krita. For reporting crashes, also get the debug symbols folder.

Note that from this release on we are not making 32 bits Windows builds anymore.

- 64 bits Windows Installer: [krita-x64-4.4.7-setup.exe](https://download.kde.org/stable/krita/4.4.7/krita-x64-4.4.7-setup.exe)
- Portable 64 bits Windows: [krita-x64-4.4.7.zip](https://download.kde.org/stable/krita/4.4.7/krita-x64-4.4.7.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.4.7/krita-x64-4.4.7-dbg.zip)

### Linux

- 64 bits Linux: [krita-4.4.7-x86\_64.appimage](https://download.kde.org/stable/krita/4.4.7/krita-4.4.7-x86_64.appimage)
- 64 bits Linux [G'Mic-Qt plugin appimage](https://download.kde.org/stable/krita/4.4.7/gmic_krita_qt-x86_64.appimage)

(If, for some reason, Firefox thinks it needs to load this as text: to download, right-click on the link.)

### OSX

Note: if you use OSX Sierra or High Sierra, please [check this video](https://www.youtube.com/watch?v=3py0kgq95Hk) to learn how to enable starting developer-signed binaries, instead of just Apple Store binaries.

- OSX disk image: [krita-4.4.7.dmg](https://download.kde.org/stable/krita/4.4.7/krita-4.4.7.dmg)

Note: the gmic-qt is not available on OSX.

### Android

This time, the Android releases are made from the release tarball, so there are translations. We consider Krita on ChromeOS and Android still **_beta_**. There are many things that don't work and other things that are impossible without a real keyboard. You can also get Krita 4.4.7 from [Google Play](https://play.google.com/store/apps/details?id=org.krita).

- [64 bits Intel CPU APK](https://download.kde.org/stable/krita/4.4.7/krita-x86_64-4.4.7-release.apk)
- [32 bits Intel CPU APK](https://download.kde.org/stable/krita/4.4.7/krita-x86-4.4.7-release.apk)
- [64 bits Arm CPU APK](https://download.kde.org/stable/krita/4.4.7/krita-arm64-v8a-4.4.7-release.apk)
- [32 bits Arm CPU APK](https://download.kde.org/stable/krita/4.4.7/krita-armeabi-v7a-4.4.7-release.apk)

### Source code

- [krita-4.4.7.tar.gz](https://download.kde.org/stable/krita/4.4.7/krita-4.4.7.tar.gz)
- [krita-4.4.7.tar.xz](https://download.kde.org/stable/krita/4.4.7/krita-4.4.7.tar.xz)

### md5sum

For all downloads:

- [md5sum.txt](https://download.kde.org/stable/krita/4.4.7/md5sum.txt)

### Key

The Linux appimage and the source .tar.gz and .tar.xz tarballs are signed. You can retrieve the public key with gpg: "gpg --recv-key 7468332F". The signatures are [here](https://download.kde.org/stable/krita/4.4.7/) (filenames ending in .sig).

## Support Krita

Krita is a free and open source project. Please consider supporting the project with [donations](https://fund.krita.org) or by [buying training videos!](https://krita.org/en/shop/) With your support, we can keep the core team working on Krita full-time.

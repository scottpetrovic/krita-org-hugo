---
title: "Krita 5.0.2"
date: "2022-01-07"
categories: 
  - "news"
  - "officialrelease"
---

Hot on the heels of Krita 5.0.0, we're releasing the first bugfix release of Krita 5! It's 5.0.2 because if you upload a beta with the version number 5.0.0 to the Windows Store, you cannot upload 5.0.0 final, but it has to be 5.0.1... So, don't worry, you didn't miss 5.0.1!

This release contains the following fixes:

- Fix a crash when changing the Instant Preview setting of a brush preset.
- Fix a crash when there are ABR brush libraries present with an uppercase ABR extension. [BUG:447454](https://bugs.kde.org/show_bug.cgi?id=447454)
- Fix a similar issue with Krita resource bundles with an upper case .BUNDLE extension
- Fix the macOS entitlements to allow uploading Krita to the Steam Store
- Fix the macOS entitlements so Krita can be accepted by the MacOS App Store
- Make Krita use the native macOS file dialog by default
- Remove the tkInter module from the embedded Python libraries on macOS.
- Fix rendering 16 bit integer images on macOS on the M1 architecture
- Fix a crash when undoing multiple layer operations too quickly. [BUG:447462](https://bugs.kde.org/show_bug.cgi?id=447462)
- Workaround a crash when a transform mask is applied to a passthrough group. [BUG:447506](https://bugs.kde.org/show_bug.cgi?id=447506)
- Filter out two new Epic Store single-dash-multi-character commandline options. Really, Epic, it's bad for to pass commandline parameters in this format!
- Fix toolbox arrow buttons not visible on starting Krita
- Fix the photoshop compatibilty shortcut profile. [BUG:447771](https://bugs.kde.org/show_bug.cgi?id=447771)
- Fix bundling AppimageUpdate into appimages.
- Restore the QImageIO fallback for loading WebP images
- Make the dock widget titlebars so they can be smaller
- Disable all accelerator keys for dockers
- Fix a race condition in the image metadata system
- Fix the tool option widget's layout sporadically going wrong. [BUG:447522](https://bugs.kde.org/show_bug.cgi?id=447522)
- Update fill layers correctly when changing the options from a Python script. [BUG:447807](https://bugs.kde.org/show_bug.cgi?id=447807)
- Fix the built-in file dialog's image preview. [BUG:447806](https://bugs.kde.org/show_bug.cgi?id=447806)
- Fix the slowness opening and closing documents if there are many resource bundles present. [BUG:447298](https://bugs.kde.org/show_bug.cgi?id=447298)
- Fix clicking external urls on Android
- Work around a possible crash on Android due to bugs in Qt's Accessibilty framework.
- Fix importing bundles on Android
- Work around issues with file permissions not being set correctly by ChromeOS

![](../images/2021-11-16_kiki-piggy-bank_krita5.png) Krita is a free and open source project. Please consider supporting the project by [joining the development fund](https://fund.krita.org), [donating](https://krita.org/en/support-us/donations/) or by [buying training videos!](https://krita.org/en/shop/) With your support, we can keep the core team working on Krita full-time.

## Download

### Windows

If you're using the portable zip files, just open the zip file in Explorer and drag the folder somewhere convenient, then double-click on the krita icon in the folder. This will not impact an installed version of Krita, though it will share your settings and custom resources with your regular installed version of Krita. For reporting crashes, also get the debug symbols folder.

Note that we are not making 32 bits Windows builds anymore.

- 64 bits Windows Installer: [krita-x64-5.0.2-setup.exe](https://download.kde.org/stable/krita/5.0.2/krita-x64-5.0.2-setup.exe)
- Portable 64 bits Windows: [krita-x64-5.0.2.zip](https://download.kde.org/stable/krita/5.0.2/krita-x64-5.0.2.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/5.0.2/krita-x64-5.0.2-dbg.zip)

### Linux

- 64 bits Linux: [krita-5.0.2-x86\_64.appimage](https://download.kde.org/stable/krita/5.0.2/krita-5.0.2-x86_64.appimage)

The separate gmic-qt appimage is no longer needed.

(If, for some reason, Firefox thinks it needs to load this as text: to download, right-click on the link.)

### macOS

Note: if you use macOS Sierra or High Sierra, please [check this video](https://www.youtube.com/watch?v=3py0kgq95Hk) to learn how to enable starting developer-signed binaries, instead of just Apple Store binaries.

- macOS disk image: [krita-5.0.2.dmg](https://download.kde.org/stable/krita/5.0.2/krita-5.0.2.dmg)

### Android

We consider Krita on ChromeOS as ready for production. Krita on Android is still **_beta_**. Krita is not available for Android phones, only for tablets, because the user interface needs a large screen.

- [64 bits Intel CPU APK](https://download.kde.org/stable/krita/5.0.2/krita-x86_64-5.0.2-release-signed.apk)
- [32 bits Intel CPU APK](https://download.kde.org/stable/krita/5.0.2/krita-x86-5.0.2-release-signed.apk)
- [64 bits Arm CPU APK](https://download.kde.org/stable/krita/5.0.2/krita-arm64-v8a-5.0.2-release-signed.apk)
- [32 bits Arm CPU APK](https://download.kde.org/stable/krita/5.0.2/krita-armeabi-v7a-5.0.2-release-signed.apk)

### Source code

- [krita-5.0.2.tar.gz](https://download.kde.org/stable/krita/5.0.2/krita-5.0.2.tar.gz)
- [krita-5.0.2.tar.xz](https://download.kde.org/stable/krita/5.0.2/krita-5.0.2.tar.xz)

### md5sum

For all downloads:

- [md5sum.txt](https://download.kde.org/stable/krita/5.0.2/md5sum.txt)

### Key

The Linux appimage and the source .tar.gz and .tar.xz tarballs are signed. You can retrieve the public key [here](https://files.kde.org/krita/4DA79EDA231C852B). The signatures are [here](https://download.kde.org/stable/krita/5.0.2/) (filenames ending in .sig).

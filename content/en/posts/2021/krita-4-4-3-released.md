---
title: "Krita 4.4.3 Released"
date: "2021-03-24"
categories: 
  - "news"
  - "officialrelease"
---

Today, we're releasing Krita 4.4.3. This is strictly a bugfix release. We spend two beta's worth of testing trying to make this a really stable release, because from now on, we're focusing on Krita 5!

This will also be the last Krita release for 32 bits Windows; further releases will be 64 bits only.

This is the first release of Krita with a universal binary for macOS: the DMG contains both an ARM and a X64 build. Note that the main problem with Krita on macOS, OpenGL frame redraws interrupting the input queue is still a problem on both processor architectures.

## Bug Fixes

### Android

- Crash when back button was pressed on splash screen
- Crash when loading files while app is still booting
- Use lastUpdateTime for copying assets
- Provide host so pathPattern could be effective
- Fix color selector covering entire screen ([BUG:432459](https://bugs.kde.org/show_bug.cgi?id=432459))
- Saved configs aren't loaded after restart ([BUG:432433](https://bugs.kde.org/show_bug.cgi?id=432433))
- Add key functions to psd_layer_effects_shadow_base ([BUG:432904](https://bugs.kde.org/show_bug.cgi?id=432904))
- Fix reloading presets from user-imported bundles ([BUG:432488](https://bugs.kde.org/show_bug.cgi?id=432488))

### Crashes

- Fix crash in halftone filter due to an access to an invalid pointer
- Fix crash when reapplying a filter with reprompting
- Fix crash when painting on a filter mask created from a vector selection ([BUG:432329](https://bugs.kde.org/show_bug.cgi?id=432329))

### MacOS

- MacOS: fix the finder plugins for showing a thumbnail or a quick look preview ([BUG:432328](https://bugs.kde.org/show_bug.cgi?id=432328))

### Scripting

- Fix handling the channel flags. Patch by Chris Venter, thanks! ([BUG:432226](https://bugs.kde.org/show_bug.cgi?id=432226))

### Stability and Performance

- Fix synchronization of zoom level between canvas and the scratchpad
- Fix normalization in Smart Patch Tool ([BUG:430953](https://bugs.kde.org/show_bug.cgi?id=430953))
- Fix performance issues in the foreground/background color button ([BUG:432936](https://bugs.kde.org/show_bug.cgi?id=432936))
- Fix saving incremental backups ([BUG:432701](https://bugs.kde.org/show_bug.cgi?id=432701))
- Fix a problem where the scratchpad could be unresponsive ([BUG:431708](https://bugs.kde.org/show_bug.cgi?id=431708))
- Fix Color as Alpha and Preserve Alpha in Custom and Clipboard brushes ([BUG:432274](https://bugs.kde.org/show_bug.cgi?id=432274))
- Fix the RGBA_brushes bundle so Krita doesn't try to recreate it on startup [(BUG:431832](https://bugs.kde.org/show_bug.cgi?id=431832))
- Fix handling of style in KisAngleSelector when the spin box must be shown flat and use the new angle selector everywhere

## Download

### Windows

If you're using the portable zip files, just open the zip file in Explorer and drag the folder somewhere convenient, then double-click on the krita icon in the folder. This will not impact an installed version of Krita, though it will share your settings and custom resources with your regular installed version of Krita. For reporting crashes, also get the debug symbols folder.

- 64 bits Windows Installer: [krita-x64-4.4.3-setup.exe](https://download.kde.org/stable/krita/4.4.3/krita-x64-4.4.3-setup.exe)
- Portable 64 bits Windows: [krita-x64-4.4.3.zip](https://download.kde.org/stable/krita/4.4.3/krita-x64-4.4.3.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.4.3/krita-x64-4.4.3-dbg.zip)

- 32 bits Windows Installer: [krita-x86-4.4.3-setup.exe](https://download.kde.org/stable/krita/4.4.3/krita-x86-4.4.3-setup.exe)
- Portable 32 bits Windows: [krita-x86-4.4.3.zip](https://download.kde.org/stable/krita/4.4.3/krita-x86-4.4.3.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.4.3/krita-x86-4.4.3-dbg.zip)

### Linux

- 64 bits Linux: [krita-4.4.3-x86_64.appimage](https://download.kde.org/stable/krita/4.4.3/krita-4.4.3-x86_64.appimage)
- 64 bits Linux [G'Mic-Qt plugin appimage](https://download.kde.org/stable/krita/4.4.3/gmic_krita_qt-x86_64.appimage)

(If, for some reason, Firefox thinks it needs to load this as text: to download, right-click on the link.)

### OSX

- OSX disk image: [krita-4.4.3.dmg](https://download.kde.org/stable/krita/4.4.3/krita-4.4.3.dmg)

Note: the gmic-qt is not available on OSX.

### Android

This time, the Android releases are made from the release tarball, so there are translations. We consider Krita on ChromeOS and Android still **_beta_**. There are many things that don't work and other things that are impossible without a real keyboard. You can also get Krita 4.4.3 from [Google Play](https://play.google.com/store/apps/details?id=org.krita).

- [64 bits Intel CPU APK](https://download.kde.org/stable/krita/4.4.3/krita_x86_64_apk-release.apk)
- [32 bits Intel CPU APK](https://download.kde.org/stable/krita/4.4.3/krita_x86_apk-release.apk)
- [64 bits Arm CPU APK](https://download.kde.org/stable/krita/4.4.3/krita_arm64-v8a_apk-release.apk)
- [32 bits Arm CPU APK](https://download.kde.org/stable/krita/4.4.3/krita_armeabi-v7a_apk-release.apk)

### Source code

- [krita-4.4.3.tar.gz](https://download.kde.org/stable/krita/4.4.3/krita-4.4.3.tar.gz)
- [krita-4.4.3.tar.xz](https://download.kde.org/stable/krita/4.4.3/krita-4.4.3.tar.xz)

### md5sum

For all downloads:

- [md5sum.txt](https://download.kde.org/stable/krita/4.4.3/md5sum.txt)

### Key

The Linux appimage and the source .tar.gz and .tar.xz tarballs are signed. You can retrieve the public key with gpg: "gpg --recv-key 7468332F". The signatures are [here](https://download.kde.org/stable/krita/4.4.3/) (filenames ending in .sig).

## Support Krita

Krita is a free and open source project. Please consider supporting the project with [donations](/support-us/donations/) or by [buying training videos!](/shop/) With your support, we can keep the core team working on Krita full-time.

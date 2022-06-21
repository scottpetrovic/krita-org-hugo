---
title: "Krita 4.4.1 Released"
date: "2020-10-29"
categories: 
  - "officialrelease"
---

Despite an extra-long beta period during which we got awesome feedback from our community, 4.4.0 was released with several regressions, that is, bugs that weren't present in 4.3.0. So today we're releasing Krita 4.4.1 with the following fixes:

- Android and ChromeOS:
    - Use SDK version 29, which means Krita doesn't need permissions to run anymore and can access external files more easily. Krita is also updated to use NDK 20 or better
    - Fix the color picker ([BUG:423254](https://bugs.kde.org/show_bug.cgi?id=423254))
    - Fix problems with events reaching the canvas if a popup message was shown
    - Use the device's locale, so the translations can be used ([BUG:427692](https://bugs.kde.org/show_bug.cgi?id=427692))
    - Fix copy and paste on Android ([BUG:423199](https://bugs.kde.org/show_bug.cgi?id=423199))
- Fix a crash when loading a file with a pattern fill layer ([BUG:427866](https://bugs.kde.org/show_bug.cgi?id=427866))
- Fix loading masks with vector selections ([BUG:428332](https://bugs.kde.org/show_bug.cgi?id=428332))
- Fix a crash in the text tool when opening the editor by double-clicking the text ([BUG:427858](https://bugs.kde.org/show_bug.cgi?id=427858))
- Fix a crash when using the move tool on a pixel selection ([BUG:428260](https://bugs.kde.org/show_bug.cgi?id=428260))

## Download

### Windows

If you're using the portable zip files, just open the zip file in Explorer and drag the folder somewhere convenient, then double-click on the krita icon in the folder. This will not impact an installed version of Krita, though it will share your settings and custom resources with your regular installed version of Krita. For reporting crashes, also get the debug symbols folder.

**NOTE for Windows Users: Microsoft has changed the way applications signed with certificates are handled. Only Digicert certificates are automatically trusted, other certificates will only be trusted if enough people bypass smartscreen to run the signed application.** **If you see the "Windows protected your PC" screen, press "More Info", then select "Run anyway". _The more people do this, the earlier Microsofts machine learning algorithm will learn Krita is perfectly fine._**

- 64 bits Windows Installer: [krita-x64-4.4.1-setup.exe](https://download.kde.org/stable/krita/4.4.1/krita-x64-4.4.1-setup.exe)
- Portable 64 bits Windows: [krita-x64-4.4.1.zip](https://download.kde.org/stable/krita/4.4.1/krita-x64-4.4.1.zip)
- [Debug symbols. (Unpack in the Krita installation bfolder)](https://download.kde.org/stable/krita/4.4.1/krita-x64-4.4.1-dbg.zip)

- 32 bits Windows Installer: [krita-x86-4.4.1-setup.exe](https://download.kde.org/stable/krita/4.4.1/krita-x86-4.4.1-setup.exe)
- Portable 32 bits Windows: [krita-x86-4.4.1.zip](https://download.kde.org/stable/krita/4.4.1/krita-x86-4.4.1.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.4.1/krita-x86-4.4.1-dbg.zip)

### Linux

- 64 bits Linux: [krita-4.4.1-x86\_64.appimage](https://download.kde.org/stable/krita/4.4.1/krita-4.4.1-x86_64.appimage)
- 64 bits Linux [G'Mic-Qt plugin appimage](https://download.kde.org/stable/krita/4.4.1/gmic_krita_qt-x86_64.appimage)

(If, for some reason, Firefox thinks it needs to load this as text: to download, right-click on the link.)

### OSX

- OSX disk image: [krita-4.4.1.dmg](https://download.kde.org/stable/krita/4.4.1/krita-4.4.1.dmg)

Note: the gmic-qt is not available on OSX.

### ChromeOS and Android Beta

This time, the Android releases are made from the release tarball, so there are translations. We consider Krita on ChromeOS and Android still **_beta_**. There are many things that don't work and other things that are impossible without a real keyboard.

- [64 bits Intel CPU APK](https://download.kde.org/stable/krita/4.4.1/krita-x86_64-4.4.1-release.apk)
- [32 bits Intel CPU APK](https://download.kde.org/stable/krita/4.4.1/krita-x86-4.4.1-release.apk)
- [64 bits Arm CPU APK](https://download.kde.org/stable/krita/4.4.1/krita-arm64-4.4.1-release.apk)
- [32 bits Arm CPU APK](https://download.kde.org/stable/krita/4.4.1/krita-arm32-4.4.1-release.apk)

### Source code

- [krita-4.4.1.tar.gz](https://download.kde.org/stable/krita/4.4.1/krita-4.4.1.tar.gz)
- [krita-4.4.1.tar.xz](https://download.kde.org/stable/krita/4.4.1/krita-4.4.1.tar.xz)

### md5sum

For all downloads:

- [md5sum.txt](https://download.kde.org/stable/krita/4.4.1/md5sum.txt)

## Support Krita

Krita is a free and open source project. Please consider supporting the project with [donations](https://krita.org/en/support-us/donations/) or by [buying training videos!](https://krita.org/en/shop/) With your support, we can keep the core team working on Krita full-time.

---
title: "Second Beta out for Krita 4.4.0"
date: "2020-09-29"
categories: 
  - "development-builds"
---

Today, we're releasing Krita 4.4.0 beta 2: we found a number of regressions and release blocking bugs.

This beta has Android builds too, since we fixed many issues with accessing files on Android: however, because we now add translations the APK files are too big for the Play Store, and you will have to download them from download.kde.org

**NOTE for Windows Users: Microsoft has changed the way applications signed with certificates are handled. Only Digicert certificates are automatically trusted, other certificates will only be trusted if enough people bypass smartscreen to run the signed application. Our builds are absolutely safe, so you can safely do that.** **If you see the "Windows protected your PC" screen, press "More Info", then select "Run anyway".**

[The full release notes bring you all the details](https://krita.org/en/krita-4-4-0-release-notes/)!

<iframe src="https://diode.zone/videos/embed/b441f360-0b94-470a-8365-5a5f44b3a617" width="560" height="315" frameborder="0" sandbox="allow-same-origin allow-scripts allow-popups" allowfullscreen="allowfullscreen" data-mce-fragment="1"></iframe>

## Bugs fixed since beta 1

- Disable the DDS file format.
- Fix crash when loading a file with reference images ([BUG:426839](https://bugs.kde.org/show_bug.cgi?id=426839))
- Fix lightness strength option for smudge engine ([BUG:426874](https://bugs.kde.org/show_bug.cgi?id=426874))
- Fix Cutoff Pattern option [BUG:426874](https://bugs.kde.org/show_bug.cgi?id=426874)
- Android: Vector/references don't get rendered ([BUG:422312](https://bugs.kde.org/show_bug.cgi?id=422312))
- Fix updates of color picker's preview ([BUG:426867](https://bugs.kde.org/show_bug.cgi?id=))
- Windows: add .lnk files for starting Krita in minimal and animation mode
- Fix crash when undoing Rectangle Selection and doing redo after
- Fix a crash when moving local selection mask ([BUG:426816](https://bugs.kde.org/show_bug.cgi?id=426816))
- Fix shortcut for Polygonal Selection Tool ([BUG:426916](https://bugs.kde.org/show_bug.cgi?id=426916))
- Fix update of color preview in MyPaint Color Selector on mouse click
- SeExpr: assert isDirty on the correct preset instance ([BUG:426911](https://bugs.kde.org/show_bug.cgi?id=426911))
- Fix snapping decorations in Create Path Tool ([BUG:426514](https://bugs.kde.org/show_bug.cgi?id=426514))
- Android: Use Storage Access Framework for all file operations ([BUG:424541](https://bugs.kde.org/show_bug.cgi?id=424541), [BUG:423670](https://bugs.kde.org/show_bug.cgi?id=423670))
- Android: show recent files on Welcome widget
- Android: Fix problem with loading/saving file layer
- Android: Fix saving for files with no extension
- Android: Fix saving with selections
- Bugfix: usage logging could not be saved to a file on Android ([BUG:427043](https://bugs.kde.org/show_bug.cgi?id=427043))

## Download

### Windows

If you're using the portable zip files, just open the zip file in Explorer and drag the folder somewhere convenient, then double-click on the krita icon in the folder. This will not impact an installed version of Krita, though it will share your settings and custom resources with your regular installed version of Krita. For reporting crashes, also get the debug symbols folder.

- 64 bits Windows Installer: [krita-x64-4.4.0-beta2-setup.exe](https://download.kde.org/unstable/krita/4.4.0-beta2/krita-x64-4.4.0-beta2-setup.exe)
- Portable 64 bits Windows: [krita-x64-4.4.0-beta2.zip](https://download.kde.org/unstable/krita/4.4.0-beta2/krita-x64-4.4.0-beta2.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/unstable/krita/4.4.0-beta2/krita-x64-4.4.0-beta2-dbg.zip)

- 32 bits Windows Installer: [krita-x86-4.4.0-beta2-setup.exe](https://download.kde.org/unstable/krita/4.4.0-beta2/krita-x86-4.4.0-beta2-setup.exe)
- Portable 32 bits Windows: [krita-x86-4.4.0-beta2.zip](https://download.kde.org/unstable/krita/4.4.0-beta2/krita-x86-4.4.0-beta2.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/unstable/krita/4.4.0-beta2/krita-x86-4.4.0-beta2-dbg.zip)

### Linux

- 64 bits Linux: [krita-4.4.0-beta2-x86\_64.appimage](https://download.kde.org/unstable/krita/4.4.0-beta2/krita-4.4.0-beta2-x86_64.appimage)
- 64 bits Linux [G'Mic-Qt plugin appimage](https://download.kde.org/unstable/krita/4.4.0-beta2/gmic_krita_qt-x86_64.appimage)

(If, for some reason, Firefox thinks it needs to load this as text: to download, right-click on the link.)

### OSX

- OSX disk image: [krita-4.4.0-beta2.dmg](https://download.kde.org/unstable/krita/4.4.0-beta2/krita-4.4.0-beta2.dmg)

Note: the gmic-qt is not available on OSX.

### Android/ChromeOS Beta

This time, the Android releases are made from the release tarball, so there are translations. We consider Krita on ChromeOS and Android still **_beta_**. There are many things that don't work and other things that are impossible without a real keyboard.

- [64 bits Intel CPU APK](https://download.kde.org/unstable/krita/4.4.0-beta2/krita-x86_64-4.4.0-beta2-release.apk)
- [32 bits Intel CPU APK](https://download.kde.org/unstable/krita/4.4.0-beta2/krita-x86-4.4.0-beta2-release.apk)
- [64 bits Arm CPU APK](https://download.kde.org/unstable/krita/4.4.0-beta2/krita-arm64-4.4.0-beta2-release.apk)
- [32 bits Arm CPU APK](https://download.kde.org/unstable/krita/4.4.0-beta2/krita-arm64-4.4.0-beta2-release.apk)

### Source code

- [krita-4.4.0-beta2.tar.gz](https://download.kde.org/unstable/krita/4.4.0-beta2/krita-4.4.0-beta2.tar.gz)
- [krita-4.4.0-beta2.tar.xz](https://download.kde.org/unstable/krita/4.4.0-beta2/krita-4.4.0-beta2.tar.xz)

### md5sum

For all downloads:

- [md5sum.txt](https://download.kde.org/unstable/krita/4.4.0-beta2/md5sum.txt)

## Support Krita

Krita is a free and open source project. Please consider supporting the project with [donations](https://krita.org/en/support-us/donations/) or by [buying training videos!](https://krita.org/en/shop/) With your support, we can keep the core team working on Krita full-time.

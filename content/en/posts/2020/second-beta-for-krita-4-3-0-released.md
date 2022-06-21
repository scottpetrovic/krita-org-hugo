---
title: "Second Beta for Krita 4.3.0 Released"
date: "2020-06-01"
categories: 
  - "development-builds"
---

This is the second beta release for Krita 4.3.0. It's later than expected because our system for making release builds was temporarily unavailable.

Since the first beta, the following issues have been addressed:

- Fix Color picking in freehand path and bezier curve tool ([BUG:373037](https://bugs.kde.org/show_bug.cgi?id=373037)).
- Fix zooming after changing the image resolution ([BUG:421797](https://bugs.kde.org/show_bug.cgi?id=421797))
- Switch the stabilizer to always use scalable distance ([BUG:421314](https://bugs.kde.org/show_bug.cgi?id=421314))
- Make sure channel thumbnails are not inverted when working with CMYK images ([BUG:421442](https://bugs.kde.org/show_bug.cgi?id=421442))
- Make it possible to use save incremental and incremental backup on files in folders that are named to look like incremental saves or backups ([BUG:421792](https://bugs.kde.org/show_bug.cgi?id=421792))
- The Python API for handling Document and Node objects is now synchronous: you do not have to add extra waitForDone calls anymore. ([BUG:401497](https://bugs.kde.org/show_bug.cgi?id=401497))
- On macOS, support for using modifier keys with canvas input actions has been improved ( [BUG:372646](https://bugs.kde.org/show_bug.cgi?id=372646), [BUG:373299](https://bugs.kde.org/show_bug.cgi?id=373299), [BUG:391088](https://bugs.kde.org/show_bug.cgi?id=391088))
- Implement touch support for Wacom tablets. Patch by P. Varet -- thanks! ([BUG:421295](https://bugs.kde.org/show_bug.cgi?id=4221295))
- Fix issues with files taking a long time to save ([BUG:421584](https://bugs.kde.org/show_bug.cgi?id=421584))
- Make the placeholder text in the text shape shorter and translatable ([BUG:421663](https://bugs.kde.org/show_bug.cgi?id=421663))
- Shift-click on a layer to see the layer in isolation doesn't change the visibility state of all layers anymore
- Animation frames outside the requested range are no longer rendered
- Make the autosave recovery dialog clearer ([BUG:420014](https://bugs.kde.org/show_bug.cgi?id=420014))
- Properly play animations and show onion skins when viewing layers in isolation ([BUG:394199](https://bugs.kde.org/show_bug.cgi?id=394199))
- Fix the position of the text shape editor on Windows ([BUG:419529](https://bugs.kde.org/show_bug.cgi?id=419529))
- Fix gamut mask rendering ([BUG:421142](https://bugs.kde.org/show_bug.cgi?id=421142))
- Fix artefacts when rendering the marching ants outline for small _or_ complex selections ([BUG:407868](https://bugs.kde.org/show_bug.cgi?id=407868), [BUG:419240](https://bugs.kde.org/show_bug.cgi?id=419240), [BUG:413220](https://bugs.kde.org/show_bug.cgi?id=413220))
- The animation timeline now correctly highlights the current frame after loading a file ([BUG:403854](https://bugs.kde.org/show_bug.cgi?id=403854))
- Correctly align the onion skin after cropping an image ([BUG:419462](https://bugs.kde.org/show_bug.cgi?id=419462))
- Fix rendering animations with odd render dimensions ([BUG:396128](https://bugs.kde.org/show_bug.cgi?id=396128))
- Set the default values for the split layer dialog to something sensible
- Fix eraser mode to be reset when the same color is picked from the canvas ([BUG:415476](https://bugs.kde.org/show_bug.cgi?id=415476))
- Fix the aspect ratio of layer and channel thumbnails
- Show the unsqueezed text of a squeezed combobox as a tooltip ([BUG:415117](https://bugs.kde.org/show_bug.cgi?id=415117))
- Add more translation context in several places
- Fix selecting colors in the stroke selection dialog ([BUG:411482](https://bugs.kde.org/show_bug.cgi?id=411482))
- Fix the memory management of documents created from Python ([BUG:412740](https://bugs.kde.org/show_bug.cgi?id=412740))

Also, Rafał Mikrut has submitted many fixes for issues with memory management and pointer access. Thanks!

[![Kiki among the waterlilies](../images/kiki_4.3.3_sm-1024x512.png)](https://krita.org/wp-content/uploads/2020/05/kiki_4.3.3_sm.png)

[The full release notes bring you all the details](/krita-4-3-release-notes/)!

Please help improve Krita by testing this beta!

## Download

### Windows

If you're using the portable zip files, just open the zip file in Explorer and drag the folder somewhere convenient, then double-click on the krita icon in the folder. This will not impact an installed version of Krita, though it will share your settings and custom resources with your regular installed version of Krita. For reporting crashes, also get the debug symbols folder.

- 64 bits Windows Installer: [krita-x64-4.3.0-beta2-setup.exe](https://download.kde.org/unstable/krita/4.3.0-beta2/krita-x64-4.3.0-beta2-setup.exe)
- Portable 64 bits Windows: [krita-x64-4.3.0-beta2.zip](https://download.kde.org/unstable/krita/4.3.0-beta2/krita-x64-4.3.0-beta2.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/unstable/krita/4.3.0-beta2/krita-x64-4.3.0-beta2-dbg.zip)

- 32 bits Windows Installer: [krita-x86-4.3.0-beta2-setup.exe](https://download.kde.org/unstable/krita/4.3.0-beta2/krita-x86-4.3.0-beta2-setup.exe)
- Portable 32 bits Windows: [krita-x86-4.3.0-beta2.zip](https://download.kde.org/unstable/krita/4.3.0-beta2/krita-x86-4.3.0-beta2.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/unstable/krita/4.3.0-beta2/krita-x86-4.3.0-beta2-dbg.zip)

### Linux

- 64 bits Linux: [krita-4.3.0-beta2-x86\_64.appimage](https://download.kde.org/unstable/krita/4.3.0-beta2/krita-4.3.0-beta2-x86_64.appimage)
- 64 bits Linux [G'Mic-Qt plugin appimage](https://download.kde.org/unstable/krita/4.3.0-beta2/gmic_krita_qt-x86_64.appimage)

(If, for some reason, Firefox thinks it needs to load this as text: to download, right-click on the link.)

### OSX

- OSX disk image: [krita-4.3.0-beta2.dmg](https://download.kde.org/unstable/krita/4.3.0-beta2/krita-4.3.0-beta2.dmg)

Note: the gmic-qt is not available on OSX.

### Android

The Android builds were made from git, not the release tarball, so they don't have translations. The beta is labeled 4.3.0-beta1 but actually contains all the fixes for beta 2, except for the commit that changed the version number.

This version of Krita for Android can load .kra files from Google Drive folders on ChromeOS, has fixes for problems with the menubar on some Samsung devices and has Samsung Air gestures integrated.

It is still not recommended to use these betas on phones, though they do install. This beta will also be available [in the Google Play Store](https://play.google.com/store/apps/details?id=org.krita).

- [64 bits Intel CPU APK](https://download.kde.org/unstable/krita/4.3.0-beta2/krita-x86_64-signed.apk)
- [32 bits Intel CPU APK](https://download.kde.org/unstable/krita/4.3.0-beta2/krita-x86-signed.apk)
- [64 bits Arm CPU APK](https://download.kde.org/unstable/krita/4.3.0-beta2/krita-arm64-signed.apk)
- [32 bits Arm CPU APK](https://download.kde.org/unstable/krita/4.3.0-beta2/krita-arm32-signed.apk)

### Source code

- [krita-4.3.0-beta2.tar.gz](https://download.kde.org/unstable/krita/4.3.0-beta2/krita-4.3.0-beta2.tar.gz)
- [krita-4.3.0-beta2.tar.xz](https://download.kde.org/unstable/krita/4.3.0-beta2/krita-4.3.0-beta2.tar.xz)

### md5sum

For all downloads:

- [md5sum.txt](https://download.kde.org/unstable/krita/4.3.0-beta2/md5sum.txt)

## Support Krita

Krita is a free and open source project. Please consider supporting the project with [donations](/support-us/donations/) or by [buying training videos!](/support-us/shop) With your support, we can keep the core team working on Krita full-time.

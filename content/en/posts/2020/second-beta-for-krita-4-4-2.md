---
title: "Second Beta for Krita 4.4.2"
date: "2020-12-24"
categories: 
  - "development-builds"
---

The Krita team is releasing the second beta of Krita 4.4.2. Ramon Miranda has just released a video of one of the star features of this release: mesh transforms:

{{< youtube DLXWynZT_8s >}}

Compared to the [first beta](/item/first-beta-of-krita-4-4-2/), the following issues have been fixed:

- The projection of vector layers no longer gets corrupted when applying a mesh transformation
- The isometric grid updates correctly and is drawn correctly ([BUG:427833](https://bugs.kde.org/show_bug.cgi?id=427833))
- The triangle color selector now reacts to mouse events correctly on scaled displays
- The mypaint shade selector now performs better and looks better
- The preview of a transformation of a group layer in an animation frame is fixed ([BUG:413968](https://bugs.kde.org/show_bug.cgi?id=413968))
- It is now possible to chain transformations: after finishing one transformation, you can continue with the next transformation with a shift-click on the layer
- An option was added for flipping the symmetry mode for mesh handles
- A warning was added when krita is started with the Qt wayland platform plugin: Krita does not support that at the moment ([BUG:430426](https://bugs.kde.org/show_bug.cgi?id=430426), [BUG:429079](https://bugs.kde.org/show_bug.cgi?id=429079))
- Painting assistant decorations in selection tools was fixed ([BUG:427658](https://bugs.kde.org/show_bug.cgi?id=427658))
- Fix editing segments of bezier vector shapes after the mesh refactoring ([BUG:430377](https://bugs.kde.org/show_bug.cgi?id=430377))
- Fix loading generator layers ([BUG:430246](https://bugs.kde.org/show_bug.cgi?id=430246), [BUG:430244](https://bugs.kde.org/show_bug.cgi?id=430244))
- Drag & Dropping empty layers no longer crashes Krita ([BUG:429049](https://bugs.kde.org/show_bug.cgi?id=429049))
- The QuickLook thumbnailer for macOS has been disabled for this release because it could crash the macOS finder ([BUG:430553](https://bugs.kde.org/show_bug.cgi?id=430553))
- The thumbnails on the welcome page now have the correct size ([BUG:430359](https://bugs.kde.org/show_bug.cgi?id=430359))

There are also six new brushes by Ramon Miranda:

[![](/images/posts/2020/rgba_brushes.png)](https://krita.org/wp-content/uploads/2020/12/rgba_brushes.png)

## Download

### Windows

If you're using the portable zip files, just open the zip file in Explorer and drag the folder somewhere convenient, then double-click on the krita icon in the folder. This will not impact an installed version of Krita, though it will share your settings and custom resources with your regular installed version of Krita. For reporting crashes, also get the debug symbols folder.

- 64 bits Windows Installer: [krita-x64-4.4.2-beta2-setup.exe](https://download.kde.org/unstable/krita/4.4.2-beta2/krita-x64-4.4.2-beta2-setup.exe)
- Portable 64 bits Windows: [krita-x64-4.4.2-beta2.zip](https://download.kde.org/unstable/krita/4.4.2-beta2/krita-x64-4.4.2-beta2.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/unstable/krita/4.4.2-beta2/krita-x64-4.4.2-beta2-dbg.zip)

- 32 bits Windows Installer: [krita-x86-4.4.2-beta2-setup.exe](https://download.kde.org/unstable/krita/4.4.2-beta2/krita-x86-4.4.2-beta2-setup.exe)
- Portable 32 bits Windows: [krita-x86-4.4.2-beta2.zip](https://download.kde.org/unstable/krita/4.4.2-beta2/krita-x86-4.4.2-beta2.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/unstable/krita/4.4.2-beta2/krita-x86-4.4.2-beta2-dbg.zip)

### Linux

- 64 bits Linux: [krita-4.4.2-beta2-x86\_64.appimage](https://download.kde.org/unstable/krita/4.4.2-beta2/krita-4.4.2-beta2-x86_64.appimage)
- 64 bits Linux [G'Mic-Qt plugin appimage](https://download.kde.org/unstable/krita/4.4.2-beta2/gmic_krita_qt-x86_64.appimage)

(If, for some reason, Firefox thinks it needs to load this as text: to download, right-click on the link.)

### OSX

- OSX disk image: [krita-4.4.2-beta2.dmg](https://download.kde.org/unstable/krita/4.4.2-beta2/krita-4.4.2-beta2.dmg)

Note: the gmic-qt is not available on OSX.

### Android

This time, the Android releases are made from the release tarball, so there are translations. We consider Krita on ChromeOS and Android still **_beta_**. There are many things that don't work and other things that are impossible without a real keyboard.

- [64 bits Intel CPU APK](https://download.kde.org/unstable/krita/4.4.2-beta2/krita-x86_64-4.4.2-beta2.apk)
- [32 bits Intel CPU APK](https://download.kde.org/unstable/krita/4.4.2-beta2/krita-x86-4.4.2-beta2.apk)
- [64 bits Arm CPU APK](https://download.kde.org/unstable/krita/4.4.2-beta2/krita-arm64-4.4.2-beta2.apk)
- [32 bits Arm CPU APK](https://download.kde.org/unstable/krita/4.4.2-beta2/krita-arm32-4.4.2-beta2.apk)

### Source code

- [krita-4.4.2-beta2.tar.gz](https://download.kde.org/unstable/krita/4.4.2-beta2/krita-4.4.2-beta2.tar.gz)
- [krita-4.4.2-beta2.tar.xz](https://download.kde.org/unstable/krita/4.4.2-beta2/krita-4.4.2-beta2.tar.xz)

### md5sum

For all downloads:

- [md5sum.txt](https://download.kde.org/unstable/krita/4.4.2-beta2/md5sum.txt)

## Support Krita

Krita is a free and open source project. Please consider supporting the project with [donations](/support-us/donations/) or by [buying training videos!](/support-us/shop) With your support, we can keep the core team working on Krita full-time.

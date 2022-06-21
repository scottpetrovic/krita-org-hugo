---
title: "New Stable Release: Krita 3.3.3"
date: "2018-01-12"
---

Today we're releasing Krita 3.3.3. This will probably be the last stable release in the Krita 3 series. This release contains several bug fixes and one very important change for Windows users:

- The Direct3d/Angle renderer is now the default for Intel users. Recent updates to the Intel display drivers have broken Krita on many more systems than before, so it's better that everyone gets this workaround by default. If you experience decreased performance, you can always try to enable OpenGL again.

Other fixes and improvements include:

- Fix an issue where it would not be possible to select certain blending modes when the current layer is grayscale but the image is rgb.
- Set the OS and platform when reporting a bug from within Krita on Windows.
- Make it possible to enter color values as percentage in the specific color selector
- Add OpenGL warnings and make ANGLE default on Intel GPUs
- Add an Invert button to the levels filter
- Implement loading and saving of styles for group layers to and from PSD
- Fix the erase mode not showing correctly when returning to the brush tool
- Save the visibility of individual assistants in .kra files
- Add an option to draw ruler tips as a power of 2
- Disable autoscroll on move and transform tools.
- Improve handling of native mouse events when using a pen and the Windows Ink API
- Fix the focal point for the pinch zoom gesture
- Fix loading netpbm files with comment.

### Download

#### Windows

Note for Windows users: if you encounter crashes, please follow [these instructions](https://docs.krita.org/Dr._Mingw_debugger) to use the debug symbols so we can figure out where Krita crashes.

- 64 bits Windows: [krita-3.3.3-x64-setup.exe](https://download.kde.org/stable/krita/3.3.3/krita-3.3.3-x64-setup.exe)
- Portable 64 bits Windows: [krita-3.3.3-x64.zip](https://download.kde.org/stable/krita/3.3.3/krita-3.3.3-x64.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/3.3.3/krita-3.3.3-x64-dbg.zip)

- 32 bits Windows: [krita-3.3.3-x86-setup.exe](https://download.kde.org/stable/krita/3.3.3/krita-3.3.3-x86-setup.exe)
- Portable 32 bits Windows: [krita-3.3.3-x86.zip](https://download.kde.org/stable/krita/3.3.3/krita-3.3.3-x86.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/3.3.3/krita-3.3.3-x86-dbg.zip)

#### Linux

- 64 bits Linux: [krita-3.3.3-x86\_64.appimage](https://download.kde.org/stable/krita/3.3.3/krita-3.3.3-x86_64.appimage)

(If, for some reason, Firefox thinks it needs to load this as text: to download, right-click on the link.)

When it is updated, you can also use the [Krita Lime PPA](https://launchpad.net/%7Ekritalime/+archive/ubuntu/ppa) to install Krita 3.3.3 on Ubuntu and derivatives. We are working on an updated snap.

#### OSX

- OSX disk image: [krita-3.3.3.dmg](https://download.kde.org/stable/krita/3.3.3/krita-3.3.3.dmg)

Note: the gmic-qt and pdf plugins are not available on OSX.

### Source code

- Source code: [krita-3.3.3.tar.gz](https://download.kde.org/stable/krita/3.3.3/krita-3.3.3.tar.gz)

#### md5sums

For all downloads:

- [md5sums.txt](https://download.kde.org/stable/krita/3.3.3/md5sums.txt)

#### Key

The Linux appimage and the source tarball are signed. You can retrieve the public key over https here: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8). The signatures are [here](http://download.kde.org/stable/krita/3.3.3/).

#### Support Krita

Krita is a free and open source project. Please consider supporting the project with [donations](/support-us/donations/) or by [buying training videos or the artbook!](/support-us/shop) With your support, we can keep the core team working on Krita full-time.

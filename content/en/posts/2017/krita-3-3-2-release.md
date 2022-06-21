---
title: "Krita 3.3.2 Released"
date: "2017-11-03"
---

Today we are releasing Krita 3.3.2, a bugfix release for Krita 3.3.0. This release fixes two important regressions:

- Krita 3.3.1 would read brush presets with textures incorrectly. This is now fixed.
- Windows 1709 broke wintab and Windows Ink tablet handling in various ways; we worked around that and it works again in this version of Krita.

Additionally, there are the following fixes and improvements:

- Animation: make it possible to export empty frames after the end of the animation.
- Animation: make it possible to render up to a 10,000 frames
- Add a command-line option to start Krita with a new, empty image: krita --new-image RGBA,8,5000,3000
- Performance: improved caching for effect and selection masks
- Performance: Fix a leak in the smudge brush
- Performance: Improve performance when using the hardware-accelerated canvas
- Performance, Windows: improve the performance when loading icons
- macOS: render the frames-per-second overlay widget correctly
- Filters: it's now possible to edit the filter's settings directly in the xml that is used to save filter definitions to .krita files.
- Filters: a new ASC\_CDL color balance filter was added, with Slope, Offset and Power options.
- Crashes: fix a crash that happened when closing a second document with infinite canvas active
- Layers: Make it possible to copy group layers
- UI: make it possible to use the scroll-wheel to scroll through patterns when the patterns palette is very narrow.
- UI: Improve drag and drop feedback in the layer panel
- UI: Hide the lock and collapse titlebar icons when a panel is floating
- G'Mic: the included G'Mic is updated to the latest release.

### Download

#### Windows

Note for Windows users: if you encounter crashes, please follow [these instructions](https://docs.krita.org/Dr._Mingw_debugger) to use the debug symbols so we can figure out where Krita crashes.

- 64 bits Windows: [krita-3.3.2-x64-setup.exe](https://download.kde.org/stable/krita/3.3.2/krita-3.3.2-x64-setup.exe)
- Portable 64 bits Windows: [krita-3.3.2.1-x64.zip](https://download.kde.org/stable/krita/3.3.2/krita-3.3.2.1-x64.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/3.3.2/krita-3.3.2.1-x64-dbg.zip)

- 32 bits Windows: [krita-3.3.2-x86-setup.exe](https://download.kde.org/stable/krita/3.3.2/krita-3.3.2-x86-setup.exe)
- Portable 32 bits Windows: [krita-3.3.2.1-x86.zip](https://download.kde.org/stable/krita/3.3.2/krita-3.3.2.1-x86.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/3.3.2/krita-3.3.2.1-x86-dbg.zip)

- Explorer Shell extension: [kritashellex-1.2.4.0-setup.exe](https://download.kde.org/stable/krita/KritaShellExtension-v1.2.4-setup.exe)

#### Linux

- 64 bits Linux: [krita-3.3.2-x86\_64.appimage](https://download.kde.org/stable/krita/3.3.2/krita-3.3.2-x86_64.appimage)

(If, for some reason, Firefox thinks it needs to load this as text: to download, right-click on the link.)

When it is updated, you can also use the [Krita Lime PPA](https://launchpad.net/%7Ekritalime/+archive/ubuntu/ppa) to install Krita 3.3.2 on Ubuntu and derivatives. There is also an updated snap.

#### OSX

- OSX disk image: [krita-3.3.2.dmg](https://download.kde.org/stable/krita/3.3.2/krita-3.3.2.dmg)

Note: the gmic-qt and pdf plugins are not available on OSX.

### Source code

- Source code: [krita-3.3.2.1.tar.xz](https://download.kde.org/stable/krita/3.3.2/krita-3.3.2.1.tar.xz)

#### md5sums

For all downloads:

- [md5sums.txt](https://download.kde.org/stable/krita/3.3.2/md5sums.txt)

#### Key

The Linux appimage and the source tarball are signed. You can retrieve the public key over https here: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8). The signatures are [here](http://download.kde.org/stable/krita/3.3.2/).

#### Support Krita

Krita is a free and open source project. Please consider supporting the project with [donations](https://krita.org/en/support-us/donations/) or by [buying training videos or the artbook!](https://krita.org/en/support-us/shop) With your support, we can keep the core team working on Krita full-time.

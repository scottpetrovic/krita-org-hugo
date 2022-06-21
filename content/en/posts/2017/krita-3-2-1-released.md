---
title: "Krita 3.2.1 Released"
date: "2017-08-25"
---

Krita 3.2.1 is a bug fix release. The following issues were fixed:

- Crash on startup if only OpenGL 2.1 is found: if you had to disable opengl for 3.2.0, you can try to enable it again
- A crash when changing layer types in the gmic-qt plugin
- A bug where gmic-qt could crash on odd-sized images
- A regression where using the text tool would break the brush tool
- The option to use the native platform's file dialogs was restored
- A bug where selecting the line tool would disable the flow slider
- Some issues with the LUT docker were fixed

### Download

#### Windows

Note for Windows users: if you encounter crashes, please follow [these instructions](https://docs.krita.org/Dr._Mingw_debugger) to use the debug symbols so we can figure out where Krita crashes.

- 32 bits Windows: [krita-3.2.1-x86-setup.exe](https://download.kde.org/stable/krita/3.2.1/krita-3.2.1-x86-setup.exe)
- Portable 32 bits Windows: [krita-3.2.1-x86.zip](https://download.kde.org/stable/krita/3.2.1/krita-3.2.1-x86.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/3.2.1/krita-3.2.1-x86-dbg.zip)

- 64 bits Windows: [krita-3.2.1-x64-setup.exe](https://download.kde.org/stable/krita/3.2.1/krita-3.2.1-x64-setup.exe)
- Portable 64 bits Windows: [krita-3.2.1-x64.zip](https://download.kde.org/stable/krita/3.2.1/krita-3.2.1-x64.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/3.2.1/krita-3.2.1-x64-dbg.zip)

- Explorer Shell extension: [kritashellex-1.2.4.0-setup.exe](https://download.kde.org/stable/krita/KritaShellExtension-v1.2.4-setup.exe)

#### Linux

- 64 bits Linux: [krita-3.2.1-x86\_64.appimage](https://download.kde.org/stable/krita/3.2.1/krita-3.2.1-x86_64.appimage)

(If, for some reason, Firefox thinks it needs to load this as text: to download, right-click on the link.)

When it is updated, you can also use the [Krita Lime PPA](https://launchpad.net/%7Ekritalime/+archive/ubuntu/ppa) to install Krita 3.2.1 on Ubuntu and derivatives.

#### OSX

- OSX disk image: [krita-3.2.1.dmg](https://download.kde.org/stable/krita/3.2.1/krita-3.2.1.dmg)

Note: the gmic-qt and pdf plugins is not available on OSX.

### Source code

- Source code: [krita-3.2.1.tar.gz](https://download.kde.org/stable/krita/3.2.1/krita-3.2.1.tar.gz)

#### md5sums

For all downloads:

- [md5sums.txt](https://download.kde.org/stable/krita/3.2.1/md5sums.txt)

#### Key

The Linux appimage and the source tarball are signed. You can retrieve the public key over https here: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8). The signatures are [here](http://download.kde.org/stable/krita/3.2.1/).

#### Support Krita

Krita is a free and open source project. Please consider supporting the project with [donations](/support-us/donations/) or by [buying training videos or the artbook!](/support-us/shop) With your support, we can keep the core team working on Krita full-time.

---
title: "Krita 3.1.4 Released"
date: "2017-05-26"
---

Today we're releasing Krita 3.1.4. This strictly a bug-fix release, but everyone is encouraged to update.

- Fix a crash when trying to play an animation when OpenGL is disabled in Krita
- Fix rendering animation frames if the directory you're trying to render to doesn't exist
- Don't open the tablet/screen resolution conflict dialog multiple times
- Don't scale down previews that are too small in the transform tool: this fixes a rare crash with the transform tool
- Don't crash when trying to close the last view on the last document while the document is modified.
- Fix a crash when cycling quickly through layers that have a color tag
- Fix loading some Gimp 2.9 files: note that Gimp 2.9's file format is not officially supported in Krita
- Fully remove the macro recorder plugin: in 3.1.4, only the menu entries had stayed around.
- Make it impossible to hide the template selector in the new image dialog; hiding the template selector would also hide the cancel button in the dialog.

#### Download

The KDE download site has been updated to support https now.

#### Windows

Note for Windows users: if you encounter crashes, please follow [these instructions](https://docs.krita.org/Dr._Mingw_debugger) to use the debug symbols so we can figure out where Krita crashes.

- 32 bits Windows: [krita-3.1.4-x86-setup.exe](https://download.kde.org/stable/krita/3.1.4/krita-3.1.4-x86-setup.exe)
- Portable 32 bits Windows: [krita-3.1.4-x86.zip](https://download.kde.org/stable/krita/3.1.4/krita-3.1.4-x86.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/3.1.4/krita-3.1.4-x86-dbg.zip)

- 64 bits Windows: [krita-3.1.4-x64-setup.exe](https://download.kde.org/stable/krita/3.1.4/krita-3.1.4-x64-setup.exe)
- Portable 64 bits Windows: [krita-3.1.4-x64.zip](https://download.kde.org/stable/krita/3.1.4/krita-3.1.4-x64.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/3.1.4/krita-3.1.4-x64-dbg.zip)

- Explorer Shell extension: [kritashellex-1.2.3.0-setup.exe](https://download.kde.org/stable/krita/kritashellex-1.2.3.0-setup.exe)

#### Linux

- - 64 bits Linux: [krita-3.1.4-x86\_64.appimage](https://download.kde.org/stable/krita/3.1.4/krita-3.1.4-x86_64.appimage)

(For some reason, Firefox thinks it needs to load this as text: to download, right-click on the link.)

A snap image for the Ubuntu App Store will be available from the Ubuntu application store. When it is updated, you can also use the [Krita Lime PPA](https://launchpad.net/%7Ekritalime/+archive/ubuntu/ppa) to install Krita 3.1.4 on Ubuntu and derivatives.

#### OSX

- OSX disk image: [krita-3.1.4.dmg](https://download.kde.org/stable/krita/3.1.4/krita-3.1.4.dmg)

### Source code

- Source code: [krita-3.1.4.tar.gz](https://download.kde.org/stable/krita/3.1.4/krita-3.1.4.tar.gz)

#### md5sums

For all downloads:

- [md5sums.txt](https://download.kde.org/stable/krita/3.1.4/md5sums.txt)

#### Key

The Linux appimage and the source tarball are signed. You can retrieve the public key over https here: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8). The signatures are [here](http://download.kde.org/stable/krita/3.1.4/).

#### Support Krita

Krita is a free and open source project. Please consider supporting the project with [donations](/support-us/donations/) or by [buying training videos or the artbook!]("/support-us/shop) With your support, we can keep the core team working on Krita full-time.

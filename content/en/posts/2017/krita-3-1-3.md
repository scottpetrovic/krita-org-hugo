---
title: "Krita 3.1.3"
date: "2017-05-01"
---

Today we're proud to release Krita 3.1.3. A ton of bug fixes, and some nice new features as well! Dmitry and Boud have taken a month off from implementing Kickstarter features to make Krita 3.1.3 as good and solid as we could make it. Thanks to all the people who have tested the alpha, the beta and the release candidate! Thanks to all the people who have worked on translations, too, and to Alexey Samoilov for picking up the maintenance of the Ubuntu Lime PPA.

[![Transform around Pivot](/images/posts/2017/pivot-1024x527.png)](/images/posts/2017/pivot.png)Transform around Pivot (Image by [David Revoy](https://peppercarrot.com)

We also have a new version of the Windows explorer integration plugin, that makes it possible to show thumbnails of .kra and .ora files: several memory leaks were fixed, and a conflict with .ora files created by an Oracle database too was resolved. Thanks to Alvin Wong!

### New Features

- scale around pivot point added
- implement context menu actions for default tool (cut, copy, paste, object ordering)
- added option to allow multiple instances of krita (BUG 377199)

The full list of changes with 50+ bug fixes can be found  [in the full release notes](/release-notes-for-3-1-3/).

#### Download

The KDE download site has been updated to support https now.

#### Windows

Note for Windows users: if you encounter crashes, please follow [these instructions](https://docs.krita.org/Dr._Mingw_debugger) to use the debug symbols so we can figure out where Krita crashes.

- 32 bits Windows: [krita-3.1.3-x86-setup.exe](https://download.kde.org/stable/krita/3.1.3/krita-3.1.3-x86-setup.exe)
- Portable 32 bits Windows: [krita-3.1.3-x86.zip](https://download.kde.org/stable/krita/3.1.3/krita-3.1.3-x86.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/3.1.3/krita-3.1.3-x86-dbg.zip)

- 64 bits Windows: [krita-3.1.3-x64-setup.exe](https://download.kde.org/stable/krita/3.1.3/krita-3.1.3-x64-setup.exe)
- Portable 64 bits Windows: [krita-3.1.3-x64.zip](https://download.kde.org/stable/krita/3.1.3/krita-3.1.3-x64.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/3.1.3/krita-3.1.3-x64-dbg.zip)

- Explorer Shell extension: [kritashellex-1.2.3.0-setup.exe](https://download.kde.org/stable/krita/kritashellex-1.2.3.0-setup.exe)

#### Linux

- 64 bits Linux: [krita-3.1.3-x86_64.appimage](https://download.kde.org/stable/krita/3.1.3/krita-3.1.3-x86_64.appimage)

A snap image for the Ubuntu App Store is also available from the Ubuntu application store. You can also use the [Krita Lime PPA](https://launchpad.net/%7Ekritalime/+archive/ubuntu/ppa) to install Krita 3.1.3 on Ubuntu and derivatives.

#### OSX

- OSX disk image: [krita-3.1.3.dmg](https://download.kde.org/stable/krita/3.1.3/krita-3.1.3.dmg)

### Source code

- Source code: [krita-3.1.3.tar.gz](https://download.kde.org/stable/krita/3.1.3/krita-3.1.3.tar.gz)

#### md5sums

For all downloads:

- [md5sums.txt](https://download.kde.org/stable/krita/3.1.3/md5sums.txt)

#### Key

The Linux appimage and the source tarball are signed. You can retrieve the public key over https here: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8). The signatures are [here](http://download.kde.org/stable/krita/3.1.3/).

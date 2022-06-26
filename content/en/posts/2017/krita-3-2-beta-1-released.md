---
title: "Krita 3.2 beta 1 Released"
date: "2017-07-18"
---

We're releasing the first beta for Krita 3.2.0 today! Compared to Krita 3.1.4, released 26th of May, there are numerous bug fixes and some very cool new features. Please test this release, so we can fix bugs before the final release!

### Known bugs

It's a beta, so there are bugs. One of them is that the size and flow sliders are disabled. We promise faithfully we won't release until that's fixed, but in the meantime, no need to report it!

### Features

- Krita 3.2 will use the gmic-qt plugin created and maintained by the [authors of G'Mic](http://gmic.eu/) We're still working with them to create binary builds that can run on Windows, OSX and most versions of Linux. This plugin replaces completely the older gmic plugin.
- We added Radian's brush set to Krita's default brushes.

[![](/images/posts/2017/new_brushes-478x1024.jpg)](/images/posts/2017/new_brushes.jpg)

These brushes are good for create a strong painterly look:

[![](/images/posts/2017/kiki_with_new_brushes_by_rad.jpg)](/images/posts/2017/kiki_with_new_brushes_by_rad.jpg)

- There are now shortcuts for changing layer states like visibility and lock.
- There have been many fixes to the clone brush
- There is a new dialog from where you can copy and paste relevant information about your system for bug reports.
- We've integrated the Smart Patch tool that was previously only in the 4.0 pre-alpha builds!

{{< youtube jI87VzDtkPY >}}

- The Gaussian Blur filter now can use kernels up to 1000 pixels in diameter

## Bug Fixes

Among the bigger bug fixes:

- Painting with your finger on touch screens is back. You can enable or disable this in the settings dialog.
- If previously you suffered from the "green brush outline" syndrome, that should be fixed now, too. Though we cannot guarantee the fix works on all OpenGL systems.
- There have been a number of performance improvements as well
- The interaction with the file dialog has been improved: it should be better at guessing which folder you want to open, which filename to suggest and which file type to use.

And of course, there were dozens of smaller bug fixes.

#### Download

The KDE download site has been updated to support https now.

#### Windows

Note for Windows users: if you encounter crashes, please follow [these instructions](https://docs.krita.org/Dr._Mingw_debugger) to use the debug symbols so we can figure out where Krita crashes.

- 32 bits Windows: [krita-3.2.0-beta.1-x86-setup.exe](https://download.kde.org/unstable/krita/3.2.0-beta.1/krita-3.2.0-beta.1-x86-setup.exe)
- Portable 32 bits Windows: [krita-3.2.0-beta.1-x86.zip](https://download.kde.org/unstable/krita/3.2.0-beta.1/krita-3.2.0-beta.1-x86.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/unstable/krita/3.2.0-beta.1/krita-3.2.0-beta.1-x86-dbg.zip)

- 64 bits Windows: [krita-3.2.0-beta.1-x64-setup.exe](https://download.kde.org/unstable/krita/3.2.0-beta.1/krita-3.2.0-beta.1-x64-setup.exe)
- Portable 64 bits Windows: [krita-3.2.0-beta.1-x64.zip](https://download.kde.org/unstable/krita/3.2.0-beta.1/krita-3.2.0-beta.1-x64.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/unstable/krita/3.2.0-beta.1/krita-3.2.0-beta.1-x64-dbg.zip)

- Explorer Shell extension: [kritashellex-1.2.3.0-setup.exe](https://download.kde.org/unstable/krita/kritashellex-1.2.3.0-setup.exe)

#### Linux

- - 64 bits Linux: [krita-3.2.0-beta.1-x86_64.appimage](https://download.kde.org/unstable/krita/3.2.0-beta.1/krita-3.2.0-beta.1-x86_64.appimage)

(For some reason, Firefox thinks it needs to load this as text: to download, right-click on the link.)

A snap image for the Ubuntu App Store will be available from the Ubuntu application store. When it is updated, you can also use the [Krita Lime PPA](https://launchpad.net/%7Ekritalime/+archive/ubuntu/ppa) to install Krita 3.2.0-beta.1 on Ubuntu and derivatives.

#### OSX

- OSX disk image: [krita-3.2.0-beta.1.dmg](https://download.kde.org/unstable/krita/3.2.0-beta.1/krita-3.2.0-beta.1.dmg)

### Source code

- Source code: [krita-3.2.0-beta.1.tar.gz](https://download.kde.org/unstable/krita/3.2.0-beta.1/krita-3.2.0-beta.1.tar.gz)

#### md5sums

For all downloads:

- [md5sums.txt](https://download.kde.org/unstable/krita/3.2.0-beta.1/md5sums.txt)

#### Key

The Linux appimage and the source tarball are signed. You can retrieve the public key over https here: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8). The signatures are [here](http://download.kde.org/unstable/krita/3.2.0-beta.1/).

#### Support Krita

Krita is a free and open source project. Please consider supporting the project with [donations](/support-us/donations/) or by [buying training videos or the artbook!](/support-us/shop) With your support, we can keep the core team working on Krita full-time.

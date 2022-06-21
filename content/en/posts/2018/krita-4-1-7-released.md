---
title: "Krita 4.1.7 Released"
date: "2018-12-13"
categories: 
  - "news"
  - "officialrelease"
---

Today we're releasing Krita 4.1.7, another bug fix release in the Krita 4.1 series.

The most important fix is a weird one: it might help your wifi connection. The problem is that we started building a widget that would show you the news feed from krita.org. The widget isn't active, and doesn't make any kind of network connection... But Qt's network manager class still checks your wifi settings all the time. See these bugs: [https://bugreports.qt.io/browse/QTBUG-46015](https://bugreports.qt.io/browse/QTBUG-46015) and [https://bugreports.qt.io/browse/QTBUG-40332](https://bugreports.qt.io/browse/QTBUG-40332).

Apart from that, we've worked around a bug in Qt 5.12 that would cause an instant crash when using a tablet. Our own builds do not use that version of Qt, so the Windows builds, macOS build and the Linux appimage are fine, but users of rolling Linux releases like Arch would suffer from this issue.

And there are more bug fixes, of course:

- Fix showing wrongly that there is no audio support in the animation timeline audio menu
- Disable the disk-based animation cache rendering backend on Windows: this would give problems with animations bigger than about 150 frames. ([BUG 401326](https://bugs.kde.org/show_bug.cgi?id=401326))
- Don't hang when trying to load recent files thumbnails for files in a location that's no longer accessible. ([BUG:401939](https://bugs.kde.org/show_bug.cgi?id=401939))
- Make it possible to use the LUT docker when Angle is enabled on Windows. We have also updated the OpenColorIO library to the latest release.
- Remember whether anti-aliasing was enabled in selection tools ([BUG:401730](https://bugs.kde.org/show_bug.cgi?id=401730))
- Add a shortcut to activate the text tool ([BUG:401655](https://bugs.kde.org/show_bug.cgi?id=401655))
- Make the toolbars movable again
- Make Select by Color Range check the entire image ([BUG:346138](https://bugs.kde.org/show_bug.cgi?id=346138))
- Enable HiDPI support by default: the problems with the canvas scaling have been solved.
- Allow krita to import more than file at a time when started from a file manager ([BUG:401476](https://bugs.kde.org/show_bug.cgi?id=401476))
- Fix using the scrollwheel in comboboxes on Linux ([BUG:399379](https://bugs.kde.org/show_bug.cgi?id=399379)) Patch by Mykola Krachkovsky.
- Fix the calculation of Average Desaturation ([BUG:400493](https://bugs.kde.org/show_bug.cgi?id=))
- Do not crash when exporting Compositions ([BUG:400627](https://bugs.kde.org/show_bug.cgi?id=400627))
- Make the move tool show the correct cursor in all modes
- Let the move tool move invisible layers
- Fix a crash in the artistic color selector ([BUG:399860](https://bugs.kde.org/show_bug.cgi?id=399860))

## Download

### Windows

Note for Windows users: if you encounter crashes, please follow [these instructions](https://docs.krita.org/en/reference_manual/dr_minw_debugger.html#dr-minw) to use the debug symbols so we can figure out where Krita crashes.

- 64 bits Windows: [krita-x64-4.1.7-setup.exe](https://download.kde.org/stable/krita/4.1.7/krita-x64-4.1.7-setup.exe)
- Portable 64 bits Windows: [krita-x64-4.1.7.zip](https://download.kde.org/stable/krita/4.1.7/krita-x64-4.1.7.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.1.7/krita-x64-4.1.7-dbg.zip)

- 32 bits Windows: [krita-x86-4.1.7-setup.exe](https://download.kde.org/stable/krita/4.1.7/krita-x86-4.1.7-setup.exe)
- Portable 32 bits Windows: [krita-x86-4.1.7.zip](https://download.kde.org/stable/krita/4.1.7/krita-x86-4.1.7.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.1.7/krita-x86-4.1.7-dbg.zip)

### Linux

- 64 bits Linux: [krita-4.1.7-x86\_64.appimage](https://download.kde.org/stable/krita/4.1.7/krita-4.1.7-x86_64.appimage)
- 64 bits Linux [G'Mic-Qt plugin appimage](https://download.kde.org/stable/krita/4.1.7/gmic_krita_qt-x86_64.appimage).

(If, for some reason, Firefox thinks it needs to load this as text: to download, right-click on the link.)

When it is updated, you can also use the [Krita Lime PPA](https://launchpad.net/%7Ekritalime/+archive/ubuntu/ppa) to install Krita 4.1.7 on Ubuntu and derivatives. We are working on an updated snap.

### OSX

- OSX disk image: [krita-4.1.7.dmg](https://download.kde.org/stable/krita/4.1.7/krita-4.1.7.dmg)

Note: the touch docker, gmic-qt and python plugins are not available on OSX.

### Source code

- Source code: [krita-4.1.7.101.tar.gz](https://download.kde.org/stable/krita/4.1.7/krita-4.1.7.101.tar.gz)

### md5sum

For all downloads:

- [md5sum.txt](https://download.kde.org/stable/krita/4.1.7/md5sum.txt)

### Key

The Linux appimage and the source tarball are signed. You can retrieve the public key over https here: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8). The signatures are [here](http://download.kde.org/stable/krita/4.1.7/) (filenames ending in .sig).

## Support Krita

Krita is a free and open source project. Please consider supporting the project with [donations](/support-us/donations/) or by [buying training videos or the artbook!](/support-us/shop) With your support, we can keep the core team working on Krita full-time.

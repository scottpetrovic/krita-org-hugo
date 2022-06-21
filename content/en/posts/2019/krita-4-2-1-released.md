---
title: "Krita 4.2.1 Released"
date: "2019-06-05"
categories: 
  - "officialrelease"
---

## Krita 4.2.1

Hot on the heels of 4.2.0, we're releasing Krita 4.2.1. Most importantly, this release fixes an issue where after painting for a long time, Krita would become slow because the undo stack would grow infinitely. There are other fixes, too: saving and loading .kra files containing vector layers with image names using non-latin1 characters has been fixed, too. Some fixes are by new contributor Carl Olsson, others by new contributor Dmitry Utkin, many thanks!

Here's the full list of fixes:

- Fix slowdown after a longer period of use ([BUG:408255](https://bugs.kde.org/show_bug.cgi?id=408255), [BUG:408133](https://bugs.kde.org/show_bug.cgi?id=408133))
- Fix loading vector layers when the image name is not latin1 ([BUG:408280](https://bugs.kde.org/show_bug.cgi?id=408280))
- Fix rectangular grid spacing limits incorrect after resizing canvas ([BUG:408166](https://bugs.kde.org/show_bug.cgi?id=408166))
- Fix layer properties window draws on top of other application windows ([BUG:408170](https://bugs.kde.org/show_bug.cgi?id=408170))
- Fix the posterize filter to use non-linear sRGB for computation
- Allow the animation render to start at frame 0 at all times ([BUG:408198](https://bugs.kde.org/show_bug.cgi?id=408198))
- Enable the Select Opaque actions for group layers ([BUG:408236](https://bugs.kde.org/show_bug.cgi?id=408236))
- Check whether the drive still exists before creating a temporary directory for animation rendering ([BUG:408246](https://bugs.kde.org/show_bug.cgi?id=408246))
- Prevent the user from deleting locked layers when pressing shift-del too quickly
- Fix copying and duplicating vector layers ([BUG:408028](https://bugs.kde.org/show_bug.cgi?id=408028))
- Fix Krita's canvas being transparent on Linux when built against older versions of Qt ([BUG:408225](https://bugs.kde.org/show_bug.cgi?id=408225))
- Fix possible small delays at the beginning of a stroke ([BUG:408133](https://bugs.kde.org/show_bug.cgi?id=408133))
- Fix folding/unfolding when clicking on a layer thumbnail
- Fix undo/redo when working with guides (patches by Summer of Code student Tusooa Zhu)
- Fix reversed Python API guides lock/show states ([BUG:408113](https://bugs.kde.org/show_bug.cgi?id=408113))
- Make the minimum size for brushes consistent through the application
- Make the auto brush spacing precision values consistent ([BUG:359453](https://bugs.kde.org/show_bug.cgi?id=359453))
- Improve selection behaviour on the layer docker ([BUG:408002](https://bugs.kde.org/show_bug.cgi?id=408002))
- Fix macOS zoom and rotate icon getting stuck ([BUG:404321](https://bugs.kde.org/show_bug.cgi?id=404321))
- Fix the vector stroke style propagating to other vector objects [(BUG:407683](https://bugs.kde.org/show_bug.cgi?id=407683))
- Fix the Document Tools plugin ([BUG:408146](https://bugs.kde.org/show_bug.cgi?id=408146))
- Fix the layer name being deselected when opening the layer name editor ([BUG:400357](https://bugs.kde.org/show_bug.cgi?id=400357))

Our builds of Krita 4.2.1 are also updated to use Qt 5.12.3, which should solve some problems with drag and drop; there might be new problems with display scaling on Windows, though, since the experimental patches for Qt that we used for 4.2.0 now give conflicts.

## Download

### Windows

Note for Windows users: if you encounter crashes, please follow [these instructions](https://docs.krita.org/en/reference_manual/dr_minw_debugger.html#dr-minw) to use the debug symbols so we can figure out where Krita crashes.

- 64 bits Windows: [krita-x64-4.2.1-setup.exe](https://download.kde.org/stable/krita/4.2.1/krita-x64-4.2.1-setup.exe)
- Portable 64 bits Windows: [krita-x64-4.2.1.zip](https://download.kde.org/stable/krita/4.2.1/krita-x64-4.2.1.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.2.1/krita-x64-4.2.1-dbg.zip)

- 32 bits Windows: [krita-x86-4.2.1-setup.exe](https://download.kde.org/stable/krita/4.2.1/krita-x86-4.2.1-setup.exe)
- Portable 32 bits Windows: [krita-x86-4.2.1.zip](https://download.kde.org/stable/krita/4.2.1/krita-x86-4.2.1.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.2.1/krita-x86-4.2.1-dbg.zip)

### Linux

- 64 bits Linux: [krita-4.2.1-x86\_64.appimage](https://download.kde.org/stable/krita/4.2.1/krita-4.2.1-x86_64.appimage)
- 64 bits Linux [G'Mic-Qt plugin appimage](https://download.kde.org/stable/krita/4.2.1/gmic_krita_qt-x86_64.appimage).

(If, for some reason, Firefox thinks it needs to load this as text: to download, right-click on the link.)

### OSX

- OSX disk image: [krita-4.2.1.dmg](https://download.kde.org/stable/krita/4.2.1/krita-4.2.1.dmg)

Note: the gmic-qt is not available on OSX.

### Source code

- [krita-4.2.1.tar.gz](https://download.kde.org/stable/krita/4.2.1/krita-4.2.1.tar.gz)
- [krita-4.2.1.tar.xz](https://download.kde.org/stable/krita/4.2.1/krita-4.2.1.tar.xz)

### md5sum

For all downloads:

- [md5sum.txt](https://download.kde.org/stable/krita/4.2.1/md5sum.txt)

### Key

The Linux appimage and the source tarball are signed. You can retrieve the public key over https here: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8). The signatures are [here](http://download.kde.org/unstable/krita/4.2.0-beta2/) (filenames ending in .sig).

## Support Krita

Krita is a free and open source project. Please consider supporting the project with [donations](https://krita.org/en/support-us/donations/) or by [buying training videos or the artbook!](https://krita.org/en/support-us/shop) With your support, we can keep the core team working on Krita full-time.

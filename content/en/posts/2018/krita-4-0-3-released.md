---
title: "Krita 4.0.3 Released"
date: "2018-05-12"
categories: 
  - "news"
  - "officialrelease"
---

Today the Krita team releases Krita 4.0.3, a bug fix release of Krita 4.0.0. This release fixes an important regression in Krita 4.0.2: sometimes copy and paste between images opened in Krita would cause crashes ([BUG:394068](https://bugs.kde.org/show_bug.cgi?id=394068)).

[![](/images/posts/2018/kiki_4.0_sm-1-1024x463.png)](/images/posts/2018/kiki_4.0_sm-1-1024x463.png)

## Other Improvements

- Krita now tries to load the system color profiles on Windows
- Krita can open .rw2 RAW files
- The splash screen is updated to work better on HiDPI or Retina displays ([BUG:392282](https://bugs.kde.org/show_bug.cgi?id=392282))
- The OpenEXR export filter will convert images with an integer channel depth before saving, instead of giving an error.
- The OpenEXR export filter no longer gives export warnings calling itself the TIFF filter
- The emtpy error message dialog that would erroneously be shown after running some export filters is no longer shown ([BUG:393850](https://bugs.kde.org/show_bug.cgi?id=393850)).
- The setBackGroundColor method in the Python API has been renamed to setBackgroundColor for consistency
- Fix a crash in KisColorizeMask ([BUG:393753](https://bugs.kde.org/show_bug.cgi?id=393753))

## Download

### Windows

Note for Windows users: if you encounter crashes, please follow [these instructions](https://docs.krita.org/Dr._Mingw_debugger) to use the debug symbols so we can figure out where Krita crashes.

- 64 bits Windows: [krita-x64-4.0.3-setup.exe](https://download.kde.org/stable/krita/4.0.3/krita-x64-4.0.3-setup.exe)
- Portable 64 bits Windows: [krita-x64-4.0.3.zip](https://download.kde.org/stable/krita/4.0.3/krita-x64-4.0.3.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.0.3/krita-x64-4.0.3-dbg.zip)

- 32 bits Windows: [krita-4.0.3-x86-setup.exe](https://download.kde.org/stable/krita/4.0.3/krita-x86-4.0.3-setup.exe)
- Portable 32 bits Windows: [krita-x86-4.0.3.zip](https://download.kde.org/stable/krita/4.0.3/krita-x86-4.0.3.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.0.3/krita-x86-4.0.3-dbg.zip)

### Linux

- 64 bits Linux: [krita-4.0.3-x86_64.appimage](https://download.kde.org/stable/krita/4.0.3/krita-4.0.3-x86_64.appimage)

(If, for some reason, Firefox thinks it needs to load this as text: to download, right-click on the link.)

When it is updated, you can also use the [Krita Lime PPA](https://launchpad.net/%7Ekritalime/+archive/ubuntu/ppa) to install Krita 4.0.3 on Ubuntu and derivatives. We are working on an updated snap.

### OSX

- OSX disk image: [krita-4.0.3.1.dmg](https://download.kde.org/stable/krita/4.0.3/krita-4.0.3.1.dmg)

Note: the touch docker, gmic-qt and python plugins are not available on OSX.

### Source code

- Source code: [krita-4.0.3.tar.gz](https://download.kde.org/stable/krita/4.0.3/krita-4.0.3.tar.gz)

### md5sum

For all downloads:

- [md5sum.txt](https://download.kde.org/stable/krita/4.0.3/md5sum.txt)

### Key

The Linux appimage and the source tarball are signed. You can retrieve the public key over https here: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8). The signatures are [here](http://download.kde.org/stable/krita/4.0.3/) (filenames ending in .sig).

## Support Krita

Krita is a free and open source project. Please consider supporting the project with [donations](/support-us/donations/) or by [buying training videos or the artbook!](/support-us/shop) With your support, we can keep the core team working on Krita full-time.

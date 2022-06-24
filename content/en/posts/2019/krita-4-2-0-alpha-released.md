---
title: "Krita 4.2.0-alpha Released"
date: "2019-05-08"
categories: 
  - "development-builds"
---

 

We're on track to release Krita 4.2.0  this month, and today we're releasing the alpha! That means that we're still fixing bugs like crazy -- just check what we've been doing this month:

[![](/images/posts/2019/bugs_april_may.png)](/images/posts/2019/bugs_april_may.png)

But of course there's much more. We've been working on this release for a long time now, since June last year when Krita 4.1 was released. We have fixed about 1500 bugs in that period, and implemented a host of new features, workflow improvements and little bits of spit and polish.

You can read all about the new features in the [release notes](/krita-4-2-release-notes/). Highlights are much improved tablet support on all platforms, HDR painting on Windows, improved painting performance, improved color palette docker, animation API for scripting, gamut masks, improved artistic color selector, an improved start screen that can now show you the latest news about Krita, changes to the way flow and opacity work when painting... And much more.

In the meantime, we've also worked [hard on the manual](https://docs.krita.org), to bring it up to date with this release. The manual for Krita 4.1.7 can still be [downloaded in epub format](https://download.kde.org/stable/krita/manual/4.1/).

**Warning**: Linux users should be careful with distribution packages. We have a [host of patches for Qt queued up](https://phabricator.kde.org/T10838), some of which are important for distributions to carry until the patches are merged and released in a new version of Qt.

## Download

### Windows

Note for Windows users: if you encounter crashes, please follow [these instructions](https://docs.krita.org/en/reference_manual/dr_minw_debugger.html#dr-minw) to use the debug symbols so we can figure out where Krita crashes.

- 64 bits Windows: [krita-x64-4.2.0-alpha-setup.exe](https://download.kde.org/unstable/krita/4.2.0-alpha/krita-x64-4.2.0-alpha-setup.exe)
- Portable 64 bits Windows: [krita-x64-4.2.0-alpha.zip](https://download.kde.org/unstable/krita/4.2.0-alpha/krita-x64-4.2.0-alpha.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/unstable/krita/4.2.0-alpha/krita-x64-4.2.0-alpha-dbg.zip)

- 32 bits Windows: [krita-x86-4.2.0-alpha-setup.exe](https://download.kde.org/unstable/krita/4.2.0-alpha/krita-x86-4.2.0-alpha-setup.exe)
- Portable 32 bits Windows: [krita-x86-4.2.0-alpha.zip](https://download.kde.org/unstable/krita/4.2.0-alpha/krita-x86-4.2.0-alpha.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/unstable/krita/4.2.0-alpha/krita-x86-4.2.0-alpha-dbg.zip)

### Linux

- 64 bits Linux: [krita-4.2.0-alpha-x86\_64.appimage](https://download.kde.org/unstable/krita/4.2.0-alpha/krita-4.2.0-alpha-x86_64.appimage)
- 64 bits Linux [G'Mic-Qt plugin appimage](https://download.kde.org/unstable/krita/4.2.0-alpha/gmic_krita_qt-x86_64.appimage).

(If, for some reason, Firefox thinks it needs to load this as text: to download, right-click on the link.)

### OSX

- OSX disk image: [krita-4.2.0-alpha.dmg](https://download.kde.org/unstable/krita/4.2.0-alpha/krita-4.2.0-alpha.dmg)

Note: the touch docker, gmic-qt and python plugins are not available on OSX.

### Source code

- Source code: [krita-4.2.0-alpha.101.tar.gz](https://download.kde.org/unstable/krita/4.2.0-alpha/krita-4.2.0-alpha.101.tar.gz)

### md5sum

For all downloads:

- [md5sum.txt](https://download.kde.org/unstable/krita/4.2.0-alpha/md5sum.txt)

### Key

The Linux appimage and the source tarball are signed. You can retrieve the public key over https here: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8). The signatures are [here](http://download.kde.org/unstable/krita/4.2.0-alpha/) (filenames ending in .sig).

## Support Krita

Krita is a free and open source project. Please consider supporting the project with [donations](/support-us/donations/) or by [buying training videos or the artbook!](/support-us/shop) With your support, we can keep the core team working on Krita full-time.

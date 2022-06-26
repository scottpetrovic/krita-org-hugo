---
title: "First Beta Release of Krita 4.1"
date: "2018-06-21"
---

Three months after the release of Krita 4.0, we're releasing the first (and probably only) beta of Krita 4.1, a new feature release! This release includes the following major new features:

{{< youtube LWpjlyUlBiA >}}

- A new reference images tool that replaces the old reference images docker.
- You can now save and load sessions: the set of images and views on images you were working on
- You can create multi-monitor workspace layouts
- An improved workflow for working with animation frames
- An improved animation timeline display
- Krita can now handle larger animation by buffering rendered frames to disk
- The color picker now has a mixing option
- Improved vanishing point assistant -- and assistants can be painted with custom colors
- Krita's scripting module can now be built with Python 2
- The first part of Ivan Yossi's Google Summer of Code work on improving the performance of brush masks through vectorization is included as well!

And there's more. Read the [full release notes](/krita-4-1-release-notes/) to discover what's new in Krita 4.1! With this beta release, the release notes are still work in progress, though.

## Download

### Windows

Note for Windows users: if you encounter crashes, please follow [these instructions](https://docs.krita.org/en/reference_manual/dr_minw_debugger.html#dr-minw) to use the debug symbols so we can figure out where Krita crashes.

- 64 bits Windows: [krita-x64-4.1.0-beta.2-setup.exe](https://download.kde.org/unstable/krita/4.1.0-beta.2/krita-x64-4.1.0-beta.2-setup.exe)
- Portable 64 bits Windows: [krita-x64-4.1.0-beta.2.zip](https://download.kde.org/unstable/krita/4.1.0-beta.2/krita-x64-4.1.0-beta.2.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/unstable/krita/4.1.0-beta.2/krita-x64-4.1.0-beta.2-dbg.zip)

- 32 bits Windows: [krita-4.1.0-beta.2-x86-setup.exe](https://download.kde.org/unstable/krita/4.1.0-beta.2/krita-x86-4.1.0-beta.2-setup.exe)
- Portable 32 bits Windows: [krita-x86-4.1.0-beta.2.zip](https://download.kde.org/unstable/krita/4.1.0-beta.2/krita-x86-4.1.0-beta.2.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/unstable/krita/4.1.0-beta.2/krita-x86-4.1.0-beta.2-dbg.zip)

### Linux

- 64 bits Linux: [krita-4.1.0-beta.2-x86_64.appimage](https://download.kde.org/unstable/krita/4.1.0-beta.2/krita-4.1.0-beta.2-x86_64.appimage)

(If, for some reason, Firefox thinks it needs to load this as text: to download, right-click on the link.)

When it is updated, you can also use the [Krita Lime PPA](https://launchpad.net/%7Ekritalime/+archive/ubuntu/ppa) to install Krita 4.1.0-beta.2 on Ubuntu and derivatives. We are working on an updated snap.

### OSX

- OSX disk image: [krita-4.1.0-beta.2.dmg](https://download.kde.org/unstable/krita/4.1.0-beta.2/krita-4.1.0-beta.2.dmg)

Note: the touch docker, gmic-qt and python plugins are not available on OSX.

### Source code

- Source code: [krita-4.1.0-beta.2.tar.gz](https://download.kde.org/unstable/krita/4.1.0-beta.2/krita-4.1.0-beta.2.tar.gz)

### md5sum

For all downloads:

- [md5sum.txt](https://download.kde.org/unstable/krita/4.1.0-beta.2/md5sum.txt)

### Key

The Linux appimage and the source tarball are signed. You can retrieve the public key over https here: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8). The signatures are [here](http://download.kde.org/unstable/krita/4.1.0-beta.2/) (filenames ending in .sig).

## Support Krita

Krita is a free and open source project. Please consider supporting the project with [donations](/support-us/donations/) or by [buying training videos or the artbook!](/support-us/shop) With your support, we can keep the core team working on Krita full-time.

---
title: "Krita 4.1.0 Released"
date: "2018-06-27"
categories: 
  - "news"
  - "officialrelease"
---

Three months after the release of Krita 4.0, we're releasing Krita 4.1!

{{< youtube N6oHLuICrHM >}}

This release includes the following major new features:

 

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

And there are a host of bug fixes, of course, and improvements to the rendering performance and more features. **Read the [full release notes](/krita-4-1-release-notes/) to discover what's new in Krita 4.1!**

\[caption id="attachment\_7657" align="aligncenter" width="500"\][![](../images/krita_41-1024x1024.png)](https://krita.org/wp-content/uploads/2018/06/krita_41.png) Image by RJ Quiralta\[/caption\]

## Note!

We found a bug where activating the transform tool will cause a crash if you had selected the Box filter previously. if you experience a crash when enabling the transform tool in krita 4.1.0, go to your kritarc file ([https://docs.krita.org/en/KritaFAQ.html#where-are-the-configuration-files-stored …](https://docs.krita.org/en/KritaFAQ.html#where-are-the-configuration-files-stored "https://docs.krita.org/en/KritaFAQ.html#where-are-the-configuration-files-stored")) and remove the line that says "filterId=Box" in the \[KisToolTransform\] section. Sorry for the inconvenience. We will bring out a bug fix release as soon as possible.

## Download

### Windows

Note for Windows users: if you encounter crashes, please follow [these instructions](https://docs.krita.org/en/reference_manual/dr_minw_debugger.html#dr-minw) to use the debug symbols so we can figure out where Krita crashes.

- 64 bits Windows: [krita-x64-4.1.0-setup.exe](https://download.kde.org/stable/krita/4.1.0/krita-x64-4.1.0-setup.exe)
- Portable 64 bits Windows: [krita-x64-4.1.0.zip](https://download.kde.org/stable/krita/4.1.0/krita-x64-4.1.0.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.1.0/krita-x64-4.1.0-dbg.zip)

- 32 bits Windows: [krita-x86-4.1.0-setup.exe](https://download.kde.org/stable/krita/4.1.0/krita-x86-4.1.0-setup.exe)
- Portable 32 bits Windows: [krita-x86-4.1.0.zip](https://download.kde.org/stable/krita/4.1.0/krita-x86-4.1.0.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.1.0/krita-x86-4.1.0-dbg.zip)

### Linux

- 64 bits Linux: [krita-4.1.0-x86\_64.appimage](https://download.kde.org/stable/krita/4.1.0/krita-4.1.0-x86_64.appimage)
- 64 bits Linux [G'Mic-Qt plugin appimage](https://download.kde.org/stable/krita/4.1.0/gmic_krita_qt-x86_64.appimage).

(If, for some reason, Firefox thinks it needs to load this as text: to download, right-click on the link.)

When it is updated, you can also use the [Krita Lime PPA](https://launchpad.net/%7Ekritalime/+archive/ubuntu/ppa) to install Krita 4.1.0 on Ubuntu and derivatives. We are working on an updated snap.

### OSX

- OSX disk image: [krita-4.1.0.dmg](https://download.kde.org/stable/krita/4.1.0/krita-4.1.0.dmg)

Note: the touch docker, gmic-qt and python plugins are not available on OSX.

### Source code

- Source code: [krita-4.1.0.tar.gz](https://download.kde.org/stable/krita/4.1.0/krita-4.1.0.tar.gz)

### md5sum

For all downloads:

- [md5sum.txt](https://download.kde.org/stable/krita/4.1.0/md5sum.txt)

### Key

The Linux appimage and the source tarball are signed. You can retrieve the public key over https here: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8). The signatures are [here](http://download.kde.org/stable/krita/4.1.0/) (filenames ending in .sig).

## Support Krita

Krita is a free and open source project. Please consider supporting the project with [donations](/support-us/donations/) or by [buying training videos or the artbook!](/support-us/shop) With your support, we can keep the core team working on Krita full-time.

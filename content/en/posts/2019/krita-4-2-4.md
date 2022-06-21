---
title: "Krita 4.2.4 Released"
date: "2019-07-31"
categories: 
  - "officialrelease"
---

We're releasing Krita 4.2.4 today. The most important fixes are to the shortcut input system and the saving system. Krita 4.2.3 had a bug where a message window would often pop up complaining about a shortcut not being finished properly; this should no longer happen. Anna Medonosova has hardened the saving system even more, especially when closing Krita after initiating a save operation.

There are some more bug fixes coming soon, and we will release 4.2.5 with those fixes in about two weeks, after the coming Krita sprint.

Additionally, we implemented a new blending mode inspired by Easy Painttool SAI's Luminosity/Shine, please help us to test its behavior ([BUG:409627](https://bugs.kde.org/show_bug.cgi?id=409627)).

## Known Issue

If touch zoom and rotation doesn't work anymore, please remove your local default.inputrc file. Go to Settings/Manage Resources and press the Open Resource Folder button. Enter the input folder and remove all files in that folder.

## Bugs Fixed

- Make it possible to use dots in filenames (note that that still might confuse your OS) ([BUG:409765](https://bugs.kde.org/show_bug.cgi?id=409765))
- Fix regression on softness sensor on Default Circle autobrush tip ([BUG:409758](https://bugs.kde.org/show_bug.cgi?id=409758))
- Clear any leftover points in the line tool on each use so there are no false starts ([BUG:408439](https://bugs.kde.org/show_bug.cgi?id=408439))
- Do not reset the opacity to zero when moving more than one shape at a time ([BUG:409131](https://bugs.kde.org/show_bug.cgi?id=409131))
- Do not ignore rotation in the bristle brush engine ([BUG:384231](https://bugs.kde.org/show_bug.cgi?id=384231))
- Fix cursor drift when using pan/zoom/rotate ([BUG:409460](https://bugs.kde.org/show_bug.cgi?id=409460))
- Fix a crash when creating an RGB image after the last used color model was CMYK ([BUG:409916](https://bugs.kde.org/show_bug.cgi?id=409916))
- Use Qt's QImageIO image import/export filter for PPM files instead of our own, broken implementation. ([BUG:409714](https://bugs.kde.org/show_bug.cgi?id=409714))
- Fix updating the brush size in the toolbar using shortcuts or drag ([BUG:408331](https://bugs.kde.org/show_bug.cgi?id=408331))
- Make generated gradient names translatable ([BUG:410034](https://bugs.kde.org/show_bug.cgi?id=410034))
- Fix a crash that could happen when closing Krita after deleting a session ([BUG:409909](https://bugs.kde.org/show_bug.cgi?id=409909))
- Fix a bug in the color picker that made it possible for the active foreground color to be transparent
- Fix a logic error in the Separate Image plugin ([BUG:410308](https://bugs.kde.org/show_bug.cgi?id=410308))
- Update the notes for the LargeRGB color profile ([BUG:410023](https://bugs.kde.org/show_bug.cgi?id=410023))
- Fix the filename reference for Rec.709 profiles
- Add a workaround for the KisShortcutsMatcher assert ([BUG:408826](https://bugs.kde.org/show_bug.cgi?id=408826))

## Download

### Windows

Note for Windows users: if you encounter crashes, please follow [these instructions](https://docs.krita.org/en/reference_manual/dr_minw_debugger.html#dr-minw) to use the debug symbols so we can figure out where Krita crashes.

- 64 bits Windows: [krita-x64-4.2.4-setup.exe](https://download.kde.org/stable/krita/4.2.4/krita-x64-4.2.4-setup.exe)
- Portable 64 bits Windows: [krita-x64-4.2.4.zip](https://download.kde.org/stable/krita/4.2.4/krita-x64-4.2.4.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.2.4/krita-x64-4.2.4-dbg.zip)

- 32 bits Windows: [krita-x86-4.2.4-setup.exe](https://download.kde.org/stable/krita/4.2.4/krita-x86-4.2.4-setup.exe)
- Portable 32 bits Windows: [krita-x86-4.2.4.zip](https://download.kde.org/stable/krita/4.2.4/krita-x86-4.2.4.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.2.4/krita-x86-4.2.4-dbg.zip)

### Linux

- 64 bits Linux: [krita-4.2.4-x86\_64.appimage](https://download.kde.org/stable/krita/4.2.4/krita-4.2.4-x86_64.appimage)
- 64 bits Linux [G'Mic-Qt plugin appimage](https://download.kde.org/stable/krita/4.2.4/gmic_krita_qt-x86_64.appimage).

(If, for some reason, Firefox thinks it needs to load this as text: to download, right-click on the link.)

### OSX

- OSX disk image: [krita-4.2.4.dmg](https://download.kde.org/stable/krita/4.2.4/krita-4.2.4.dmg)

Note: the gmic-qt is not available on OSX.

### Source code

- [krita-4.2.4.tar.gz](https://download.kde.org/stable/krita/4.2.4/krita-4.2.4.tar.gz)
- [krita-4.2.4.tar.xz](https://download.kde.org/stable/krita/4.2.4/krita-4.2.4.tar.xz)

### md5sum

For all downloads:

- [md5sum.txt](https://download.kde.org/stable/krita/4.2.4/md5sum.txt)

### Key

The Linux appimage and the source .tar.gz tarball are signed. You can retrieve the public key over https here: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8). The signatures are [here](http://download.kde.org/unstable/krita/4.2.0-beta2/) (filenames ending in .sig).

## Support Krita

Krita is a free and open source project. Please consider supporting the project with [donations](https://krita.org/en/support-us/donations/) or by [buying training videos or the artbook!](https://krita.org/en/support-us/shop) With your support, we can keep the core team working on Krita full-time.

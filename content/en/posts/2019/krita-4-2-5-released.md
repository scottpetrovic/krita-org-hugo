---
title: "Krita 4.2.5 Released"
date: "2019-08-02"
categories: 
  - "officialrelease"
---

We found that Krita 4.2.4 still had a bug handling shortcuts when certain tools were active. We've worked hard to fix that bug as quickly as possible, and as a consequence, we're releasing Krita 4.2.5 today. Everyone is urged to update to this new release.

## Bugs Fixed

- Fix an assert in the transform tool when working with a tablet and touch
- Fix continued transformation in the transform tool
- Fix updates in the transform tool
- Show the publication time in the welcome page news ticker in the user's preferred short date/time format
- Fix using the tangent-normal brush when the canvas is rotated or mirrored ([BUG:404408](https://bugs.kde.org/show_bug.cgi?id=404408))
- Make it possible again to create new palettes and save them in the resource folder, instead of the current document ([BUG:410137](https://bugs.kde.org/show_bug.cgi?id=410137))
- Make Krita not gobble up all available memory when loading a JPG file with specific metadata ([BUG:410242](https://bugs.kde.org/show_bug.cgi?id=410242))
- Constrain assistant editors to the viewport, so they can always be manipulated
- Make sure Krita stores changes to brush presets in the current session by default ([BUG:410463](https://bugs.kde.org/show_bug.cgi?id=410463))
- Remove an assert that could be triggered when opening the first image in a session
- Update the version of the default input settings profile, so the rotate/zoom action will be activated even if the user already had a local kritadefault.profile file
- Fix a crash on using the move tool while the image is being opened ([BUG:398968](https://bugs.kde.org/show_bug.cgi?id=398968))
- Make sure the painting tools don't block anymore (BUG:409968,408826,409275)
- Make the shortcut handling system more tolerant when shortcuts overlap ([BUG:409968](https://bugs.kde.org/show_bug.cgi?id=409968))
- Fix a crash in the transform tool
- Make the transform tool and the move tool more responsive

## Download

### Windows

Note for Windows users: if you encounter crashes, please follow [these instructions](https://docs.krita.org/en/reference_manual/dr_minw_debugger.html#dr-minw) to use the debug symbols so we can figure out where Krita crashes.

- 64 bits Windows: [krita-x64-4.2.5-setup.exe](https://download.kde.org/stable/krita/4.2.5/krita-x64-4.2.5-setup.exe)
- Portable 64 bits Windows: [krita-x64-4.2.5.zip](https://download.kde.org/stable/krita/4.2.5/krita-x64-4.2.5.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.2.5/krita-x64-4.2.5-dbg.zip)

- 32 bits Windows: [krita-x86-4.2.5-setup.exe](https://download.kde.org/stable/krita/4.2.5/krita-x86-4.2.5-setup.exe)
- Portable 32 bits Windows: [krita-x86-4.2.5.zip](https://download.kde.org/stable/krita/4.2.5/krita-x86-4.2.5.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.2.5/krita-x86-4.2.5-dbg.zip)

### Linux

- 64 bits Linux: [krita-4.2.5-x86_64.appimage](https://download.kde.org/stable/krita/4.2.5/krita-4.2.5-x86_64.appimage)
- 64 bits Linux [G'Mic-Qt plugin appimage](https://download.kde.org/stable/krita/4.2.5/gmic_krita_qt-x86_64.appimage).

(If, for some reason, Firefox thinks it needs to load this as text: to download, right-click on the link.)

### OSX

- OSX disk image: [krita-4.2.5.dmg](https://download.kde.org/stable/krita/4.2.5/krita-4.2.5.dmg)

Note: the gmic-qt is not available on OSX.

### Source code

- [krita-4.2.5.tar.gz](https://download.kde.org/stable/krita/4.2.5/krita-4.2.5.tar.gz)
- [krita-4.2.5.tar.xz](https://download.kde.org/stable/krita/4.2.5/krita-4.2.5.tar.xz)

### md5sum

For all downloads:

- [md5sum.txt](https://download.kde.org/stable/krita/4.2.5/md5sum.txt)

### Key

The Linux appimage and the source .tar.gz tarball are signed. You can retrieve the public key over https here: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8). The signatures are [here](http://download.kde.org/unstable/krita/4.2.0-beta2/) (filenames ending in .sig).

## Support Krita

Krita is a free and open source project. Please consider supporting the project with [donations](/support-us/donations/) or by [buying training videos or the artbook!](/support-us/shop) With your support, we can keep the core team working on Krita full-time.

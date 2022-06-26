---
title: "Krita 4.0.4 released!"
date: "2018-06-13"
---

Today the Krita team releases Krita 4.0.4, a bug fix release of Krita 4.0.0. This is the last bugfix release for Krita 4.0.

Here is the list of bug fixes in Krita 4.0.4:

- OpenColorIO now works on macOS
- Fix artefacts when painting with a pixel brush on a transparency mask ([BUG:394438](https://bugs.kde.org/show_bug.cgi?id=394438))
- Fix a race condition when using generator layers
- Fix a crash when editing a transform mask ([BUG:395224](https://bugs.kde.org/show_bug.cgi?id=395224))
- Add preset memory to the Ten Brushes Script, to make switching back and forward between brush presets more smooth.
- Improve the performance of the stroke layer style ([BUG:361130](https://bugs.kde.org/show_bug.cgi?id=361130), [BUG:390985](https://bugs.kde.org/show_bug.cgi?id=390985))
- Do not allow nesting of .kra files: using a .kra file with embedded file layers as a file layer would break on loading.
- Keep the alpha channel when applying the threshold filter ([BUG:394235](https://bugs.kde.org/show_bug.cgi?id=394235))
- Do not use the name of the bundle file as a tag automatically ([BUG:394345](https://bugs.kde.org/show_bug.cgi?id=394345))
- Fix selecting colors when using the python palette docker script ([BUG:394705](https://bugs.kde.org/show_bug.cgi?id=394705))
- Restore the last used colors on starting Krita, not when creating a new view ([BUG:394816](https://bugs.kde.org/show_bug.cgi?id=394816))
- Allow creating a layer group if the currently selected node is a mask ([BUG:394832](https://bugs.kde.org/show_bug.cgi?id=394832))
- Show the correct opacity in the segment gradient editor ([BUG:394887](https://bugs.kde.org/show_bug.cgi?id=394887))
- Remove the obsolete shortcuts for the old text and artistic text tool ([BUG:393508](https://bugs.kde.org/show_bug.cgi?id=393508))
- Allow setting the multibrush angle in fractions
- Improve performance of the OpenGL canvas, especially on macOS
- Fix painting of pass-through group layers in isolated mode ([BUG:394437](https://bugs.kde.org/show_bug.cgi?id=394437))
- Improve performance of loading OpenEXR files (patch by Jeroen Hoolmans)
- Autosaving will now happen even if Krita is kept very busy
- Improve loading of the default language
- Fix color picking when double-clicking ([BUG:394396](https://bugs.kde.org/show_bug.cgi?id=394396))
- Fix inconsistent frame numbering when calling FFMpeg ([BUG:389045](https://bugs.kde.org/show_bug.cgi?id=389045))
- Fix channel swizzling problem on macOS, where in 16 and 32 bits floating point channel depths red and blue would be swapped
- Fix accepting touch events with recent Qt versions
- Fix integration with the Breeze theme: Krita no longer tries to create widgets in threads ([BUG:392190](https://bugs.kde.org/show_bug.cgi?id=392190))
- Fix the batch mode flag when loading images from Python
- Load the system color profiles on Windows and macOS.
- Fix a crash on macOS ([BUG:394068](https://bugs.kde.org/show_bug.cgi?id=394068))

## Download

### Windows

Note for Windows users: if you encounter crashes, please follow [these instructions](https://docs.krita.org/en/reference_manual/dr_minw_debugger.html#dr-minw) to use the debug symbols so we can figure out where Krita crashes.

- 64 bits Windows: [krita-x64-4.0.4-setup.exe](https://download.kde.org/stable/krita/4.0.4/krita-x64-4.0.4-setup.exe)
- Portable 64 bits Windows: [krita-x64-4.0.4.zip](https://download.kde.org/stable/krita/4.0.4/krita-x64-4.0.4.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.0.4/krita-x64-4.0.4-dbg.zip)

- 32 bits Windows: [krita-4.0.4-x86-setup.exe](https://download.kde.org/stable/krita/4.0.4/krita-x86-4.0.4-setup.exe)
- Portable 32 bits Windows: [krita-x86-4.0.4.zip](https://download.kde.org/stable/krita/4.0.4/krita-x86-4.0.4.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.0.4/krita-x86-4.0.4-dbg.zip)

### Linux

- 64 bits Linux: [krita-4.0.4-x86_64.appimage](https://download.kde.org/stable/krita/4.0.4/krita-4.0.4-x86_64.appimage)

(If, for some reason, Firefox thinks it needs to load this as text: to download, right-click on the link.)

When it is updated, you can also use the [Krita Lime PPA](https://launchpad.net/%7Ekritalime/+archive/ubuntu/ppa) to install Krita 4.0.4 on Ubuntu and derivatives. We are working on an updated snap.

### OSX

- OSX disk image: [krita-4.0.4.dmg](https://download.kde.org/stable/krita/4.0.4/krita-4.0.4.dmg)

Note: the touch docker, gmic-qt and python plugins are not available on OSX.

### Source code

- Source code: [krita-4.0.4.tar.gz](https://download.kde.org/stable/krita/4.0.4/krita-4.0.4.tar.gz)

### md5sum

For all downloads:

- [md5sum.txt](https://download.kde.org/stable/krita/4.0.4/md5sum.txt)

### Key

The Linux appimage and the source tarball are signed. You can retrieve the public key over https here: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8). The signatures are [here](http://download.kde.org/stable/krita/4.0.4/) (filenames ending in .sig).

## Support Krita

Krita is a free and open source project. Please consider supporting the project with [donations](/support-us/donations/) or by [buying training videos or the artbook!](/support-us/shop) With your support, we can keep the core team working on Krita full-time.

---
title: "Krita 4.2.6 released"
date: "2019-09-10"
categories: 
  - "officialrelease"
---

A bit later than expected, because of a regression found during [beta testing](/item/help-beta-test-krita-4-2-6/), we're releasing Krita 4.2.6. Over 120 people have participated in the beta test survey, so this is something we'll repeat for the next release.

This release also contains an important workaround for users with an AMD Ryzen 5 3500 CPU. This CPU has a bug in its hardware random generator that caused crashes.

### New features:

- Add new layer from visible to layer right-click context menu.
- When running Krita for the first time on Windows, Angle is now the default renderer. **Note** that if you have an NVidia GPU and Krita's window is transparent, you need to select Angle manually in Krita's settings; if you have another GPU and you have problems with the canvas not updating, you might need to manually select OpenGL in the same window.

We want to especially thank Karl Ove Hufthammer for his extensive work on polishing the translatable string.

### Bugs fixed

- Allow selection overlay to be reset to default. ([BUG:410470](https://bugs.kde.org/show_bug.cgi?id=410470))
- Set date for bundle creation to use ISO-Date. ([BUG:410490](https://bugs.kde.org/show_bug.cgi?id=410490))
- Fix freeze with 32bit float tiff by using our own tiff reader for the thumbnails. ([BUG:408731](https://bugs.kde.org/show_bug.cgi?id=408731))
- Ensure filter mask button is disabled appropriately depending on whether the filter supports it. ([BUG:410374](https://bugs.kde.org/show_bug.cgi?id=410374))
- Enable the small color selector if opengles is available as well ([BUG:410602](https://bugs.kde.org/show_bug.cgi?id=410602))
- Fix mixed Zoom, Pan, Rotate on macOS ([BUG:410698](https://bugs.kde.org/show_bug.cgi?id=410698))
- Ensure that checkboxes are shown in menus even when using the fusion theme
- Isolate Layer Crash ([BUG:408785](https://bugs.kde.org/show_bug.cgi?id=408785))
- Properly fix font resetting when all the text in the editor removed ([BUG:409243](https://bugs.kde.org/show_bug.cgi?id=409243))
- Fix lags in Move Tool when using tablet device ([BUG:410838](https://bugs.kde.org/show_bug.cgi?id=410838))
- Fix Shift and Alt modifiers in Outline Selection Tool ([BUG:410532](https://bugs.kde.org/show_bug.cgi?id=410532))
- Ensure Convert group to Animated Layer shows text in the toolbar. ([BUG:410500](https://bugs.kde.org/show_bug.cgi?id=410500))
- Allow 'Add Clone Layer' to Work on Multiple Layers ([BUG:373338](https://bugs.kde.org/show_bug.cgi?id=373338))
- Fix saving animated transparency masks created through conversion ([BUG:409895](https://bugs.kde.org/show_bug.cgi?id=409895))
- Partially fix the curve change despite 'Share curve across all settings' checked ([BUG:383909](https://bugs.kde.org/show_bug.cgi?id=383909))
- Try harder to make sure that the swap location is writable
- Properly handle timezones in bundles
- Make sure all the settings dialogs pages are always shown in the same order
- Make the settings dialog fit in low-res screens ([BUG:410793](https://bugs.kde.org/show_bug.cgi?id=410793))
- Remove misleading ‘px’ suffix for ‘move amount’ shortcut setting
- Make string for reasons for image export problems translatable ([BUG:406973](https://bugs.kde.org/show_bug.cgi?id=406973))
- Fix crash when creating a bezier curve ([BUG:410572](https://bugs.kde.org/show_bug.cgi?id=410572))
- Fix deadlocks in KoShapeManager ([BUG:410909](https://bugs.kde.org/show_bug.cgi?id=410909), [BUG:410572](https://bugs.kde.org/show_bug.cgi?id=410572))
- Fix a deadlock when using broken Wacom drivers on Linux ([BUG:410797](https://bugs.kde.org/show_bug.cgi?id=410797))
- Fix absolute brush rotation on rotated canvas ([BUG:292726](https://bugs.kde.org/show_bug.cgi?id=292726))
- Fix deadlock when removing reference image ([BUG:411212](https://bugs.kde.org/show_bug.cgi?id=411212))
- Fix a deadlock in handling of vector objects ([BUG:411365](https://bugs.kde.org/show_bug.cgi?id=411365))
- Fix autosave saving only once ([BUG:411631](https://bugs.kde.org/show_bug.cgi?id=411631))

## Download

### Windows

Note for Windows users: if you encounter crashes, please follow [these instructions](https://docs.krita.org/en/reference_manual/dr_minw_debugger.html#dr-minw) to use the debug symbols so we can figure out where Krita crashes.

- 64 bits Windows: [krita-x64-4.2.6-setup.exe](https://download.kde.org/stable/krita/4.2.6/krita-x64-4.2.6-setup.exe)
- Portable 64 bits Windows: [krita-x64-4.2.6.zip](https://download.kde.org/stable/krita/4.2.6/krita-x64-4.2.6.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.2.6/krita-x64-4.2.6-dbg.zip)

- 32 bits Windows: [krita-x86-4.2.6-setup.exe](https://download.kde.org/stable/krita/4.2.6/krita-x86-4.2.6-setup.exe)
- Portable 32 bits Windows: [krita-x86-4.2.6.zip](https://download.kde.org/stable/krita/4.2.6/krita-x86-4.2.6.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.2.6/krita-x86-4.2.6-dbg.zip)

### Linux

- 64 bits Linux: [krita-4.2.6-x86_64.appimage](https://download.kde.org/stable/krita/4.2.6/krita-4.2.6-x86_64.appimage)
- 64 bits Linux [G'Mic-Qt plugin appimage](https://download.kde.org/stable/krita/4.2.6/gmic_krita_qt-x86_64.appimage).

(If, for some reason, Firefox thinks it needs to load this as text: to download, right-click on the link.)

### OSX

- OSX disk image: [krita-4.2.6.dmg](https://download.kde.org/stable/krita/4.2.6/krita-4.2.6.dmg)

Note: the gmic-qt is not available on OSX.

### Source code

- [krita-4.2.6.tar.gz](https://download.kde.org/stable/krita/4.2.6/krita-4.2.6.tar.gz)
- [krita-4.2.6.tar.xz](https://download.kde.org/stable/krita/4.2.6/krita-4.2.6.tar.xz)

### md5sum

For all downloads:

- [md5sum.txt](https://download.kde.org/stable/krita/4.2.6/md5sum.txt)

### Key

The Linux appimage and the source .tar.gz and .tar.xz tarballs are signed. You can retrieve the public key over https here: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8). The signatures are [here](http://download.kde.org/unstable/krita/4.2.0-beta2/) (filenames ending in .sig).

## Support Krita

Krita is a free and open source project. Please consider supporting the project with [donations](/support-us/donations/) or by [buying training videos or the artbook!](/support-us/shop) With your support, we can keep the core team working on Krita full-time.

---
title: "Krita 4.2.3 Released"
date: "2019-07-17"
categories: 
  - "officialrelease"
---

Today we're releasing Krita 4.2.3. This is mostly a bug fix release, but has one new feature: it is now possible to rotate the canvas with a two-finger touch gesture. This feature was implemented by Sharaf Zaman for his 2019 Google Summer of Code work of porting Krita to Android. The feature also works on other platforms, of course.

The most important bug fix is a workaround for Windows installations with broken, outdated or insufficient graphics drivers. The core of the issue is that our development platform, Qt, in its current version needs a working OpenGL or Direct3D installation as soon as there is a single component in the application that uses QML, a technology for creating user interfaces. We have managed to work around this issue and especially users of Windows 7 systems that have become a bit messy should be able to run Krita again.

## Bugs Fixed

- Make it possible for Krita to use a software renderer on Windows ([BUG:408872](https://bugs.kde.org/show_bug.cgi?id=408872))
- Fix the caption of the Background Color color selection dialog ([BUG:407658](https://bugs.kde.org/show_bug.cgi?id=407658))
- Fix the tag selector combobox so it is possible to select resources that have a tag that's longer than fits in the combobox ([BUG:408053](https://bugs.kde.org/show_bug.cgi?id=408053))
- Make it possible for the Krita startup window to become as narrow as before adding the news widget ([BUG:408504](https://bugs.kde.org/show_bug.cgi?id=408504))
- Fix copy/pasting of animation frames ([BUG:408421](https://bugs.kde.org/show_bug.cgi?id=408421), [BUG:404595](https://bugs.kde.org/show_bug.cgi?id=404595))
- Make the polygon and outline selection tool handle the control modifier correctly ([BUG:376007](https://bugs.kde.org/show_bug.cgi?id=376007))
- Add a reload script button to the Python scripter plugin
- Fix a crash in the Overview docker when there is no image open
- Fix drag and drop of fill layers between opened files ([BUG:408019](https://bugs.kde.org/show_bug.cgi?id=408019))
- Fix loading EXR files that have more than one layer with the same name ([BUG:409552](https://bugs.kde.org/show_bug.cgi?id=409552))
- Hide vanishing points preview lines when assistants are hidden ([BUG:396158](https://bugs.kde.org/show_bug.cgi?id=396158))
- Fix the Mirror All Layers Horizontally function
- Fix switching profile to default when changing channel depth in the New Image dialog ([BUG:406700](https://bugs.kde.org/show_bug.cgi?id=406700))
- Disable AVG optimizations for some 32 bit blending modes ([BUG:404133](https://bugs.kde.org/show_bug.cgi?id=404133))
- Fix a crash when pressing cancel when trying to create an 8 bit/channel linear gamma RGB image
- Fix colors drifting when using the native macOS color selection dialog ([BUG:407880](https://bugs.kde.org/show_bug.cgi?id=407880))
- Make sure Stroke Selection paint correctly with the selection border in the middle of the selection ([BUG:409254](https://bugs.kde.org/show_bug.cgi?id=409254))
- Fix saving Krita when perspective assistants are present ([BUG:409249](https://bugs.kde.org/show_bug.cgi?id=409249))
- Fix issues with transformations being pixelated ([BUG:409280](https://bugs.kde.org/show_bug.cgi?id=409280))
- Make it possible to hide all layers except the selected one with shift-click ([BUG:376086](https://bugs.kde.org/show_bug.cgi?id=376086))
- Fix cloning keyframe channels that are not opacity channels
- Fix a hang when trying to paint while playing an animation of an empty image ([BUG:408749](https://bugs.kde.org/show_bug.cgi?id=408749))
- Fix Isolated Mode when multiple windows are open ([BUG:408150](https://bugs.kde.org/show_bug.cgi?id=408150))
- Make the gradient editor show the right editor for stop and segmented gradients (but creating new gradients in Krita is still broken)
- Make Krita use the integrated GPU on dual-GPU Apple computers
- Fix a freeze when pressing delete when making a polygonal selection ([BUG:408843](https://bugs.kde.org/show_bug.cgi?id=408843))
- Fix the --export commandline option to return 0 when the export is successful ([BUG:409133](https://bugs.kde.org/show_bug.cgi?id=409133))
- Fix support for the KDE Plasma global menu ([BUG:408015](https://bugs.kde.org/show_bug.cgi?id=408015))
- Fix a crash when using the shrink option of the deform brush ([BUG:408887](https://bugs.kde.org/show_bug.cgi?id=408887))

## Download

### Windows

Note for Windows users: if you encounter crashes, please follow [these instructions](https://docs.krita.org/en/reference_manual/dr_minw_debugger.html#dr-minw) to use the debug symbols so we can figure out where Krita crashes.

- 64 bits Windows: [krita-x64-4.2.3-setup.exe](https://download.kde.org/stable/krita/4.2.3/krita-x64-4.2.3-setup.exe)
- Portable 64 bits Windows: [krita-x64-4.2.3.zip](https://download.kde.org/stable/krita/4.2.3/krita-x64-4.2.3.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.2.3/krita-x64-4.2.3-dbg.zip)

- 32 bits Windows: [krita-x86-4.2.3-setup.exe](https://download.kde.org/stable/krita/4.2.3/krita-x86-4.2.3-setup.exe)
- Portable 32 bits Windows: [krita-x86-4.2.3.zip](https://download.kde.org/stable/krita/4.2.3/krita-x86-4.2.3.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.2.3/krita-x86-4.2.3-dbg.zip)

### Linux

- 64 bits Linux: [krita-4.2.3-x86\_64.appimage](https://download.kde.org/stable/krita/4.2.3/krita-4.2.3-x86_64.appimage)
- 64 bits Linux [G'Mic-Qt plugin appimage](https://download.kde.org/stable/krita/4.2.3/gmic_krita_qt-x86_64.appimage).

(If, for some reason, Firefox thinks it needs to load this as text: to download, right-click on the link.)

### OSX

- OSX disk image: [krita-4.2.3.dmg](https://download.kde.org/stable/krita/4.2.3/krita-4.2.3.dmg)

Note: the gmic-qt is not available on OSX.

### Source code

- [krita-4.2.3.tar.gz](https://download.kde.org/stable/krita/4.2.3/krita-4.2.3.tar.gz)
- [krita-4.2.3.tar.xz](https://download.kde.org/stable/krita/4.2.3/krita-4.2.3.tar.xz)

### md5sum

For all downloads:

- [md5sum.txt](https://download.kde.org/stable/krita/4.2.3/md5sum.txt)

### Key

The Linux appimage and the source .tar.gz tarball are signed. You can retrieve the public key over https here: [ 0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8). The signatures are [here](http://download.kde.org/unstable/krita/4.2.0-beta2/) (filenames ending in .sig).

## Support Krita

Krita is a free and open source project. Please consider supporting the project with [donations](https://krita.org/en/support-us/donations/) or by [buying training videos or the artbook!](https://krita.org/en/support-us/shop) With your support, we can keep the core team working on Krita full-time.

---
title: "Krita 3.1 Beta 4 Released"
date: "2016-11-16"
---

Here is the fourth Krita 3.1 beta! From the Krita 3.1 on, Krita will officially support OSX. All OSX users are urged to use this version instead of earlier "stable" versions for OSX. We're releasing a fourth beta because of more changes to the code that actually saves your images... We've tried to make it much safer, but please do test this!

These are the most important fixes:

- Improve the framerate of the stabilizer
- Fix a regression with saving animations in the previous beta (3.0.92)
- Fix some crashes when drawing in the scratch pad
- Make the color selector in the color-to-alpha filter work properly

Note: the beta still contains the colorize mask/lazy brush plugin. We will probably remove that feature in the final release because the current algorithm is too slow to be usable, and we're still looking for and experimenting with new algorithms. With the current beta you will get a preview of how the user interface will work, but keep in mind that the we _know_ that it's too slow to be usable and are working on fixing that

The fourth beta is also much more stable and usable than earlier builds, and we'd like to ask everyone to try to use this version in production and help us find bugs and issues!

You can find out more about what is going to be new in Krita 3.1 in the [release notes](/release-notes-for-krita-3-1). The release notes aren't finished yet, but take a sneak peek all the same!

### Windows

Note for Windows users: if you encounter crashes, please follow [these instructions](https://docs.krita.org/Dr._Mingw_debugger) to use the debug symbols so we can figure out where Krita crashes.

- 32 bits Windows: [krita-3.0.93-x86-setup.exe](http://download.kde.org/unstable/krita/3.0.93/krita-3.0.93-x86-setup.exe) (MD5 Hash: ad8d773b10772616e5d8ed623c648a80)
- Portable 32 bits Windows: [krita-3.0.93-x86.zip](http://download.kde.org/unstable/krita/3.0.93/krita-3.0.93-x86.zip) (MD5 Hash: a4632822eeea5ce572544ea9a3b53d41)
- [Debug symbols. (Unpack in the Krita installation folder)](http://download.kde.org/unstable/krita/3.0.93/krita-3.0.93-x86-dbg.zip) (MD5 Hash: dc59208feabb7af99267984a6fe5a5e1)

- 64 bits Windows: [krita-3.0.93-x64-setup.exe](http://download.kde.org/unstable/krita/3.0.93/krita-3.0.93-x64-setup.exe) (MD5 Hash: 2930af181a810c4974d7f056d751e766)
- Portable 64 bits Windows: [krita-3.0.93-x64.zip](http://download.kde.org/unstable/krita/3.0.93/krita-3.0.93-x64.zip) (MD5 Hash: 9d895b6727d835e0267e4c20aa3d8934)
- [Debug symbols. (Unpack in the Krita installation folder)](http://download.kde.org/unstable/krita/3.0.93/krita-3.0.93-x64-dbg.zip) (MD5 Hash: 3beca45f6ba2b3c43ce70aee2b27742d)

### Linux

- 64 bits Linux: [krita-3.0.93-x86_64.appimage](http://download.kde.org/unstable/krita/3.0.93/krita-3.0.93-x86_64.appimage) (MD5 Hash: ff3e3f49fbd095504b7cdb3af5698c96)

A snap image for the Ubuntu App Store is available in the beta channel.

### OSX

- OSX disk image: [krita-3.0.93.dmg](http://download.kde.org/unstable/krita/3.0.93/krita-3.0.93.dmg) (MD5 Hash: acd4056716f8c272d8975ed9ca8f0a9d)

### Source code

- Source code: [krita-3.0.93.tar.gz](http://download.kde.org/unstable/krita/3.0.93/krita-3.0.93.tar.gz) (MD5 Hash: 6c26648fe82887ad28a0bf84711292cc)

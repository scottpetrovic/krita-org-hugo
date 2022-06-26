---
title: "Krita 3.0.1 Beta Builds"
date: "2016-08-23"
---

We've made a new set of development builds in the road to Krita 3.0.1. Here are the most important bug fixes:

- Saving and exporting is much more robust (but make sure your temp folder has space)
- Using the threshold filter as a mask and the threshold filter preview for colorspaces other than 8 bits RGBA have been fixed.
- The 3_texture brush tip has been fixed
- Saving templates works again
- The color labels in the layer box look better
- The layout of the grids and guides docker is fixed
- Multi-threading in general has been improved, thanks to a patch by Andrew Savonichev
- Scaling is done before transformation of a brush so the new ratio option now looks more correct
- Some display issues (black screens) when using assistants on NVida GPU's have been fixed
- Switching brushes is much faster and doesn't leak memory

In other news, the Krita team will get together in Deventer, the Netherlands, this weekend to meet in person! We'll be fixing bugs, discussing and planning new features and plans for new training videos and more!

#### Windows

On Windows, Krita supports Wacom, Huion and Yiynova tablets, as well as the Surface Pro series of tablets. The portable zip file builds can be unzipped and run by double-clicking the krita link.

Krita on Windows is tested on Windows 7, Windows 8 and Windows 10. There is only a Windows 64 bits build for now. Also, there is debug build that together with the DrMingw debugger can help with finding the cause of crashes. See the new [FAQ entry](https://docs.krita.org/KritaFAQ#How_can_I_produce_a_backtrace_on_Windows.3F). The Windows builds can be slower than usual because vectorization is disabled.

- [krita-3.0.99.90-x64-beta.zip](http://files.kde.org/krita/3/windows/devbuilds/krita-3.0.99.90-x64-beta.zip) (MD5 e98b07a732e05bcb86ba038badcb44a4)
- [krita3-x64-dbg-latest.zip](http://files.kde.org/krita/3/windows/debugbuilds/krita3-x64-dbg-latest.zip) (MD5 65220e9f12ead3bf2752c4db989634f4)

#### Linux

For Linux, we offer [AppImages](http://appimage.org/) that should run on any reasonable recent Linux distribution. You can download the appimage, make it executable and run it in place. No installation is needed. At this moment, we only have appimages for 64 bits versions of Linux. This appimage has experimental desktop integration.

- [krita-3.0.99.90-x64.appimage](http://files.kde.org/krita/3/linux/devbuilds/krita-3.0.99.90-x64.appimage) (MD5 2a39fddc1dece779ea36c3d03d08bb60)

You can also get Krita from [Ubuntu’s App Store in snap format](https://uappexplorer.com/app/krita.krita). This version includes the translations for Krita itself. Install with

snap install --beta krita

#### OSX and MacOS

Krita on OSX will be fully supported with version 3.1. Krita 3.0 for OSX is still missing Instant Preview and High Quality Canvas scaling. There are also some issues with rendering the image — these issues follow from Apple’s decision to drop support for the OpenGL 3.0 compatibility profile in their display drivers and issue with touchpad and tablet support. We are working to reimplement these features using OpenGL 3.0 Core profile. For now, we recommend disabling OpenGL when using Krita on OSX for production work. Krita for OSX runs on 10.9, 10.10, 10.11 and is reported to work on MacOS too.

- [krita-3.0.99.90.dmg](http://files.kde.org/krita/3/osx/devbuilds/krita-3.0.99.90.dmg) (a4c2dc7c51aa43adee7acceacaf82164)

#### Source

- [krita-3.0.99.90.tar.gz](http://files.kde.org/krita/3/source/krita-3.0.99.90.tar.gz) (MD5 e5b50274b617cb5356030aa22cbcdf1b)

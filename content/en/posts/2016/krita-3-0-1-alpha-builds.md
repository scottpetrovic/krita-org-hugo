---
title: "Krita 3.0.1 Alpha Builds"
date: "2016-08-16"
---

Last week the merge window closed and Krita entered a four week stabilization phase. Several very interesting branches were merged, with features ranging from a new head-up-display for quickly changing brush settings, a wavelet filter, a threshold filter, to a an upgrade for all number entry boxes: those support maths now! Sadly, we haven't managed to dot all the i's on the video-export branch for saving animated gifs and videos, so that's not in.

And because of broken hardware, we couldn't make builds for a week. Krita still needs volunteers who can help out making proper builds for all operating systems -- right now, it's still the maintainer who does that on his own, next to all the other work. But with the disks replaced, we've got new builds now!

These builds are already several bug fixes behind, of course, but still, please do test them! If you find a bug, please, please, please do check whether it has already been reported in bugs.kde.org before reporting!

We'll be back next week with the first beta builds! The release is still planned for September5th.

#### Windows

On Windows, Krita supports Wacom, Huion and Yiynova tablets, as well as the Surface Pro series of tablets. The portable zip file builds can be unzipped and run by double-clicking the krita link.

Krita on Windows is tested on Windows 7, Windows 8 and Windows 10. There is only a Windows 64 bits build for now. Also, there is debug build that together with the DrMingw debugger can help with finding the cause of crashes. See the new [FAQ entry](https://docs.krita.org/KritaFAQ#How_can_I_produce_a_backtrace_on_Windows.3F). The Windows builds can be slower than usual because vectorization is disabled.

- [krita-3.0.1-alpha2-x64.zip](http://files.kde.org/krita/3/windows/devbuilds/krita-3.0.1-alpha2-x64.zip) (a0ee7187035d890445c468a381d3fc2c)
- [krita3-x64-dbg-latest.zip](http://files.kde.org/krita/3/windows/debugbuilds/krita3-x64-dbg-latest.zip) (a0c100335a7d55cfc2710fe1cb2b39a2)

#### Linux

For Linux, we offer [AppImages](http://appimage.org/) that should run on any reasonable recent Linux distribution. You can download the appimage, make it executable and run it in place. No installation is needed. At this moment, we only have appimages for 64 bits versions of Linux. This appimage has experimental desktop integration.

- [krita-3.0.1-Alpha2-d33dbe0-x86_64.appimage](http://files.kde.org/krita/3/linux/devbuilds/krita-3.0.1-Alpha2-d33dbe0-x86_64.appimage) (f61f8991a517a7835ceebf7159288d8e)

#### OSX and MacOS

Krita on OSX will be fully supported with version 3.1. Krita 3.0 for OSX is still missing Instant Preview and High Quality Canvas scaling. There are also some issues with rendering the image — these issues follow from Apple’s decision to drop support for the OpenGL 3.0 compatibility profile in their display drivers and issue with touchpad and tablet support. We are working to reimplement these features using OpenGL 3.0 Core profile. For now, we recommend disabling OpenGL when using Krita on OSX for production work. Krita for OSX runs on 10.9, 10.10, 10.11 and is reported to work on MacOS too.

- [krita-3.0.1-Alpha2.dmg](http://files.kde.org/krita/3/osx/devbuilds/krita-3.0.1-Alpha2.dmg) (26a2ee299e63aed6a0a77b6c5a78ab0b)

#### Source

The source tarball now includes the translations.

- [krita-3.0.99.89.tar.xz](http://files.kde.org/krita/3/source/krita-3.0.99.89.tar.xz) (af9424c06ce6b1504859a5abd703955a)

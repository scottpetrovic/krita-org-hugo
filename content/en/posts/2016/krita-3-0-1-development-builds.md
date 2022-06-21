---
title: "Krita 3.0.1 Development Builds"
date: "2016-07-22"
---

Because of unforeseen circumstances, we had to rejig our release schedule, there was no release last week. Still, we wanted to bring you a foretaste of some of the goodies that are going to be in the 3.0.1 release, which is now planned for September 5th. There's lots to play with, here, from bug fixes (the double dot in file names is gone, the crash with cheap tablets is gone, a big issue with memory leaks in the graphics card is solved), to features (soft-proofing, among others). There may also be new bugs, and not all new features may be working correctly. Export to animated gif or video clips is still in development, and probably will not work well outside the developers' computer.

After all, this is a _development_ snapshot. Still, please experiment with it and test it, and we're pretty sure that for many purposes it might be better already than the 3.0 stable release!

On the OSX front we've made progress, too, and this build should run fine on OSX 10.9 upwards, including 10.10. All libraries are updated to the latest version, too.

#### Windows

On Windows, Krita supports Wacom, Huion and Yiynova tablets, as well as the Surface Pro series of tablets. The portable zip file builds can be unzipped and run by double-clicking the krita link.

Krita on Windows is tested on Windows 7, Windows 8 and Windows 10. There is only a Windows 64 bits build for now. There is now also a debug build that together with the DrMingw debugger can help with finding the cause of crashes. See the new [FAQ entry](https://docs.krita.org/KritaFAQ#How_can_I_produce_a_backtrace_on_Windows.3F). The Windows builds can be slower than usual because vectorization is disabled.

- [krita-3.0.1-Alpha-ef558bb-x64.zip](http://files.kde.org/krita/3/windows/devbuilds/krita-3.0.1-Alpha-ef558bb-x64.zip) (MD5: b4e4bc6563fdf1fd62f2b90ba66b3b6e)
- [krita3-x64-dbg-latest.zip](http://files.kde.org/krita/3/windows/debugbuilds/krita3-x64-dbg-latest.zip) (MD5: c039820a78272f2502cc3270b1cc7307

#### Linux

For Linux, we offer [AppImages](http://appimage.org/) that should run on any reasonable recent Linux distribution. You can download the appimage, make it executable and run it in place. No installation is needed. At this moment, we only have appimages for 64 bits versions of Linux.

- [krita-3.0.1-Alpha-4c91a18-x86\_64.appimage](http://files.kde.org/krita/3/linux/devbuilds/krita-3.0.1-Alpha-4c91a18-x86_64.appimage) (MD5: 772ca9e719cf00d4de49fe68c226c41f)

#### OSX and MacOS

Krita on OSX will be fully supported with version 3.1. Krita 3.0 for OSX is still missing Instant Preview and High Quality Canvas scaling. There are also some issues with rendering the image — these issues follow from Apple’s decision to drop support for the OpenGL 3.0 compatibility profile in their display drivers and issue with touchpad and tablet support. We are working to reimplement these features using OpenGL 3.0 Core profile. For now, we recommend disabling OpenGL when using Krita on OSX for production work. Krita for OSX runs on 10.9, 10.10, 10.11 and is reported to work on MacOS too.

- [krita-3.0.1-Alpha-4c91a18.dmg](http://files.kde.org/krita/3/osx/devbuilds/krita-3.0.1-Alpha-4c91a18.dmg) (MD5: 1d0faca3c92a36527c6fae048e442ce8)

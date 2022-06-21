---
title: "New Krita 3.0 Alpha/Development Windows Builds"
date: "2016-04-19"
---

Until now, we have made all Windows releases of Krita with Microsoft's Visual C++ compiler. Krita 2.9 was built with the 2012 version, 3.0 with the 2015 version of Visual C++. Both compilers have problems building the [G'Mic library](http://gmic.eu/), and, recently, the latest version of the [Vc library](https://github.com/VcDevel/). G'Mic provides a wide range of filters and Vc lets us optimize the code that blends pixels and creates brush masks.

We cannot fix the libraries, we cannot fix the Microsoft compiler, and we don't want to make Krita slower and less functional, so there was only one solution left: find a different compiler. That is pretty scary so late in the development cycle, because every compiler has different quirks and bugs. We are actually [making these builds on Linux](http://www.valdyas.org/fading/index.cgi/hacking/krita/mxe_krita.html).

We have now prepared new builds for you to test. There are four builds: with and without debugging information, and for 32 and 64 bits Windows. If you encounter a crash, please download the debug build and try to reproduce the crash. Compared to 3.0 alpha, a number of bugs are fixed. These builds also have more features: the camera raw import plugin and the PDF import/export plugin are included. The 32 bits build now also includes G'Mic, which was completely impossible with Visual Studio. The only feature present on Linux that is still not available on Windows is OpenJPEG support, for loading and saving .jp2 files (not jpeg files, that is present and correct).

You can find all builds here: [http://files.kde.org/krita/3/windows/devbuilds](http://files.kde.org/krita/3/windows/devbuilds). You can verify your downloads with the sha1 checksum files. Direct downloads of the non-debug builds:

- [32 bits](http://files.kde.org/krita/3/windows/devbuilds/krita-master-f38b47e-x86.zip)
- [64 bits](http://files.kde.org/krita/3/windows/devbuilds/krita-master-f38b47e-x64.zip)

To run, simply extract the zip file somewhere and navigate into the bin folder, there execute krita.exe. There is no need anymore for Visual Studion C runtimes! Krita 3.0 looks in a different location for its configuration and resource files, so your existing 2.9 installation is completely untouched.

Setting up the builds was easier than expected, thanks to the [MXE](http://mxe.cc/) project, but it still took time away from fixing bugs, so we're considering extending the 3.0 release schedule with another month. if you're on Windows, please give these builds a good, thorough work-out!

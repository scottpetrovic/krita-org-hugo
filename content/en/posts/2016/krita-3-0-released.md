---
title: "Krita 3.0 Released"
date: "2016-05-31"
---

Today the Krita team releases Krita 3.0, the Animation Release. Wrapping up a year of work, this is a really big release: animation support integrated into Krita's core, Instant Preview for better performance painting and drawing with big brushes on big canvases, ported to the latest version of the Qt platform and too many bigger and smaller new features and improvements to mention!

[![krita-3.0](../images/krita-3.0-1024x559.png)](https://krita.org/wp-content/uploads/2016/05/krita-3.0.png)

Many of the new features were funded by the [2015 Kickstarter campaign](https://www.kickstarter.com/projects/krita/krita-free-paint-app-lets-make-it-faster-than-phot?ref=users). A big thank-you to all our backers! The remaining stretch goals will be released with Krita 3.1, later this year. And don't forget that we've still got seven days in the current [kickstarter campaign](https://www.kickstarter.com/projects/krita/krita-2016-lets-make-text-and-vector-art-awesome), We're nearly funded, so there should still be time to reach some stretch goals this year, too!

The full list of improvements is too long for a release announcement. Please check out the [extensive release notes we prepared](https://krita.org/krita-3-0-release-notes/)!

Note: Krita 3.0 load and saves its configuration and resources in a different place than 2.9 so it's possible to use both versions together without conflicts. Here is a [tutorial on migrating resources](https://docs.krita.org/KritaFAQ#My_resource_disappeared_with_installing_3.0.21_Did_Krita_delete_them.3F).

### Downloads

#### Windows

On Windows, Krita supports Wacom, Huion and Yiynova tablets, as well as the Surface Pro series of tablets. Trust, Bosto, Genius, Peritab and similar tablets are not supported at this moment because we lack testing hardware that allows us to reproduce reported bugs.

The portable zip file builds can be unzipped and run by double-clicking the krita link. If you want to use the installer builds, please uninstall Krita 2.9 first.

For Windows users, Alvin Wong has created [a shell extension](https://github.com/alvinhochun/KritaShellExtension) that allows you to preview krita images in Windows Explorer. You can install it separately, but it is also included in the setup installers.

If your virus scanner or other security software complains please verify the [sha1 checksum](https://en.wikipedia.org/wiki/SHA-1#Data_integrity) noted below: if the checksum checks out, the files are safe.

Krita on Windows is tested on Windows 7, Windows 8 and Windows 10.

- [krita-3.0-x64.zip](http://files.kde.org/krita/3/windows/krita-3.0-x64.zip) (8d0b3819a94e2731bfa6265a573526bb65f0e568)
- [krita-3.0-x86.zip](http://files.kde.org/krita/3/windows/krita-3.0-x86.zip) (0cd0ebb41e17163e26928affc9bf4bfbe7b315c0)
- [krita-3.0-x64-setup.exe](http://files.kde.org/krita/3/windows/krita-3.0-x64-setup.exe) (c47285e1457c1492c7ee184835ea70d9ac26fdc5)
- [krita-3.0-x86-setup.exe](http://files.kde.org/krita/3/windows/krita-3.0-x86-setup.exe) (82f68755eeeb28dbbaa7f29db15338a98b07f4a6)
- [kritashellex\_1.1.0.1\_setup.exe](http://files.kde.org/krita/3/windows/kritashellex-1.1.0.2-setup.exe) (4fb24f073b0dfccae79050423bc8596e3218ae7d)

#### Linux

For Linux, we offer [AppImages](http://appimage.org/) that should run on any reasonable recent Linux distribution. For Ubuntu 12.04 and CentOS 6.x you need the appimage that is built without support for OpenMP. We are working on updating the [Krita Lime repository](https://launchpad.net/~dimula73/+archive/ubuntu/krita): for now, you can use that to install the krita3-testing build. Helio Castro is packaging [Krita for Redhat/CentOS/Fedora](http://www.heliocastro.info/?p=241).

You can download the appimage, make it executable and run it in place. No installation is needed. At this moment, we only have appimages for 64 bits versions of Linux.

- [krita-3.0-x86\_64.appimage](http://files.kde.org/krita/3/linux/krita-3.0-x86_64.appimage)  (cc4d007aff15369d7ae90160649f9594f256ec2c)
- [krita-3.0-no-openmp-x86\_64.appimage](http://files.kde.org/krita/3/linux/krita-3.0-no-openmp-x86_64.appimage) (39d6d14d0607b7db37ea70b7057ebbaebca19a27)

You can also get Krita from [Ubuntu's App Store in snap format](https://uappexplorer.com/app/krita.krita), thanks to Michael Hall's help. Note that you cannot use the snap version of Krita with the NVidia proprietary driver, due to a limitation in Ubuntu and that there are no translations yet.

#### OSX

Krita on OSX will be fully supported with version 3.1. Krita 3.0 for OSX is still missing Instant Preview and High Quality Canvas scaling. There are also some issues with rendering the image -- these issues follow from Apple's decision to drop support for the OpenGL 3.0 compatibility profile in their display drivers. We are working to reimplement these features using OpenGL 3.0 Core profile. For now, we recommend disabling OpenGL when using Krita on OSX for production work. Krita for OSX is tested on 10.9 and 10.11 since we do not have access to other versions of OSX.

- [krita-3.0.dmg](http://files.kde.org/krita/3/osx/krita-3.0.dmg) (dcf9a5bd31efe3a2ce89dff77f7e10e23b704f54)

#### Source

A source archive is available for distributions wishing to package Krita 3.0. If you're a curious user, it is recommended to build Krita directly from the git repository instead, so you get all fixes daily fresh. See David Revoy's [guide for an introduction to building Krita](http://www.davidrevoy.com/article193/guide-building-krita-on-linux-for-cats). If you build Krita from source and your version of Qt is lower than Qt 5.6.1, it is necessary to also rebuild Qt using the patches in krita/3rdparty/ext\_qt.

- [krita-3.0.tgz](http://download.kde.org/stable/krita/3.0/krita-3.0.tgz.mirrorlist) (6e0f7763e2ed5e266d916e7f76fadbaaf2c84eb5)

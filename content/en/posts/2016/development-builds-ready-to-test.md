---
title: "Development Builds Ready To Test"
date: "2016-04-28"
---

So... Yesterday, Dmitry tried to fix an ancient bug that made it inconvenient to work with dockers, popups and the canvas: sometimes the focus would go haywire, and if you'd try to enter a value in a docker, or zoom while the cursor wasn't over your image, things would go wrong. Well... There's this fix, and it needs _testing_. It really needs testing before we can make it part of Krita 3.0. So, here are new builds for Windows, Linux and OSX. Please help by downloading them and giving them a good work-out. There are a dozen or so other fixes in there as well, but I won't bore you with _those._ Please test! Spend an hour or two painting, transforming, swapping brushes, setting colors! You can download all of these and use them without interfering with any of your Krita 2.9 settings.

### Download

**Windows:** Unzip and run the bin/krita.exe executable!

- Zip archive: [Windows 64-bit Beta 1 (zip)](http://files.kde.org/krita/3/windows/devbuilds/krita-3.0-Beta-master-4a58260-x64.zip)
- Zip archive: [Windows 32-bit Beta 1 (zip)](http://files.kde.org/krita/3/windows/devbuilds/krita-3.0-Beta-master-4a58260-x86.zip)

**The OSX disk image** still has the known issue that if OpenGL is enabled, the brush outline cursor, grids, guides and so on are not visible. We’re working on that, but don’t expect to have rewritten the canvas before 3.0 will be released.

- Disk Image: [OSX Beta 1](http://files.kde.org/krita/3/osx/devbuilds/krita3-beta1-75295e0.dmg)

**The Linux appimage:**After downloading, make the appimage executable and run it. No installation is needed. For CentOS 6 and Ubuntu 12.04, a separate appimage without G'Mic is provided: it is no longer possible to build the latest version of G'Mic in a way that can run on those distributions.

- AppImage [Linux AppImage Beta 1](http://files.kde.org/krita/3/linux/devbuilds/krita-3.0-Beta-master-no_gmic-4336582-x86_64.appimage) for modern distributions
- AppImage [Linux AppImage Beta 1](http://files.kde.org/krita/3/linux/devbuilds/krita-3.0-Beta-master-4336582-x86_64.appimage) for ancient distributions

---
title: "New Development Builds Ready"
date: "2016-05-05"
---

There are new development builds ready, with a bunch of bug fixes since the last beta. Please test thoroughly, we're getting really close to the second beta! These builds have the following fixes:

- The Settings and Windows menu actions now can have shortcuts assigned to them
- Loading of images with group layers and layers in different colorspaces now always works correctly
- Several issues with onion skinning are fixed
- Make it possible again to load KPP (paintop presets) as images
- Don't leave the pan tool when accidentally double clicking
- Fix a crash when closing Krita if the canvas mirror option is active
- Fix layouts in the advanced color selector configuration dialog
- Fix saving shortcuts
- Fix the duplicate F4 shortcut
- Fix the order of application of color curves in the Curves filter (first per-channel, then composite rgb curve, then lightness curve)
- Fix saving and loading of the image resolution in non-US locales
- Fix updating the global selection mask
- Fix the file dialog on some Linux distributions where most image types were not shown
- Show the webp image type in the file dialog
- Fix initialization of the Tool Options docker
- Fix using the canvas extension buttons with a tablet stylus
- Fix jumping of the mirror axis handle
- Make imagepipe and spray brush compatible with Instant Preview
- Fix crashes in the text tool when changing font properties
- Make it possible to use autospacing with Instant Preview
- Fix loading of fil layers
- Fix infinite loop when using the vector gradient tool
- Fix extreme slowness in the color selector
- Fix showing the page preview in the PDF export dialog
- Fix using shortcuts when the cursor is not over the canvas
- Fix the location of translations on Window

### Download

**UPDATE 05.05.16:** Now there in also a Windows Shell Extension package available! Just install it and Windows Explorer will start showing preview and meta information for Krita files

- Installation package: [kritashellex_1.1.0.1_setup.exe](http://files.kde.org/krita/3/windows/kritashellex_1.1.0.1_setup.exe)

**Windows:** Unzip and run the bin/krita.exe executable!

- Zip archive: [krita-3.0-Beta-master-962bfe1-x64.zip](http://files.kde.org/krita/3/windows/devbuilds/krita-3.0-Beta-master-962bfe1-x64.zip)
- Zip archive: [krita-3.0-Beta-master-962bfe1-x86.zip](http://files.kde.org/krita/3/windows/devbuilds/krita-3.0-Beta-master-962bfe1-x86.zip)

**The OSX disk image** still has the known issue that if OpenGL is enabled, the brush outline cursor, grids, guides and so on are not visible. We’re working on that, but don’t expect to have rewritten the canvas before 3.0 will be released.

- Disk Image: [krita3-beta1-8ec9263.dmg](http://files.kde.org/krita/3/osx/devbuilds/krita3-beta1-8ec9263.dmg)

**The Linux appimage:**After downloading, make the appimage executable and run it. No installation is needed. For CentOS 6 and Ubuntu 12.04, a separate appimage is provided with g'mic built without OpenMP (which makes it much slower)

- AppImage [krita-3.0-Beta-master-37389d5-x86_64.appimage](http://files.kde.org/krita/3/linux/devbuilds/krita-3.0-Beta-master-37389d5-x86_64.appimage) for modern distributions
- AppImage [krita-3.0-Beta-master-962bfe1-no-openmp-x86_64.appimage](http://files.kde.org/krita/3/linux/devbuilds/krita-3.0-Beta-master-962bfe1-no-openmp-x86_64.appimage) for ancient distributions

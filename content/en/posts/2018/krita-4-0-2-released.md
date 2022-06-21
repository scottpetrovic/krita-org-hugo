---
title: "Krita 4.0.2 released"
date: "2018-05-10"
categories: 
  - "officialrelease"
---

Today the Krita team releases Krita 4.0.2, a bug fix release of Krita 4.0.0. We fixed more than fifty bugs since the Krita 4.0.0 release! See below for the full list of fixed isses. We've also got fixes submitted by two new contributors: Emmet O'Neil and Seoras Macdonald. Welcome!

Please note that:

- The reference image docker has been removed. Krita 4.1.0 will have a new reference images tool. You can test the code-in-progress by downloading the nightly builds for Windows and Linux. You can also use Antoine Roux's [reference images docker](https://github.com/antoine-roux/krita-plugin-reference) python plugin.
- Translations are broken in various ways. On Linux everything should work. On Windows, you might have to select your language as an extra override language in the Settings/Select language dialog. This might also be the case on macOS
- The macOS binaries are now signed, but do not have G'Mic and do not have Python scripting.

If you find a new issue, please consult this [draft document on reporting bugs](https://phabricator.kde.org/T7492) before reporting an issue. After the 4.0 release more than 150 bugs were reported, but most of those reports were duplicates, requests for help or just not useful at all. This puts a heavy strain on the developers and makes it harder to actually find time to improve Krita. Please be helpful!

[![](images/kiki_4.0_sm-1-1024x463.png)](https://krita.org/wp-content/uploads/2018/03/kiki_4.0_sm-1.png)

## Improvements

### Windows

- Patch QSaveFile so working on images stored in synchronized folders (dropbox, google drive) is safe. [BUG:392408](https://bugs.kde.org/show_bug.cgi?id=392408)
- Enable WinInk or prompt if WinTab cannot be loaded

### Animation

- Fix canvas update issues when an animation is being rendered to the cache [BUG:392969](https://bugs.kde.org/show_bug.cgi?id=392069)
- Fix playback in isolated mode [BUG:392559](https://bugs.kde.org/show_bug.cgi?id=392559)
- Fix saving animated transparency and filter masks, adjustment layer [BUG:393302](https://bugs.kde.org/show_bug.cgi?id=393302)
- set size for a few timeline icons as it is painfully small on Windows
- Fix copy-pasting pixel data from animated layers [BUG:364162](https://bugs.kde.org/show_bug.cgi?id=364162)

### Brushes

- Fix keeping "eraser switch size/opacity" option when saving the brush [BUG:393499](https://bugs.kde.org/show_bug.cgi?id=393499)
- Fix update of the preset editor GUI when a default preset is created [BUG:392869](https://bugs.kde.org/show_bug.cgi?id=392869)
- Make strength and opacity sliders from 0 to 100 percent in brush editor

### File format support

- Fix saving state of the selection masks into .kra
- Read multilayer EXR files saved by Nuke [BUG:393771](https://bugs.kde.org/show_bug.cgi?id=393771)
- PSD: convert the image if its colorspace is not supported
- Don't let autosave close currently running actions

### Grids

- increase the range for the pixel grid threshold
- only allow isometric grid with OpenGL enabled [BUG:392526](https://bugs.kde.org/show_bug.cgi?id=392526)

### Crashes

- Fix a hangup when closing the image [BUG:393916](https://bugs.kde.org/show_bug.cgi?id=393916)
- Fix a crash when duplicating active global selection masks [BUG:382315](https://bugs.kde.org/show_bug.cgi?id=382315)
- Fix crashes on undo/redo of vector path points operations [BUG:393209](https://bugs.kde.org/show_bug.cgi?id=393209), [BUG:393087](https://bugs.kde.org/show_bug.cgi?id=393087)
- Fix crash when deleting palette [BUG:393353](https://bugs.kde.org/show_bug.cgi?id=393353)
- Fix crash when resizing the Tool Options for the shape selection tool [BUG:393217](https://bugs.kde.org/show_bug.cgi?id=393217)

### User interface

- Show the exact bounds in the layer properties dialog
- Add ability for vanishing point assistants to show and configure radial lines
- Make the Saturation slider update when picking a color that has Value 100 [BUG:391934](https://bugs.kde.org/show_bug.cgi?id=391934)
- Fix "Break at segment" to work correctly with closed paths
- Disable right-clicking on popup palette [BUG:391696](https://bugs.kde.org/show_bug.cgi?id=391696), [BUG:378484](https://bugs.kde.org/show_bug.cgi?id=378484)
- Don't let the color label widget mess up labels when right button is pressed [BUG:392815](https://bugs.kde.org/show_bug.cgi?id=392815)
- Fix Canvas position popping after pop-up palette rotation reset [BUG:391921](https://bugs.kde.org/show_bug.cgi?id=391921) (Patch by Emmet O'Neil, thanks!)
- Change the behaviour of the add layer button [BUG:385050](https://bugs.kde.org/show_bug.cgi?id=385050) (Patch by Seoras Macdonald, thanks!)
- Clicking outside preview box moves view to that point [BUG:384687](https://bugs.kde.org/show_bug.cgi?id=384687) (Patch by Seoras Macdonald, thanks!)
- Implement double Esc key press shortcut for canceling continued transform mode [BUG:361852](https://bugs.kde.org/show_bug.cgi?id=361852)
- Display flow and opacity as percentage instead of zero to one on toolbar

### Other

- Fix build on ARM [BUG:393010](https://bugs.kde.org/show_bug.cgi?id=393010)
- Fix a number of warnings generated by [PVS-Studio](https://www.viva64.com/en/pvs-studio/)

## Download

### Windows

Note for Windows users: if you encounter crashes, please follow [these instructions](https://docs.krita.org/Dr._Mingw_debugger) to use the debug symbols so we can figure out where Krita crashes.

- 64 bits Windows: [krita-x64-4.0.2-setup.exe](https://download.kde.org/stable/krita/4.0.2/krita-x64-4.0.2-setup.exe)
- Portable 64 bits Windows: [krita-x64-4.0.2.zip](https://download.kde.org/stable/krita/4.0.2/krita-x64-4.0.2.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.0.2/krita-x64-4.0.2-dbg.zip)

- 32 bits Windows: [krita-4.0.2-x86-setup.exe](https://download.kde.org/stable/krita/4.0.2/krita-x86-4.0.2-setup.exe)
- Portable 32 bits Windows: [krita-x86-4.0.2.zip](https://download.kde.org/stable/krita/4.0.2/krita-x86-4.0.2.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.0.2/krita-x86-4.0.2-dbg.zip)

### Linux

- 64 bits Linux: [krita-4.0.2-x86\_64.appimage](https://download.kde.org/stable/krita/4.0.2/krita-4.0.2-x86_64.appimage)

(If, for some reason, Firefox thinks it needs to load this as text: to download, right-click on the link.)

When it is updated, you can also use the [Krita Lime PPA](https://launchpad.net/%7Ekritalime/+archive/ubuntu/ppa) to install Krita 4.0.2 on Ubuntu and derivatives. We are working on an updated snap.

### OSX

- OSX disk image: [krita-4.0.2.dmg](https://download.kde.org/stable/krita/4.0.2/krita-4.0.2.dmg)

Note: the gmic-qt and python plugins are not available on OSX.

### Source code

- Source code: [krita-4.0.2.tar.gz](https://download.kde.org/stable/krita/4.0.2/krita-4.0.2.tar.gz)

### md5sum

For all downloads:

- [md5sum.txt](https://download.kde.org/stable/krita/4.0.2/md5sum.txt)

### Key

The Linux appimage and the source tarball are signed. You can retrieve the public key over https here: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8). The signatures are [here](http://download.kde.org/stable/krita/4.0.2/) (filenames ending in .sig).

## Support Krita

Krita is a free and open source project. Please consider supporting the project with [donations](https://krita.org/en/support-us/donations/) or by [buying training videos or the artbook!](https://krita.org/en/support-us/shop) With your support, we can keep the core team working on Krita full-time.

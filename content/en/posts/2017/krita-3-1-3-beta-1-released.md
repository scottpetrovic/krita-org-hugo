---
title: "Krita 3.1.3 beta 1 released"
date: "2017-04-07"
---

A week after the alpha release, we present the beta release for Krita 3.1.3. Krita 3.1.3 will be a stable bugfix release, 4.0 will have the vector work and the python scripting. The final release of 3.1.3 is planned for end of April.

We're still working on fixing more bugs for the final 3.1.3 release, so please test these builds, and if you find an issue, check whether it's already in the [bug tracker](https://bugs.kde.org/buglist.cgi?bug_severity=critical&bug_severity=grave&bug_severity=major&bug_severity=crash&bug_severity=normal&bug_severity=minor&bug_status=UNCONFIRMED&bug_status=CONFIRMED&bug_status=ASSIGNED&bug_status=REOPENED&list_id=1431433&product=krita&query_format=advanced), and if not, report it!

Things fixed in this release, compared to 3.1.3-alpha:

- Added the credits for the 2016 Kickstarter backers to the About Krita dialog
- Use the name of the filter when creating a filter mask from the filter dialog instead of "effect"
- Don't cover startup dialogs (for instance, for the pdf import filter) with the splash screen
- Fix a race condition that made the a transform mask with a liquify transformation unreliable
- Fix canvas blackouts when using the liquify tool at a high zoom level
- Fix loading the playback cache
- Use the native color selector on OSX: Krita's custom color selector cannot pick screen colors on OSX
- Set the default PNG compression to 3 instead of 9: this makes saving png's much faster and the resulting size is the same.
- Fix a crash when pressing the V shortcut to draw straight lines
- Fix a warning when the installation is incomplete that still mentioned Calligra
- Make dragging the guides with a tablet work correctly

#### Note for Windows Users

**We are still struggling with Intel's GPU drivers; recent Windows updates seem to have broken Krita's OpenGL canvas on some systems, and since we don't have access to a broken system, we cannot work around the issue.** For now, if you are affected, you have to disable OpenGL in krita/settings/configure Krita/display.

#### Windows

Note for Windows users: if you encounter crashes, please follow [these instructions](https://docs.krita.org/Dr._Mingw_debugger) to use the debug symbols so we can figure out where Krita crashes.

- 32 bits Windows: [krita-3.1.3-beta.1-x86-setup.exe](http://download.kde.org/unstable/krita/3.1.3-beta.1/krita-3.1.3-beta.1-x86-setup.exe)
- Portable 32 bits Windows: [krita-3.1.3-beta.1-x86.zip](http://download.kde.org/unstable/krita/3.1.3-beta.1/krita-3.1.3-beta.1-x86.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](http://download.kde.org/unstable/krita/3.1.3-beta.1/krita-3.1.3-beta.1-x86-dbg.zip)

- 64 bits Windows: [krita-3.1.3-beta.1-x64-setup.exe](http://download.kde.org/unstable/krita/3.1.3-beta.1/krita-3.1.3-beta.1-x64-setup.exe)
- Portable 64 bits Windows: [krita-3.1.3-beta.1-x64.zip](http://download.kde.org/unstable/krita/3.1.3-beta.1/krita-3.1.3-beta.1-x64.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](http://download.kde.org/unstable/krita/3.1.3-beta.1/krita-3.1.3-beta.1-x64-dbg.zip)

#### Linux

- 64 bits Linux: [krita-3.1.3-beta.1-x86\_64.appimage](http://download.kde.org/unstable/krita/3.1.3-beta.1/krita-3.1.3-beta.1-x86_64.appimage)

A snap image for the Ubuntu App Store is also available. You can also use the [Krita Lime PPA](https://launchpad.net/%7Ekritalime/+archive/ubuntu/ppa) to install Krita 3.1.3-beta.1 on Ubuntu and derivatives.

#### OSX

- OSX disk image: [krita-3.1.3-beta.1.dmg](http://download.kde.org/unstable/krita/3.1.3-beta.1/krita-3.1.3-beta.1.dmg)

### Source code

- Source code: [krita-3.1.3-beta.1.tar.gz](http://download.kde.org/unstable/krita/3.1.3-beta.1/krita-3.1.3-beta.1.tar.gz)

#### md5sums

For all downloads:

- [md5sums.txt](http://download.kde.org/unstable/krita/3.1.3-beta.1/md5sums.txt)

#### Key

The Linux appimage and the source tarbal are signed. You can retrieve the public key over https here: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8). The signatures are [here](http://download.kde.org/unstable/krita/3.1.3-beta.1).

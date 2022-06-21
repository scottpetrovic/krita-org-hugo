---
title: "Krita 3.1 Release Candidate"
date: "2016-11-30"
---

Due to illness, a week later than planned, we are still happy to release today the first release candidate for Krita 3.1. There are a number of important bug fixes, and we intend to fix a number of other bugs still in time for the final release.

- Fix a crash when saving a document that has a vector layer to anything but the native format (regression in beta 3)
- Fix exporting images using the commandline on Linux
- Update the OSX QuickLook plugin to use the right thumbnail sizes
- Improved zoom menu icons
- Unify colors on all svg icons
- Fix tilt-elevation brushes to work properly on a rotated or mirrored canvas
- Improve drawing with the stabilizer enabled
- Fix isotropic spacing when painting on a mirrored canvas
- Fix a race condition when saving
- Fix multi-window usage: the tool options palette would only be available the last openend window, now it's available everywhere.
- Fix a number memory leaks
- Fix selecting the saving location for rendering animations (there are still several bugs in that plugin, though -- we're on it!)
- Improve rendering speed of the popup color selector

You can find out more about what is going to be new in Krita 3.1 in the [release notes](https://krita.org/en/release-notes-for-krita-3-1). The release notes aren't finished yet, but take a sneak peek all the same!

### Windows

Note for Windows users: if you encounter crashes, please follow [these instructions](https://docs.krita.org/Dr._Mingw_debugger) to use the debug symbols so we can figure out where Krita crashes.

- 32 bits Windows: [krita-3.0.94-x86-setup.exe](http://download.kde.org/unstable/krita/3.0.94/krita-3.0.94-x86-setup.exe) (MD5 Hash: 1fa424258d455f92aac071c47d820095)
- Portable 32 bits Windows: [krita\_3.0.94-x86.zip](http://download.kde.org/unstable/krita/3.0.94/krita_3.0.94-x86.zip) (MD5 Hash: fa00cc3575a56083916885626ff97d88)
- [Debug symbols. (Unpack in the Krita installation folder)](http://download.kde.org/unstable/krita/3.0.94/krita-3.0.94-x86-dbg.zip) (MD5 Hash: 538fefc19ca79cec36346a2b2564162e)

- 64 bits Windows: [krita-3.0.94-x64-setup.exe](http://download.kde.org/unstable/krita/3.0.94/krita-3.0.94-x64-setup.exe) (MD5 Hash: 908f52aee5deee6971783ce3c019e93e)
- Portable 64 bits Windows: [krita\_3.0.94-x64.zip](http://download.kde.org/unstable/krita/3.0.94/krita_3.0.94-x64.zip) (MD5 Hash: 4af2829289476d172032a68d26e55789)
- [Debug symbols. (Unpack in the Krita installation folder)](http://download.kde.org/unstable/krita/3.0.94/krita_3.0.94-x64-dbg.zip) (MD5 Hash: ee90e2c3e679a74d9fe77eec305f84f4)

### Linux

- 64 bits Linux: [krita-3.0.94-x86\_64.appimage](http://download.kde.org/unstable/krita/3.0.94/krita-3.0.94-x86_64.appimage) (MD5 Hash: e48aa1a805fbb631ab7d908d41c3ab84)

A snap image for the Ubuntu App Store is available in the beta channel.

### OSX

- OSX disk image: [krita-3.0.94.dmg](http://download.kde.org/unstable/krita/3.0.94/krita-3.0.94.dmg) (MD5 Hash: c8fc18364587481d346009f3921a9142)

### Source code

- Source code: [krita-3.0.94.tar.gz](http://download.kde.org/unstable/krita/3.0.94/krita-3.0.94.tar.gz) (MD5 Hash: a8822566df7743405b37b72f22a1db53)

---
title: "Krita 2.9.1 Released"
date: "2015-03-16"
---

The first bugfix release for Krita 2.9 is out! There are now builds for Windows, OSX and CentOS 6 available. While bug fixing is going on unabated, Dmitry has started working on the Photoshop layer style Kickstarter feature, too: drop shadows already work, and the rest of the layer styles are coming.The goal is to have this feature done for Krita 2.9.2, which should be out next month. And we're working on a new Kickstarter project!

- Fix the outline cursor on CentOS 6.5
- Update G’Mic to the very latest version (but the problems on Windows are still not resolved)
- Improve the layout of the filter layer/⁠mask dialog’s filter selector
- Fix the layout of the pattern selector for fill layers
- Remove the dependency of QtUiTools, which means that no matter whether the version Qt installed and the version Qt Krita was built agast differ, the layer metadata editors work
- Fix a bug that happened when switching between workspaces
- Fix bug 339357: the time dynamic didn’t start reliably
- Fix bug 344862: a crash when opening a new view with a tablet stylus
- Fix bug 344884: a crash when selecting too small a scale for a brush texture
- Fix bug 344790: don’t crash when resizing a brush while drawing
- Fix setting the toolbox to only one icon wide
- Fix bug 344478: random crash when using liquify
- Fix bug 344346: Fix artefacts in fill layers when too many parallel updates happened
- Fix bug 184746: merging two vector layers now creates a vector layer instead of rendering the vectors to pixels
- Add an option to disable the on-canvas notification messages (for some people, they slow down drawing)
- Fix bug 344243: make the preset editor visible in all circumstances

**Note on G'Mic on Windows**: Lukas, David and Boudewijn are trying to figure out how to make G'Mic stable on Windows. The 32 bits 2.9.1 Windows build doesn't include G'Mic at all. The 64 bits build does, and on a large enough system, most of the filters are stable. We're currently trying different compilers because it seems that most problems are causes by Microsoft Visual Studio 2012 generating buggy code. We're working like crazy to figure out how to fix this, but please, for now, on 64 bits Windows treat G'Mic as entirely experimental.

**Note for Windows users with an Intel graphics board**: If krita shows a black screen after opening an image, you need to update your Intel graphics drivers. This isn't a bug in Krita, but in Intel's OpenGL support. Update to 10.18.14 or later. Most Ultrabooks and the Cintiq Companion can suffer from outdated drivers.

**Note on OSX**: Krita on OSX is still experimental and not suitable for real work. Many features are still missing. Krita will only work on Mavericks and up.

**Downloads**

- Linux:
    - Distributions are expected to create packages for their bleeding edge repositories
    - Ubuntu and derivatives can use Krita Lime, as usual: [https://launchpad.net/~dimula73/+archive/ubuntu/krita](https://launchpad.net/%7Edimula73/+archive/ubuntu/krita)
    - OpenSUSE users can the KDE:Extra repo: [http://download.opensuse.org/repositories/KDE:/Extra/](http://download.opensuse.org/repositories/KDE:/Extra/)
- Windows. From Vista and up, Windows 7 and up is recommended. There is **no** Windows XP build. If you have a 64 bits version of Windows, don’t use the 32 bits build! The zip files do not need installing, just unpacking, but do not come with the Visual Studio C runtime that is included in the msi installer.
    - 32 bits Windows: [http://files.kde.org/krita/windows/krita_x86_2.9.1.0.msi](http://files.kde.org/krita/windows/krita_x86_2.9.1.0.msi) or [http://files.kde.org/krita/windows/krita_x86_2.9.1.0.zip](http://files.kde.org/krita/windows/krita_x86_2.9.1.0.zip) (This version does not include G’Mic.)
    - 64 bits Windows: [http://files.kde.org/krita/windows/krita_x64_2.9.1.0.msi](http://files.kde.org/krita/windows/krita_x64_2.9.1.0.msi) or [http://files.kde.org/krita/windows/krita_x64_2.9.1.0.zip](http://files.kde.org/krita/windows/krita_x64_2.9.1.0.zip)

OSX:

- [http://files.kde.org/krita/osx/krita-2.9.1.0.dmg](http://files.kde.org/krita/osx/krita-2.9.1.0.dmg)

---
title: "New Development Builds"
date: "2014-09-23"
categories: 
  - "development-builds"
tags: 
  - "krita-2-9"
---

After a hiatus -- Siggraph 2014 first, then two weeks of vacation, We've got new builds for you! These builds have the following improvements:

- KICKSTARTER: Fix brush antialiasing
- OCIO: Implement an option to disable changing currently selected color when changing exposure/gamma
- X11: Fix a crash with newer evdev drivers
- OCIO: set black and white points of the image in the OCIO docker
- Fix saving 16 bit grayscale images to tiff, jpeg and ppm
- Fix loading and saving of blending modes to PSD We're still missing several blending modes, though. At least these are missing for rgb:
    - inverted divide
    - pass through
    - darker color
    - lighter color
- Fix saving assistants (again)
- Fix a bug that randomly disabled Krita tablet support
- Update the preview of the MyPaint color selector when a new color is set
- Add zooming/panning to the overview docker

[![overview](/images/posts/2014/overview-300x181.png)](https://krita.org/wp-content/uploads/2014/09/overview.png)

- Update G'Mic to 1.6
- Fix loading of Auto Spacing for predefined brushes
- Fix incorrect enabled state of widgets in layer box after switching the node
- block clipboard brush when it's not active as it was interfering with other brushes
- Fixes for ink depletion of saturation
- Let the popup palette use tags instead of a manual configuration system to select between sets of brushes

[![improved_popup](/images/posts/2014/improved_popup-300x235.png)](https://krita.org/wp-content/uploads/2014/09/improved_popup.png)

- Add a color slider docker: this adds a HSV/HSL/HSI/HSY' slider docker to Krita

[![colorsliders](/images/posts/2014/colorsliders.png)](https://krita.org/wp-content/uploads/2014/09/colorsliders.png)

Windows build:

- [http://files.kde.org/krita/windows/krita\_x64\_2.8.79.17.msi](http://files.kde.org/krita/windows/krita_x64_2.8.79.17.msi)

OSX build (still experimental, no OpenColorIO or OpenEXR):

- [http://files.kde.org/krita/osx/krita-2.8.79.17.dmg](http://files.kde.org/krita/osx/krita-2.8.79.17.dmg)

Linux build:

- [https://launchpad.net/~dimula73/+archive/ubuntu/krita](https://launchpad.net/~dimula73/+archive/ubuntu/krita)

In the mean time, lots of improvements to the transform tool are being worked on.

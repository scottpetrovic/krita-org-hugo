---
title: "Krita 2.9.9 Released"
date: "2015-11-05"
---

The ninth semi-monthly bug fix release of Krita is out! Upgrade now to get the following fixes and features:

### Features

- Show a message when trying to use the freehand brush tool on a vector layer
- Add a ctrl-m shortcut for calling up the Color Curves filter dialog. Patch by Raghavendra Kamath. Thanks!
- Improve performance by not updating the image when adding empty layers and masks.

### Fixes

- Fix typing in the artistic text tool. A regression in 2.9.8 made it impossible to type letters that were also used as global shortcuts. This is now fixed.
- Don't crash when opening an ODG file created in inkscape. The files are not displayed correctly, though and we need to figure out what the issue is.
- Fix the gaussian blur filter: another 2.9.8 regression where applying a gaussian blur filter would cause the right and bottom edge to become semi-transparent.
- Fix calculating available memory on OSX. Thanks to René J.V. Bertin for the patch!
- When duplicating layers, duplicate the channel flags so the new layers are alpha locked if the original layers were alpha locked.
- Fix a number of hard to find crashes in the undo system and the compositions docker.
- Another exiv2-related jpeg saving fix.
- Add a new dark pass-through icon.

Go to the [Download page](https://krita.org/download/krita-desktop/) to get the freshest Krita! (And don't forget to check out [Scott's book](/posts/new-krita-book-release-and-giveaway/), or [Animtim's latest training DVD](/posts/secrets-of-krita-the-third-krita-training-dvd/) either!)

### Krita Next

The next version of Krita will be 3.0 and we're definitely getting there! There is a lot of development going on fixing issues with shortcuts, issues with the opengl canvas, issues with icons... And making packages. Ubuntu Linux users can already use the Krita 3.0 Unstable packages in the [Lime](https://launchpad.net/~dimula73/+archive/ubuntu/krita) repository, and we're working on Windows and OSX packages.

Here's a demo by Wolthera:

{{< youtube kWHK68iCRHk >}}

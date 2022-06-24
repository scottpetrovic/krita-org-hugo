---
title: "Release Notes for Krita 3.2"
date: "2017-07-17"
---

## Release Notes for Krita 3.2

There are numerous bug fixes and some very cool new features since Krita 3.1.4. Check out [GDQuest](http://gdquest.com/)'s overview video below with all the changes:

{{< youtube f9K48jXml4s >}}

### G'MIC Plugin

Krita 3.2 uses the gmic-qt plugin created and maintained by the [authors of G'Mic](http://gmic.eu/).  This plugin replaces completely the older gmic plugin. On Windows and Linux, the plugin is bundled with Krita and should work out of the box. It's still rather experimental, though it's considerably more up to date and stable than the previous gmic integration.

On OSX, we cannot for now provide the plugin for a number of reasons: the underlying g'mic library needs X11 to show dialogs for e.g. interactive colorize, we have trouble actually compiling the binary and have it run and once that hurdle is taken, OSX breaks the plugin by limiting shared memory to chunks of 40 megabytes.

### Touch Painting

You can now paint with your fingers. This was in Krita 2.8, but was lost when we did our Qt5 port. It's back! If you don't want this, you can disable touch painting support in the settings dialog.

### Smart Patch Tool

Clean up and remove elements you don't want. This was previously going to be in Krita 4.0, but we managed to get it in this release! Check out the demo below. The tool is in the toolbox with its own set of tool options.

{{< youtube jI87VzDtkPY >}}

### New Brush Presets

We added Radian's brush set to Krita's default brushes. These brushes are good for create a strong painterly look.

[![](/images/pages/updated_presets_rad-478x1024.jpg)](/images/posts/2017/updated_presets_rad.jpg)

## Other Features

- There are now shortcuts for changing layer states like visibility and lock.
- There is a new dialog from where you can copy and paste relevant information about your system for bug reports.
- The Gaussian Blur filter now can use kernels up to 1000 pixels in diameter
- There is a new blending mode: Hard Overlay

## Bug Fixes

- There have been many fixes to the clone brush
- If previously you suffered from the "green brush outline" syndrome, that should be fixed now, too. Though we cannot guarantee the fix works on all OpenGL systems.
- There have been a number of performancei mprovements as well
- The interaction with the file dialog has been improved: it should be better at guessing which folder you want to open, which filename to suggest and which file type to use.
- Some cleanups when handling OpenGL
- Show a clearer error when loading the wintab32.dll file fails on Windows
- Fix a regression where bezier tools couldn’t close the curve and couldn’t create a second curve
- Fixes for working with multiple windows in subwindow mode where one of the documents is set to "stays on top"
- Fix resetting the Level of Detail cache when changing the visibility of a layer: this fixes an issue where after changing the visibility of a layer, the color picker would pick from an older version of the layer.
- Save the last used folder in the Reference Images Docker
- Don’t create nested autosave documents.
- Add recognizing uc-logic tablets on Linux
- Improve the stabilizer
- Fix loading a custom brush preset that uses the text brush
- Fixes to saving jpg or png images without a transparency channel

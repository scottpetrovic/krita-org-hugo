---
title: "Krita 2.8.1 Released"
date: "2014-03-28"
---

Hot on the heels of Krita 2.8.0, we're releasing Krita 2.8.1! This release contains a lot of bug fixes and improved support for the Surface Pro 2 tablet on Windows.

- support for surface pro 2 on Windows
- fixed several memory leaks
- save single layer CMYK images correctly to PSD
- BUG:331805 Do not let the selection grow bigger than the image on invert
- BUG:329945: fix the unsharp mask filter
- Fix tablet support on OSX
- Fix convolution operations when the resulting alpha is 0
- BUG:332022 Fix mirror mode in color smudge and filter ops
- Make the warp tool handles less obtrusive
- BUG:331758 Make the transform tool scale filter selector work
- BUG:332070 Fix crash when selecting a template with stylus double-click
- BUG:331950: set the document modified status when changing layer properties
- BUG:331890: Fix loading of multi-layered PSD files, including 16 bit ones
- BUG:331708: Fix crash in undo/redo of transformations
- BUG:331759: improve performance of the OpenGL canvas in some cases
- Make it possible to use the OpenGL canvas on more GPU/driver combinations
- Fix crash in pixelize filter
- Fix the emboss filter to apply to the whole image
- Fix crash when loading an image that has a broken colorspace id
- BUG:331702: Fix crash when loading a 16 bit/channel PSD image
- Fix crash in the oilpaint filter
- Fix crash when applying a gradient
- Fix crash when trying to create a selection in the artistic text tool
- Fix not being able to add new canvas input shortcuts
- Improve the crash reporter on Windows

Download [Krita 2.8.1 for Windows](http://kritastudio.com/desktop.html) from the Krita Studio website, or update on Linux using your package manager.

Krita 2.8.2 will contain the improved support for uc-logic/evdev based tablets on Linux.

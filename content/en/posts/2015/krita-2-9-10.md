---
title: "Krita 2.9.10"
date: "2015-12-09"
---

The tenth bugfix release already! There are quite a few fixes, though the focus these days is really on getting Krita 3.0 ready for the first alpha release. Of particular interest to owners of a system with an AMD processor is the option to disable vectorization support. That might improve performance, but _only_ for users of AMD systems! We've also got a fix by a new contributor, Nicholas LaPointe!

Here's the full, unordered, list:

- Fix crash in artistic text tool selection (bug 354907)
- Fix saving tags: use the UTF-8 codec to save the tags instead of the locale codec (bug 356306)
- Do no longer allow users to save 16 bit/channel linear gamma sRGB files to PNG without a profile
- Do not crash when scaling down an image if the scaling factor gets too close to 0 (bug 356156)
- Add a basic storyboard template
- Fix generating the .kra and .ora thumbnail (bug 355884)
- Fix loading some PSD files by Photoshop after saving from Krita (bug 355110)
- Add an option to disable the vectorization speed up. This is for broken AMD processors.
- Add an option to log OpenGL calls for debugging purposes
- Remember the last-used profile when importing an untagged 16 bit/channel PNG image
- Fix a number of import/export filters that reported the wrong error code after the user pressed cancel. Patch by Nicholas LaPointe, thanks!
- Fix a rare crash that could happen during slow operations (bug 352918)
- Fix an even rarer crash that could happen when recalculating the image under some circumstances. (bug 353043)
- Fix a crash when switching sub-windows after removing a layer (bug 355205)
- Improve memory usage when saving images by now creating a big image then scaling it down for the thumbnail
- Make the small color selector consistent in color layout with other color selectors (bug 353505)
- Fix a crash that occasionally happened when working with multiple images (bug 354975)
- Fix a crash when using painting assistants (bug 353152)
- Fix a race condition that could happen during complex operations (bug 353638)
- Fix a crash in the shortcut system (bug 345562)
- Restore the window correctly after going to canvas-only and back (bug 352018)

There are packages for Ubuntu Linux, Windows and OSX in the [usual place](https://krita.org/download/krita-desktop/)! Steam users will be able to get the new packages shortly through the beta channel, and Stuart is also working on packages from the Animation branch. And speaking of animation... Later this week, we'll probably have new animation branch packages for Ubuntu Linux and Windows!

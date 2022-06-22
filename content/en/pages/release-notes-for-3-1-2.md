---
title: "Release Notes for 3.1.2"
date: "2017-01-27"
---

## Release Notes for Krita 3.1.2

Krita 3.1.2, released on January 31st 2017, is a bugfix release with a few extra features thrown in for good measure.

Audio Support for Animations

<iframe src="https://www.youtube.com/embed/s08oHOjxo84" width="100%" height="450" frameborder="0" allowfullscreen="allowfullscreen"></iframe>

Import audio files to help with syncing voices and music. In the demo on the left, Timothée Giet shows how scrubbing and playback work when working with audio.

- Available audio formats are WAV, MP3, OGG, and FLAC
- A checkbox was added in the Render animation dialog to include the audio while exporting
- [See the documentation](https://docs.krita.org/Audio_for_Animation) for more information on how to set it up and use the audio import feature.

Audio is not yet available in the Linux appimages. It is an experimental feature, with no guarantee that it works correctly yet -- we need your feedback! See [Phabricator](https://phabricator.kde.org/T2371) for the development discussion.

### Other Changes

- Ctrl key continue mode for Outline Selection tool: if you press ctrl while drawing an outline selection, the selection isn't completed when you lift the stylus from the tablet. You can continue drawing the selection from an arbitrary point.
- Allow deselection by clicking with a selection tool: you can now deselect with a single click with any selection tool.
- Added a checkbox for enabling HiDPI to the settings dialog.
- remove the export to PDF functionality. It is having too many issues right now. ([BUG:372439](https://bugs.kde.org/show_bug.cgi?id=372439))

### Bug Fixes

- fix a number of bugs with creating and editing bundles ([BUG:352151](https://bugs.kde.org/show_bug.cgi?id=352151))
- fix loading presets with embedded patterns ([BUG:374745](https://bugs.kde.org/show_bug.cgi?id=374745))
- Fix to the erase mode button so it keeps track of the blending mode ([BUG:348290](https://bugs.kde.org/show_bug.cgi?id=348290))
- Fix creating a brush from a stamp ([BUG:373846](https://bugs.kde.org/show_bug.cgi?id=373846))
- Load 16-bit RGBA TIFF files that have no embedded ICC profile as gamma corrected sRGB  ([BUG:375479](https://bugs.kde.org/show_bug.cgi?id=375479))
- Make it possible to use the same language for translations as the desktop ([BUG:374928](https://bugs.kde.org/show_bug.cgi?id=374928))
- Fix a possible crash in the brush engine when using older Wacom tablets on Windows 10 and a stylus that does not support rotation ([BUG:375253](https://bugs.kde.org/show_bug.cgi?id=375253))
- Add extra precision to the gray slider in the levels filter ([BUG:375201](https://bugs.kde.org/show_bug.cgi?id=375201))
- Fix settings for cumulative undo
- Hide text for buttons with an icon in the toolbar
- Restore the default favorite blending modes
- Make it possible to delete system tags ([BUG:347607](https://bugs.kde.org/show_bug.cgi?id=347607))
- Restore a step of 0.1 for the crop tool ratio spinbox ([BUG:374021](https://bugs.kde.org/show_bug.cgi?id=374021))
- Fix saving the name of a local selection mask ([BUG:374383](https://bugs.kde.org/show_bug.cgi?id=374383))
- Fix crash when creating a document after closing it with opacity keyframes ([BUG:374381](https://bugs.kde.org/show_bug.cgi?id=374381))
- Icon updates for redo, mirror view, rotation, smoothing modes, merging layers, rotating canvas, split layer, color to alpha
- fix crash when attempting to use a document that has a 16-bit float XYZ color space
- Fixed making the fullscreen action checkable again ([BUG:373906](https://bugs.kde.org/show_bug.cgi?id=373906))
- Don't reset the OCIO settings when moving the window ([BUG:373481](https://bugs.kde.org/show_bug.cgi?id=373481))
- Fix saving pass-through mode for group layers
- Make user visible color space names in color models consistent
- Fix a crash when using two windows ([BUG:371124](https://bugs.kde.org/show_bug.cgi?id=371124))
- Fix a possible crash with the undo stack ([BUG:374524](https://bugs.kde.org/show_bug.cgi?id=374524))
- Fix confusion when saving per-stylus presets between sessions ([BUG:374957](https://bugs.kde.org/show_bug.cgi?id=374957))
- Don't generate thumbnails without a height or width ([BUG:373835](https://bugs.kde.org/show_bug.cgi?id=373835))
- Fix a potential crash when switching to the tool options in the toolbar ([BUG:374497](https://bugs.kde.org/show_bug.cgi?id=374497))
- Fix exporting animation that doesn't start with the first frame
- Don't reset the animation export range every time when exporting an animation

---
title: "Last week in Krita - Week 45"
date: "2014-11-11"
tags: 
  - "krita-2-9"
---

### UI

Scott Petrovic revamped the UI of the transform tools for better readability and usability, and is now heading towards changing around the brush-settings.

<iframe src="//www.youtube.com/embed/Xh5rw6yLnwg" width="560" height="315" frameborder="0" allowfullscreen="allowfullscreen"></iframe>

Boudewijn  changed around the way background colour works: now Krita uses white as the default transparency-fill colour. You can set this from opaque to transparent in the new-file dialogue to get the transparency checkers back. The new file dialogue will remember this for next time as well! There's still some bugs involved with this, but hopefully they'll be fixed soon.

The crop tool now has grey handles instead of ugly yellow ones.

### Kickstarter

Dmitry Kazakov is still busy on the transform masks. Transform masks are saved transformations so they may be applied non-destructively. The major holdback is several bugs which make the transform masks a little glitchy and unpredictable. In effect, this makes the current work on the transform masks similar to polishing an octogonal wheel till it's round: Without it, we'd still have a wheel, but it would be uncomfortable to use.

There's a seperate branch for Layer Effects started. Currently, the plan is to have Layer Effects a seperate thing from Filter Layers and Filter Masks. The reason is to ensure 100% compatibility with PSD, and Layer Effects have some peculiar interactions with eachother that aren't possible with the current Filter Layers and Masks. We wish you to give the same if not greater flexibility that photoshop offered. That said, current work involve getting saving and loading done right, as well as putting the basic architecture in place.

### Modal View Controller Branch (or: Multiple documents)

Boudewijn fixed a bug that would slow down Krita to a standstill due to the tools docker constantly being told that there was a new document, even when just switching out of the program and back in again.

Brush settings returned to the brush editor.

Several crashes have been fixed.

Overall, there's still quite a few bugs, but every week a major blocker gets fixed.

### Animation-plug-in

The animation plug-in is also being refactored in this branch.

- Refactoring is necessary because the architecture of the Animation Plug-in was awkward to work with.
- Right now, animation has been folded into the main Krita program, so we have a single program for both illustration and animation.
- Filestructure is also currently being worked on.
- There's been correspondence about funding this feature, which is good, because then we can have someone work on this properly instead of during lunchbreaks.

### Bug fixes

A nasty bug with the pop-up docker was fixed. Basically, when changing a brush-preset that was also in the pop-up docker, the pop-up docker not understand the brush had been changed, resulting in a crash. This is fixed for the next release.

A crash with the spray brush tool has been fixed.

The filter-layer dialogue wouldn't show it's preview, resulting in a unwieldy large dialogue that was of no help. Now that the preview thumbnails have been fixed, the dialogue is smaller and more helpful!

The Triangle Color Selector widget has been fixed: It would not communicate well with other color pickers, resulting in it not knowing the color in the Pop-up palette, and giving confusing feedback in the Color-to-alpha dialogue(making it seem as if the filter would erase black instead of white).

### Other

Some of Krita's ICC profiles have been changed or removed. This was partially due to licensing issues(remember, Krita is GPL), and sometimes because the ICC profile itself was dodgy. This does not solve the strange bug with PNGs having weird sRGB profiles yet. If you are experiencing that problem, open and re-save your png with a non-colour managed software, such as GIMP or MS paint. This will strip the profile info.

New workspaces were added by Timothée Giet:

- "Big_Paint" is the classic view for painting on big screen resolution (1920x1080)
- "Big_Paint_2" is a variation using wide dockers on both sides
- "Big_Vector" is a set of dockers useful for working with vector shapes
- "Small_Paint" is a minimal set of dockers for painting on very small screen (this one is used by default at first start)
- "Small_Vector" is a minimal set of dockers for working with vector shapes on very small screen
- "VFX_Paint" for big screens, and using wide dockers on both sides to have LUT management always visible.

If you [follow the git logs](https://projects.kde.org/projects/calligra/activity), you may notice a lot of strange little commits that only change one or two lines: This is clean-up of the Calligra code, including Krita. This allows for making porting to QT5 a lot easier, which is the main goal for Krita 3.0.

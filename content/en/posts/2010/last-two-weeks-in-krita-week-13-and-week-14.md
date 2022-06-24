---
title: "Last Two Weeks in Krita -- week 13 and week 14"
date: "2010-04-13"
---

Last Two Weeks in Krita

A two week report again -- Easter Monday I was still a bit too tired from the Easter celebrations to actually write anything.

Apart from work done on pigment and other KOffice libraries, there were 88 commits in these two weeks: everyone took it easy during Easter. Besides, the easy bugs for the 2.2 release have been fixed, what's left is pretty hard! We're now at 57 bugs for Krita. There are a number of platform bugs for KOffice that are quite as important, though.

Week 14 was the last week of the first phase of Lukas' sponsored Krita involvement. He will now focus on writing his thesis on Krita Brush Engines, do his exams and be back to work on the 2.3 release in June. But let's see what was achieved during the past period, which started end of January:

- a set of benchmarks to measure performance progress and regressions
- optimized the pixel brush (500 px brushes are now perfectly usable)
- compatibility with photoshop brushes (masks only, not dynamics yet)
- optimized pixel access (up to 6 times faster)
- optimized flood fill
- made smudge 12 times faster
- canvas mirroring (with some caveats, the work isn't completely done yet, and the paint mirroring isn't ready either.)
- Default button for brush presets

Also, since I'm bound to give a fair overview, this is what was tried but didn't work out (yet):

- One particular type of brush optimization: the compute-a-quarter, copy to the other quarters. Lukas got this working, but it turned out to be slower.
- Vectorization of blend modes.

And all the time, Lukas has also been busy improving the quality of the brush engines, of course -- his thesis will be worth learning Slovak for!

### Krita 2.2

The second beta of Krita 2.2 has been released. We still know of a number of serious issues, one of the most important being the convolution code -- this is what makes the blur filter tick, and that's quite important. Also, there are still critical bugs, not all unittests run and there's some weirdness on 64-bit architectures that Boudewijn is trying to track down.

For fast painting, the OpenGL canvas is recommended. However, that has its own problems currently, notably with the brush outline cursors, so we cannot make it the default.  

Now... If you want to help us find issues we are not yet aware of, try installing Beta 2.2 (or, if you're ambitious, trunk) and help testing!  

### Summer of Code

We have four horses running in the race for the Google Summer of code: Adam Celarek, Marc Pegon, Jose Luis Vergara Toloza and Dmitry Kazakov. Color selectors, a new tranformation tool, a comic brush and impasta and multi-threading Krita's update mechanism. Tonight we'll learn the number of slots KDE will get initially -- and soon whether any of these project proposals will get a slot. All of them are really good: as a mentor, one thing that surprised me this year was the low number of duds. There are always a number of copy-paste proposals, but none for Krita this year.

### Code

Development now has split: trunk is frozen except for bug fixes, and there is a separate branch for feature development, like the default button for brush settings. That won't be in 2.2, but will be in 2.3. All in all, 2.3 looks set to become the great release we want it to be. I'm toying with the idea of renumbering it to 3.0 -- it's that big a difference from 2.0.

**Adam** fixed a bug where the display would show artefacts after resizing or cropping. He also fixed the crop tool: lock ratio now works correctly. In the early days of Krita 2, we considered making the root group layer visible and have it hold the global selection (Krita has per-layer as well as global selections, Krita 1 only had per-layer selections). That didn't work out, but the option to show the root group layer was still present. And buggy, so Adam removed it. Adam also fixed a crash in the text brush as well as a bug with the spacing. Drawing a line on a shape layer was fixed, and two more crashes: one in the perspective grid, one when deleting layers.

**Boudewijn** finished a refactoring: it's now harder for programmers to accidentally leak memory, if you forget to delete an unused undo transaction, you get an assert, but there were still places where that happened. He also played with the Get Hot New Stuff feature of KDE 4.4: it's now possible to share brush presets using Get Hot New Stuff. We disabled mipmapping, since it isn't finished yet.

**Cyrille** fixed a number of memory leaks in the tile engine, among others in the undo code. He also had to disable the brightness and level filters in the filter brush engine: they are currently too slow. Krita's metadata framework now recognized the XMP Multi Media Schema. Cyrille cleaned up a number of brush engines, like the grid brush. Cyrille fixed a bug when saving and loading colors to xml: this fixes saving and loading generator layers. The scratch pad didn't respect the brush spacing: now it does.

Spurred on by [David Revoy](http://davidrevoy.com/?article29/free-brush-kit-for-chaos-and-evolutions)'s _very_ cool set of brushes, made for the [Chaos and Evolutions instruction dvd](http://www.blender3d.org/e-shop/product_info_n.php?products_id=122), Cyrille implemented scaling and rotation for image brushes and fixed it for animated brushes.

Krita has a special algorithm to smooth out your hand-drawn lines. It's necessary, partly because graphcs tablets don't all have a high resolution, partly because it's harder to control a stylus than a brush or a pen. Cyrille made the smoothing a little bit stronger, but it's likely something we'll have to tweak. David Revoy [noted that he had to scroll to switch between the two most used blend modes](http://forum.kde.org/viewtopic.php?f=138&t=87088&p=154308#p154308): that was reason for a quick fix!

Cyrille fixed a bug when copying selections, as well as a bug in the smudge tool, several unit tests, lots of bugs when converting between color modes and finally alpha-lock painting on colormodels with high channel depths.

**Dmitry** fixed a crash that occurred when undoing after you cancelled adding a filter layer. He then went on to fix several bugs in the recomposition of the layer stack with masks.

**Lukas** added a "default settings" button to the brush settings popup. He expanded the hairy brush to have connected paths between bristles. There was a small issue where you wouldn't get feedback about the brush size when changing the size using the , and . shortcuts (those can be changed by the user, by the way), and Lukas made sure the user gets feedback now. Internally, Krita has two paint surfaces: one that autoextends, and one that is fixed. Lukas fixed a bug when using a fixed paint device as a selection mask. Finally, **Enkithan** created new icons for Lukas' new brush engines, and those were committed as well.  

![](/images/posts/2010/krita-default-preset.png)  

**Sven** fixed a crash and corruption when scaling a bitmap brush, made sure that the settings widgets for brush settings get deleted, fixed the outline of the hairy brush and made sure that if you create a canvas the size of your screen, it's in pixels, not in postscript points. Sven changed the superslider to also update the values when you move the mouse out of the widget: a really nice usability change! The popup palette didn't completely work with tablets yet -- part of it are Qt issues, but another issue, the color selection using the embedded triangle, was fixed by Sven. Finally, Sven fixed the saving of generator layers.

### Finally

Make sure to check out [David Revoy's Experiments with Krita on the forum!](http://forum.kde.org/viewtopic.php?f=138&t=87088)

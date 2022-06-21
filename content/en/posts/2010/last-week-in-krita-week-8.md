---
title: "Last week in Krita -- week 8"
date: "2010-03-02"
---

You wouldn't _believe_ how hard it is to focus on writing Last Week in Krita with three hackers around -- which is the case right now. We're at a 44 commit/day high-water mark for monday -- work has been very brisk, and Krita _is_ beginning to feel quite snappy, even with biggish images. Last week we had 101 commits, and we're at under 90 bugs now! This sprint is such a blast -- Vera, Dmitry, Adam and Peter have gone by now. Lukáš, Cyrille and Sven are still around (and me, of course, I _live_ here. The bathrooms have both broken down, the house is all a-buzz with the sound of fans trying to keep up with cd krita; make -j6 install being executed and huge quantities of m&m's and other nibbles are being consumed.

### Vision

[I've blogged it](https://valdyas.org/fading/software/a-vision-for-krita/), [Cyrille has blogged it](http://blog.cberger.net/2010/02/27/krita-meeting-2010-%E2%80%93-day-1-2/) -- but let's set those three paragraphs down again:

> Krita is a KDE program for sketching and painting, offering an end–to–end solution for creating digital painting files from scratch by masters.
> 
> Fields of painting that Krita explicitly supports are concept art, creation of comics and textures for rendering.
> 
> Modelled on existing real-world painting materials and workflows, Krita supports creative working by getting out of the way and with snappy response.

That's what we're aiming for. I already [dissected these statements](http://www.valdyas.org/fading/index.cgi/hacking/lastweekend.html) -- they are quite dense and more full of meaning than they might seem at first blush. Reactions have been positive, on the whole: and it's important to state once again that we won't stop anyone from trying to fill any hole in the free software spectrum we might be leaving open now. Anyone wants to fork Krita to make a photo editor? That's fine with us, Krita is intentionally [free software](http://www.fsf.org/).

It's also not like we hate or disdain photography: a single glance at Dmitry's or Cyrille's equipment should be enough to disabuse anyone of that notion. But painting is where it's at for Krita. Pure creativity, concept art, cartoons, textures -- and that's a tall order already. Not that pruning Krita is [not a painful process...](http://blog.cberger.net/2010/03/02/the-difficult-choice-of-removing-features/)

### Code

Many Krita hackers were travelling last week, and when we were together in Deventer, we had a lot of things to talk about. Not just the vision, but Peter was present all weekend long to help us with discussions about interaction and usability. Whenever we strayed from the path, he would put us straight: "remember, this is your vision: what that feature, or this implementation be useful to a master painter?". Sometimes that means getting rid of some features we had cloned from Photoshop, even... A list of what has been discussed has been [put up on the wiki](http://wiki.koffice.org/index.php?title=Krita/Usability). It's in a very short style, and we will have to make careful designs for some of these suggestions.

We also agreed on yet another api change for our filters: this time, the api will be much simplified, hopefully making writing filters a lot easier.

Boudewijn fixed a bug where Krita wouldn't be able to load JPG files from a path with a non-ascii character in it -- one would think that these bugs would all have been gone with the millennium, but no. He also started removing features: there is no krita-based [Flake shape](http://wiki.koffice.org/index.php?title=Libs/Flake) anymore: our vision for Krita is that it is not an office component. On the same track, he disabled a number of KOffice plugins that make no sense for Krita, like the database plugin. There are still issues here: it looks like KOffice co-packages some plugins that should be split, like the two shape selection dockers.

Cyrille worked very hard on making the shapes that we do support work well, added the alpha darken composite operation to the [OpenGTL](http://www.opengtl.org)\-based CTL colorspaces plugin (this is used for painting in wash mode), fixed bugs in the tile engine (which helped with memory usage), fixed crashes when loading jpg or tiff files with unusable profiles, used one of the Krita project's Wacom Art Pens to fix the rotation support, simplified the calculation of spacing between strokes, reduced memory usage again, and fixed the distance sensor when painting.

Dmitry optimized the image recomposition algorithm, fixed a crash in the filters and fixed a big bug where painting on a second layer would lead to recomposition artefacts.

Lukáš continued work on the next generation iterators; those aren't used yet, but should improve for instance filters when we port them. Lukáš also spent his evenings optimizing and improving brush engines: sumi-e got ink soaking, the soft brush aspect rotation, density -- to simulate dust on the canvas, airbrush, size changing, ui improvements, and the grid brush got fixed scaling and border jitter. And Lukáš also did more work on the abr-brush compatibility, loading also the dynamics of abr brushes, not just the mask. Now we need to do something with the dynamics!

Sven fixed the brush outline cursor feature and once again cleaned up a whole lot of code in brush engine department.

Vera Lukman fixed bugs in the popup palette and added some visual improvements: and then we discovered that Qt 4.5 doesn't recognize the tablet devices, while Qt 4.6 doesn't send middle/right mouse button events if you click using the stylus button. Now this **is** a problem -- it might be Qt, it might be X11, it might be the drivers, it might be distribution-specific, but right now there is no known-good setup that supports all the tablet features Krita relies on.

### T-Shirts!

And group photo (Lukáš, Vera, Sven, Peter, Dmitry, front: Boudewijn, Cyrille, Adam):

![](../images/krita-team.jpg)

Irina has organized the t-shirts, and [Araprint](http://araprint.nl) has, with magnificent service, converted the design to make it possible to print in five colors and _delivered_ the t-shirts to our place when we, because of a power-cut and attendant confusion, had forgotten to collect them:

![](../images/img_1772.jpg)

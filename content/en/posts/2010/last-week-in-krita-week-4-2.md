---
title: "Last Week in Krita -- Week 4"
date: "2010-02-01"
---

Last week was hugely exciting for us developers, because Lukáš, having finished the last of his exams, could get started on our action plan! Lukáš first week was very, very intensive. His poor laptop hardly managed to keep up with the production of [callgrind](http://www.valgrind.com) output, so we had to distribute that task a bit. What he did was in the first place, using [QTestLib](http://doc.trolltech.com/4.6/qtestlib-manual.html)'s new benchmarking feature, write a bunch of performance tests for common things like composing two images, fetching and writing pixels, painting strokes. Then he ran these benchmarks under callgrind, so he could see where the hotspots were.

The good news: there are plenty of places where we can optimize so Krita will get a lot faster. The bad news: there's a lot of work to do! You can read all about Lukáš ' work in [his weekly blog](http://lukast.mediablog.sk/log/?p=163) and in [the report on our wiki](http://wiki.koffice.org/index.php?title=Krita/Benchmarking). Today, Lukáš spent most of his time investigating Krita's brush rendering code. During an animated discussion with Øyvind Kolås (aka Pippin), Dmitry, Cyrille and me, we formulated an approach that might combine flexibility, performance and low memory consumption for Krita's autobrush feature. Maybe we'll see the first commits tomorrow!

Even better: [Thomas Thym showed that Krita is gaining a userbase:](http://ungethym.blogspot.com/2010/01/still-alive.html) 

![](http://krita2d.org/images/stories/thomas_thym_kids.jpg)  

Yay for budding artists everywhere!

### Code

Again, lots of commits: 96. And that doesn't count the work in pigment or KOffice. The bug count is creeping up again, to 90...

Adrian Page made sure Krita's png filter also works with libpng 1.4, did a bit of make-it-compile-on-windows work, and then on Saturday settled down to unify as far as possible Krita's two canvases: the opengl and qpainter canvas. Lots of duplicated code removed, and even better: the start of work to fix [Bug 148207: Pixel Pencil lines are messy](https://bugs.kde.org/show_bug.cgi?id=148207).

Boudewijn helped Lukáš here and there with the benchmarking code, but [\=because he switched jobs](http://www.valdyas.org/fading/index.cgi/done_working_at_hyves.html), didn't do much coding, except for some token work on the mixer canvas. Cyrille promptly fixed a bug in there!

Cyrille Berger was going strong: trying to figure out how much of a perfomance hit Krita would suffer if we using a 0 - 1.0 scale for opacity instead of 0-255. Turns out that currently, that's a bit much, but there now is nice api in pigment to use opacity with the extra precision. He then added a grayscale 32 bits float/channel colorspace and set out to achieve a hugely important milestone: we can now load a multilayer .exr file, with different colorspaces for different layers, and save it in a .kra file without losing any information! Cyrille was elated enough that he decided to go and do some painting in Krita instead of implementing the .exr export right away.

Having refreshed his mind by creating a spot of art, Cyrille went on (I'm giving him two paragraphs, since his work won't fit in one) to improve our curve handling code, fix replaying of the spray brush in the recorder, add a build mode that makes it possible to both have debug messages _and_ optimized code, fixed some bugs in the metadata handling, fixing the saving of XMP, made it possible to store non-icc color profiles in .kra files, fixed loading layers that have a different colorspace than the image, updated the collection of shiva filters and generators, and started to really hunt for memory leaks. Krita now has a built-in memory leak detector.

Edward Apap cleaned up the user interface of brush engine settings tabs and then set out to replace the convolution code with an [FFTW-based](http://www.fftw.org) approach. We've seen no code yet, except when he posted a snippet to the #krita irc channel... FFTW-based convolution should be much faster than the current approach.

Sven Langkamp fixed a crash in the sumi-e brush engine, helped Lukáš with some benchmarking code and optimized the startup of Krita a bit more.

Finally, Vera Lukman integrated her recent color palette with the color selection system of Krita, which means it really works now. This sparked an [interesting discussion on the mailing list](http://lists.kde.org/?l=kde-kimageshop&m=126456739221635&w=2) on what kinds of color selection mechanism would be useful in the palette. I am sure we will be discussing that a lot in Deventer, in three weeks!

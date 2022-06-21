---
title: "Last -- how much is it? -- weeks in Krita"
date: "2010-05-12"
---

I'm really late with Last Week in Krita, am I not? Yes, I am... There are a couple of reasons, most of them concerned with plain business. Last week I was in Bangalore, [helping students find their way through the KOffice source code](http://www.valdyas.org/fading/index.cgi/urlaub/bangalore_1.html). The week before, I was in Helsinki, trying to figure out which bugs in KOffice should have priority together with Tasos and Lassi from the Nokia mobile office team. The week before that, I was in Magdeburg, for a KO GmbH Board meeting. And in the meantime, a release candidate happened, which is always a reason for a slowdown of development, _and_ we were busy with the Google Summer of Code preparations.

Still, let's get updated on the state of Krita! Since the last instalment, we've had a mere 50 or so commits. And we're at 59 bugs. Well, Lukáš was finishing his thesis and Cyrille was hunting for a research post at a university and everyone was preparing the 2.2 release -- still, work should pick up when the Summer of Code students get started!

### Summer of Code

I already mentioned it on my [blog](http://www.valdyas.org/fading/index.cgi/software/gsoc2010.html), but there are _four_ Krita Google Summer of Code projects this year. At the Krita sprint, we weren't sure whether we could handle a single project, since we really want to push for user-readiness for Krita 2.3. But that idea evaporated in the face of the enthousiasm of the students. **Marc Pegon**, mentored by **Sven Langkamp** is going to create a great new transformation tool for Krita -- one of the real must-haves for our vision. **Adam Celarek**, mentored by **Boudewijn Rempt** is going to work on new an innovative color choosers for Krita -- and Karbon. **Pentalis a.k.a. Jose Luis Vergara Toloza**, mentored by double gsoc alumnus **Lukáš Tvrdý** is going to add a new brush engine meant for comics and impasto to Krita. Impasto will also, if done right, be [very useful for texturing](http://forum.kde.org/viewtopic.php?f=137&t=87460&p=156018&hilit=texturing+game#p156018). **Dmitry Kazakov**, mentored by Krita veteran Bart Coppens, is going to make Krita's image recomposition and display multi-threaded.

Coding will start in two weeks!

### Conferences

Lukáš Tvrdý will speak about brush engines and working on Krita at the [Libre Graphics Meeting](http://www.libregraphicsmeeting.org) in Brussels as well as at [Akademy 2010](http://akademy.kde.org/). Boudewijn will be at the LGM as well, and probably at Akademy, and Cyrille intends to visit Akademy this year, but not the LGM.

### Code

We didn't have a record number of commits, but we had a very pleasingly large number of contributors!

**Adam Celarek** worked on the magnetic selection tool, adding another algorithm for edge detection.

**Ana** cleaned up some of our desktop files.

**Boudewijn** fixed warnings in the code (a six hour train journey to Magdeburg is suitable for little else...), fixed the preset toolbar button for the preset popup and reenabled the things he was working that weren't ready for 2.2: psd import, mypaint-compatible paintop and the color mixer.

**Cyrille Berger** added a benchmark for the mask generator, fixed randomness in the autobrush masks, made the spacing slider exponential, added support for HSV transformations to the normal brush. He also divided the brush options into categories, a very welcome improvement. Radians and degrees don't mix -- so there was a little bug to be fixed there as well.

**Dmitry Kazakov** fixed a bug when showing transparency around the edges of an image, removed a bad memory leak in the memento manager (which keeps the image undo information) and generally started cleaning up Krita's tile manager core in preparation for his summer of code project

**Edward Apap** made the convolution code about twice as fast, fixed a problem with noise in the convolution painter, then increased the performance of the convolution code again, added a motion blur filter, made the convolution code report progress to the user (which reminds me: we still need to do the same for the load/save/import/export code!) and he finally started a lens blur filter.

**Lukáš Tvrdý** doubled the performance for spray paintop and did some other cleanups while finishing his thesis.

**Vera Lukman** made the popup color selector more precise and fixed a bug that occurred when hovering over the popup palette.

---
title: "Last Two Weeks in Krita -- week 29 and 30"
date: "2010-08-06"
---

A period of relative quiet, when most Google Summer of Code students were busy working on the algorithms for the second part of gsoc project: Marc Pegon on warping, José Luis Vergara on bumpmapping. Boudewijn was in Bangalore hacking on the core architecture of KOffice, Cyrille was still moving and Sven preparing for his exams.

[![](http://fc01.deviantart.net/fs71/i/2010/205/1/7/Tribal_Warrior_by_Animtim.png)](http://animtim.deviantart.com/art/Tribal-Warrior-172587048)

Art by Animtim

### Blogs

It's hard to keep up -- witness this irregular update on what's going on in Krita! -- but most of the summer of code students blog regularly. And Lukas is regular as clockwork -- every Monday morning an update on what happened last week!

- [Lukas: Week 29: Performance and bugs](http://lukast.mediablog.sk/log/?p=298)
- [Lukas: Week 30: Custom Brush Works](http://lukast.mediablog.sk/log/?p=309)
- [Pentalis: Impasto and the halftone brush beta](http://pentalis.org/kritablog/?p=157)
- [Pentalis: Impasto in Krita](http://pentalis.org/kritablog/?p=222)
- [Marc: At Last, Image Warping!](http://www.kdedevelopers.org/node/4296)

### Code

Eighty-seven commits in two weeks -- where week 28 had 68. Still, lots of good progress as you can already see from the blogs. We're in the last stages of the Google Summer of Code period, and much time goes either into polish or into setting up the last features from the plan.

**Adam Celarek** is mostly done with the features for the Next Generation color selectors. He spent these weeks polishing, bugfixing, improving support with the various colorspaces Krita supports, implemented a history of recently used colors, synchronizing the current color with the rest of the KOffice system, and a minimal shade selector.

**Ana Beatriz Guerrero López** (who [did the same for Karbon](http://www.koffice.org/news/last-two-weeks-in-koffice-week-29-and-30/), fixed building Krita on ARM platforms.

**Boudewijn** fixed a usability bug in Krita, noted by Fabian: a pasted layer was not made active, ported Krita to the new QWidget-agnostic canvas code in KOffice and started working on a combined brush engine selector/brush settings/preset selector popup -- without any concrete results, though.

**Burkhard Lück** fixed some problems with marking user-visible texts for translation.

**Dmitry Kazakov** implemented a swapper for image data. Krita is now on its fifth or so tile engine, and this is the second tile engine that includes swapping to a file. Bart Coppens and Casper Boemann implemented the first swapfile implementation, back in the single-thread days of Krita. The new one first starts swapping out undo information, and then, if memory is still tight, swaps out current image tiles. This sounds very simple -- but the actual implementation is quite hairy, especially since Dmitry has made Krita very aggressivly multi-threaded!

**José Luis Vergara** implemented a new bumpmap filter, the Phong-bummapper. It's pretty fast, and the first step to a proper impasto effect -- which is very similar to bumpmapping. Paint creates ridges and valleys, and light from single sources creates shadows over this height map. Animtim showed some work using the hatching brush on the [forum](http://forum.kde.org/viewtopic.php?f=138&t=89406):

![](http://fc00.deviantart.net/fs71/f/2010/213/c/5/TiteElfe_Hachures_by_Animtim.png)

**Lukáš Tvrdý** fixed the brush outline for predefined bitmap brushes when scaling is applied, fixed the origin of the duplicate paintop, hacked for fun on the sketch brush, adding another mode, Chrome, fixed the sensors that determine many brush parameters, like size, and improved the performance of using the predefined brushes. Now [Deevad's brush set](http://www.davidrevoy.com/?article29/free-brush-kit-for-chaos-and-evolutions), which is default in Krita, works really well! Then he went on to optimize the line-drawing algorithm Krita uses, improved the performance of the autobrush by checking whether we really use some randomness in the computation. Lukáš next task was fixing the issues we have with creating custom brushes. This is something **you** (yes, I'm looking at you, google analytics is all-powerful!) can help us test. We need input here from everyone on what works, what's cool, what's confusing since it is very nearly a completely new feature. Get compiling! If you have trouble, ask on the forum, ask here, ask on the mailing list or irc, but don't hesitate. We'll help you get a working Krita so you can help us create a great Krita.

**Marc Pegon** started working on perspective transformation in his new transform tool. He added the following instructions, which I should copy into the manual I am writing:

Hold Meta key and move the mouse to apply a 3D rotation to the selection + a perspective projection. Horizontal movement rotates around the Y axis, and vertical movement rotates around the X axis.

He also added some gui polish (**testing needed!**), progress information... And then begon to work on the warp mode. This is so cool, so much fun to play with:

![](/images/posts/2010/krita_warp.png)

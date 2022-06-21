---
title: "Last week in Krita -- week 45"
date: "2009-11-09"
---

Krita 2.1 has been branched, so trunk is open again. This means that developers have pushed all their pent-up changes into trunk, as well as re-enabled all the features that didn't make the cut for 2.1. For some of those features that was because they were crashy, and this means that trunk is once again not for the faint of heart! So, if you want to test-drive krita and report bugs, you should switch to the 2.1 branch, where we are still fixing bugs for the release.

So, what's new in trunk? Adrian Page fixed bug [209652](https://bugs.kde.org/show_bug.cgi?id=209652) and that means that Windows users can open JPEG files. The fix is also applied to the 2.1 Windows build.

Lukas Tvrdy made it possible to change the size of the currently used autobrush by pressing shift and dragging the cursor over the canvas. Lukas has also added a very cool grid-based brush engine and improved the spray brush engine by generalizing the color source. See his [blog](http://lukast.mediablog.sk/log/)!  

![Using the Grid Brush](http://krita2d.org/images/stories/screenshots/krita_grid_brush.png "Grid Brush")  

Dmitry Kazakov has fixed a very long-standing bug in the convolution code. Now the alpha channel in the destination paint device is updated correctly, and that made it possible to remove some ugly hacks in Krita. Another cool feature landing in trunk this week Dmitry coded: masks now have an opacity and a blending mode setting. As Dmitry said in his commit message "It makes sense in some circumstances". Dmitry also fixed [bug 212235](https://bugs.kde.org/show_bug.cgi?id=212235), which prevented newly created custom images from being displayed correctly when Krita uses it's new tile manager. Great work -- now we need a similar fix for loading images! The new tile manager, by the way, despite being a bit buggy here and there, has been enabled in trunk so it gets a good testing. Compared to the old tile manager, it has zero lock contention, measured with [mutrace](http://git.0pointer.de/?p=mutrace.git).

Matthew Woehlke has improved the random generator. An application like Krita has a very special requirement of its random generator, namely that it is repeatably random (so, for instance, a noise filter layer always is the same until the settings change.) His improvements have been backported to the 2.1 branch.

Cyrille Berger (who has just finished writing his Phd thesis -- congratulations!) fixed a number of bugs: both jpeg and png export filters now correctly save the resolution of the image, the shiva filter extension has been improved, painting in the high channel-depth [OpenCTL colorspaces](http://www.opengtl.org/) is fixed. And Cyrille has started on a new color mixer docker, the digital color mixer, which looks a bit like the Krita 1.6 color docker, but promises to be much improved.

Sven Langkamp has implemented a new feature: if you use Krita shape tools on vector layers, shapes are created. They don't yet use the Krita brushes to draw themselves, but that might just be the next step.

Vera Lukman, who started working on Krita as part of the Season of KDE initiative hasn't yet committed to trunk, but she has been working assiduously on a new gui concept: [quick brush and color selection palette](http://wiki.koffice.org/index.php?title=Krita/Quick_sketch_Pallete) in a working branch in svn.

Boudewijn Rempt extended the paint tool with a pan feature: press space, click and drag to pan the image. You don't even need to keep the spacebar pressed down. Another new feature Boudewijn added: pressing the escape key toggles the visibility of the toolbox and dockers. Great for his X61t tablet, where in tablet mode, escape and the cursor keys are the only keys available. A long-standing wish, namely being able to select a color from the canvas without switching to the powerful color picker tool was implemented as well, after some [discussion](http://forum.kde.org/viewtopic.php?f=139&t=83497) on the forum. This lead to some discussion, since we are running out of keyboard modifiers in the default tool. People with dual screen setups: please test trunk! Boudewijn has attempted to fix bug 186944, but he hasn't a dual screen setup, so he cannot test! Boudewijn has put in some work on making Krita compatible with the .myb brush format from [](http://mypaint.intilinux.com/). Result: Version 2.0 brushes load correctly, but painting hasn't been implemented yet. The painterly color mixer, originally implemented by Emanuele Tamponi, doesn't crash anymore ([bug 211918](https://bugs.kde.org/show_bug.cgi?id=211918)), but it also doesn't mix yet. Boudewijn is trying to fix that issue, more news next week.

To finish off with some statistics: we had about 80 messages on our mailing list and 78 commits to subversion. We're now at 61 bugs, of which 20 are crash bugs. There are also 100 wishes open. See you next week!

---
title: "September Update"
date: "2012-09-23"
---

It's been some time since I last gave an update on what's happening with Krita. And that's not because nothing is going on, but rather because of extreme business. Well, that and some real life. But there are some pretty exciting developments that will hopefull result in a great 2.6 release!

Using the very cool [Vc library](http://code.compeng.uni-frankfurt.de/projects/vc) by KDE hacker Matthias Kretz, **Sven Langkamp**has started to vectorize parts of Krita. That means that finally we've started to use the modern capabilities of CPU's to do several calculations at the same time: MMX, SSE, AltiVec, AVX and so on. Vc nicely abstracts this for us. In the first place, the calculation of the autobrush masks was optimized. This made painting a lot smoother already. Next up, Sven is looking into optimizing the color blending code.

[LittleCMS 2.4](http://www.littlecms.com/) supports both 16 and 32 bits floating point now, in addition to 8 and 16 bit integer. This means that the HDR colorspaces Krita has had since 1.5 can now be handled by LittleCMS. Previously we were using the [OpenCTL](http://www.opengtl.org) library created by Cyrille Berger for this. While this library is an amazing free software equivalent to the non-free CTL library used by movie studios, the colorspace implementations we wrote for Krita were not too complete, missing a lot of blending modes. Now that we are using LittleCMS instead, we get all these blending modes for free, plus a nice performance improvement. Next, I need to fix the the OpenColorIO integration which I somehow broke.

**Dmitry Kazakov**came back from the summer camp and immediately got pushed a lot of fixes for zooming in Krita. There are still some issues left, but zooming in and out feels a lot more natural now. More fixes are upcoming. Dmitry also started his next period of sponsored work, and more about that in another post!

**Torio Mlshi** came back after a period of absence has started working on the animation plugin again! This is great news -- there's a lot of demand for a good, supported animation mode in paint applications. Just check the [forum](http://forum.kde.org/viewtopic.php?f=156&t=94646&start=45&hilit=animation)!

The summer came and went, with all the Krita Google Summer of Code students passing their final grading! There is some clean up work needed, but [Carlos Licea's sand painting brush](http://pedepinico.blogspot.nl/) looks likely to be included in 2.6, as does the [infinite canvas implemented by Shrikrishna Holla](http://blog.shrrikrishnaholla.in). Shivaraman Ayer's work on integrating the perspective grid into the perspective assistant is nearly done. The 3D model assistant needs more work -- but then, that was always an enormous amount of work! [Joe Simon's printing dialog](http://jsimon3.wordpress.com/) needs a number of new dependencies which most distributions don't pack yet. But his work is done, too, and we'll try to get it into 2.6.

In the meantime, work on Krita Sketch proceeds at a frenzied pace. The initial interaction design by **Arjen Hiemstra** was fleshed out with a full graphical design by **Timothee Giet**. Arjen is now implementing the core functionality: canvas, gestures, multi-touch, while **Dan Jensen** is implementing the design in Qt Quick. Me, I'm working on implementing the [Deviant Art](http://www.deviantart.com)[stash API, both for Krita Sketch and for Krita Desktop.](http://www.deviantart.com)

Also a subject for another post: [KO GmbH](http://www.kogmbh.com) is preparing itself to offer commercial support for professional users of Krita. We're still working on a website (with Timothee Giet) and trying to figure out how much to charge... But the goal is to give, for example, studios, access to a professional, high bit depth painting application in a way that gives them peace of mind. **Simon Legrand** has been helping us figure out how to go about it. Let's see where this leads!

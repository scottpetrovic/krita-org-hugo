---
title: "Last Week in Krita -- Week 5"
date: "2010-02-11"
---

Oh, oh -- it's already Thursday of Week 6... I'm horribly late, and it's all my own fault: this week was a very busy week in KOffice and I was too tired to do much in the evenings. And it's not as if nothing happened in week 5. As Lukáš blogged, in his second week, [he has managed to make painting a lot faster](http://lukast.mediablog.sk/log/?p=173), and even though his last optimization caused some weird artefacts when painting, and had to be reverted pending a better solution. It's now easy, even enjoyable, to paint with a 200 pixel brush on a big canvas. For optimal performance, check whether your system supports Krita's OpenGL canvas.

However, now that Krita can use big canvases and big brushes, one thing became painfully clear: we leak memory. In the running up to the 2.1 release, I fixed a lot of memory leaks, but this time it was Cyrille's turn.

### Code

We had about 130 commits this week. That includes, however, a batch of more than 30 commits that were previously developed in a separate branch. More of that later! We're over 90 bugs again, at 92.

Adam Celarek fixed bugs in the tools, like [Bug 217818 - "Select Area by Path" Outline is Drawing Unusually Thick](https://bugs.kde.org/show_bug.cgi?id=217818) and also cleaned up the painting of selections when switching between qpainter and opengl canvas, added selecting by painting and finally started cleaning up some cruft in the base libraries in KOffice.

Boudewijn got the paint mixing palette finally in a state where mixing makes marks on the palette: mixing itself isn't yet fixed.

As said earlier, Cyrille spent a lot of time on fixing memory leaks in Krita. He also worked on the openexr export filter, making it possible to save RGB16 files and improving memory usage. When that was done, Cyrille started to have real fun, as he said, with the recording feature, adding recording to lots of Krita tools. This is important for two reasons: action recording is a great feature for users, and we will be able to use to develop more complex performance benchmarks. Cyrille also helped Lukas out by implementing a fast atan2 function. Then I was wondering why I couldn't use the rotation of my Wacom Art pen to rotate the green bell peppers from one of the gimp brushes, and Cyrille rallied to add support for rotation input and fixed the gimp brushes to support rotation. Finally, Cyrille got annoyed by our long standing broken unittests and fixed a few of them.

Dmitry Kazakov had been working for months on fixing a structural issue in Krita: when recompositing an image that contains blur filter layers, weird things would happen. This was rather a big operation, so he developed it in a git branch and committed this week. There were a few follow-up commits needed to fix new bugs. And, here's a plea for **help**: if you can, please checkout Krita from svn, compile it and test it thoroughly with complex and large layer stacks. Come to #krita on irc.freenode.net or our forums and report issues with rendering the final image, whether you see artefacts, experience slowness or whatever. We need to get this tested really well and widely before we release 2.2!

Edward Apap, who was still busy with his fast-fourier-transform version of convolution, found time to fix a bug in the old tile engine. Dmitry's new tile engine is the default, but we keep the original engine around to test for regressions, and it had bitrotted a bit.

Lukáš Tvrdý was busy improving the performance of the pixel brush, with [great results.](http://lukast.mediablog.sk/log/?p=173). And when he was bored writing his thesis (on brush engines in Krita) in the evenings, he worked on a new brush engine: the particle brush engine, which creates strokes from travelling particles according to physical laws (Euler integration, Verlet integration, etc.). Let nobody say anymore that free software doesn't innovate!  

![](http://krita2d.org/images/stories/krita_particle_brush.png)  

Finally, Sven Langkamp went on porting brush engines to the new preset system. We're not done yet, but close. Though the filter brush engine proves to be very obstinate!

See you next week, hopefully a bit earlier!

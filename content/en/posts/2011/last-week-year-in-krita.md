---
title: "Last Week/Year in Krita"
date: "2011-01-10"
---

2010 -- what a ride! Krita as a project came together, acquired a vision and really invested an enormous amount of energy in making Krita ready for real users. There'll always be bugs, I'm afraid, and there'll always be new improvements to make and the next release will always be better than the previous one. But there's no doubt that with [Krita 2.3.0](http://krita.org/component/content/article/9-krita-updates/66-krita-230-released) we've created something quite solid.

Here's the result of ace tester and champion bug reporter Sinozukke's experiments with the sketch brush:  

![](https://krita.org/wp-content/uploads/2011/01/sketch-experiment.jpg)  

Going over my old Last Week in Krita posts, I'm myself amazed at how much has actually happened in 2010 -- apart from two major releases, 2.2 and 2.3! And the growth of the team is stunning as well. We're planning a 2011 sprint, but we won't fit in my house anymore!

For me personally, 2010 was quite a bit rockier than 2009. Parts of it were excellent, parts of it were plain tough, and I have learned that commuting for three hours a day gave me lots of time for Krita that I somehow don't have when working from home. But...

### 2011 is going to rock!

Since Krita development has moved to git, together with the change from KOffice to [Calligra Suite](http://www.calligra-suite.org), it's much easier to do development in branches. That means that features land in master (what used to be called trunk) much later, but in a more complete state. It also makes it trickier to report on what's going on!

Together with [MyPaint](http://mypaint.intilinux.com/) maintainer **Martin Reynolds**, **Sven Langkamp** has been busy fixing the MyPaint brush engine plugin for Krita. A really nice example of cross-project cooperation, and the mypaint brush engine is very nearly ready for prime-time. Some brushes are still a bit slow -- and the Krita mypaint plugin will never be as fast as using the brushes natively in MyPaint since we need to convert between the way the MyPaint brush engine code expects image data and the way Krita stores it. But it's usable, not just a really cool hack. And moreover, it's a great example of the way different projects can work together!

**Cyrille Berger** is busy with a special vector shape to make it easy to create a layout of boxes for comics -- and possibly speech bubbles as well. He also made it possible to use a pattern as a source for your brush coloring, added progress reporting to the macro replayer and made it possible to record applying filters in a macro. Plus the long-standing [filter api refactoring](http://community.kde.org/Krita/Filter_API_Discussion_Notes)...

**Geoffry Song** and **Cyrille Berger** have improved the assistant feature that has been a promise for so long and made it usable. With assistants you can construct your image using ellipses, boxes, splines and lines. Then you can paint, and if you come near one of the lines, your brush will be magnetically attracted (and the strength is a setting) but you're still painting. You can modify, move and delete the assistants on the canvas and even load and save a construction of assitants for reuse in another painting.

![](https://krita.org/wp-content/uploads/2011/01/krita-guides.jpg)  

**Silvio Heinrich** worked on improvements of the usability of the present management.

**Boudewijn Rempt** has made a feature return we lost in 2006 -- guides that you can drag out of the rulers. One small bug left, though -- the guides aren't long enough. It's likely, too, that Krita users will let the guides remain in the their repository in the rulers and use the ultra-cool assistants instead to construct their paintings!

**Matus Talcik** implemented a brand new history docker with thumbnails -- and now is investigating OpenCL integration in Krita.  

**Lukas Tvrdy** created a new brush engine inspired by alchemy and made mirroring work -- not the canvas mirroring one uses to check the painting now and then, but painting and seeing the mirror half appear. As demonstrated by Animtim:

![](https://krita.org/wp-content/uploads/2011/01/mirrortux.png)  

And there's much more coming: everyone is full of plans for cool stuff -- and we're not forgetting to keep the bugs down either.

### Krita Sprint

The Krita team is growing and growing... Last month, we've seen Silvio Heinrich, Matus Talcik and Geoffry Song produce patches! So much that for the next sprint, we can no longer use my kitchen table. We're trying to find a nice new location.

But apart from a location, a t-shirt is a must as well! So... Go to the [forum and show us what you think a well-dressed Krita contributor should wear in 2011!](http://forum.kde.org/viewtopic.php?f=137&t=92453) b

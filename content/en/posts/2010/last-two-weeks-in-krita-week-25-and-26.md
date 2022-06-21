---
title: "Last Two Weeks in Krita -- week 25 and 26"
date: "2010-07-04"
---

I'm writing from my hotel room in Tampere, Finland where I am attending [Akademy](akademy.kde.org). Soon, Lukáš Tvrdý will be giving his presentation on writing brush engines for Krita. He already put the [slides up](http://lukast.mediablog.sk/lukas_tvrdy_fun_krita.pdf). Yesterday Lukáš and me discussed the action plan for 2.3 and we arrived at a little recalibration, which should appear on the wiki soon.

Although we sorely miss the work of Cyrille Berger, who is looking for a house now that he has been accepted for a post-doc in Linköping and training two puppies, Krita development proceeded at a fast pace in the past two weeks.

If you check out Krita trunk you'll get a smooth transform tool, a completely multi-threaded image recomposition backend that with some changes to come will make it possible to move big vector shapes smoothly on screen (and gives pippin parallelism envy), a hatching brush, a sketching brush and an eraser toggle. No progress on the color selectors: Adam had some exams this week.

Next week, Krita 2.2.1 will be released. This incorporates quite a few bug fixes and is a very nice version of Krita to work with, though definitely not as cool and smooth and exciting as trunk. _If_ you want to help with [testing](http://slangkamp.wordpress.com/2010/06/25/we-need-more-bug-reports/), consider installing trunk. We are ready to help whichever way you contact us, forum, irc, mailing list -- you can even mail me [directly](mailto:boud@kde.org).

### Code

**Cyrille Berger** fixed a crash when closing the filter dialog following a suggestion by Christoph Feck. This fix got backported to Krita 2.2.1 which will be released next week.

**Dmitry Kazakov** was unstoppable: he added a fast way to shallow copy pixels from one paint device to another (where a paint device can be a layer, but also a brush while painting or a temporary pixel storage created in the middle of a complex operation), added a compression framework so krita files can be loaded and saved faster (this will also be used when swapping, and maybe even for in-memory storage of undo information), fixed a bug in the transaction framework, made painting faster (note that we need testers here, if you see glitches while painting, inform Dmitry!) and implemented a multi-threaded optimizer for the update scheduler. If you have a complex image with many layers and at least a dual core computer, you will see a big improvement in the redraw speed. More is to come from Dmitry!

**José Luis Vergara** implemented a gui for setting the options for the hatching brush. He celebrated committing an "ugly but elegant" hack that made the hatching brush look really good and work fast with some liquor, then went on to fix the brush outline for the hatching brush and rounded off with cleaning up his code. Pentalis (as JLV is usually known) now is thinking about the implementation of the impasto feature.

**Lukáš Tvrdý** cleaned up the code and the user interface for paintops with related options and then started working on a really challenging thing: fully supporting Photoshop's ABR brushes. We have a fairly good reverse engineering of the closed, proprietary format, and now support quite a few features. However, a full implementation would likely take more time, so we decided yesterday to document the progress. The full implementation has been postponed to 2.4 -- the current support is already quite good though! We support brush tip dynamics, bitmap brushes, computation brushes and mirroring.

During the weekend, Lukáš felt like having a break, so he implemented a completely new brush engine, called "Sketch", inspired by Project Harmony. Thanks to Ricardo Cabello for giving permission to base our implementation on his work!

**Marc Pegon** started fixing some minor bugs in the undo/redo functionality of the transform tool. Then he made it possible to change the center of the rotation, added horizontal and vertical shearing to the transform worker class (a long standing todo! -- at least five years) and fixed some display corruption. And then, with a big commit, Marc made the interaction with the transform tool quite smooth. Instead of actually transforming all the layer data, we now transform whatever is visible on screen and when the user presses "apply" transform the real data in as few steps as possible.

**Michael Drueing** continued his quest to make Krita compile with Microsoft's Visual C++ compiler. I hope to meet some of the KDE Windows guys this week in Tampere and learn how to do that myself -- and also to learn about the issues packaging Krita for Windows.

**Sven Langkamp** made it possible to turn off the creation of backup files, made sure that we always show a cursor, even if the user selected a 3d cursor but not the opengl canvas, and made it possible to resize the canvas to the size of the current selection.

Sven also figured out what Boudewijn was doing wrong with the MyPaint brush engine. It now works -- it isn't smooth yet, of course, and there are still quite a few issues, but you can paint with MyPaint brushes in Krita now!

Finally, Sven added two new gradients -- but these are not your ordinary gradients! They are updated automatically and show a gradient from current foreground to current background color and from foreground to transparent.  

![](http://www.krita.org/images/stories/krita-gradients.png)  

### Manual

I have been trying to organize the Krita manual. I'm still not sure what the best approach is for initial development. The content navigation on Userbase has to be added manually (previous, up, next etc), and that makes reorganizing more difficult. Plus, if the text on userbase is leading, working on the train is hard. So, ideally, the manual text is in svn.

On the other hand, if the manual is on Userbase, everyone who has a copy of Krita trunk can chip in and start filling in sections with a rough draft. I really only has to be rough: technically correct and about the right topics. It will later be edited into proper, understandable English by a real editor, paid for by the generous donations from our community.

### Conclusion

I still think we're nicely on track for a great Krita 2.3 release, though we could use more help. Of course... But if you've always been interested in getting involved but didn't really know what to hack on, please approach us, and we'll find you some nice bugs to get started with, or maybe some UI polishing!

And just for fun: this is what Krita looked like ten years ago:

![](http://www.krita.org/images/stories/screenshots/kimageshopbrush_grab.jpg)

And this is today:

![](http://www.krita.org/images/stories/screenshots/krita-2010.png)

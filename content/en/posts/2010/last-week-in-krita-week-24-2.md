---
title: "Last Week in Krita -- Week 24"
date: "2010-06-21"
---

Last week, Krita development really picked up, and if today's commit rate is anything to go buy, this week will be just as good! We had fifty commits in week 24. Our bug count is now 58, but that's after Sven Langkamp closed half a dozen bugs today. People seem to like Krita 2.2 and do very nice work with it. If you give 2.2 a try and you experience a problem, please inform us about it. There's a very cool and handy Report Bug menu option in the Help menu!

Lukas worked on better support for Photoshop brushes and some refactoring of the spray brush. Read his [blog!](http://lukast.mediablog.sk/log/?p=255). Our Google of Code students have been busy as well. Adam has been working on the layout for [the new color selectors](http://celarek.at/2010/06/krita-gsoc-layouting-code-for-colour-selector-mostly-done/). Dmitry Kazakov has moved mountains with some big refactorings to make Krita thread-safe and much faster: he will blog tomorrow, he promised! Marc Pegon has started [fixing bugs in the transform tool](http://www.kdedevelopers.org/node/4248). And finally, Pentalis has been [improving the hatching brush](http://pentalis.org/kritablog/?p=138), adding a working gui.

And Sven made his first painting with Krita and one of the Krita Wacom tablets: ![](http://lukast.mediablog.sk/tests/alien_thumb.png)

Read on for more details!

### Code

**Adam Celarek** refactored his Next Generation Color Selectors plugin so the names of the classes make more sense. The generation of swatches (or colour patches) from the image now works. He was also busy experimenting with the layout of the color selector widge, fixed a crash in the color selectors and finally fixed a small bug in Krita's QPainter canvas that would cause too much of the screen being redrawn, making painting in the bottom-right corner as fast as in the top-left again!

**Dmitry Kazakov** refactored the undo/redo code in Krita, hiding the Qt mechanism for the Krita developer. See his [design document on the wiki](http://wiki.koffice.org/index.php?title=Krita/Transactions_Design). This was a huge amount of work! Then he added working with regions to the underlying image storage classes in Krita, in preparation for [the execution of the filter api redesign](http://wiki.koffice.org/index.php?title=Krita/Transactions_Design) he and Cyrille Berger discussed in Deventer. Finally, Dmitry uncovered a bug in our handling of the undo stack. We're discussing that issue now!

**José Luis Vergara, aka Pentalis** experimented with a DDA algorithm for hatching, created a new options widget for his hatching brush engine, cleaned up his code big-time ("Roleplayer's summary: Cha +2, Con +1.")

**Lukas Tvrdy** helped José with the gui for his brush engine, added support for Photoshop brushes to the Spray brush engine, removed the "rate" setting from the freehand tool, creating an "airbrush" option instead which brush engines can use to implement continuously flowing colour. This was a long-standing todo!

**Marc Pegon** committed the beginning of a new transform tool, one that will also be able to deform and shear.

**Sven Langkamp** moved the brush blending mode from the tool options palette to the top toolbar. He also added a quick toggle button to enable/disable erasing, which made it possible to remove the eraser brush engine completely.

### That's it!

As you have seen, there's plenty of things going on again! So why not join the team -- Boudewijn has written [a nice introduction on how to get involved with Krita](http://krita.org/component/content/article/7-krita-information/49-how-to-join-krita), and that needs debugging as well!

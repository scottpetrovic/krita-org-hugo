---
title: "Last Week in Krita -- Week 27"
date: "2010-07-13"
---

Week 27 saw about 40 commits to Krita. Especially Sven Langkamp did a lot of cleaning up in our bug list, so we're at 59 bugs now, despite having received quite a few new reports. Sven's call for testing did work, but we still need more thorough testing if Krita 2.3 is going to be the Ready For You release!

And look what [Ico-dY](http://www.turnangel.com) has made with the trunk version of Krita:  

[![](https://krita.org/wp-content/uploads/2010/07/girl_in_blossom_xkrita.jpg)](http://forum.kde.org/viewtopic.php?f=138&t=88985)  

### Code

**Adam Celarek** already [blogged](http://celarek.at/2010/07/krita-gsoc-colour-selectors-with-colourspaces-support/) about his work: this week he spent time polishing his new color selectors and adding support for colorspaces to them.

**Boudewijn Rempt** "fixed" a bug in our handling of metadata. Well, it's a quote-unquote fix, because it is more a paper-over of the problem that many real-world files have invalid names in the name/value pairs in their metadata. For now, we change the invalid names to something properly scary, like "INVALID", but don't halt krita when encountering the name anymore.

**Dmitry Kazakov** fixed a problem with threading and masks. He also optimized our implementation of shared pointers and weak shared pointers. These days, Qt provides all that stuff, but there is by now so much code using the home-grown implementations that refactoring would take a prohibitive amount of effort. And not only that, it would be hard to be certain that we'd be getting the behaviour the Krita code is used to. Dmitry then optimized the tiles backend by adding a memory pool. Dmitry also enabled the new update scheduler by default. **This really needs testing!** We need to know about all kinds of glitches and other problems you see when working with Krita trunk and images with multiple layers. Then Dmitry optimized some cases where we copy pixels around.

**José Luis Vergara** added the ability to control the levels of separation controlled by the pressure curve in the GUI to the hatching brush engine -- and now the hatching brush engine is feature complete. Testing please! (And cool artwork to show off!). José is now continuing his Google Summer of Code project by looking into a possible implementation for impasto layers.

**Mart Pegon** worked on the [transformation tool](http://www.kdedevelopers.org/node/4271). He fixed a bug with shearing, missing icons and undo/redo bugs. He's now thinking about perspective and free transform for the transformation tool

**Sven Langkamp** polished the brush settings popup by using toggle buttons for the brush tip selection instead of tabs. he re-activated the custom brush brush tip, fixed a crash that occurred when painting after changing the image's color space, fixed a crash in the perspective transformation tool, another crash that occurred when moving a whole image, the order of layers when separating an image into different layers for every channel and yet another problem in the perspective transformation tool.

### Wiki

The Krita developers wiki has moved to [http://community.kde.org/Krita](http://community.kde.org/Krita). The KDE wiki maintainers are, meanwhile, busy upgrading the KDE wikis to a new version.

---
title: "Last week in Krita -- week 2"
date: "2010-01-20"
---

Last week in Krita -- week 2

I am not sure -- last week _felt_ like a quiet week in which nothing much happened. But the numbers show otherwise: the Krita team made about 95 commits. And our testers have been busy as well, so we are now over 90 bugs. Eek! Soft feature freeze has hit, which was accompanied by a frenzied adding of todo's to the [2.2 feature list](http://wiki.koffice.org/index.php?title=Schedules/KOffice/2.2/Feature_Plan#Krita). After the Big Freeze, the Big Thaw has set in in the Netherlands, showing that once again, coding and weather are not synchronized.

### Code

Sven Langkamp improved startup time of Krita by optimizing the code for loading gimp-style brushes, fixed the full-screen shortcut as well as the show/hide dockers shortcut. Sven also made it possible to save presets by name and have them restored by name, as well as fixing bug in a race condition on startup caused by presets trying to access a gimp-type brush resource before that resource was loaded. Krita loads all its resources in threads on startup, so we can present a usable application as quickly as possible. This design dates back to the days when Patrick Julien was maintainer, and we've kept faithful to it. Sven also fixed the painting of the brush outline cursor. This is not the definitive solution, however, there is still some ugliness in the code that's irksome to the developers, but for the user, there won't be much of a visible change. Still, we like to run a clean ship!

As an example of that cleanliness, Adam Celarek continued cleaning up tool code. He removed some constructs that had seemed a good idea in 2004, but that never were used! He also made the tools behave better, so the Escape key now ends a polygonal selection.

Lukáš Tvrdý added a "flow" option to the new soft brush brush engine. This is not to be confused with Photoshop's flow slider, having something like that is still a todo for 2.2. Lukáš also started porting his brush engines to Sven's refactored preset code. Tomorrow, that's Wednesday, Lukáš will have is last exam and barring having to redo one or two (which nobody expects!), he can get started on the [Action Plan](http://wiki.koffice.org/index.php?title=Krita/ActionPlan) after a bit of rest and recreation.

Vera Lukman cleaned up code related to the brush & color palette, making sure memory is freed. Vera has started an internship, but her boss has okay her visit to the Netherlands, so she'll be at the Krita sprint for sure!

Adrian Page continued updating Krita's plugins (of which there are many -- most Krita functionality is implemented in a plugin) to KDE 4 standards, removing obsolete constructions that were outputting user-visible warnings on Krita startup.

Boudewijn Rempt did some work on the mixer canvas: this is a big feature and most of it had to be rewritten after the code had bitrotted since Emanuele Tamponi became to busy with university to work on Krita. Expect more inconcusive "did some work on the mixer canvas" messages in the weeks to come! Boudewijn also 'finished' the gif import and export filter. Now on the topic of the gif filter, here's a big, fat **warning**. Krita is an application for painting and working with true color images. It only supports true color, ranging from 8 bit/channel to 32 bit/channel. Krita is **not** a pixel-precise, indexed-color based smiley or icon creation application. If you want to save your work as a gif file, you have most certainly chosen the wrong application to work with. Still, the code is there now, and any one looking to improve it can get started with the [Gif filter junior jobs](http://wiki.koffice.org/index.php?title=Junior_Jobs#Krita). Boudewijn also implemented some caching mechanisms that improved performance when showing thumbnails in the layer box, using selections or painting.

Cyrille Berger did some work on painting assistants. These are plugins that "guide" in an artistically fuzzy way your freehand painting. The line tool gives you a perfectly straight line (unless you use the curve brush), the line assistant makes the line look more hand-drawn. Then Cyrille started working on a refactoring of the pigment library, which culminated this week with the fixing of a crash on exit, as well as the caching of colorspace objects. This should help a lot with memory consumption and with performance, but we need to measure. Building on Sven's work, Cyrille also fixed the recording of paint strokes which I broke a long time ago. Spurred on by a question on the [forum](http://forum.kde.org/viewtopic.php?f=139&t=85187&hilit=krita), Cyrille fixed the reading of ISO settings in the bracketing-to-hdr plugin, fixed a crash when using the color curve filter on 16 bit rgba images, and fixed a number of issues in our support of metadata. Cyrille also did lots of work on [OpenGTL](http://www.opengtl.org).

On Sunday (which, since I tend to write these articles on Monday or Tuesday, I take for the last day of the coding week) Dmitry Kazakov posted the latest version of his proposed refactoring of the way Krita combines layers into one result image. This refactoring is needed because we still have some errors in the handling of our adjustment layers and because of threading issues. The patch is complex and needs careful testing, fortunately Dmitry has added plenty of unittests.

Marc Pegon's patch that fixed drag-and-drop from Firefox into Krita was committed, so Marc has earned his place in the about box. Marc is currently investigating weirdnesses in the local selection mask mechanism, sleuthing away through Krita's code base.  

![](http://krita2d.org/images/stories/krita-feature-images/krita-gif-selection-mixer.png)  

Krita showing off a loaded animated gif (don't save it!), the new layout of the option panel for selection tools and the new layout for the mixer (which doesn't work yet).

### T-shirts!

It's not a commit... But Kubuntiac continued designing optimized versions of the t-shirt design for black t-shirts, and [aMan presented his own design](http://forum.kde.org/viewtopic.php?f=137&t=85022&p=144583&hilit=krita#p144489). The final design needn't be ready until mid-Februrary, Irina Rempt discovered when investigating t-shirt printing possibilities. So there's plenty of time to get out [your favourite graphics app](http://krita.org) and do a design! As a side-note: the t-shirts won't be paid for by the Krita project, instead, every cent we have received (and we are still receiving donations!), will be used to further development. Given the fixed costs, we will likely print a run of 15 or so. One thing I'm thinking about is setting up a little webshop to sell things like mugs, t-shirts and Krita branded Cintiq tablets with packaged copies of Krita.

That all for now -- if you have comments, go to to our [forums](http://forum.kde.org/viewforum.php?f=136) and discuss!

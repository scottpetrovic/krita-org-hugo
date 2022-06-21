---
title: "One beta released, another beta to go"
date: "2010-10-18"
---

So, quite silently (because I was too lazy^Wbusy to write the announcement) Krita 2.3 beta 2 has been released. However, we had to decide to have another beta since the number of release blockers hasn't materially decreased and the number of crash reports has increased. Now this doesn't mean Krita's quality has detoriated: it means that more people have tested Krita and reported issues. And that, actually, makes me _very_ happy. We need people to test Krita and report issues if we want this release to be great!

And it's not like no work has been done in the meantime. Lukáš Tvrdý has joined Ixonos as a Qt developer -- and here's an example for students at universities all round the world: if you join an open source project like Krita and prove your worth it can be worth a _lot_ to you when you get your degree. Having this kind of experience working in an international team developing an application for actual uses does put you miles ahead of your fellow students who've done nothing but school projects and perhaps some php for the local soccer club. Get [involved](http://krita.org/component/content/article/7-krita-information/49-how-to-join-krita)! You have got nothing to lose but some time and everything to gain -- a fun time, fun, friends and a really good story for your first job interviews.

Anyway, even though Lukáš has joined Ixonos, he's still be doing stuff in his spare time. Dmitry is now our sponsored student. Sven, even though in the middle of exams has kept up his bug fixing. Cyrille, me -- everyone is pulling together to make Krita 2.3 release-ready. But if it's necessary, we will slip the release date.

Of course, release-ready doesn't mean that every imaginable feature has been implemented. David Revoy has asked where his mixing brush is -- we will do that for 2.4. Would, actually, make a great little project for a student eager to get to know Krita development before applying for Google Summer of Code next year... The [2.4 feature plan](http://wiki.koffice.org/index.php?title=Schedules/KOffice/2.4/Feature_Plan#Krita) is already bulking out -- as I said the other day when someone asked about KDE 5, I hope we haven't got any big porting effort for the next ten years, but just development of features and increasing stability and performance!

**[Andreas Esau](http://ndee85.blogspot.com/)** is the latest artist to discover Krita. First he produced this enormously powerful sketch:

![](https://krita.org/wp-content/uploads/2010/10/ndee_sketchbrush_small.jpg)  

Then followed on with one of the first screencasts for Krita 2.3. Watch and enjoy! 

Markku Myllymäki from Finland has been experimenting with the vector support of Krita:

![](https://krita.org/wp-content/uploads/2010/10/kritari_supherkri.png)  

### Code

We had particular trouble with the smudge brush engine in this period. The source of all our trouble is that we want to make it possible for the footprint of the smudge area to change following pressure during painting -- something no other applications support.

**Boudewijn Rempt** made sure Krita 2.3 doesn't load incompatible plugins, fixed a crash that happeend when closing krita while the filter dialog is open, fixed some memory leaks, removed the old perspective transformation tool (the new one has the beginning of the same functionality and can be extended to provide the full functionality; the old perspective transformation tool was now too different from the normal transformation tool to be kept around). Boudewijn added an improved cross-hair cursor (nicked from the Gimp) and fixed the comic book templates icons with icons provided by Animtim.

**Lukáš Tvrdý** fixed the rectangular brush mask with spikes, simplified and sped up the brush mask cursor for brushes with a lower density, optimized painting some more and added oversampling to curve-based brush masks. Lukáš separated the mature and the experimental brush engines in the gui. Note that we do **not** yet guarantee preset compatibility for the experimental brush engines!

**Cyrille Berger Skott** fixed the rectangular brush mask, the merging layers with different colorspaces than the grouplayer, the rotation of layers using the menu as well as the rotation of layers and images at 90, 180 and 270 degrees. He fixed the usefulness of the color-to-alpha filter on transparent layers and a problem with the smudge paintop. He fixed a crash when moving a layer using the move tool, as well as moving of group layers. The feather selection action crashed; after getting the Cyrille treatment, it knows how to behave. And the convolution worker now respects the channel flags again. A crash that happened when applying a color transformation filter like brightness/contrast to EXR layers (like 32 bit float RGB) got temporarily fixed by downscaling to 16 bit LAB and then back.

**Dmitry Kazakov** made the flatten operation not lose layer data outside the image bounds. He also fixed the checkers painting in the OpenGL-based canvas. Dmitry fixed a paint bug in the duplicate brush, a usability bug in the same brush engine, the brush outline when the color picker is activated and made the maximum RAM usage of Krita configurable. Following up on his summer-of-code work, Dmitry removed two (and-a-half...) race conditions in the tile backend and one in the image merger that computes the final image from that layers. Dmitry made all Krita tools support panning and color picking.

**Sven Langkamp** fixed problems with the move tool, especially when moving shape selections and when moving masks. He fixed the loading of old-style brush presets, fixed a crash that occurred on adding a mask to a shape layer. Sven fixed removing shapes from shape selections, the display of local selections in the layer box thumbnails and the updating of the selection projection.

**Adam Celarek**, in the Essen feature branch (so this is for 2.4 already), improved his next generation curve selection widgets. He improved the performance of the NG color selectors. Adam fixed the scratchpad to support transactions so experimenting with the filter brush engine in the scratchpad is now possible.

**Marc Pegon** fixed several bugs in the new transformation tool, especially initializing the perspective transformation option and warp mode. Marc also submitted his internship paper on writing the transform tool to his university. You can download it [here](http://www.valdyas.org/%7Eboud/pegon_report.pdf) -- a good example of combining work on Krita, the Google Summer of Code and internship requirements at university.

### Envoi

Cyrille Berger put [the Krita extensions](http://extensions.krita.org) website online. This is the natural home for all plugins that don't really fit in the Krita vision, aren't totally ready yet or that the author is unsure about submitting in trunk. There's a build service and a page for every extension. So if you have a great idea for a photo-manipulation plugin for Krita -- write it, and submit it! For now, just mail us at the mailing list, ping us on irc or post it on the forum. We're working on a sumbissions page.

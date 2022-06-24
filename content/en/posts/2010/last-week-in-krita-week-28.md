---
title: "Last Week in Krita -- week 28"
date: "2010-07-21"
---

Sixty-eight commits last week -- and thanks to the untiring work of the latest tester to join Krita, Animtim, we're at 71 bugs. In week 28, the Krita team decided to start using the "Major" category for bugs to determine which bugs will be 2.3 release blockers. The categorization is still fluid, but there is no doubt that we are bracing ourselves for the final onslaught. [Lukáš Tvrdý is in bug-fixing mode](http://lukast.mediablog.sk/log/?p=292) as well, spurred on by observations from Deevad.

This is [Animtim's first result in Krita](http://forum.kde.org/viewtopic.php?f=138&t=89173):  

![](/images/posts/2010/character_design_with_krita_by_animtim.png)  

### Google Summer of Code

- Marc Pegon reports on [his work on the transformation tool](http://www.kdedevelopers.org/node/4288)
- José Luis Vergara writes about his work on [the Impasto feature](http://pentalis.org/kritablog/?p=157) for Krita.

### Code

**Adam Celarek** made great progress with the [new generation color selectors](http://community.kde.org/Krita/Community_Mockups_and_Wishlist#Color_selector_mockup). He fixed performance issues, some crashes, added the settings to the kritarc file so Krita remembers you current settings -- with some more polish, this will be the default color selector for Krita for 2.3.

**Ana Beatriz Guerrero López** fixed compilation of Krita on ARM processors

**Boudewijn Rempt** made it possible for plugins to add settings panes to Krita's preferences dialog.

**Dmitry Kazakov** implemented a memory pool for tiles in Krita, optimized the projection update queue so it updates in tiles, cleaned up the freehand painting tool by making the "wash" mode of painting less special and more integrated into Krita's core, incidentally fixing a race condition, and added configuration options for the update scheduler -- you can now play with three settings:

- useUpdateScheduler - you can disable the scheduler by setting this option to false. KisProjection backend will be used instead.
- updatePatchWidth/updatePatchHeight the size of the patches produced after splitting huge update areas
- maxCollectAlpha/maxMergeAlpha/maxMergeCollectAlpha the parameters of optimization process

Note that there's no gui for this: you need to edit .kde4/share/config/kritarc. Then he fixed a bug in the optimized code for copying pixel data, fixed a bug in the adjustment layer dialog, a race condition in when creating the projection of a layer, fixed a bug where transparency masks didn't work correctly for layers with a non-transparent default color, made clone layers work correctly at last and finally started work on swapping image data out to disk. Phew!

**Lukáš Tvrdý** improved the performance of KisPainter's polygon drawing code, implemented support for drawing QPainterPaths on a Krita paint device, fixed the DDA line drawing code -- and that is now used to draw aliased lines of one pixel wide, which means our Pen brush engine now has nice results. Then Lukáš focussed on a bug reported by David Revoy: the painting of brush outlines. David has already tried the new version and likes it!

**Sven Langkamp** made sure that when the user uses a tool that doesn't support painting, the user can see that the brush engine selector is disabled, using Enkithan's icons. He fixed the preferences dialog, where the undo limit was settable, but the setting not saved, worked together with Lukáš to fix the Pen brush engine, fixed a crash reported by Animtim and fixed a bug in the polyline tool.

### Envoi

Not everyone might know it, but this attempt at a chronicle of what is happening in Krita development has had for some time a little sister, [Last Week in KOffice](http://www.koffice.org/news/last-week-in-koffice-week-28/). Now this is my own opinionated report of what happens in Krita, and as such it has a place on planet.kde.org, but for Last Week in KOffice I strive for a little more distance. But a quite a bit of what happens in KOffice has relevance to Krita as well. You might want to check it out, now and then...

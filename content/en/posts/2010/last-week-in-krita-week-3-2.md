---
title: "Last week in Krita -- week 3"
date: "2010-01-25"
---

Last week in Krita -- week 3

Week 3 finally saw a drop in the number of bugs: we're at 86 now. And apart from all the work done on the KOffice libraries -- and every improvement there is an improvement in Krita, and despite many hackers being busy with exams or papers, we managed a grand total of 130 commits, making it hard to keep up. And the [2.2 feature plan](http://wiki.koffice.org/index.php?title=Schedules/KOffice/2.2/Feature_Plan#Krita) shows a marked increase in green! And we have also started on a [feature plan for 2.3](http://wiki.koffice.org/index.php?title=Schedules/KOffice/2.3/Feature_Plan#Krita).

### Code

Cyrille Berger fixed more bugs in our handling of metadata, especially ISO values. Following refactoring of pigmentcms, Cyrille fixed bugs in loading .kra files. Cyrille also refactored the memory management of colorspace plugins. A feature that was first implemented in 2007 and broken (by Boudewijn) in 2008 was once again reinstated: thanks to Sven's work on the brush presets, Cyrille could fix stroke recording and make it possible to edit recorded strokes, making possible, for instance, to change the brush preset used when painting the recorded stroke. The way Krita stored data for response curves, for instance for pressure sensitivity was inefficient, so Cyrille created a better, more generic way of handling this data.

Lukáš Tvrdý found the time, next to his last exam, to port a number of his brush engines to the new preset-support architecture. Additionally, he finished work on his particle brush engine, but didn't quite get round to committing it.

Boudewijn Rempt, following Dmitry's suggestions improved some caching mechanisms in our paint device code. Boudewijn changed Krita's opengl-based canvas implementation to use GL\_RGBA16 whereever possible. People using one of the new wide gamut monitors (that might have up to 12 bit/channel display panels) should now be able to actually see the difference between 8 and 16 bit/channel colorspaces. Also, since OpenGL is still a tricky business, what with proprietary, closed source drivers causing no end of trouble on Linux, Boudewijn made sure that if enabling OpenGL causes a crash, Krita will revert to the Arthur canvas next time krita is started. As promised last week, there was also some inconclusive work on the psd filter and the mixer canvas, but it looks likely that by the end of week 4, mixing will once again be possible. Boudewijn fixed a bug in the [OpenRaster](http://create.freedesktop.org/wiki/OpenRaster) saving code. On a related note: Jon Nordby, a MyPaint developer, managed to get OpenRaster support into Gimp's mainline!

Edward Apap started tackling the perspective transformation tool. This has bitrotted to a large extent, so the renewed attention is very welcome. This led to an interesting discusson on #krita about transformation tools: ideally, we'd have one tool, with a good interpolation strategy that can warp and deform images with much more freedom than the current two transformation tools can provide. Edward also fixed the blur filters so they work with filter layers, cleaned up the selections menu, fixed a crash in the brush preview, implement variable radius selection feathering made it possible to configure whether you want your curves antialiased or not and fixed the settings page for color management as well as a cleanup of the other settings pages. Oh, and he added aspect locking for the grid configuration.

Sven Langkamp made it possible to actually select presets. There are a few more small steps needed, but soon I will upon adventurous artists to start working on a preset sets we for our brush engines we can ship with 2.2!

Patrick Spendrin cleaned up after us and made Krita compile on Windows again.

Dmitry Kazakov posted the next version of his composition update patch: this patch fixes bugs when using filter layers. It is still experimental, so he just presented a patch for everyone to test, and a couple of problems were discovered and fixed. I expect his patch to be committed this week, after he has done his last exam.

### Lukáš gets started!

That's it for last week: this week will see Lukáš' first week of working on Krita full-time, made by the more than 160 generous sponsors! We had a kick-off meeting on Sunday afternoon, and created a benchmarking structure, as noted above. The first day is over now, when I'm writing this, so I can already say that we now have benchmark tests in place for the tiles backend, the pixel access functions and a roundtrip test: loading, rendering and saving a big multilayer document. Let's see what conclusions we can draw from that -- and expect a big update by the end of the week.

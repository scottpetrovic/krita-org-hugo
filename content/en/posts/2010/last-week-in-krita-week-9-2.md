---
title: "Last week in Krita -- week 9"
date: "2010-03-11"
---

Eeek! It's _Thursday_ already! And this week has been so busy with work-work that last week, the Sprint week already seems like ages ago! Of course, I had been writing an article for [dot.kde.org](http://dot.kde.org) since Sunday, but still! Anyway, here it is. First some statistics: we had more than 160 commits in week 9. We went down to about seventy bugs, even when new bugs were being reported quite briskly.

This was a huge task writing it all down; I am afraid it's an equally huge read! And don't forget to read [Lukáš weekly blog about his sponsored work!](http://lukast.mediablog.sk/log/) (It was biweekly this time, but that was because I didn't give him a chance to write anything but code...) We are really happy with the work Lukáš has been doing and really glad that he has agreed to work on Krita, fixing bugs and adding polish for the 2.3 release during July and August. This has been made possible by the generous sponsorship of **Silvio Grosso** who has promised another two thousand euros for the project! Thanks!  

### Code

**Cyrille Berger** was extremely busy. I dread summing up all his achievements during the sprint week, but here we go... Cyrille optimized the convolution painter -- made it about 8 times faster. Edward Apap still has a task here, but Edward has just started a new job and that simply _eats_ energy. Users can now limit the number of undo steps, which can save a lot of memory when painting. An ugly bug when moving a layer up in the layer stack was fixed -- the layer you are moving now stays selected. In general, Cyrille polished the layer box greatly. Cyrille fixed a bug when flattening an image with vector layers. The panorama plugin was retired: it was never finished and doesn't fit in Krita anymore. A shortcut clash was removed: now ctrl-shift-h hides the selection and ctrl-h hides the dockers and toolbox. Cyrille fixed a performance issue when using full-screen Boudewijn had introduced. Following Lukáš' new iterator design, Cyrille created a full set of next-generation iterators. These should be quite a bit faster.

A bug where smudge couldn't use a predefined (gimp) brush got squashed. When Lukáš was optimizing floodfill, Cyrille got busy with gradients, which saw a huge speed-up. All sprint long, all developers were struggling with tablet support. If it wasn't that Fedora wouldn't recognize the tablet at all, we would hit a bug in Qt 4.6 where the stylus buttons wouldn't be recognized. Kudo's go to Nokia's Thomas Zander who prepared a patch for Fedora that made Lukáš very happy. Still, Cyrille spent some time working around the stylus button bug, which made Vera and Boudewijn very happy.

Third paragraph for Cyrille! Spacing between brush footprints has long been an issue. During the sprint week, Cyrille first implemented a new method for calculating spacing, and then refined it from day to day. While Sven was busy implementing preset images, Cyrille was hit by a flash of inspiration, and came up with the idea to (ab)use png files for our brush presets: now we store the preview of the preset as a png image and the settings as a chunk of xml inside the png. And even though the whole thing has a .kpp extension, konqueror shows a nice preview when browsing around.

Lens correction was ported to a shiva filter, so we could get rid of our C++ plugin. In general, people who are _concerned_ about the retirement of filters should look into Shiva: there's so much that you can do with relatively little code -- it's a really easy way to create filters that Krita doesn't ship by default.

* * *

**Dmitry Kazakov** spent lots of time investigating memory issues and fixed quite a number of bad leaks. Merging layer stacks with masks was a bit buggy; Dmitry fixed that after doing a spot of design with Boudewijn. It was cold in the cellars of the church where and when we were working on this -- the memory is vivid! Dmitry fixed a really difficult bug in the transaction system, which led to a change in api in Krita. And finally, to be prepared for more memory leak hunting, Dmitry added facilities for debugging the memory usage of tiles.

* * *

**Lukáš** started by adding HSV dynamics to the soft brush -- everyone interested in digital painting would be well advised to spend some time experimenting with this brush engine. It's lots of very effective fun! The 3D cursor Lukáš had implemented during the Google Summer of Code had been broken by a refactoring of our OpenGL canvas (Boudewijn blames himself, but Lukáš maintains that that's nonsense) -- this was fixed, and together with advances in OpenGL drivers for Intel chips mean that Boudewijn could see the 3d brushes for the first time.

Then Lukáš spent two days working on optimizing the ordinary brush again: [the idea we originally had of computing only a quarter of a circle brush](http://lukast.mediablog.sk/log/?p=173) was revisited. This time, Lukáš got it working without bugs or artefacts -- but then we discovered through careful measurement that it wasn't any faster at all! Big disappointment, but it's great to know that Lukáš could pull of this difficult bit of work after all. Lots of work was done on other brush engines, like the deform brush and the soft brush. The spay brush engine got an airbrush mode.

Flood fill was determined to be slow when Cyrille was trying to follow a tutorial from the now-defunct Corel Painter magazine, and that meant he had to stop following the tutorial. Insupportable! Our resident performance fixer, Lukáš got on the case and made flood fill _much_ faster.

The scratchpad (fourth paragraph for Lukáš) poses some additional constraints on brush engines, namely, they cannot access the image or node, and have to make do with a paint device. Lukáš fixed the brush engines that weren't well-behaved. He also implemented a new widget for setting the brush diameter. The Photoshop brush compatibility effort wasn't forgotten either, though we still have work to do here. Alexandre Prokoudine has started a [project to bind all reverse engineering efforst together.](http://github.com/prokoudine/re-lab)

Smudging is really important for artists -- I so wish my laptop's touch screen would assign a wacom id to my finger so I could smudge like I do on paper -- but Krita's smudge brush has some problems, and one of those is its performance. Lukáš started working on the smudge brush performance, something he continued doing the current week -- after having taken two days of well-deserved rest.

* * *

**Sven**'s first act of daring was fixing the brush outline cursor mode. This is now actually fast enough to use all the time! And Sven could clean up huge tracts of land^W code doing so. A fix to the smudge 3d cursor model let Boudewijn see smudging with a cut-off finger for the first time!

Sven cleaned up the brush options widget and made the checkboxes in the sidebar active. This feels much more natural and makes the actual options pane smaller, which is a very nice side-effect. He then went on to add the scratchpad canvas Boudewijn (q.v.) created to the brush options widget. This was actually an idea by Peter Sikking: instead of a relatively boring squiggle, let users experiment when fiddling with options. Next step here will be making the last stroke dynamic, i.e., change when an option changes. First Sven made sure that there is an area in the preset popup that will be cut out to make the preset preview: then he implemented code to save and load the preset preview image with the preset.

The filter brush engine had become a mess, and Sven was the brave janitor who cleaned it up.

Finally, both Sven and Boudewijn had been working on a [special kind of slider](http://www.valdyas.org/fading/index.cgi/hacking/krita/superslider.html). Justin Noel then got interested and created the widget for us. Integrating the widget in Krita took Sven a bit more time; and we still don't use it everywhere -- but it is way cool!

* * *

**Boudewijn** implemented a mini-canvas -- well, when I say mini, I have to add that it's actually infinite -- to use as a scratchpad in the brush designer and in the color mixer. It's mini in the sense that it doesn't support the wash brush mode nor zooming: but paint, pan and color picker are supported. He also made sure that the brush engines in the brushes combobox are always in the same (alphabetical) order. Boudewijn added **,** amd **.** as shortcuts to make the brush diameter smaller and larger respectively.

There was quite a bit of work done on the mypaint brush engine as well: it's going in the right direction but still doesn't work, and we still don't know whether it's going to be fast enough.

The gif _export_ filter was disabled: if we're a high-end painting application, then people shouldn't use Krita to save gif files, and, in fact, we were mighty bad at it. The quick access palette was moved to right-click, and middle click now pans. The cubism filter was disabled: it was slow and unreliable and besides, a bit of a gimmick.

Boudewijn added a bmp import filter: before, we could only export as bmp -- bmp import used to be done by the obsolete GraphicsMagick filter. The airbrush brush engine was removed: the rate functionality is now part of the general pixel brush. Boudewijn fixed a _big_ memory leak in the selection handling and a crash when using the vector layers.

The really nice thing about this weekend + week of hacking is, even more than the coding achievements I've listed above, the opportunity to sit at the same kitchen table, munch m&m's or peanuts -- and help each other. There was lots of high bandwidth communication, there was walking about time, there was also knocking off around 22:00 for a beer and a chat -- a great time!  

And by Friday, Krita had progressed enough that even Boudewijn could use it paint his first entry in the [form gallery](http://forum.kde.org/viewforum.php?f=138)! Polish artist Przemysław Gołąb (better knows as n-pigeon) started enthusiastically working on [mockups](http://wiki.koffice.org/index.php?title=Krita/Community_Mockups_and_Wishlist) for Krita-the-paint application. Before we implement those, there will have to be a lot of discussion and, importantly, thorough interaction design, but it's great to see the energy!  

### Sprint wrapup

Even though by Sunday all shower cabins in my house had broken, standards of hygiene were relentlessly maintained: the bathtub at least was spared us. [Last Krita sprint](http://www.valdyas.org/fading/index.cgi/hacking/krita/hackathon-1.html) had only two guests staying at my place. Since then we have had some KOffice sprints with more people, but this time we had seven extra people for dinner, and four for breakfast (the other three stayed in bed & breakfast places in Deventer). Without the cooperation of my daughters and all the help of my wife Irina (who also took care of the [t-shirts](http://forum.kde.org/viewtopic.php?f=137&t=85022)) it wouldn't have been possible: many thanks!  

The visit to the blender team was a great success. The [Blender](http://www.blender.org) developers seem very interested in [OpenGTL](http://www.opengtl.org), as is the [RamenHDR developer](http://ramenhdr.blogspot.com/2010/03/more-news-and-gsoc.html). We got the germ of an idea for some cool open content project, but that will have to wait until 2.3. It was great of the Blender team to welcome us to their headquarters were we were allowed to be present at their weekly meeting -- held on Thursday because Boudewijn had a scheduling problem on Friday. Mighty interesting, seeing a movie in development! Storyboarding -- wouldn't that be something to help when developing software? Has that been done already?

Thanks to [Peter Sikking](http://www.mmiworks.net/eng/publications/2010/03/working-on-vision-with.html). He stayed with us all weekend, from Friday evening to Monday morning. He led our [vision discussion](http://www.krita.org/component/content/article/10-news/34-last-week-in-krita-week-8) and then was available for help with [interaction design issues](http://wiki.koffice.org/index.php?title=Krita/Usability). The scratchpad and slider were his ideas, and he's well earned his place in our about box!

Finally, without the monetary sponsorship for travel and lodging from the KDE e.V. this sprint wouldn't have been possible. Thanks!

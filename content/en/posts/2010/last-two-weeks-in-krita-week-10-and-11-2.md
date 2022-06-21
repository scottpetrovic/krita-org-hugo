---
title: "Last Two Weeks in Krita -- Week 10 and 11"
date: "2010-03-22"
---

[Week 9's Last Week in Krita](http://krita.org/component/content/article/10-news/35-last-week-in-krita-week-9) was so long and late that the satisfied feeling of a job well done lasted all week this week -- and only on waking up on Friday morning I realized I hadn't written about Week 10 yet! But then, these two weeks have been quite quiet, with only 54 commits in week 10 and 47 in week 11. The bug count remained relatively stable at 66. A report on the [Sprint](http://www.valdyas.org/fading/index.cgi/hacking/lastweekend.html) was published on [dot.kde.org](http://dot.kde.org/2010/03/15/second-krita-sprint-ends-tea).

You can read Lukáš' report for [Week 10](http://lukast.mediablog.sk/log/?p=218) and [Week 11](http://lukast.mediablog.sk/log/?p=222) -- and [a bonus blog on the soft brush](http://lukast.mediablog.sk/log/?p=224) with some amazing artwork by n-pigeon!

Week 11 also saw the [first beta release of Krita 2.2 (together with KOffice)](http://www.koffice.org/news/koffice-2-2-beta-1/): this still is not the no-excuses release, but it is a major improvement over 2.1.

### Code

Boudewijn started porting the existing gui code to the new [slider widget](http://www.valdyas.org/fading/index.cgi/hacking/krita/superslider.html) -- and then it was discovered that we needed to clean up the API and separate the slider class into two: one for integers and one for doubles. This put a bit of a spanner into the porting effort. Following a suggestion by Cyrille, Boudewijn fixed a bug in the loading of images with vector layers. Finally, Boudewijn started to fix a bug in the mirror horizontally and mirror vertically code. There is one bug remaining: the selection itself should also be mirrored, and a solution for that has eluded him until now.

Apart from being busy with the preparation of the 2.2 beta, Cyrille made sure that if you copy or cut a selection and then paste it that the pasted bit of image is placed at the same location it came from. He also fixed the resizing on canvas of the brush using shift and the tablet stylus. Cyrille followed up by carrying out the refactoring of the slider spinbox widget mentioned earlier. A crash when closing the filter dialog using the titlebar close button was squashed. The filter gallery widget is now hidden by default: users who prefer the gallery to be visible can now enable it by dragging the separator to the right, and there's now a nice configuration setting for that. Cyrille fixed the fade setting of the autobrush. The fast color transfer filter was fixed: now the loading of the reference image works. Cyrille, after discussing the issue with Boudewijn, fixed saving Krita .kra images by saving the default pixel color for a layer. A leak in the shape/vector-based selections was fixed. Alpha lock was fixed in a number of brush engines.

Lukáš was busy in week 10 with the smudge brush engine. This is now much faster, though we now have a problem with artefacts appearing. In Week 11, Lukáš first investigated the possibilities for speeding up Krita using processor vectorization. This turned out to be a red herring, so after that, Lukáš continued working on canvas mirroring. Here we have two different features: drawing an image on one side, with the other side automatically being filled in by the mirroring code, which is [a time-saving feature when designing characters](http://www.youtube.com/watch?v=kGOtGDQ-K-g), and mirroring the canvas view so the artist can see his complete work mirrored -- essential to check whether there are any errors in perspective or anatomy in the drawing. As part of his thesis work, Lukáš committed a lot of fixed to his various brush engines.

{{< youtube kGOtGDQ-K-g >}} 

Sven improved the looks of the spinbox slider widget, fixed a crash in the QPainter based canvas, cleaned up the options widget for the shape tools and fixed the outline and resizing for the sumi-e (or bristle-based) brush engine.

Adrian, Adam, Dmitry, Edward, Marc and Vera were too busy with internships, work or university to work on Krita during these weeks -- we hope to see them back soon! Emanuele Tamponi, the author of the Kubelka-monk colorspaces (that do realistic color mixing) returned to the #krita irc channel after a long hiatus with a proposal for a google summer of code project -- and José Luis Vergara from Chile joined us for the first time to discuss another, but related, idea for a Google Summer of Code project.

### Webshop

Krita as a project is growing very fast: we've got lots of new contributors, we're getting near user-readiness. And we've got a way cool t-shirt design by Adam Celarek. So after some discussion on irc, we decided to open a [Krita web shop](http://www.zazzle.com/kritashop*)! The first thing available are [two versions](http://www.zazzle.com/krita_2010_hackfest_tshirt-235295277583544794) of the [Krita 2010 hackfest t-shirts](http://www.zazzle.com/krita_2010_hackfest_clean_version_tshirt-235685415713172054) and the [Krita 2005 Hackathon t-shirt](http://www.zazzle.com/2005_krita_hackathon_shirt-235055660414629595). We're also considering doing posters with cool art made with Krita and other stuff.

### Summer of Code

An old contributor, Emanuele Tamponi, a new contributor, Marc Pegon and an artist newly interested in Krita, José Luis Vergara have already contacted the Krita team about Google Summer of Code projects. Emanuele is interested in continuing work on the kubelka-monk colorspaces, Marc would like to implement a new transform tool and José is mostly interested in improving realistic painting through color mixing and texturing. We have [put up some more ideas on KDE's Google Summer of Code page](http://community.kde.org/GSoC/2010/Ideas#Krita). Of course, we don't know how many slots KDE will receive, nor how many of those slots will be available to Krita, but much depends on having a solid set of great proposals. So, if you're a student and if you're interested in digital painting, you are welcome to come and create a proposal for Krita!

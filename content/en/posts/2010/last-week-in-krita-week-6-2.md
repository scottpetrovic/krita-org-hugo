---
title: "Last week in Krita -- week 6"
date: "2010-02-15"
---

Last week in Krita -- week 6

Last week was a frustrating week for your correspondent: he didn't manage to get much work done on Krita, also because he had to leave for Kämpfelbach-Ersingen on Friday for the KPresenter sprint. Lukáš Tvrdý had a hard time as well: this week wasn't about performance improvmements, but interoperability, and the goal was to read version 6 Photoshop ABR brushes, and those are entirely undocumented. More of that later!

A measure of the issues this project causes is the number of commits: only about 67. We're currently at 95 bugs. Still, there's some good stuff to report on!

### Code

Adam Celarek rearranged the default set of dockers. This wasn't a total success, but it shows that we need to discuss our default settings in Deventer. But if _you_ have an opinion on that, let's discuss it on the [Krita forums](http://forum.kde.org/viewforum.php?f=136). There are some constraints, like Krita must fit on Boudewijn's tablet laptop's screen (1024x768) and there must be a minimum number of layers visible in the layerbox. Adam also has been branching out to other parts of KOffice and KDE! In Krita, Adam worked around [a bug in Qt](http://bugreports.qt.nokia.com/browse/QTBUG-8035), continued cleaning up our tools code, fixed a layout bug in a color docker, brought the Krita vector tools closer to the KOffice vector tools, made shape selection with an ellipse work _and_ started work on restoring the magnetic selection. (That was originally created by [Emanuele Tamponi during the 2006 google summer of code](http://dot.kde.org/2006/09/05/koffice-summer-code-students-deliver-goods), but never got ported to KOffice 2.x.)

Cyrille Berger continued having fun with Krita's recorder function, adding recording to the fill tool. He also fixed a number of crashes, mostly not yet reported, fixed a bug in the specific color selector when working with floating point channels. Cyrille finally fixed a bad, bad, bad, bug in Krita's OpenGL canvas, making it possible again to use OpenGL with colorspaces with more than 8 bits/channel. There were also some [fixes in OpenGTL](http://www.opengtl.org).

Dmitry Kazakov went on to fix bugs in recomposition code. Like I said [last week](http://krita.org/component/content/article/10-news/31-last-week-in-krita-week-5), this code needs thorough testing by users in real-life circumstances. Give Dmitry a hand and stress his code by creating images with many layers of different types! Show us what Krita cannot handle, so we can fix it! Dmitry also fixed a crash in the cubic spline code.

Edward Apap fixed a bug in the painting code, cleaned up our maths toolbox and then committed a really nice innovation: fast-fourier transformation based convolution for big kernels. That might sound like gibberish, but it means that you should be able to blur large images with big blur sizes without being able to go for a coffee. (And at the same time, Edward fixed issues with the selection of channels to blur: you can blur only a subset of channels now.)

Marc Pegon got his subversion account this week -- congrats! He had been working for some weeks on bugs in our local selection framework. Krita is unique in that we don't have just a global selection and one type of masks, but we have global selections, transparency masks that mask out part of a layer, filter masks that filter part of a layer _and_ local selection masks that protect the selected part of a layer. Marc did a lot of work, fixed a crash, made it possible to move a local selection to another layer, fixed some more usability issues and finally fixed the thumbnail for the selection masks.

Lukáš' task for this week was to make it possible to use Photoshop brushes in Krita. Now this is a problem: the freely available Photoshop 6 documentation only discusses a very primitive type of brush, and I have been told that even recent Photoshop SDK documentation doesn't discuss the CS brush format. Fortunately, Gnome's Valek Filippov had already reverse engineered the V6 ABR format, and there is some code in Gimp and a C#-based viewer application for newer Photoshop brushes. Armed with a set of test brushes and this information, Lukáš dived in, and at the end of the week, painting with ABR brushes basically worked. This week, Lukáš will work on optimizing our iterators -- which should improve Krita's performance all-over.

Apart from that, when writing his thesis on Krita brush engines in the evenings and in the weekend, Lukáš continues to have new ideas for his brush engines, and he made the Sumi-E brush engine twice as fast. and gave it basic bidirectional paint transfer ability: that is to say, on brush onset, it will grab the color from the canvas to paint with. He also improved the soft brush in new ways,

Sven Langkamp continued porting brush engines to the new preset framework: the mixer brush and the filter brush fell before his scythe. He also helped out Lukáš with the integration of the ABR brush in Krita. Oh, and the checkbox to enable/disable a particular option for a brush are now shown in the list:

![](http://krita2d.org/images/stories/krita-feature-images/krita_checkboxes_options.png)  

This will likely need some fine-tuning in Deventer, there was already a discussion about whether the text should be aligned, or not.

Boudewijn helped Lukáš with the integration of his ABR brush parser in the Krita brush system. He also (temporarily, hopefully) hid the mouse position label in the Krita statusbar, following Lukáš [discovery that Krita would repaint its whole window whenever the mouse changed position.](http://www.valdyas.org/fading/index.cgi/software/repainting.html)

### Sprint

The sprint is getting closer and closer. This week, we'll have to decide which t-shirt design to use and print! Don't hesitate to discuss your preferences and ideas [on the forum before it's too late](http://forum.kde.org/viewtopic.php?f=137&t=85022&start=30)!

### Manual

After a promising start on the [file import/export chapter](http://userbase.kde.org/Krita/Manual/ImportExport) of our [new manual](http://userbase.kde.org/Krita/Manual/), not much happened, unfortunately. A good manual is something we really need by september, when we will try to release the all-singing, all-dancing 2.3 version, and we should get started now! If you know what you're doing with a graphics application, and if you can compile Krita from subversion -- [it's not as hard as it sounds!](http://wiki.koffice.org/index.php?title=Build_KOffice), please consider helping out here. Developers are notoriously bad at documentation -- we cannot do this on our own! But don't worry if your English isn't acceptable to the Queen (or the President), we might be able to get some professional editing when all the pieces are in place.

### Coda

Oh, and we have comments now. But for a fun discussion, [join the forum](http://forum.kde.org/viewforum.php?f=136)!

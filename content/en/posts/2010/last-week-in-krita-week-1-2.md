---
title: "Last week in Krita -- week 1"
date: "2010-01-11"
---

Wheee! Week 1! This week turned out to be a sort of flying start of 2010 for Krita, with lots happening in the source, preparations being made for the February sprint and some work on the manual being done.

#### Code

There have been about 70 commits this week, which is kind of a record.

The week started with Cyrille Berger starting work on a new OpenEXR import/export plugin. OpenEXR is kind of a complex library, and the previous import/export plugin was using API's that made it impossible to handle multi-layer OpenEXR images. The new plugin has been designed from the start to do just that. While working on this plugin, Cyrille noticed that we are having some problems with memory consumption. This was partly caused by [OpenGTL](http://opengtl.org) leaking memory, so Cyrille committed lots of fixes in that library as well. We're still not done, though: Dmitry is looking into some leakage problems in the tiles engine, and LLVM is still using way too much memory. Cyrille also fixed a number of crashes in the bracketing-to-hdr feature.

Boudewijn Rempt finished the import side of the new gif filter. Actually, I'm not sure whether Krita ever could _load_ gifs -- I think the old GraphicsMagick-based filter only provided export for gif. Boudewijn is now working on making export to gif work again -- but it is a bit of a why-bother thing. Krita simply doesn't support and won't ever (probably...) support indexed images, so Krita will never be the tool of choice for creating animated smileys. But it's not much code, since we can follow the lead of Shawn Rutledge's read/write qimgio [gif plugin](http://gitorious.org/qt-gif-plugin). This code adds a new dependecy to Krita, namely [giflib](http://sourceforge.net/projects/giflib/). Boudewijn also did some work on the Photoshop filter, but there's nothing finished there yet, and he implemented a unittest that shows that the mypaint-compatible brush engine is beginning to come together. (I still need to find a voice here... First person, third person...)

Adrian Page fixed a lot of problems with OpenGL on Windows. Krita now uses the OpenGL 2.0 core API for our shaders. Kai-uwe Behrmann started a discussion on the mailing list about why Krita doesn't use the full capabilities of the 30-bit displays that are becoming available. Boudewijn provided a first patch to make that work, which was reviewed by Adrian and needs more work. It looks like it _will_ be possible, but it might cause OpenGL to take some slow paths: there's some more work to be done here. Adrian also did some much-needed janitorial work removing deprecated constructs from almost all Krita plugins.

Marc Pegon joined us on #krita and started working on a very annoying bug: drag and drop of images from konqueror would work, but if you tried to drag an image from Firefox, nothing would happen. Marc sleuthed his way through the code and managed to produce his first patch just in time for inclusion in this weeks' Last Week in Krita. It'll be committed today. Welcome to the team, Marc!

Adam Celarek came back from his holiday in Tyrol and committed a big cleanup of the selection tools. The selection and paint tools now share the same common behaviour and the settings for the selection tools are represented by nice new icons created by Enkithan. Note that the shortcut for hiding the dockers is now ctrl-h, not Escape, since Adam discovered that setting the shortcut to Escape hid the most obvious way to close a patch in the polygon tools.

Lukáš Tvrdý was busy with his exams, but still managed to commit a new brush engine, the Soft Brush, which gives a very nice cloudy and almost-wet effect when using the right settings.

Those brush settings... There are so many now that it might be easier to write your own brush engine than to discover the best settings for some engines. We've long wanted to introduce the concept of presets, so you can save and load particular settings for particular brush engines. Well, Sven Langkamp is this weeks hero because he started working on that and came a long way towards this goal. He cleaned out reams of duplicate code in the brush engines to begin with and then continued to make saving and loading of presets work. There is still a lot to do, but the progress is enormous.  

![](http://krita2d.org/images/stories/krita-feature-images/krita-presets-1.png)  

#### Manual

A quality application needs a quality manual. Krita 1.6 had a pretty good manual, one that went beyond the usual listings of menu items and dialog screens. Unfortunately, Krita 2 is really and thoroughly a different application from 1.6: we might be able to salvage a paragraph here and there, but that's it. So I've started a new manual on [Userbase](http://userbase.kde.org), which is the current place for application documentation. And since userbase is a wiki, anyone can grab a chapter and write a few lines! The goal with this manual is once again to produce a useful manual that teaches people how to use Krita. Please go through [the table of contents](http://userbase.kde.org/Krita/Manual/)! We also want to integrate video tutorials in this manual, for instance by hosting the videos on vimeo or something like that, and embedding them in the manual.  

I hardly dare to say this... But I really expect that by this time next year the first books about Krita will start being written.

#### Bugs

Erm... We're at 87 bugs at the time of writing, despite a good number being closed this week. And our unittests aren't too hot either... And, as said above, we have to watch our memory consumption a bit. But that's par for course in this stage of development: everyone is rushing to get the [promised features](http://wiki.koffice.org/index.php?title=Schedules/KOffice/2.2/Feature_Plan#Krita) (check it out, the plan has got colors now) in before the [soft freeze](http://wiki.koffice.org/index.php?title=Schedules/KOffice/2.2/Release_Plan#Soft-freeze.2C_January.2C_13th_2010) hits us. (Which is a weird thing to say, since it's been a hard freeze all over Europe for weeks now!)

#### Sprint

Well, the sprint is coming closer and closer. I've booked accomodation now, since there's no way I can fit all the attendants in my house -- and for the vision session, we even might have to find an alternative to the kitchen table!

And since a good sprint is a sprint with a t-shirt, I've [made a call for designs](http://www.valdyas.org/fading/index.cgi/software/krita/krita-hackathon-2010-shirt.html). Our webmaster Kubuntiac has replied with [a very cool design](http://forum.kde.org/viewtopic.php?f=137&t=85022), but the issue is still wide open, of course, and no artist should feel prevented from joining in the fray! Just a note: black t-shirts seem favoured by most hackers...

That all for now -- if you have comments, hie yourself to our [forums>](http://forum.kde.org/viewforum.php?f=136) and discuss!

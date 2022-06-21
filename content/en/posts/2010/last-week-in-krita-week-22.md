---
title: "Last week in Krita -- week 23"
date: "2010-06-07"
---

Krita development is picking up speed again! We had a bit of a slow period, but it's hard to keep track of everything that's happening again, whether in trunk or on the mailing list.  

Two weeks ago the Summer of Code coding started for real, with Adam committing the first versions of new [color selectors and palette generators for Krita](http://celarek.at/2010/06/krita-gsoc-implemented-algorithm-for-extracting-colours-and-ported-mypaint-algorithm-for-shade-selector/) and Dmitry working really hard on  making the tile engine thread-safe and rewriting the undo/redo code.  

This week, week 24 Marc Pegon has started hacking on the transformation tool. And Pentalis, after having had a bit of a stiffish time getting his tablet to work with his freshly installed Fedora Linux, came in strong with a first cut of his [hatching brush engine](http://pentalis.org/kritablog/?p=91).  

Boudewijn did some coding as well: you can now save documents as templates, and for good measure, Boudewijn added a slightly complex image template for classical waffle-iron comic book pages. Just an example to inspire people to make really good Krita templates! And we need more icons for the template screen.  

Sven started getting back into Krita hacking now his new laptop has arrived by fixing a bug that caused Krita to crash when loading brush presets that have a hue setting. And then he continued with something planned for a long time: the reorganization of the brushes and stuff toolbar. We've put the blending mode on top as well as an easy toggle for the eraser:

![](https://krita.org/wp-content/uploads/2010/06/erased_angel.png)

There's more work to be done there in time for 2.3 to make this important part of Krita as smooth and useful as possible, of course.  

Last weekend, some Krita hackers, namely Boudewijn, Cyrille and Sven met during the [KOffice sprint in Essen](http://wiki.koffice.org/index.php?title=Meetings/Mid_2010_meeting). Most of the time was taken up with KOffice stuff, but we did find some time to discuss our favourite subject, soccer^Wkrita. The toolbox reorganization was one thing we discussed in Essen, another was ways to implement faster saving.  

Regular readers of these updates will join me, I am sure, in cheering for Lukas who graduated last week! And that means that he started working yesterday again on the action plan!  

Till next week -- then the regular service with commit counts, bug counts and everything will be resumed!

---
title: "Soft Freeze!"
date: "2011-09-03"
---

This week, Krita development entered the stage called "Soft Freeze" -- and that means that next week, we'll see the first beta release of Krita 2.4! It also means that we won't be adding new features to what will become Krita 2.4 anymore, so in the past few weeks, a small avalanche of new features landed. And that's excluding the Google Summer of Code projects, about which more later.

So, Sven Langkamp, inspired by the Adaptable GIMP project, added a plugin to create an [Adaptable Krita framework](http://slangkamp.wordpress.com/2011/08/29/adaptable-krita/). Silvio Heinrich added two new dockers: one to create sets of images for use as references while painting, the other one a new, artistic, color selector with a palette creation feature. Boudewijn Rempt added the basics for a new way to create layers and masks from existing layers and masks. That one needs a bit of work still...

### DVD pre-order period ends!

![](http://krita.org/images/stories/comic-dvd/comics-with-krita-dvd-cover.jpg)

When we start releasing beta's, it's also the time to stop taking in pre-orders for the [Comics in Krita DVD](http://krita.org/component/content/article/10-news/90-draw-comics-in-krita-dvd). Until **September 14th** you can still pre-order the DVD + comic book at the reduced price of €20 plus €10 shipping. After September 14th, the price will be €27.50 (plus €10 shipping).  The response to our pre-order offer has been amazing, but if you haven't taken advantage of the pre-order offer -- don't hesitate to do so now! The proceeds of the DVD will be used to fund more Krita development!

The DVD itself is finished now, music, comic book and everything. We're nearly ready to go to press!

### Google Summer of Code

The official Google Summer of Code period has ended as well. All students working on Krita have passed -- but that doesn't mean they are done already!

Srikanth Tiyyagura has implemented the Get Hot New Stuff uploading and downloading of resources like brush preset packs, tagging of resources using GIMP-compatible XML files and Nepomuk, and is now working with a mock-up created by [David Revoy](http://www.davidrevoy.com/portfolio.html) to make tagging work even more smoothly.

Dmitry Kazakov's work is still in a separate branch, which is being tested by artists for regressions. He's managed to implement his idea of only handling user input in the GUI thread, and do everything else in the background. This leads to much smoother painting, for instance and much better stability. There are some small issues that need to be worked out, and Dmitry will be working on that after he's returned from a short, but well-earned holiday. This branch will be merged in time for 2.4. 

Siddharth Sharma has been digging around Photoshop's PSD file format. He isn't done yet, for now the filter only supports single-layer images of all color spaces (except indexed color) in all channel depths, and now he's working on multi-layer images. When that is done, we'll merge his new filter code to 2.4, and Siddharth will continue working on the other features of the PSD file format that can be mapped to the way Krita works.

Bruno Morais from Brazil had a bit of a late start due to exams, but he's working full-speed on implementing the SIOX selection algorithm, and won't stop before he's done. The algorithm works fine now, so he's started working on the user interface.

### Envoi

With our feet firmly set on the road towards the Krita 2.4 release, it's more important than ever that everyone joins in. Krita needs to be tested, tested and tested! Let's work together to find all bugs. The bugs we find need to be triaged -- and for that all you need is Krita and a bugs.kde.org account. And I need people to help me spread the word and write about Krita! Let's get together and make Krita 2.4 amaze the world!

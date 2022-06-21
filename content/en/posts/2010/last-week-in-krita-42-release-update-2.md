---
title: "Last Week in Krita 42 -- release update"
date: "2010-10-28"
---

Well... Krita 2.3 hasn't been released yet. The third beta has been tagged this week, and will be released soon. Lots of bug fixes there! But there are still a number of bugs that block release as well as some failing unittests. We don't want to release with known crashes, for instance. So all those blockers need to be fixed before we can create the first Release Candidate.

You might also have heard something about problems in the KOffice community. Since Krita is based on KOffice technology, those problems might affect our release schedule. There's nothing fatal going on, though.

Within the KOffice community there has been a long-standing disagreement about the architecture of the core component called "Flake" -- the object component technology that ties together various kinds of content in one document and that is used for the vector layers in Krita, as well as the tool system.  Beyond those disagreements, there are also interpersonal issues that have been plaguing the KOffice (but not the Krita!) community for a long time.  

What is going to happen now is that the people who cannot come to agreement anymore go their own way, each of them taking a version of KOffice and pursuing their vision. It's best characterized as a divorce: there will be, at least for some time, two projects based on KOffice.  

Krita is not going to strike out on its own -- although the developers and contributors discussed that amongst themselves. But Krita is not going to be part of both versions of KOffice: there's one Krita project and one team, and Krita will continue in one of those versions of KOffice. Worst thing that might happen is that people running trunk will have to use "svn switch" to move to another source tree checkout.  

The most important thing to note here is that the Krita developers are all together. There's no loss of focus or of fun for us, and we're pulling together to make Krita 2.3 really ready for artists. We're working and looking towards releasing Krita 2.3 this year, after fixing the release blockers.  

The bottom line: Krita 2.3 will still be released this year, and it will rock!

### News

Krita featured in the second installment of the [KDE Commit Digest](http://commit-digest.org/issues/2010-10-17/), where Boudewijn gave an overview of some of the core techological advances in Krita 2.

Sven Langkamp [discussed his attempt](http://slangkamp.wordpress.com/2010/10/25/parallel-brush-mask-processing/) at gaining the next level in painting performance, 500 pixel diameter brushes on 6000x6000 pixel canvas using Qt Concurrent.

And Cyrille Berger [presented his rendition](http://forum.kde.org/viewtopic.php?f=138&t=91068&p=174772#p174772g) of the [Övertorneå Kyrka](http://www.overtorneaforsamling.se/index.php?option=com_content&view=article&id=48&Itemid=64):

![](https://krita.org/wp-content/uploads/2010/10/overtorneakyrka_700.png)  

  

### Code

It might seem slow going, but we managed to get down to four failing unittests, two major bugs, thirteen known crashes, making 67 bugs in all. A new face^Wname on Krita's irc channel, William Steidtmann is diving deep into Krita's histogram calculation code where he has discovered some bugs. No commits  yet -- but very promising hints of fixes coming up.  

**Cyrille Berger** fixed the loading of jpg images with some invalid exiv tags as well as a very nasty rounding bug in the channel scaling code.

**Dmitry Kazakov** fixed a lot of bugs in Krita's vector layers, made it possible to add effect masks to shape layers (though there are still performance issues here that might be difficult to solve) and fixed a memory leak that occurred when showing filter previews.

**Laurent Montel** in one of his regular sweeps through the entirety of KDE's code repository fixed a bunch of memory leaks.

**Lukáš Tvrdý** fixed border artifacts when using the Gaussian blur filter in an effect mask or layer, fixed the small-tiles filter and a bunch of smaller bugs.

**Sven Langkamp** fixed a bug where the ordinary tools could paint on local selection masks -- this sounds cool, but in practice the painting was limited by the selection itself and nothing really worked. He fixed scaling for vector layers, mirroring of layers, improved the performance of the specific color selector and fixed a bug where the popup palette was very slow when selecting a color with the tablet.

### Envoi

It's difficult to say whether we will need a fourth or even a fifth beta, but we are committed to making this release great. I think we have fixed the original set of crash bugs by now, but the really good work-out given to Krita by everyone who's been testing has uncovered new bugs -- and that's great! We don't mind at all if you use the beta's to find new bugs for us to fix.

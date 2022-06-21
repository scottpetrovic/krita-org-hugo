---
title: "Week 47 in Krita"
date: "2009-11-23"
---

Lots of thanks to Kubuntiac for filling in for me last week -- unfortunately personal circumstances forced me to be relatively uninvolved last week. This also meant that week 47 was a bit quiet, since the projects I am working on -- mypaint compatible brush engine, alpha locking, color mixing palette, bug fixing -- were on hold. I did start on .psd filter though, for loading and saving photoshop 6 compatible files. Nice, mindless messing with bits and bytes.

You might wonder why only version 6? That's because Adobe's legal department has told me if they give me access to the latest PhotoShop SDK I couldn't work on free software graphics applications anymore. So I have been working with the old, freely available SDK for version 6 and have looked at the free implementations in Gimp, libpsd, ImageMagick/GraphicsMagick and Scribus, as well as KDE's .psd QImageIO plugin. The early stages have been committed, but they don't import anything yet.

But if I were absent most of the time, the rest of the team has been working really hard. There have been 58 commits to krita, 21 mails to the mailing list, reams and reams of discussion on irc. We're current at 62 bugs, of which 17 are crash bugs -- too much still! -- and there are 102 open wishes. On the forum front, life has been a bit quiet -- [though there an interesting discussion on Vera's popup palette.](http://forum.kde.org/viewtopic.php?f=137&t=83958&p=138292#p138292)

Cyrille Berger fixed a bug in the JPEG2000 filter he wrote last week so files with an upper-case extension won't crash Krita anymore. He also fixed loading masks from Gimp XCF files. Cyrille also added a linear RGB color profile, which gives better results when blending colors in the RGB colorspace. Cyrille has been working on a nice new feature: brushes can now also be rotated. Gimp has had this for ages of course, but it's new in Krita. We have to take care, though, since the brush popup palette threatens to grow beyond the limits of my screen!  

![](http://krita2d.org/images/stories/screenshots/krita_angle.png "Brush Rotation")  

Lukáš Tvrdý has implemented an opacity sensor option for the chalk paintop, so the opacity factor in the ink depletion can be controlled by pressure, for instance. And because ink depletion is a weird concept for a chalk simulation it can be turned off as well.

Adrian Page fixed a crash on OSX and made the XCF filter work on Windows

Dmitry Kazakov was really busy the last few weeks at university, but commited some fixes to the tile engine this week, as well as proposed for review the beginning of work to improve the performance and stability of the image recomposition.

Vera Lukman fixed a crasher bug in her new popup palette for quick access to favourite brushes and colors. She made the popup accessible using middle click: we are discussing possible candidates for keyboard shortcuts. She has also been struggling with making the widget transparent and nice, but it looks like we're hitting a Qt bug here.

That's it for this week -- next week we'll hopefully see the germ of a gif import filter, get the psd filter halfway working, some interesting news and who knows what else!

  

_Feel free to comment on this article on the [Krita Forums](http://forum.kde.org/viewtopic.php?f=137&t=84017)_

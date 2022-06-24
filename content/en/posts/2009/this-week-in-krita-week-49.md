---
title: "This Week in Krita -- Week 49"
date: "2009-12-08"
---

Last Week in Krita -- week 49

The most exciting and amazing things last week was of course the response to our fund raiser: more than 150 people replied and donated money! Thank you all! We reached the target in three days instead of the three months we thought we'd need. Oyvind Kolas, the maintainer of Gegl, told us that we KDE folks always are too modest and set our sights too low. He might be right! Someone even approached me to tell me he thought it a pity that the goal had been reached already, because he had wanted to donate as well. But! Even though we have enough to have Lukas work on Krita for three months now, if you want to help out, you can still donate. One option would be to have Lukas work on Krita for a fourth month, fixing bugs in the running up to the release -- a very worthy goal!

And a necessary one, since the publicity the fund raiser gave us had the effect of more people trying Krita, and the more users you have, the more bugs are found. So we're now at nearly seventy bugs, despise closing more than half a dozen bugs during last week (not counting wishes). We will need to work hard at getting that number down!

Last week, despite the distractions of the ongoing fund raiser, Krita developers created 60 commits. Krita is now, excluding KOffice libraries, at 138,221 lines of code, still fairly modest!

Sven Langkamp [fixed bug 195618 -- misplacing of shapes on crop](https://bugs.kde.org/show_bug.cgi?id=195618). He also fixed [bug 216990: Normalize when selection an ellipse, fixes selection when dragging right to left](https://bugs.kde.org/show_bug.cgi?id=216990) and fixed a crash when trying to select pixels on a shape layer.

Cyrille Berger worked on improved compatibility with different versions of [OpenGTL](http://www.opengtl.org). Cyrille also fixed some bugs in importing images and implemented dodge and burn filters. Together with the filter brush, you can now paint with dodge and burn as well. This also involved the implementation of OpenCTL based color transformations. Cyrille fixed the saving of layer groups in [OpenRaster](http://create.freedesktop.org/wiki/OpenRaster).

Boudewijn Rempt set some first steps towards the creation of a new GIF filter, mainly inspired by the code for loading and saving gif files in [Gimp](http://www.gimp.org). He also continued working on the PSD filter, but that is a long, hard slog. We still cannot read layer data correctly, unfortunately. Boudewijn, assisted by Cyrille, also finished a new 2.2 feature, [requested by Enkithan](http://forum.kde.org/viewtopic.php?f=138&t=82862): alpha locking when painting, filling or applying gradients.

Lukáš, who is right now busy with exams at university, optimized the spray brush, fixed the selection outline, added an aspect ratio switch to particles for the spray brush.

Vera Lukman, who is going up for her finals at university, started adding the ability to have recently used and favourite colors in the popup palette:

![](http://krita2d.org/images/stories/popup_palette_with_colors.png)  

Dmitry Kazakov fixed [bug 215493:](https://bugs.kde.org/show_bug.cgi?id=215493) rectangular selection cannot be undone.

Adrian Page fixed several compilation issues on Windows that were introduced during the week and cleaned up the handling of the line tool: if you press SHIFT, lines no longer are constrained to angles of 90 degrees, but 15 degrees.

The work Cyrille and Lukáš have been doing over the past week adding new possiblities to the ordinary pixel brush have borne fruit: now options like "size" or "opactiy" can not only be controlled by the stylus pressure, but also by inputs like tilt or time. As an example of the possiblities this give, look at the painting of some bamboos Enkithan has done, using the "time" input for the "size" and "mix" option:

![](/images/posts/2009/bamboo-brush.png)  

All in all a productive week, with two big new features completed and a lot of useful fixes, optimizations and polish committed. As our web master Kubuntiac said, using 2.1 already feels old if you've tried trunk -- but trunk is still much less stable than 2.1, and bug reports against 2.1 are _very_ welcome. We have contacted Heise about their experiences with Krita -- remember that they declared 2.1 to be "absturzfreudig", and they did answer, but we haven't yet got the details needed to know what was going on, but it might be a 64 bit problem, so I have converted my development system to 64 bit.

And once again, I cannot repeat this too often: **thank you all for your support of Krita!**

  

As always, Feel free to comment on this story on [the forums](http://forum.kde.org/viewtopic.php?f=137&t=84415#p140449).

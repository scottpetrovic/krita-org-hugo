---
title: "Krita Starts Supporting OpenColorIO"
date: "2012-06-18"
---

Krita has supported color management since 2004. In fact, there's no way around color management in Krita -- no switch to turn it off, it's the cornerstone of how Krita works with images. But, as Kai-Uwe Behrmann [explains](http://www.oyranos.org/2012/06/movie-luts-inside-icc-profiles/), there are several ways of approaching color management. For print, ICC is the way to go. That's what Krita has always focussed on, and that's why professional artists can use Krita in a workflow that includes sending CMYK tiff files to publishers. Krita depends heavily on [LittleCMS](http://www.littlecms.com): in fact, we don't just use LCMS for classic color management tasks, but also for things like the curve adjustment filter.

But Krita has also supported, since 2005, working on openEXR images, which are mainly used in the film studio world. Now, the movie world has a different approach to color management than the print world. For instance, there is a big difference between the way colors look when projected onto a screen compared to a monitor, and there need to be ways of compensating for that.

In the film production world, the preferred library to provide color management is [OpenColorIO](http://www.opencolorio.org), ocio for short. In the past two weeks I integrated ocio into the Krita display pipeline. It's still completely optional, but when present will make it possible to select source and display profiles for any image in 16 or 32 bits floating point RGB colorspaces. This works fastest with the OpenGL canvas, but should also work fine with the ordinary canvas.

Of course, there are still quite a few bugs, since nobody has used the feature in anger yet -- but still: it's a big milestone!

![](/images/posts/2012/krita_opencolor_io.jpg)

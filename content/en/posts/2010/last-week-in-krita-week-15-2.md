---
title: "Last Week in Krita -- Week 15"
date: "2010-04-22"
---

As we near the 2.2 release, the developers are getting tired with running. Or so it seems -- we only had 25 commits in Week 15. And while Lukáš now is really focussing on his thesis, Boudewijn is quite busy in his new job as a full-time KOffice developer and part-time manager, and Cyrille is busy trying to get a research place at a university. But some of the commits were quite interesting! We're still at about 56 bugs, but the number of unittest failures has decreased a lot. On the topic of bugs: testing beta and release candidates really helps! Please badger your distribution to package the beta and rc releases of KOffice so you can install Krita and give it a good test!

### Code

**Adam Celarek** fixed a [bug with tool activation](https://bugs.kde.org/show_bug.cgi?id=185767) on vector layers, as well as a nasty bug when you'd use the crop tool on a vector layer.

**Boudewijn Rempt** boldly deleted _all_ old gimp-style brushes. You know them -- the bell pepper, the starburst, the various round and fuzzy round brushes that have been greeting the user of Krita (and Gimp) since last century. But we're not leaving our users in the lurch: instead we are the first free graphics application to package [David Revoy's](http://www.davidrevoy.com/?article29/free-brush-kit-for-chaos-and-evolutions) guaranteed useful and _free_ set of brush tips! Boudewijn also added David's color swatches. Please give them a good workout! It might very well be necessary to tweak them a bit to account for differences in the way Krita works and Gimp works, for instance with regards to spacing. **Enkithan** prepared new icons for the image templates, and Boudewijn committed those as well. What we really need is a better set of templates as well. If you have good ideas, join us on irc or the forum and we'll guide you through the (intricate, but not difficult) process of creating new image templates! Boudewijn also received his [Chaos & Evolutions DVD and found it money well spent](http://www.blender3d.org/e-shop/product_info_n.php?products_id=122)!  

**Cyrille Berger** fixed some some very stubborn crashes when converting images between different colorspaces.

**Dmitry Kazakov** fixed [a bug that would cause crashes when painting, if Krita was built in a mode that enables asserts](https://bugs.kde.org/show_bug.cgi?id=232524). Asserts are warnings a developer builds into his application so he gets alerted when the application enters into a wrong state: normally they are de-activated when an application is built for users. That doesn't mean that passing the boundaries of the expected is good for users either... In any case, great fix!

**Lukáš Tvrdý** was on a bit of a roll with his brush engines. The hairy brush gained anti-aliases strokes and some optimizations, as well as a way to use blending modes for brush hairs. Ink depletion is now optional, and off by default. Enable it for the authentic sumi-e effect! The hairy brush now can also use the rotation and opacity sensors. Spacing for the soft brush was changed, which makes the brush engine more useful, and, even more fun, the softness curve can be controlled using the pressure of your tablet. [Look at Lukas having fun with the hairy brush:](http://forum.kde.org/viewtopic.php?f=138&t=87358)  

![](https://krita.org/wp-content/uploads/2010/04/chumac_thumb.jpg)  

**Sven Langkamp** fixed the loading of generator layers. Generators are a kind of filters that don't take input; one could create flame, dust, fog, clouds, fractal generator layers -- but right now, we've only implemented the solid color generator layer. And finally, Sven removed the non-working preset button on the toolbar (it is supposed to show a preview of the preset, but we disabled that during the sprint) with an ordinary button.

### Discussions on the forum

I want to really invite everyone to join the discussion on the [forum](http://forum.kde.org/viewtopic.php?f=138&t=87088&start=20) about the design of the brush options/preset selection popup. It's something we really need a proper interaction design for, but it's good to have a wide ranging discussion first. Join in!

---
title: "Krita in March 2011"
date: "2011-03-23"
---

Busy times ahead... We're working towards the first snapshot release of Calligra, which will be taken from git master. And git master already contains many delectable improvements over Krita 2.3.x... And the Calligra sprint in Berlin is coming up, as well as the Krita sprint in Amsterdam and [Libre Graphics Meeting](http://www.libregraphicsmeeting.org) in Montreal. And then it's time for Akademy, again in Berlin.

### Code

We had a couple of really nice contributions from newcomers in the past few weeks! Bug fixes and even some feature development.

**Srikanth Tiyyagura** implemented a long standing [wish](https://bugs.kde.org/show_bug.cgi?id=127571): the ability to split an image into a number of tiles. He's still working on refining his patch, but the first part has been committed. Srikanth has also been fixing bugs in the layerbox.

**Valentin Cheillon** fixed a bug in the filter dialog: the scrollwheel whould change the active filter instead of scroll through the list of filters. He's now looking into fixing some more bugs.

**Geoffry Song** improved a very important part of Krita: the smoothing of freehand lines. This is something that I already blogged about in [2004](http://www.valdyas.org/fading/index.cgi/hacking/krita/learning_cpp.html?seemore=y). Since then, many people have contributed improvements: Adrian Page, Cyrille Berger, Bart Coppens and many others. I guess the work is never done -- it is kind of a tough problem -- but with Geoffry's latest work we have something really nice.

**Silvio Heinrich** created a new "smudge" brush engine. Smudge between quotes because it's also a color mixing brush... And some iterations later, the speed is much improved! Already, David Revoy and Animtim have create create art with it: 

Ryu by David Revoy

![](https://krita.org/wp-content/uploads/2011/03/speedpaint_ryu_deevad_plassy_smudge.jpg)  

Ganesh by Animtim

![](https://krita.org/wp-content/uploads/2011/03/ganapainti_720.png)  

**Dmitry Kazakov**, again sponsored by Silvio Grosso, has been working on fixing issues with really big images. While not perfect yet, the tile pooler is now useful again, even when using multi-layer images of about 10000x10000 pixels. The pooler mainly improves painting speed when starting a new stroke, and so is extremely important, even if it's a hidden feature.

**Cyrille Berger** has fixed a bug in the color profile handling in the pgn import/export code. He fixed bugs in tonemapping, improved the sensor handling, especially for brush footprint spacing

**Marc Pegon** fixed a bug in the transform tool: when scaling up/down an image using the transform tool from one of the corners when there is perspective, the corner now strictly 'follows' the mouse cursor.

**Sven Langkamp** merged the mypaint brush engine plugin into master, where it's available for every artist to test! He also fixed saving predefined (gimp-compatible) brushes: angle and scale were not saved, as well as locale problems in Krita brush presets. Sven made it possible to select different layers in different views on the same image: there's some fallout here, so please give the layer handling in the layer box a good test!

**Lukáš Tvrdý** has worked on improving the multihand tool some more: there's now support for an airbrush mode and you can mirror vertical, horizontal or both. He fixed the flickering of the experimental brush engine.

### And more

Don't forget to checkout [episode three](http://forum.kde.org/viewtopic.php?f=138&t=94197) of Wasted Mutants! And if you're in Montreal for the Libre Graphics Meeting, join Animtim in his Draw Comics With Krita workshop!

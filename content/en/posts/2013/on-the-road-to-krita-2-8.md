---
title: "On the Road to Krita 2.8"
date: "2013-11-13"
---

The Krita team is working really hard on the next release -- Krita 2.8, expected to be released end of December, early January.  And it's shaping up to be a memorable release! There is a host of interesting features, and many, many bug fixes as well. Let's take a look at what's coming!

### Tablet Support

Krita has relied on Qt's graphics tablet support since Krita 2.0. We consciously dropped our own X11-level code in favour of the cross-platform API that Qt offered. And apart from the lack of support for non-Wacom tablets, this was mostly enough on X11. On Windows, the story was different, and we were confronted by problems with offsets, bad performance, no support for tablets with built-in digitizers like the Lenovo Helix.

So, with leaden shoes, we decided to dive in, and do our own tablet support. This was mostly done by Dmitry Kazakov during a week-long visit to Deventer, sponsored by the Krita Foundation. We now have our own code on X11 and Windows. Drawing is much, much smoother because we can process much more information and issues with offsets are gone.

### OpenGL and Shaders

Krita was one of the first painting applications to support OpenGL to render the image. And while OpenGL gave us awesome performance when rotating, panning or zooming, rendering quality was lacking a bit.

That's because by default, OpenGL scales using some fast, but inaccurate algorithms. Basically, the user had the choice between grainy and blurry rendering.

Again, as part of his sponsored work by the Krita Foundation, Dmitry took the lead and implemented a high-quality scaling algorithm on top of the modern, shader-based architecture Boudewijn had originally implemented.

The result? Even at small zoom levels, the high-quality scaling option gives beautiful and fast results!

![](/images/posts/2013/krita_high_quality_filtering.png)

(Image by [Timothee Giet](http://timotheegiet.com/) -- view separately to see it properly)

We hit a snag here, though: on Windows, Krita didn't render anymore on Nvidia graphics cards with the latest drivers. But our awesome community of users did a whip round and pretty soon the Krita Foundation was presented with enough money to get a new Nvidia card -- and within half an hour of getting the card installed, the issue was fixed!

### G'Mic

Krita 2.8 will have initial support for the [G'Mic set of very nearly magic image processing algorithms](http://gmic.sourceforge.net/), out of the box. Developed by Lukáš Tvrdý, this new plugin makes it really easy to, for instance, color line-art, a feature in huge demand by artists.

### Windows

We have been making Krita builds for Windows for about a year now. Since the [original OpenGL refactoring in May](http://www.valdyas.org/fading/index.cgi/hacking/krita/gl2.html), Krita has supported OpenGL on Windows as well. While still not perfect, our builds are improving enough that Krita 2.8 will be the first stable Krita release for Windows.

### Clones Array and Wraparound Drawing Mode

We've featured these before. The [Clones Array](http://krita.org/item/197-new-clones-array-tool) tool is especially handy for artists working on tile-based games, while [wraparound drawing mode](http://krita.org/item/196-new-wraparound-tool) is awesome for making textures that need to be tiled seamlessly.

### And more...

Sascha Suelzer has improved on resource tagging system. Camilla Boemann has been improving the PSD import and export filter and the crop tool. Michael Martini then started polishing the crop tool even further. Dmitry rewrote the code that mirrors a layer (not to be confused with the canvas mirroring mode...) There are a huge number of bug fixes,  the default brush presets have been carefully tuned and have really nice new icons,  Sahil Nagpal fixed a bunch of filters for his Google Summer of Code project, masks are now grayscale-based, making it easier to paint on them -- and much, much more. I am already dreading writing the release announcement!

### Give it a spin

Windows users can give the current development version a spin by downloading the packages from [KO GmbH's download page](http://www.kogmbh.com/download.html#kritagemini), while Ubuntu users can use [Dmitry's Krita Lime repository](https://launchpad.net/~dimula73/+archive/krita).

### Support Krita and Get Support

While much of the work on Krita is done by enthousiastic volunteers, the Krita Foundation is currently sponsoring Dmitry Kazakov to work full-time on Krita. Please help the Krita Foundation by subscribing to the development fund!

 

<table><tbody><tr><td><input type="hidden" name="on0" value="Krita Development Funding">Krita Development Funding</td></tr><tr><td><select name="os0"><option value="Bronze">Bronze : €5,00 EUR - monthly</option> <option value="Sliver">Sliver : €10,00 EUR - monthly</option> <option value="Gold">Gold : €25,00 EUR - monthly</option> <option value="Platinum">Platinum : €100,00 EUR - monthly</option> <option value="Diamond">Diamond : €250,00 EUR - monthly</option></select></td></tr></tbody></table>

  ![](/images/posts/2013/pixel.gif)

And if you are a professional Krita user, either individually or in a VFX studio setting, remember that KO GmbH offers commercial support for Krita, too. Check out the [Krita Studio website](http://www.kritastudio.com) for more information!

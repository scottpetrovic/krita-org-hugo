---
title: "First Beta of Krita 2.4 released"
date: "2011-09-14"
---

Krita 2.4 draws near!

Today, the Krita team is releasing the first 2.4. Already usable, but not perfect yet, this is the perfect moment for you to install Krita and try to break it. Help us out and find those bugs for us! Detailed instructions after the commercial break.

### Great new features and improvements!

In according with our master plan, Krita 2.4 development has focussed on making painting as fast and fun as possible. The brush editor has seen an enormous amount of work, with many new possibilities for fine-tuning Krita's brush engines for the effect you want. We have a new brush preset palette, which makes it easier to pick the right brush preset while painting, and you can add your favourite presets to the right-click popup palette. We have also new shortcut keys to make resize your active brush, change opaicity or darken or lighten the current color.

Srikanth Tiyyagura's Google Summer of Code project has been fully integrated: this brings Get Hot New Stuff integration to all Krita resources, including brush presets. Share and enjoy!

We fully expect artists to have many hundred presets, so Srikanth added a tagging feature -- you can add tags to your presets and query the installed presets by tag. In short, Krita 2.4 lets you get organized.

Take the [tour to see the main improvements!](http://krita.org/component/content/article/8-press-releases/94-krita-24-beta-release-visual-tour "Krita 2.4 Visual Tour")  

Of course there are many, many more features. Krita 2.4 has new brush engines, a new color selector, a way to manage reference images, drag and drop compatibility with other applications.  And, of course, there's lots of cool work which likely won't be in 2.4, but in a later release, like Matus Talcik's opencl filter plugin or Torio Mishi's animation plugin. Just browse this condensed list:  

- new colorengine plugin that uses lcms2: this is preferred for performance and stability reasons and we urge all distributions to compile krita against lcms2.(Cyrille Berger and Boudewijn Rempt)
- a history docker showing the undo/redo history (Matus Talcik)
- the filter api has been refactored to make it easier to create new filter plugins (Cyrille Berger and Dmitry Kazakov)
- MyPaint brush engine support (experimental, will probably not be in the final release) (Sven Langkamp)
- New color sources (pattern, gradient, random) for brushes (Cyrille Berger, Silvio Heinrich)
- improved convolution filters (Jose Luis Vergara)
- new smudge+paint brush engine (Silvio Heinrich)
- make krita work much better with large images (Boudewijn Rempt)
- New blending modes (Arcus Tangent, Gamma Light, Gamma Dark, Geometric Mean, Vivid Light, Pin Light, Grain Merge", "Grain Extract", "Hard Mix", "Copy Red/Green/Blue/Opacy", Additive-Substractive, improved divide, Soft Light, Hard Light, Atop, HSY, HSV, HSL, HSI, dissolve and Overlay) (Silvio Heinrich)
- made the burnd, dodge and color burn blend modes compatible with Photoshop (Silvio Heinrich)
- create an experimental multihand-tool which allows the user to paint with several brushes at the same time (Lukas Tvrdy)
- add a workspaces features: you can save named configurations of dockers for different purposes (Sven Langkamp)
- add symmetry, mirror and translate mode for painting (Lukas Tvrdy)
- add a channel selection docker (Sven Langkamp)
- add new sensors and make it possible to influence a brush parameter with more than one sensor (like pressure, random, tilt and so on) (Cyrille Berger)
- improve canvas rotation (Silvio Heinrich)
- Fix embedding of icc profile data in JPG and PNG files (Cyrille Berger)
- Fix brush preset data when editing a .kpp brush preset file in Krita (Cyrille Berger)
- Add support for DNG and Panasonic RAW2 raw image files (Cyrille Berger, Sven Langkamp)
- Make it possible to select different layers in different views (Sven Langkamp)
- Improve the tiles backend to make projection updating faster (Dmitry Kazakov)
- Improve scaling gui when using the transform tool (Marc Pegon)
- Improve handling of layerbox when using a tablet (Dmitry Kazakov and Jose Luis Vergara)
- Add an opacity setting to brush presets
- Improve smoothing of the freehand tool (Geoffry Song)
- Make it possible to remove painting assistants (Geoffry Song)
- New feature: split an image in a set of rectangles (Srikanth Tiyyagura)
- Make painting obey channel locks
- Improve compatibility with GIMP's XCF file format (import only) (Silvio Heinrich, Lukas Tvrdy)
- Improve painting speed with the default autobrush (Geoffry Song)
- the sketch brush no supports density, line width and offset scale sensors.
- Integrate Get Hot New Stuff with Krita's resource management for brushes, presets, patterns and gradients (Srikanth Tiyyagura)
- Add hexadecimal input to the specific color selector (Sven Langkamp)
- Load blending modes defined in OpenRaster (Boudewijn Rempt)
- Make it possible to load single-layer PSD images (may not be in the 2.4 release) (Siddharth Sharma)
- Add opacity, size and flow sliders to the toolbar (Sven Langkamp and Silvio Heinrich)
- The line tool now supports pressure and tilt (Lukas Tvrdy)
- Add keyboard shortcut for changing luminosity of the active color (darker: K, lighter: L) (Lukas Tvrdy)
- Configurable "Show just the canvas" mode (Boudewijn Rempt)
- Improved selected color preview in the advanced color selector (Adam Celarek)
- Add simple support for BMP, GIF, XPM and XBM formats. (Boudewijn Rempt)
- Add preset management to the preset editor popup (Jose Luis Vergara)
- Improve the preset editor in many ways (Sven Langkamp, Jose Luis Vergara, Silvio Heinrich, Cyrille Berger, Lukas Tvrdy)
- Fix margins in export to PDF (Sven Langkamp)
- Add a "save incremental" option which saves your work with an auto-incrementing suffix (Jose Luis Vergara)
- Use brush presets in the right-click popup palette (Sven Langkamp)
- Add Nepomuk and GIMP-xml-based tagging to all Krita resources (Srikanth Tiyyagura)
- Make it possible to disable and enable the on-canvas preview of filters (Sven Langkamp)
- Make it possible to add a new ICC profile from Krita instead of copying it to certain directories (Boudewijn Rempt)
- Fix a problem where switching tools would make Krita, especially selecting colors, slower and slower (Boudewijn Rempt)
- Smooth out the canvas zooming in non-opengl mode (Boudewijn Rempt)
- New mode for the Text brush: it now can spray the letters of the text, one letter per dab.    (Lukas Tvrdy)
- New feature: the Image Docker, which makes it easy to create and browse sets of reference images (Silvio Heinrich)
- New color selector based on the color wheel. Picking the three color dimensions (hue, saturation, lightness) separated from each other with this color selector should be more convenient. (Silvio Heinrich)
- Implement drag & drop between Krita and other applications, like Dolphin, Gimp, Gwenview, Firefox and so on, and more advanded drag & drop between instances of Krita. (Boudewijn Rempt)
- New Text Tool: this places the text tool that creates artistic text vector objecs where users who come from Photoshop expect it. (Sven Langkamp)
- Improve brush outline mode (Sven Langkamp)
- Add a splash screen to Krita (Boudewijn Rempt)
- Make it possible to add, remove and hide resources (Srikanth Tiyyagura)
- New implementation for the curve brush with curvy, recurvy and smooth effects (Lukas Tvrdy)
- Add taskset docker (Sven Langkamp

Phew! Time for a screenshot:

![](/images/posts/2011/coolscreen24.png)  

### Splash screen!  

During the beta and release candidate periods, we'll pick splash screen designs from the contest thread for every release. The winning splash will be used for the final release.

The winner will receive a DVD+Comic pack for free -- and two runners up will get the Drawing Comics with Krita DVD!

[Look here](http://forum.kde.org/viewtopic.php?f=137&t=96909) for the rules -- but it's easy: done with Krita and fits in the template.  

### Drawing Comics with Krita Training DVD

So you want to start painting with Krita? You could do worse than take a lesson or two from one the masters. Get the Drawing Comics with Krita Training DVD by Timothee Giet. Pre-orders will be valid until Saturday: after that, we'll have to charge the full price. [Order yours now!](http://krita.org/component/content/article/10-news/90-draw-comics-in-krita-dvd)

### How to install and report bugs

If you want to join us in our effort to iron the bugs and issues out of Krita before we release 2.4, you're very welcome! Many Linux distributions will package 2.4 beta 1 and make it available for you to download. Take care to also install the debug (dbg) packages! That will help a lot when reporting issues.

Alternatively, you can build Krita from source. This is made easy with Kubuntiac's krita build script, which you can find at the [forum.](http://forum.kde.org/viewtopic.php?f=139&t=92880)

If you find a bug, you can use the bug reporter to tell us about the issues. If you encounter a crash, the bug reporting dialog will appear automatically. If you have a non-crash bug, go to the help menu chose the "Report Bug" options. You will need a bugs.kde.org account -- but hey, they're free!

If you want to discuss your findings, join us on irc (#krita on irc.freenode.net, [Konversation](http://konversation.kde.org) is a good and friendly client), on the [mailing list](https://mail.kde.org/mailman/listinfo/kimageshop) or the [Krita forums](http://forum.kde.org/viewforum.php?f=136), whichever you prefer.

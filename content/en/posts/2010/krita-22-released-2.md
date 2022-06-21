---
title: "Krita 2.2 Released"
date: "2010-05-25"
---

Coinciding with the [Libre Graphics Meeting](http://libregraphicsmeeting.org) which started today in Brussels, the Krita team proudly presents Krita 2.2!

More than twelve developers have poured about 1600 changes into this version of Krita, the first one we consider to be approaching user-readiness. Krita 2.2 includes the first phase of Lukáš Tvrdý's sponsored work on improving performance and usability. [Thanks to all our sponsors](http://krita.org/index.php&option=com_content&id=20)!

Highlights of Krita 2.2 are the new brush engines, developed by Lukáš Tvrdý for his University thesis, the new brush settings preset system, mainly created by Sven Langkamp, new file filters created by Cyrille Berger for xcf, jpeg2000 and OpenEXR, action recording, also created by Cyrille Berger, much more extensive use of [OpenGTL](http://www.opengtl.org), also by Cyrille, a new core image handling system by Dmitry Kazakov and a quick-access popup palette for recently used colors and brushes by Vera Lukman. There are beautiful new icons by Enkithan. And, of course, hundreds of other bigger and smaller improvements!

Development continues for Krita 2.3 which will be released near the end of this year. [Four Google Summer of Code students](http://www.valdyas.org/fading/index.cgi/software/gsoc2010.html) join Lukáš who is committed to another summer of full-time hacking, thanks to our many sponsors. Thanks go especially to Silvio Grosso, who has donated another very large sum to make help us improve Krita even more! We are now putting the finishing touches to the action plan for this effort, please read all about it at [our wiki](http://wiki.koffice.org/index.php?title=Krita/ActionPlan2). For 2.3, the focus will be on performance, usability, performance, a good user manual, performance and improved compatibility with non-X11 platforms.

Please read [the full changelog for an almost exhausting list](http://krita.org/component/content/article/11-changelogs/44-krita-22-changelog) of changes, or read on for more details about what makes Krita 2.2 cool!  

Some Linux distributions have made or will make Krita 2.2 available in special repositories. For Deb ian this is [http://qt-kde.debian.net/](http://qt-kde.debian.net/). For openSUSE  11.2 with KDE 4.4:  
[http://download.opensuse.org/repositories/KDE:/KDE4:/Playground/openSUSE\_11.2\_KDE4\_Factory\_Desktop](http://download.opensuse.org/repositories/KDE:/KDE4:/Playground/openSUSE_11.2_KDE4_Factory_Desktop/). Note that depending on your distribution, you might have to install additional packages from KOffice. You can also download the [source](http://download.kde.org/download.php?url=unstable/koffice-2.2.0/koffice-2.2.0.tar.bz2) yourself.  

### Brush Engines

Krita has many different brush engines. Click on the combobox that says "Pixel Brush" on startup to start exploring all the brush engines available to you:

![](https://krita.org/wp-content/uploads/2010/05/krita-2.2-announcement-1.png)  

The chalk brush gives you a line with soft, broken edges and a bit of a speckled effect.

![](https://krita.org/wp-content/uploads/2010/05/krita-2.2-announcement-2.png)  

The curve brush has three different methods to wiggle and jiggle while you're sketching.

  

![](https://krita.org/wp-content/uploads/2010/05/krita-2.2-announcement-3.png)  

Then you can deform whatever you have created in a myriad ways:

![](https://krita.org/wp-content/uploads/2010/05/krita-2.2-announcement-4.png)  

The grid brush has many, many different options to fill you screen with varicolored particles, ellipses or pixels arranged in a grid.

![](https://krita.org/wp-content/uploads/2010/05/krita-2.2-announcement-5.png)  

The hairy brush -- formerly known as Sumi-E -- has sprouted new options and deserved a new name. You can achieve wonderfully realistic smeary effects with it, as well as traditional sumi-e effects.

![](https://krita.org/wp-content/uploads/2010/05/krita-2.2-announcement-6.png)  

The particle brush is another brush that draws for you -- in a sense. Reminiscent of [Alchemy](http://al.chemy.org), you can use the particle brush to quickly put down areas and blocks of color.

![](https://krita.org/wp-content/uploads/2010/05/krita-2.2-announcement-7.png)  

The soft brush is an experimental brush engine that puts down a stroke that is softer than the pixel brush, with a more randomness to it.

![](https://krita.org/wp-content/uploads/2010/05/krita-2.2-announcement-8.png)  

The spray brush can spray pixels, ellipses, rectangles and images in random patterns on your canvas.

![](https://krita.org/wp-content/uploads/2010/05/krita-2.2-announcement-9.png)  

Finally, the old stand-by brush engines, like the pixel brush, the smudge brush, the duplicate brush and the eraser have received a lot of love. The pixel brush now can load Photoshop's ABR brush tips (with some limitations), the default set of Gimp GBR and GIH brush tips has been updated with David Revoy's set of Chaos and Evolutions brushes and there are many new options for you to play with.

![](https://krita.org/wp-content/uploads/2010/05/krita-2.2-announcement-10.png)  

Note that David's brushes are fairly big. Krita can handle such big brushes now. But you might want to scale the brushes down by default, by changing the size option:

![](https://krita.org/wp-content/uploads/2010/05/krita-2.2-announcement-11.png)  

### Brush Settings

That screenshot already shows you the next big thing in Krita: brush setting presets. There's no denying that Krita's brush engines are complicated beasts, and you wouldn't want to lose that perfect combination of settings -- so it's possible to save brush settings and share them with others.

![](https://krita.org/wp-content/uploads/2010/05/krita-2.2-announcement-12.png)  

Note the area on the right: this is the scratchpad where you can test your settings. The top part is used as the image for you brush preset when you save it. And did you see the blue sliders in the settings pane? Those are really easy to use with a tablet or with a mouse -- and even with the keyboard. Thanks go to Justin Noel for the first version of this very cool widget!

If you click on the second tab, you see all the brush presets saved for the current brush engine. You can search, add and remove them. Now all that's left for all of you artists is to start making presets and share them with other Krita users! (Note though that while we hope to keep the 2.2 preset format stable and compatible, Krita 2.3 might bring changes based on your feedback.)

![](https://krita.org/wp-content/uploads/2010/05/krita-2.2-announcement-13.png)  

And check this out: the presets are stored as PNG files with all the information embedded in them, and that means that any file browser will show you the preview right away.

![](https://krita.org/wp-content/uploads/2010/05/krita-2.2-announcement-14.png)  

### Recording

Krita can now record and playback whatever you paint -- and you can even edit your recorded macro.

![](https://krita.org/wp-content/uploads/2010/05/krita-2.2-announcement-15.png)  

### Usability

Instead of the right-click menu, Krita now shows a quick access palette:

![](https://krita.org/wp-content/uploads/2010/05/krita-2.2-announcement-16.png)  

This palette allows you to select your most used brush engines (using presets instead of engines is planned for 2.3), your recently used colors and a color wheel to quickly select a new color.

There are a number of new, useful shortcuts: , and . (comma and dot) make the current brush size larger and smaller. Ctrl-h toggles visibility of the dockers and toolbox. Pressing space or middle-mouse button now pans the canvas. Press shift and drag your mouse cursor to visually resize your brush on canvas.

### And More

There are many more things that are hard to show off in a screenshot: the new image engine, the new file filters, all the other bug fixes, the performance improvements...

It's well worth to explore Krita now! If you haven't tried Krita 2 before, then this is the right time to check it out. Krita 2.3 will be much better, but we will need your input for that! Most Linux distributions will make binary packages available, so install it and start having lots of fun! Show off your art in our [gallery](http://forum.kde.org/viewforum.php?f=138) and share your experiences with us on the [forums, #krita on irc.freenode.net or the](http://forum.kde.org/viewforum.php?f=136) [mailing list](https://mail.kde.org/mailman/listinfo/kimageshop).

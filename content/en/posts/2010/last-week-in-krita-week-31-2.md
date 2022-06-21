---
title: "Last Week in Krita -- week 31"
date: "2010-08-10"
---

The most memorable occasion in the past weekend was also a very joyous one: Cyrille Berger were married in Kalix, Sweden! I am sure that every reader will join me in a round of congratulations and wishes for happiness! Cyrille is one of the pillars of Krita, of course, and Hanna has committed to Krita as well!  

We're nearing the end of the Summer of Code time and are beginning the long, hard slog towards a useful release. Silvio Grosso has once again offered to extend Lukáš Tvrdý's full-time involvement in Krita -- one reason I am very confident about this release! I have started writing for the manual for real, writing reams of text. David Revoy has prepared a big, multi-page pdf showing exactly where he thinks we still have usability issues. Reassuringly, many of his points coincide with Peter Sikking's ideas. And we've begun the process of identifying what needs to be fixed and what will need to be disabled.

I am already excited about the things artists will be able to do with 2.3 -- if you all help us by testing Krita throughout this period.

On that note, I am pleased to announce that there will be a Krita Bug Day (or rather weekend) August 21 and 22. More details will follow, but what we need there is go through our bugs and verify those on as many different systems as possible.

### Blogs and press

[Linux Magazin](http://www.linux-magazin.de/) has published a very nice 1-page article on Krita. Boudewijn is mentioned as co-author, but all he did was deliver screenshots and a fact sheet -- the following choice quote is from the main author "Fur den anspruchsvollen Digital-Kunstler, der seine Werke am Rechner entwirft und bearbeited, bleiben bij Krita fast keine Wunsche offten."!  
  

- [Pentalis: Phong bumpmaps, and using the deform brush to make molten gold](http://pentalis.org/kritablog/?p=225)  
    
- [Lukas Tvrdy: Week 31: Fixing custom and predefined brushes](http://lukast.mediablog.sk/log/?p=313)

### Code

**Adam Celarek** was again busy with his Summer of Code project: the Next Generation Color Selector. David Revoy remarked about it:

> ... this color selector is simply the best color selector for me.  
> I love this tool, configured this way: auto palette from the image on right, color shade on bottom, and last picked color on the very bottom.

Most of Adam's work has gone into the minimal shade selector, adding shortcuts and polishing. Adam also fixed display issues with the canvas rulers that occurred when a selection was active.  

![](https://krita.org/wp-content/uploads/2010/08/colorsel_ng.png)  

**Boudewijn Rempt** finally had most of a Saturday to himself. He first enabled a preview of the integrated brush designer, a one-stop place for selecting the brush engine, configuring the settings for a preset and a preset. Some people like it, but there are still issues with spit and polish there. Also, Boudewijn fixed a memory leak.

**José Luis Vergara** fixed the a bug both in the smudge brush as in the hatching brush: neither respected the selection when painting. At the same time, the code for the smudging brush was cleaned up considerably. Then he went on with his Google Summer of Code project: the impasto effect. Now the phong bump map filter is fast enough to use as an adjustment layer, and there's a gui to configure the filter. Next step -- the impasto effect?

**Lukáš Tvrdý** was in bug-fixing mode this week, mainly focussed on fixing issues when painting with colored brushes as masks, then fixing bugs in the on-canvas brush scaling feature, fixing the scaling of Gimp Image Hose (.gih) brushes -- we use those a lot now, with David Revoy's Chaos and Evolutions brush set being our default. Finally he fixed issues with the brush outline cursor.

**Marc Pegon** finished the warp transformation mode and started designing the free transform user interface, implemented undo/redo for warp transform and prepared the way for two more methods of warping the image on-canvas.

**Sven Langkamp** fixed a very nasty bug: it turned out that when using the pixel selection mode (opposed to the vector selection mode) the rightmost column and bottom-most row of pixels couldn't be selected.

### Envoi

Krita is beginning to look _good_... Give it a try yourself!

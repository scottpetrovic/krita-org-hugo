---
title: "Last Week in Krita -- Week 32 and a bit of 33"
date: "2010-08-20"
---

Today is the final day of the Google Summer of Code period. For Krita, this year's Google Summer of Code has been an amazing success. The ming boggles at the results the students have achieved, especially when you realize that during the Krita sprint we seriously considered not joining this year because we were afraid it would detract from our goal of making Krita 2.3 ready for serious users!

Well, with the multi-threaded canvas updating, canvas rotation, next-generation color selector, transformation tool, hatching brush and phong bumpmap filter, we're getting so close! Now it's time for stabilizing, polishing and.... bug fixing! Here's a screenshot of Krita showing off the canvas rotation and canvas border color:

![](https://krita.org/wp-content/uploads/2010/08/krita_rotation.png)  

### Bug Day

As [Lemma has blogged](http://www.confuego.org/archives/29-BugDay-revival-take-2-Sunday-22nd-August-2010.html) this Sunday is Krita bug day. We have a [set of 21 bugs](https://bugs.kde.org/buglist.cgi?query_format=advanced&short_desc_type=allwordssubstr&short_desc=&product=krita&long_desc_type=substring&long_desc=BUGDAY&bug_file_loc_type=allwordssubstr&bug_file_loc=&keywords_type=allwords&keywords=&bug_status=UNCONFIRMED&bug_status=NEW&bug_status=ASSIGNED&bug_status=REOPENED&emailassigned_to1=1&emailtype1=substring&email1=&emailassigned_to2=1&emailreporter2=1&emailcc2=1&emailtype2=substring&email2=&bugidtype=include&bug_id=&votes=&chfieldfrom=&chfieldto=Now&chfieldvalue=&cmdtype=doit&order=Reuse+same+sort+as+last+time&field0-0-0=noop&type0-0-0=noop&value0-0-0=) that we would like to validate on as many different systems as possible.

The advantage of joining in Bug Day is that it means getting a recently compiled Krita from svn on your system -- and that means you can also play with all the cool stuff that's going to be in 2.3! I'll be around most of today and tomorrow on #krita to help people getting Krita compiled. Start with the [build guide](http://wiki.koffice.org/index.php?title=Building/Building_KOffice)!

### Blogs

- [Pentalis:Krita phong filter GUI linked, thoughts on Impasto Effect](http://pentalis.org/kritablog/?p=239)
- [Marc Pegon: GSoC Conclusion - Screencasts](http://www.kdedevelopers.org/node/4314)
- [Adam Celarek: Krita GSoC: Colour selectors once more](http://celarek.at/2010/08/krita-gsoc-colour-selectors-once-more/)

### Code

**Adam Celarek** added shortcuts to the color selector:

- **S** is now for color Selector
- **C** is now for Common colors
- **H** is now for colour History
- **M** is for Mypaint shade selector
- **N** is for miNimal shade selector

Then he implemented drag and drop for colors, added hsv to the minimal shade selector as well as the ability to create a custom gradient, improved the layout of the color selector, prettified the Mypaint-style color selector by using anti-aliasing -- and then started on a new curve widget. This will be the third curve widget in Krita. Incrementally, we'll be getting there. Adam is now enjoying a well-earned vacation!

**Boudewijn Rempt** improved performance of convolution filters by improving the performance of the calculation of the exact bounds of a layer: in Krita, like in Photoshop, but unlike, Gimp, layers are as big as their contents, they don't have a fixed size. That makes it pretty hard to figure out how big layers, are, exactly, though, and that is often very useful information. Boudewijn also replaced the themable cross-hair cursor with a custom cross-hair cursor. Next step should be making the cross-hair cursor scale with the zoom factor...

**Cyrille Berger** improved the robustness of the new [lcms2](http://www.littlecms.com) based color engine, disabled spellchecking in the text text shape for Krita -- no more red squiggles under your text! -- fixed a regression in saving and polished the color selection mechanism a bit: now Krita remembers which colorspace you used last.

**Dmitry Kazakov** re-implemented canvas mirror and implemented canvas rotation. This really is awesome and so smooth! Use the pan tool to rotate the canvas: if you press shift, a dial will appear in the middle of the screen and you can rotate the canvas around that dial. Click on the dial and the rotation will be reset. There are also keyboard shortcuts:

- **Ctrl+\[** -- rotate left 15deg
- **Ctrl+\]** -- rotate right 15deg
- **Ctrl+'** -- reset canvas position

**José Luis Vergara** polished the gui for the phong bumpmap filter and implemented a number of extensions to the filter to make it much more versatile. The filter is a bit slower now under some circumstances -- though optimizations are being investigated -- but it's still real-time if you use it as a filter mask or filter layer.

**Lukáš Tvrdý** implemented a global curve for pressure mapping, implemented added a configuration option to set the background color of the area around the canvas, following a suggestion by David Revoy, prepared the chalk brush engine for merging with the soft brush engine (which might itself be merged with the autobrush engine at one point), improved the color selection strategy for the freehand tool and improved the separate color picker tool to follow the freehand tool color picker improvements. Lukáš is now on vacation as well.

**Marc Pegon** added similitude and rigid functions to the warp transformation, made sure that if the layer is warped beyond the image borders, the pixels are not cropped off and fixed two bugs in the transform tool, a crash when transforming a flake layer and a bounds error

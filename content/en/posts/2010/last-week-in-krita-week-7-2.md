---
title: "Last Week in Krita -- Week 7"
date: "2010-02-23"
---

Week 7 saw [Lukáš working hard on the performance of Krita's basic method for accessing pixels: the iterators](http://lukast.mediablog.sk/log/?p=194). There were about 75 commits, and the bug count crept up to 104! We were joined on our irc channel and forum by [Project Durian's](http://durian.blender.org/) Ben Dansie. Check out his [sketches and user advice](http://forum.kde.org/viewtopic.php?f=138&t=85891)!

### Code

Adam Celarek finished the first phase of the magnetic selection tool: it works now, though only with Qt 4.6 (which will be the required minimum version for Krita 2.2 anyway). Some user testing of the magnetic selection tool would be appreciated! You can enable compilation by removing the comments in koffice/krita/plugins/tools/selectiontools/CMakeLists.txt.

Cyrille Berger fixed a heap of bugs, helped Lukáš design a new iterator api and finally worked on the exr export filter, making it possible to save "multi-layer" exr files -- multi-layer in exr actually means single-layer-with-lots-of-channels.

Lukáš spent Monday making it possible to paint with ABR brushes; then on Tuesday he [significantly sped up Krita's iterators](http://wiki.koffice.org/index.php?title=Krita/Benchmarking#Horizontal_Iterator) by adding caching. Then he went on to create an experimental iterator with a simplified code structure: benchmarks prove that this iterator is even faster. However, it is not used anywhere in Krita yet -- we would need to investigate where it would be worth porting code to it. At the same time, during the evenings when working on his thesis, Lukáš significantly improved the performance of the sumi-e brush, the result of his first Google Summer of Code project. The particle-based brush engine got some TLC, and now uses correct arithmetic for opacity calculation. Then he went on to add code to control the density of the sumi-e bristles, and added spacing and scaling to the soft brush.

Enkithan created new icons for the local selection masks, and Marc Pegon added them to Krita.

Sven Langkamp ported the duplicate, mypaint-compatible and filter brush engines to the preset architecture and did some work on abr brush loading. He also made it possible to filter the list of available presets to make it easier to find the one you are looking for.

Vera Lukman put the finishing touches to the quick brush and and color selection palette: this feature is "done" for 2.2. For 2.3 we will have to integrate it with the brush presets system.

### Manual

Leonhard Landrock worked on the [Getting Started](http://userbase.kde.org/Krita/Manual/Starting_Krita) chapter of the manual -- that was when we discovered that Krita doesn't impose many limits on the size of the image or the resolution. At least not directly: indirectly you're limited by the memory of your computer, since our current tiles engine doesn't support swap yet. Very nice and thorough work by Leonhard!

### Envoi

This week a large subset of the Krita developers will gather in Deventer for the second Krita sprint. The t-shirts have been ordered and should be ready Friday afternoon, the shower cabin in the bathroom has been repaired and the guest rooms reamed out. Let 'em come!

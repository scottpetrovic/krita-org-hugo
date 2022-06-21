---
title: "Last Week in Krita -- up to week 37 and almost the first 2.3 beta!"
date: "2010-09-15"
---

Hey everyone! Bugsbane filling in here for Boud, this time so hopefully you'll forgive the inevitable errors and omissions... especially if you coded what I omitted! Anyway, caveats aside it's been an \*active\* couple of weeks in Krita-land. Where to even begin...

First up, Krita is now in feature freeze preparing for the big 2.3 release soon. (Artists... start your tablets!) Having put in the new stuff you'll read about below, developers have been shifting gears to making Krita stable and functional by squashing as many bugs as possible, starting with Bugday on the 22'nd last month.

##### Bugday

Krita's Bugday had a small, committed group turn out to triage and try and recreate 21 particularly troublesome bugs that had been hard to recreate before. 14 of them are now resolved one way or the other with many being fixed outright. Many thanks to Lemma and Boud for coordinating as well as all our testers for turning out and helping make 2.3 the best Krita release ever!

### Enhancements:

While we're in feature freeze now though, Krita dev's still managed to squeeze in some last minute goodies for you to enjoy beforehand. For example:

If you're a new user, you'll find getting started with Krita easier now, thanks to **Boud**'s new tutorial image that will open up on Krita's first-run ([revision 1170649](http://websvn.kde.org/trunk/koffice/krita/AUTHORS?revision=1170649&view=markup "See revision 1170649")). Boud also added a soft light and hard light blending mode for your layering and painting pleasure ([revision 1170511](http://websvn.kde.org/trunk/koffice/krita/AUTHORS?revision=1170511&view=markup "See revision 1170511")) as well adding hard-light to Krita's Gimp (.xcf) import ([revision 1170649](http://websvn.kde.org/trunk/koffice/krita/AUTHORS?revision=1170649&view=markup "See revision 1170649")).

Not content with that, he's been refining the main user interface bar for the 2.3 release, incorporating suggestions from pro artist David Reevoy (concept designer for Blender's next movie Sintel). With preparations for 2.3's release coming to a close, we're getting ready for the next chapter with Boud disabling plugins destined for future releases and working more on importing MyPaint brushes. In a future release it should be possible to have them show up as just another Krita preset.

Your community contributions to Krita's fundraiser powered **Lukas** as he sped up painting with predefined brushes by 15%-30% and made the brush outline dynamic so it changes shape with pressure, rotation, angle etc r1168475. He also improved Krita's new Harmony-like brush called the sketch brush as seen in [AnimTim](http://forum.kde.org/memberlist.php?mode=viewprofile&u=29566 "AnimTim's Profile on the Forums")'s painting Tribal Warrior in the [Showcase](showcase "Krita Showcase"). If you want a beautifully organic, hand drawn look to your illustrations, the Sketch Brush is definitely worth trying! Stay tuned for a blog post from Lukas, coming soon. 

Working with Lukas, **Pentalis** introduced a more elegant way of having brush strokes stay within selections where they exist. He also gave Krita's KisPainter code a “full facelift" which he's shy about sharing, but deserves credit for anyway. ;-)

In a smaller, but “close-to-my-artists-heart” commit, **Slangkamp** added the ability to pan the canvas, zoom in and out, with only the middle mouse button / tablet pen. This is similar to Gimp / Inkscape, however without needing to hold Ctrl to zoom (or use the keyboard at all). For me personally, this almost doubles my workflow speed. Give it a try now. Trust me. You'll like it. :)

Speaking of panning, some artists have wished for a way to be able to pan beyond the edge of the canvas. Your wish has now been granted with **Dmitry's** new feature he [blogged](http://dimula73.blogspot.com/2010/09/krita-free-scrolling-and-masks.html) about "vast scrolling". Now any part of the canvas can be moved anywhere. Combined with middle mouse scroll and pan, you now have a very fast, easy navigation workflow.

Last, but not least **CyrilleB** has been busy improving many things with some thorough bug squashing, in areas as diverse as subpixelisation, correcting autobrush positioning, keeping Krita running through missing brushes, it's memory usage controlled and dealing with YCbCr colorspaces.

We're determined to make Krita as stable and free of bugs as possible for 2.3, so we're all grateful for the bugs squashed, including the many others not listed here by the whole team.

### The Wider Krita World

##### Aaron Siego Puts out a Call For the Perfect Natural, Elegant, Krita-Made Wallpaper

In his own words:

"looking at the increasingly impressive Krita showcase page, a pondering occurred to me: \[...\] would it be possible to create an image that would work as a desktop wallpaper using Krita? If so, could we also make a splash screen background that matches it for the log in process that was more elegant than what we have right now?"

Checkout [the thread here](http://forum.kde.org/viewtopic.php?f=137&t=90247 "Aarons call for Krita Wallpapers") to see more details of what's needed, for a chance to see your artwork shipping with KDE workspaces worldwide!

##### Krita is on DeviantArt!

As we get ready to gear up for our first release designed to take Krita out into the wider world of artists we've set up a [group for Krita over at DeviantArt](http://krita-free-art-app.deviantart.com/ "Krita's DeviantArt group"). It's young now, but take a look at the [budding gallery of artwork](http://krita-free-art-app.deviantart.com/favourites/ "Krita's Gallery on DeviantArt") that has used Krita already up and suggest anything that you know has used Krita somewhere. This is a great opportunity to spread free and open source software outside the traditional tech circles, and we need your artistic help!

  

\*Phew!\* While there's actually a \*lot\* more we could write about here, I need to stop somewhere! Even as I've been typing this I see new enhancements happening on IRC faster than I can write about them, so if you really want the full news #krita and [the forums](http://forum.kde.org/krita "The Krita Forums") are the places to be. See you there!

And this is what Krita currently looks like -- very close, but not quite to the final release:

![](https://krita.org/wp-content/uploads/2010/09/krita_girl_in_blossom_by_enrico_guarniere.png)

Image is "Girl in Bloom" By Enrico Guarnieri (Ico-dY), July 10,2010  
Krita file available from the [Krita.org/showcase](http://Krita.org/showcase "Krita showcase")

---
title: "Interview with Lars Pontoppidan"
date: "2017-11-13"
categories: 
  - "artist-interview"
coverImage: "griffon.png"
---

### ![](/images/posts/2017/griffon.png)

### Could you tell us something about yourself?

Yes certainly! I'm Lars Pontoppidan; a 36 year old, self-employed programmer, game developer, musician and artist.

I've been drawing and painting since I could put my pen to the paper - so about 35 years.

I made my first recognizable painting when I was around 3 or 4 - my mom still has it framed at her house.

I've always wanted to end up at some level where I could combine all my skills and hobbies. Somewhere along the way I found out that game development demand a lot of the skills I possess - so 1.5 years ago, I decided to cancel all my contracts with my clients and go for a new path in life as "indie game developer". I've now found out that it's probably the worst time I could ever get into indie game development. The bubble has more or less already burst. There's simply too many game releases for the consumers to cope with at the moment. But hey I've tried worse so it doesn't really bother me - and I get to make art with Krita!

### Do you paint professionally, as a hobby artist, or both?

Both I'd say. I've always been creating things on a hobby level - but have also delivered a lot of designs, logos and custom graphics as self-employed. I like the hobby work the most - as there are no deadlines or rules for when the project is done.

### What genre(s) do you work in?

![](/images/posts/2017/c_front.png)Cartooning, Digital painting, Animation and Video game art. All these (and maybe more) blend in when producing a game. I also like painting dark and gloomy pictures once in a while.

I think I've mostly done cartoon styled work - but with a grain of realism in it. My own little mixture.

I started out with pencil and paper - moved to the Deluxe Paint series, when I got my first Amiga - and ended up with Krita (which is an absolute delight to work with. Thanks to you guys!). I still occasionally do some sketching with pencil and paper - depending on my mood.

### Whose work inspires you most -- who are your role models as an artist?

\* A list too long for me to compile here, of sci-fi fantasy artists. Peter Elson is the first that comes to mind. These artists, in my opinion, lay the very foundation of what's (supposedly) possible with human technology - and currently, the only possibility to get a glimpse of how life might look like other places in the vast universe that surrounds us. It's mind blowing how they come up with all the alien designs they do.

\* Salvador Dalí - It's hard to find the right words for his creations - which, I think, is why his works speak to me.

\* "vergvoktre" He's made some really dark, twisted and creepy creations that somehow get under my skin.

### How and when did you get to try digital painting for the first time?

The very first digital painting program I've ever tried was KoalaPainter for the Commodore 64. I had nothing but a joystick and made, if I recall correctly, a smiley face in black and white.

Thankfully my Amiga 500 came with a copy of Deluxe Paint IV, a two-button mouse and the luxury of a 256+ color palette.

### What makes you choose digital over traditional painting?

The glorious "Undo" buffer. I mean... It's just magic.Especially in the first part of the day (before the first two cups of coffee) where your hand just won't draw perfect circles, nor any straight lines.

### How did you find out about Krita?

I read an article about the Calligra office suite online. It described how Calligra compared to Open Office. I eventually installed it to see how it compared to Open Office and boom there was Krita as part of the package. This was my first encounter - unfortunately it ended up with an uninstall - because of stability issues with the Calligra suite in general.

### What was your first impression?

The first impression was actually really good - unfortunately it ended up a bit in the shadows of the Calligra suite's combined impression. This wasn't so positive after a few segfaults in the different applications. Luckily I tried Krita later when it entered the Qt5 based versions. I haven't looked back since.

### What do you love about Krita?

![](/images/posts/2017/Typical_layer_setup.png)The brush engines and the "Layers" docker.

The brushes, and most of the default settings for them, just feel right. Also the many options to tweak the brushes are really awesome.

The layers docker was actually what gave me the best impression of the program - you had working group layers - and you could give any layer the same names! None of the graphic creation applications I used a few years back had these basic, fundamental features _done right_ (Inkscape and GIMP - I'm looking at you). Krita's layers didn't feel somewhat broken, hacked-on and had no naming scheme limitations. A small thing that has made a big difference to me.

### What do you think needs improvement in Krita? Is there anything that really annoys you?

Uhm... I was going to write 'speed' - but everybody is screaming for more of that already. I know how the developers are doing their best to get more juice.

Some great overall stability would be nice. I've only ever had 2 or 3 crashes with GIMP over a long period of time - the count is a bit higher with Krita - on a shorter time scale.

My biggest feature request would be: Cut'n'paste functionality _through_ multiple layers, that also paste in separate layers. This would greatly improve my workflow. I've always worked with a group layer containing separate layers for outline, color, texture, shadow etc. - on each e.g. movable part in a character rig. So I would really benefit from a (selection based) cut'n'paste that could cut through all the selected layers - and paste all these separate selection+layers elsewhere in the layer tree.

### What sets Krita apart from the other tools that you use?

I find that most of Krita's tools actually do what you expect them to do - without any weird limitations or special cases. Plus the different brushes, brush engines and all the flexibility to tweak them, are real killer features.

The non-destructive masks (Transparency, Filter and Transform) are also on my list of favourite features. I use these layer types a lot when creating game art - to make them blend in better with the game backgrounds.

And maybe the single most important thing: it's free and open source. So I'm quite certain I will be able to open up my old Krita files many years into the future.

... and speaking of the future; I really look forward to getting my hands dirty with the Python scripting API.

### If you had to pick one favourite of all your work done in Krita so far, what would it be, and why?

![](/images/posts/2017/day_night.png)

It would have to be the opening scene of my upcoming 2D game "non". It's using a great variety of Krita's really awesome and powerful features. The scenes in the game features full day and night cycles where all the lighting and shadows change dynamically - this makes it especially hard to get beautiful _painted_ scenes in all the states each scene has between day and night. Krita's tool set makes it easier and quicker for me to test out a specific feature for an object or sprite - before throwing it into the game engine.

The biggest scene I have so far is 10200x4080 pixels - Krita was actually performing decently up to a certain point where I had to break the scene into smaller projects. I'm not blaming Krita for this :-)

### What techniques and brushes did you use in it?

For cartoon styled work I use a Group layer containing: \* background blend (Transparency Mask) \* shadows (Paint layer) \* outlines (Paint layer) \* textures (Group layer) \* solid base color(s) (Paint layer)

For outlines I use the standard Pixel brush 'Ink\_gpen\_10' - it has a really nice sharp edge at small tip sizes. For texturing I mostly use the 'Splatter\_thin' Pixel brush - with both standard and custom brush tips and settings depending on the project at hand. For shadowing I really like the 'Airbrush\_pressure' and 'Airbrush\_linear\_noisy' Pixel brushes. I use a selection mask based on the solid base color layer (Layer name -> Right mouse click -> Select Opaque) - and start shadowing the object.

### Where can people see more of your work?

In my games: [http://games.blackgrain.dk/](http://games.blackgrain.dk/) On my band album covers: [https://barricadecph.bandcamp.com/](https://barricadecph.bandcamp.com/)

![](/images/posts/2017/c_back.png)

### Anything else you'd like to share?

I'd like to thank everyone involved with Krita for making this great open source and free software available to the world. I hope to soon get enough time on my hands to help the project grow.

Take care and be nice to each other.

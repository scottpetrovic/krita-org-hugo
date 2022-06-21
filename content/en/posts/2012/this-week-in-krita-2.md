---
title: "This week in Krita..."
date: "2012-02-16"
---

### Mango!

This week we heard from [David Revoy](http://www.davidrevoy.com) that he's back in Amsterdam to work on the [concept art](http://mango.blender.org/gallery/) for the [Blender Institute's](http://www.blender.org/blenderorg/blender-institute/) latest open movie project, [Mango](http://mango.blender.org). _And_ he's using mostly Krita to produce his artwork! We also heard from [Nicolò Zubbini](http://mango.blender.org/team/) who will give Krita's OpenEXR and HDR support a workout in this project.  This will be plenty exciting for the Krita team, since 16/32 bit floating point channel support hasn't been really tested in any sort of real workflow yet.

![Pink spaceship by david revoy](../images/pink-battle-worn-outside_mango_concept-art_04_sm.png)

 

Blender Foundation | Artwork by David Revoy | CC BY 3.0

So cool... You can get the hi-res version in [Mango's press pack](http://mango.blender.org/production/mango-press-kit/), together with other cool concept art!

### Too long ago...

It's been a really long time since I last gave everyone an update on the state of Krita development -- so let's do that now...

### The long road to victory^W2.4

The Krita team is working really hard on the last things that need to be fixed before we can release Krita 2.4. It's been seven beta releases now! To be fair, that's also because Krita is part of a larger package, and every app needs to be ready to release the whole.

Given the long wait for the release, it's really great to see more and more artists discovering Krita, going to the extreme lengths of compiling it themselves from our source code repositories. Hardly a day goes by without some cool new image showing up on the [forum](http://forum.kde.org/viewforum.php?f=138&sid=b29e95ded4e53c92a260d4692de3900e), or somewhere on the web

### But there are bugs!

We're at under 120 known bugs...That's a lot more than the 42 we had as a goal for the 2.3 release, but then, more users means more reports!

I regularly need most of my Saturday to triage new bugs and check progress on existing bugs and am happy if I can fix one or two myself! So if you want to help out with Krita development, one thing you could do is become the official Krita Bug triager. It's not an easy job, but we can help anyone get started. And it's really important: we try to have all new bugs triaged by the Saturday after they were reported the very latest, and that the Krita team really loves everyone who makes the effort of reporting a bug.

### Libre Graphics Meeting

Some members of the Krita team will try to visit the 2012 edition of the [Libre Graphics Meeting](http://www.libregraphicsmeeting.org), which is being held in Vienna this year. Me, Lukas and Animtim have already signed up! As usual, the LGM needs help from anyone who wants to support free and open source graphics software development and communities. Check out their [pledgie](http://pledgie.com/campaigns/16614) if you want to help! This is the yearly conference that means most for the Krita team!

### And for the future...

The Krita team has been discussing what [we'd like to do for 2.5 already](http://lists.kde.org/?l=kde-kimageshop&m=132765818014567&w=2). We're closely looking at what artists want from Krita, but we're also quite limited in manpower these days -- some of us have left university for their first real, full-time job, gotten married or are now in a bad crunch to finish up at university. But there's plenty of interesting stuff left to work on -- if you read this and think, "hm... wow, I want to work on that" -- contact us!

So, obvious, OpenEXR/HDR support in Krita (which uses [OpenGTL](http://www.opengtl.org)) needs to be improved for Mango. For painters, textured brushes  [(http://www.davidrevoy.com/index.php?article107/textured-brush-in-floss-digtial-painting](http://www.davidrevoy.com/index.php?article107/textured-brush-in-floss-digital-painting) and smooth strokes as in Gimp Painter ([https://bugs.kde.org/show\_bug.cgi?id=281267](https://bugs.kde.org/show_bug.cgi?id=281267)) are essential. The action recorder needs to be extended ([https://bugs.kde.org/show\_bug.cgi?id=245295](https://bugs.kde.org/show_bug.cgi?id=245295)), and we might want to integrate the G'Mic library for a second time ([http://gmic.sourceforge.net/index.shtml](http://gmic.sourceforge.net/index.shtml)).

The mixing brush saga should continue: there's still more to be gained here. We really want to improve the painting assistants -- that could be a cool Summer of Code project! The transform tool should be extended to make it easier to paint patterns in perspective. There is a cool project brewing for the color adjustment filter, which needs extending. And much, much more, like the tablet version of Krita -- Krita Touch Cyrille Berger has started hacking on!. No screenshots yet, but you can [follow the progress for this in our git repository](https://projects.kde.org/projects/calligra/repository/show?rev=krita-touch-cyrille_berger).

### Summer of Code

Yes, it's that time of the year again. If you're a student and you have good coding skills and knowledge of graphics, consider submitting a proposal for Krita. Check out our [current set of ideas,](http://community.kde.org/GSoC/2012/Ideas#Calligra_Krita) or come up with your own!

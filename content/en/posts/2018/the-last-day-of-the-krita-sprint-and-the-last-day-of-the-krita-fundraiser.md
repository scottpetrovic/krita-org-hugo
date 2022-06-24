---
title: "The Last Day of the Krita Sprint and the Last Day of the Krita Fundraiser"
date: "2018-10-14"
categories: 
  - "news"
---

[![](/images/posts/2018/2018-fundraiser-hero2.png)](https://krita.org)

We fully intended to make a post every day to keep everyone posted on what's happening here in sunny Deventer, the Netherlands.

[![](/images/posts/2018/IMG_8849-200x300.jpg)](/images/posts/2018/IMG_8849.jpg)

And that failed because we were just too busy! I'm triaging bugs even as I'm working on this post, too! We are on track to have fixed about a hundred bugs during this sprint. On the other hand, the act of fixing bugs seems to invite people to test, and then to report bugs, so in the past ten days, there were fifty new reports. That all makes for a very hectic sprint indeed!

[![](/images/posts/2018/bugs_fixed-1.png)](/images/posts/2018/bugs_fixed-1.png)

All through the week, we all touched many different parts of Krita, sharing knowledge and making everyone of us more all-round when it comes to Krita's codebase. Remember, [people have been working on this code since 1999](https://phabricator.kde.org/R37:547279396fd1e263242d8f56263ab05aa32ec1ac). Nobody back then expected we'd have millions of users one day!

[![](/images/posts/2018/team.png)](/images/posts/2018/team.png)

At the Krita headquarters, one usually cooks for two or three, cooking for eight was a bit of a challenge, but cook we did, for Wolthera, Irina, Boudewijn, Dmitry, Ivan, Jouni, Emmet and Eoin. Let's go through the days, menu and bugs!

### Saturday: Minestrone

On Saturday, we merged Michael Zhou's Summer of Code work on improving the palette docker and making it possible to save palettes in your .kra project file. Of course, that meant that all through the week we had to fix issues here and there caused by this merge, but that was to be expected. All through the week, using the nightly builds must have been a roller-coaster experience for our testers!

And we got a lot more done, too: Jouni was demonstrating his clone frames and frames cycle feature, Eoin added a global kinetic scrolling feature, where you can pan pretty much every list with the middle-mouse button. That makes Krita much nicer to use on touchscreens.

### Sunday: Pasta with tomato sauce

On Sunday, we really got into our stride. Wolthera updated the user manual with all the new features -- if you haven't [checked out the manual, do so, we're quite proud of it](https://docs.krita.org)! Emmet fixed the color picker tool, which had a bit of trouble showing the correct value for the alpha channel. There were smaller and larger bug fixes, but a very nice new feature was added as well: new contributor Reptorian, after coding a bunch of new blending modes, put his teeth into a larger feature: a symmetric difference mode for the selection tools.

This is not the first time that someone with little or no background in C++ does really useful work for Krita. In fact, it happens all the time, and for this we worked together with Alberto Flores who was working [on his very first patch](https://phabricator.kde.org/D16157). And he did make it!

### Monday: Moussaka

On Monday, we fixed a nasty little bug where the order in which you select layers in the layerbox would influence the order in which layers would be merged. There were fixes to the animation timeline.

The big feature of Monday was making it possible to import SVG files as a vector layer. Originally, and silly enough, an SVG file would be imported as a raster layer when using the layer/import image as layer function.

Dmitry started working on making Krita's canvas support display scaling properly.: this work would go on all through the week.

Jouni started working on fixing the sound stuttering when playing an animation. That patch is ready to land, and when we released on Thursday, it turns out that this was the thing we got most questions about.

And we fixed bugs...

### Tuesday: Honey-braised pork, sesame beans and cabbage in oyster sauce

On Tuesday we did a bunch of bug triaging and assigned bugs to the people present. Then there were crash fixes, python fixes, ui polish... And we also looked into what would be needed to support HDR monitors, but that's going to be a long slog!

### Wednesday: Stuffed bellpeppers

On Wednesday, Dmitry refined the way users can modify and work with selections: now one should hover over the selection border to start moving a selection. And a lot of bugs and crashes were fixed all long day long, but we also started preparing for the release itself, by backporting all the fixes to the 4.1 branch.

### Thursday: Dining out at Da Mario, and a release

This was the day we had to redo the release three times! But we did release in the end, with almost fifty bugs fixed.

But there was also fixing being done!

Eoin fixed a bug in the animation curve editor, fixed bugs in the bristle and smudge brushes. Wolthera fixed a regression in the color selector. Turns out that if you replace a division by two with a multiplication by 0.5, you shouldn't keep dividing it...

Dmitry also pushed the final set of fixes for using display scaling correctly in Krita. That's another very, very long standing bug finally fixed!

And it's not just people at the sprint who are busy! Mehmet Salih Çalışkan submitted two patches, one for the text tool, one for the brush editor, and today his patches were pushed. Anna Medonosva was fixing issues with the artistic color selector.

In the afternoon, we went out for a walk and met the Deventer sheep herd, as well as the shepherd.

[![](/images/posts/2018/IMG_8914.jpg)](/images/posts/2018/IMG_8914.jpg)

That evening, none of us cooked, we went out to Da Mario instead to have dinner together with one of the more local supporters of Krita.

### Friday: Ajam pedis and sambal goreng beans

Emmett fixed [a really hard bug where sometimes when smudging black gets mixed into the color](https://bugs.kde.org/show_bug.cgi?id=394299). We're pretty sure there are more bugs like this in the database, but we'd need some testing done to see which bugs those are. It's one thing that makes the bugs database such a mess: we have lots of duplicates, but often the fact that they're duplicates isn't apparent at all.

Jouni fixed issues with the G'Mic integration, Boudewijn looked into the problem with saving a group layer with a transparency mask to OpenRaster: that needs updating the OpenRaster standard though. But he didn't waste the entire day, he also fixed loading line end markers for vector lines on Windows and macOS. Ivan fixed macOS-specific issues in the animation timeline.

Later in the afternoon we discussed options to reduce the mess in bugzilla a bit by using a helpdesk system and/or an a question/answer type site. Bugzilla really should only contain bugs, not user support type questions!

### Saturday: Runner beans and meatballs with mint sauce

Saturday was our day off. All work and no play and all that sort of thing. We visited a nearby town, called Zwolle. It's a pretty place, a little larger than Deventer, and it has kept one of its town gates, the Sassenpoort. Previously used as the town's archive, it's now and then open to the public, and well worth a visit. Zwolle has been [barbaric enough to close its local history museum because it wasn't turning a profit](https://www.destentor.nl/zwolle/het-doek-is-gevallen-voor-stedelijk-museum-zwolle~aa690500/), but there's still the Fundatie, a modern art museum, which was showing a smallish [exhibition of works by sculptors Giacometti and Chadwick](https://www.museumdefundatie.nl/en/giacometti-chadwick/).

And in the evening we went back to hacking. Jouni is _this_ close to [fixing audio playback for animations](https://phabricator.kde.org/D16067): in fact, it's ready to be merged!

### Sunday: Black pudding with beetroot and stewed pears

And today, while Jouni has already gone back to Finland, we're back at fixing bugs! But this was one loooong sprint, more of a marathon, and we're getting a bit frazzled now. Still, there are more bugs to be fixed!

### The End

Tomorrow, our marathon coders will wend their way homewards. The fundraiser will end, at the very great amount of 25,000 euros (it's actually more, because people have also been donating directly through Krita's bank account, and the website doesn't count that.). And we will be fixing bugs, and work on achieving that polish and stability that makes all the difference!

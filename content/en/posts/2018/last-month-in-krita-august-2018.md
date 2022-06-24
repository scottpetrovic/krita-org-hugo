---
title: "Last Month in Krita: August 2018"
date: "2018-09-07"
categories: 
  - "news"
---

We used to do a weekly development news post... Last Week in Krita. But then we got too busy doing development to maintain that, and that's kind of a pity. Still, we'd like to share what we're doing with you all -- and not just through the [git history](https://github.com/KDE/krita)! So, let's try to revive the tradition...

In August, we started preparing for our next big Fund Raiser. Mid-September to mid-October, we'll be raising funds for the next round of Krita development. The last fund raisers were all about features: this will be all about stability and polish. **Zero Bugs**, while obviously unattainable, is to be the rallying cry! We're moving to a new payment provider, to make it possible to [donate](/support-us/donations/) to Krita with other options than paypal or a direct bank transfer. Credit cards, various national e-payment systems and even bitcoin will become possible. It's up already [on our donation page](/support-us/donations/)!

We've already made a good start on stability and polish by fixing our unittests -- small bits of code that test one or another function of Krita and that we run to see whether new code breaks something. We also fixed almost a hundred bugs. And, of course, the [Google Summer of Code](/item/kritas-2018-google-summer-of-code/) came to an end.

But let's look at some highlights in a bit more detail:

### Polish, polish, polish

After porting Krita to Qt5, we were left with dozens of unittests that didn't work anymore. They wouldn't build, they would hang, they would give the wrong results or even crash. August was almost too warm to really work on anything too complicated, so all we did was fix stuff. Well, apart from all the other work we've been doing, of course...

### Improving Selections

Dmitry, one of our core developers, whose work is funded by your donations, has been working for a couple of weeks on [improving selections](https://phabricator.kde.org/T3920) in Krita. Selections in Krita are a bit different from other applications, since we have both local and global selections, and selections can be visualized with marching ants or as a mask. And a selection can either consist of pixels, or of vector objects. So, he has worked on like:

- Painting on the selection mask in realtime
- Make it possible to have more than one local selection
- Adding opaque, intersect opaque and remove opaque from the global selection
- A selection is automatically created when you select "show global selection".
- Conversions between vector and pixel selections
- Making it possible to modify selections

{{< youtube gWv--Do9L0E >}}

### Rewriting Resource Management

Resources are things you want to use with Krita. Brush tips for instance, or brush presets. Or gradients, or patterns, or workspaces. Some resources come with Krita by default, some you'll create yourself, some you'll want to download. Krita's resource system dates back to the 20th century, or, if you prefer, the previous millennium. It was designed in the days when a 50 pixel brush was **BIG**, and patterns would be 128 x 128 pixels. These days, people want to use 1000 pixel brushes, 5000 pixel patterns and lots of them.

The original design for handling resources doesn't scale any more! And besides, after over twenty years of hack work, it's a mess. Doing a rewrite is [almost always a mistake](https://www.joelonsoftware.com/2000/04/06/things-you-should-never-do-part-i/), but... We're working on rewriting that part of Krita anyway. Boudewijn is making lots of progress, but nothing much that anyone can see, except for [the Phabricator task](https://phabricator.kde.org/T379). It's been something we've been planning and discussing for a long time. All bugs with tagging, adding, removing and changing resources should be fixed in one big bang!

That's the plan at least...  There's still a way to go!

[![](/images/posts/2018/resource_db_explorer-300x145.png)](/images/posts/2018/resource_db_explorer.png)

And then, there were the usual surprises and little extras:

### New and unexpected

A pretty amazing new feature is the gamut mask, created by Anna Medonosova. This includes both editing and applying of the mask to the artistic color selector. See [James Gurney's blog post for some background information](https://gurneyjourney.blogspot.com/2008/01/color-wheel-masking-part-1.html).

[![](/images/posts/2018/gamut-300x300.png)](/images/posts/2018/gamut.png)

There's now also a debug log docker, so Windows users don't have to mess with debug view again:

[![](/images/posts/2018/log-docker-300x300.png)](/images/posts/2018/log-docker.png)(Artwork by [Iza Ka](http://LifeFinalEdited.pl))

And there's more, of course! Reptorian has created a bunch of new blending modes and is now working on a new selection intersection mode. Jouni has been fixing issues to the reference images docker and has implemented [clone frames for animation](https://phabricator.kde.org/T8764)!

---
title: "April Development Update"
date: "2020-04-03"
categories: 
  - "news"
---

With near infinite difficulty we managed to release Krita 4.2.9 in the last week of March... So now it's time to look ahead! All Krita developers work from home anyway, whether they do sponsored work or are volunteers, but it's quite hard to keep focus these days. Several of us are in quarantine, others are in lock-down -- with people in Hong Kong, China, India, Russia, Poland, Germany, the Netherlands, U.S.A, Canada, Mexico and Brazil we live under a wide variety of pandemic responses. The [Libre Graphics Meeting](https://libregraphicsmeeting.org/2020/en/index.html) in Rennes has been moved to 2021, as has the Krita Developers Sprint that was going to happen right after LGM.

But life goes on, and we're on the verge of another edition of Google Summer of Code. Krita has received a bunch of excellent proposals! Let's keep our fingers crossed for our prospective students!

And, of course, a lot is happening in [Krita's repository](https://invent.kde.org/kde/krita)! About two weeks ago we merged the [resource management rewrite branch](https://phabricator.kde.org/T379) into master. Now, let's unpack this in what we've been doing, and what this means... For the past five years, we've been working on rewriting the way Krita handles things like brush presets, brush tip and tags. This turned out to be a huge amount of work, sucking up lots and lots of energy. But in March we felt we could risk merging everything into master so it would get into the development builds.

So we merged... But we all knew that the branch wasn't ready yet. There are bugs, there are things lacking, but it was time to take this step -- now more people can look into the resource handling changes. Of course, this gave an immediate spike in the number of open bugs:

[![](/images/posts/2020/Screenshot_20200402_105349.png)](https://krita.org/wp-content/uploads/2020/04/Screenshot_20200402_105349.png)In general, we're not exactly close to zero bugs... Even though we close more bugs year over year than there are reported, the number keeps climbing. There must be something wrong with my maths...

[![](/images/posts/2020/Screenshot_20200402_105503.png)](https://krita.org/wp-content/uploads/2020/04/Screenshot_20200402_105503.png) Open, new and closed bugs in the past year.

This week we also discussed our roadmap: 4.2.9 will be the last 4.2 release. We'll release 4.3.0 in about two months, but it won't be the release with all the resource work done. What's currently master will be 5.0, and it will be the release where the old text tool will be finally gone. It will have the resource rework, and probably also lots of new features and summer of code work.

But we've been working so hard on fixing bugs, that all of us want a bit of a change, so it's also time to work on fun features.

One of the features we're working on goes under the code-name "RGBA Brushes". Starting with [the work of Peter Schatz](https://invent.kde.org/kde/krita/-/merge_requests/277), Ramon Miranda and Dmitry are creating something rather fun. You can read all about it on [Krita Artists](https://krita-artists.org/t/use-alpha-channel-in-brush-tips-or-add-an-overlay-tip/4147). I'll let Ramon show it!

{{< youtube BMQzJ5n6LPE >}}

Talking of [Krita Artists](https://krita-artists.org/)... This discussion site, set-up and managed by Raghukamath, is getting more and more popular. It's now the first place anyone should go who has a question, who wants to show off their artwork, or who wants to discuss possible new features for Krita.

What else is going on... Emmet and Eoion are working on the [Animation Next Project](https://phabricator.kde.org/T12769) -- this means they are methodically going through all the papercuts, bugs and feature requests for Krita's animation feature with a goal of improving the complete experience of making an animation in Krita.

Ivan is, among other things, working on work-arounds for the sorry state of display drivers on macOS. We would like to get Krita in the Apple Store... But still feel it isn't good enough.

Sharaf is working on getting Krita in the ChromeOS Play store and the fdroid Android store. Krita on Android is pretty stable, thanks to his previous work, and we've seen it work just fine on the Pixel Book Google has lent us -- it was Google who approached us with the idea of getting Krita on their "big screen devices", that is, Chromebooks. Krita on the Play Store will be a free download, but we will ask users for a donation on ChromeOS and Android: we do need to keep development sustainable.

As for a roadmap...  Those, in our experience, never come true. But we do want to have more fun with brushes, improve the assistants, improve the new text tool. There's work to be done on layer styles, even though they are already much better in the master branch than in the stable branch.

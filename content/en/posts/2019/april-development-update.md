---
title: "April Development Update"
date: "2019-04-11"
categories: 
  - "news"
---

It's April already... We're long overdue for a development update, especially since we haven't had a new release for quite some time.

The reason for both those facts is that our maintainer has had some health issues since December that seriously slowed down not just his part of the development work, but also made it really hard to create new releases -- all releases are still prepared by one person, and if that person temporarily loses the use of one arm, things that should happen, don't happen. The arm is back in action, but that wasn't the only issue, and things are still a bit slowed down.

Apart from that, we're making quite good progress towards our next release, which should happen next month.

In the first place, we've got a new full-time developer! Tiar, who is well known in [Krita's Reddit community](https://www.reddit.com/r/krita/), graduated from university just when the increased income from Steam made it possible to hire someone to help out with this year's big goal: bug fixing! Tiar started March 1st, and has already fixed more than a dozen or so tough bugs. Krita now finally has a real Nearest Neighbour scaling method, for instance.

We had an intermezzo in between fixing bugs: the [HDR functionality](/item/krita-4-2-0-the-first-painting-application-to-bring-hdr-support-to-windows/). This was mainly developed by Dmitry, in cooperation with Intel and gives Krita unique possibilities: there is no other application where you can create HDR images and actually see what you're doing.

Since we finished that feature, though, we've been doing nothing but [triaging and fixing bugs](https://bugs.kde.org/component-report.cgi?product=krita).

[![](../images/bugs.png)](https://bugs.kde.org/component-report.cgi?product=krita)

Not that all bugs are our own doing: we updated our builds to use Qt 5.12, the new LTS release of our development platform. And unfortunately, the ride has not been smooth. We've had problems with tablet support, with painting images and with Python support. And more. We now have a host of [patches](https://phabricator.kde.org/source/krita/browse/master/3rdparty/ext_qt/) in Qt's review system, patches we apply to Qt when building our binaries.

These patches are so essential that as soon as a Linux distribution moves to Qt 5.12, their version of Krita is utterly broken, no matter whether it's the last stable release for Linux (4.1.18) or a build from our master branch. If you're using Krita on Linux, you _have_ to use the appimage.

But many bugs are our own fault, of course. It's not possible to develop software and not break things. Sometimes software grows almost organically, to the breaking point. That's the case with Krita's resources system. Resources are things like brushes and gradients. We've always had bugs creating, modifying, saving, deleting resources or tags. So we started a big project to improve the situation last year. It looks like the project won't be finished for 4.2, even though our maintainer already has put in several months of work on it. Our new target for the rewritten resources system is the 4.3 release, which we aim to release in September.

If you want to take a sneak peek at what's coming in 4.2, apart from bug fixes, check out the [draft of the release notes](/krita-4-2-release-notes/).

If you're using Windows or Linux you can use the nightly builds to test and help us find more issues before we release  ( [Windows](https://binary-factory.kde.org/job/Krita_Nightly_Windows_Build/) | [Linux](https://binary-factory.kde.org/job/Krita_Nightly_Appimage_Build/) ). Thanks to Ivan Yossi's work, we also might have nightly builds for macOS soon.

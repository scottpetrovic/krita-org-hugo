---
title: "Krita in 2019 and 2020"
date: "2020-01-14"
categories: 
  - "news"
---

## 2019

Let's have some statistics first! Statistics are fun! (And notoriously unreliable) We started 2019 with about 450 open bugs -- and that's how we ended 2019. That said, we had **1236** new bug reports and closed **1272**. Still, our 2018 fund raiser was all about getting rid of bugs, and that seems to be a tough proposition.

According to openhub, we had **2271** commits from **60** contributors. This excludes translation commits, because those are still done in a subversion repository, apart from Krita.

We had **nine** releases (4.2.0 to 4.2.8) in 2019, slightly less than we'd planned, we'd wanted to have twelve releases. But one of those releases was 4.2.0, which made HDR editing available to artists for the first time; no other application supported that when 4.2.0 was released in May.

We had **four** [Google Summer of Code students](/item/our-2019-google-summer-of-code-students/?utm_source=dlvr.it&utm_medium=twitter), and most of their work has already been merged and will be in Krita 4.3.0: a new magnetic selection tool, the history docker and the [android port](https://binary-factory.kde.org/job/Krita_Nightly_Android_Build/).

Next to fixing bugs, we're work on that 4.3.0 release, but the main reason why 4.3.0 didn't happen in 2019 was because rewriting the core system for loading brushes, gradients and so turns out to be much more work than we had ever thought. We should have approached that much more gradually, but we couldn't figure out how to make that work.

We had **2,346,618** unique downloads from the download page on this website; that excludes downloads from other download sites, downloads from release announcements or downloads from the various stores. At a guess, we'll have topped 3,000,000 downloads in total this year.

We kicked off [**krita-artists.org**](http://krita-artists.org) as our new discussion and support site, and we've already got more than **1000** active users.

We also had the largest [Krita Sprint](/item/krita-2019-sprint/) ever.

Through the donation button on krita.org and the donation page you see after a download, we got **€29,715.20** in donations. We made enough money apart from the donations from the Windows Store and Steam that this year we could hire **three** new full-time developers. And we got a [grant from Epic](/item/krita-receives-epic-megagrant/), too.

In short, 2019 was a year when Krita saw a huge growth, almost scarily so!

If you want to play with what will become Krita 4.3.0, check out the nightly builds! ([Windows](https://binary-factory.kde.org/job/Krita_Nightly_Windows_Build/), [Linux](https://binary-factory.kde.org/job/Krita_Nightly_Appimage_Build/), [macOS](https://binary-factory.kde.org/job/Krita_Nightly_MacOS_Build/))

[![](/images/posts/2020/electrichearts_20190316_kiki_a_sm-2-1024x508.png)](/images/posts/2019/electrichearts_20190316_kiki_a_sm-2.png)

## 2020

Our plans for 2020 are first and foremost to release Krita 4.3.0, with new features, lots of bug fixes, lots of performance improvements and the new resource management system. That's going to take time, unfortunately. It's that we're releasing bug-fix releases that sometimes have smaller fun features all the time, otherwise it would feel [like we're doing something we shouldn't be doing](https://www.joelonsoftware.com/2000/04/06/things-you-should-never-do-part-i/). That is, doing too big a rewrite. We are making progress, though and we're going to have a small hacking sprint in February focused on the resources rewrite.

We'll have our yearly large contributor sprint directly after the [Libre Graphics Meeting](https://libregraphicsmeeting.org) in Rennes, France, hosted by [ActivDesign](https://activdesign.eu/). It's the first time in many years that we'll have a contributor get-together that's not in Deventer!

We've also got lots of ideas for improving our way of working, for performance improvements to the brush engines, new features for the brush engines, workflow improvements (like a search function for the UI).

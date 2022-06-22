---
title: "Krita in 2018 and 2019"
date: "2018-12-24"
categories: 
  - "news"
---

At the end of the year, we looked [back on 2017 and looked forward to 2018](/item/looking-back-looking-forward/), it's getting time to repeat the exercise! On the whole, 2018 was a better year for Krita than 2017. We hit some major milestones!

We **released [Krita 4.0](/item/krita-4-0-0-released/)**, which included Python scripting, the new, but sadly underpowered text tool, switched from ODG to SVG for vector graphics -- and much, much more.

{{< youtube a-CY4hmkg_I >}}

And after that, we released [4.0.1](/item/krita-4-0-1-released/), [4.0.2](/item/krita-4-0-2-released/), [4.0.3](/item/krita-4-0-3-released/), [4.0.4](/item/krita-4-0-4-released/), [4.1.0](/item/krita-4-1-0-released/) (with the [new reference images tool, session management and more](/krita-4-1-release-notes/)), [4.1.1](/item/krita-4-1-1-released/), [4.1.3](/item/krita-4-1.3-released/), [4.1.5](/item/krita-4-1.5-released/) and [4.1.7](/item/krita-4-1.7-released/). That's ten releases in one year, which means we're getting closer to our goal of a release every month. Are we totally satisfied? Not quite... We had also wanted to release 4.2.0 this year, with all the work done by our Google Summer of Code students. Unfortunately, one essential part is still unfinished, and that leads to some extra instability when working with larger images. In the meantime, more and more new code accumulates in the master branch in Git -- we're in danger of forgetting what's in there, so we've [started on the release notes already](/krita-4-2-release-notes/)!

Speaking of [**Google Summer of Code**](https://summerofcode.withgoogle.com/archive/)... We participated through the [KDE](https://www.kde.org) umbrella in 2018. We had three students, who all completed their projects succesfully. All the code has been merged -- true, we still need to do some fixing, but it was a good year.

And in 2019 there will be another edition of the Google Summer of Code. While it's not certain, of course, that KDE will participate again, we've already [put up some ideas for projects students could work on. They are quite challenging, so take a look](https://community.kde.org/GSoC/2019/Ideas)! And if you're a student and are interested, now is the time to get to know our developer community!

[![](/images/posts/2018/2018-fundraiser-hero2.png)](https://krita.org/wp-content/uploads/2018/09/2018-fundraiser-hero2.png)

We also had a [**succesful fundraiser**](/fundraising-2018-campaign/). We didn't use Kickstarter this time, so it was pretty [hard to actually drive traffic to the fundraiser](https://mail.kde.org/pipermail/kde-community/2018q4/004976.html). On the other hand, what with Kickstarter's cut, the actual net result was pretty much the same as with the 2016 fundraiser. We got about seven to eight months of development funded!

[![](/images/posts/2018/busy.png)](https://krita.org/wp-content/uploads/2018/12/busy.png)Our community has grown as well. Krita gets downloaded almost **two million times** a year -- and that's just from our own website. There's the Windows Store, there's the rejuvenated Steam Store, community-driven flatpak, Windows download sites and Linux distributions being more and more up-to-date.

As the Krita core team, we love interacting with our users, but it's honestly getting too much for half a dozen people, who also want to do some coding! So we've got a new [Questions and Answers](https://ask.krita.org) website -- though the idea there was that it would turn into a community of Krita users helping each other, and that hasn't happened yet!

 

So, 2018 was a pretty good year for Krita! What will 2019 bring?

Of course there will be new releases. We're working hard on what will become Krita 4.2. As said above, there's already a lot of cool stuff available in the daily builds, but there are two special projects going on right now:

Working closely together with Intel, we're preparing **support for painting in** [**HDR**](https://phabricator.kde.org/T9256). We're really running ahead of the pack here: this technology is so new that there's barely any hardware that supports it, and the only OS that has some support is Windows 10... (There's preliminary work going on in graphics drivers for Linux/X11 as well.)

But we've got it working, as a proof of concept, and the feel of painting on a wide-gamut, 1000 nits monitor is magical! We want to make sure that the support for HDR visuals becomes part of Qt itself, so other applications can follow. And then, of course, that hardware gets more widespread and OS support improves.

The other big project that ate many, many hours in 2018 and isn't nearly done is the rewriting of the **resources system**. Resources are things like brush tips and presets, patterns and gradients. When KImageShop was started, twenty years ago, disks were small, memory was limited and people thought a 1024x768 pixel image was huge. Patterns and brushes and so on were small, too, and people would keep only a few around.

These days, resources are huge, and people keep lots and lots of them around. Our code for handling resources has grown into a huge ball of knotty twine, kept together with chewing gum. We started designing a new system in 2017, and in 2018 we spent a lot of time on its implementation. That's still ongoing. The new system will be much more memory friendly, reduce startup time and be much more reliable. At least, that's what we're working for!

And, of course, we're still going to spend a good bit of time on fixing bugs, improving performance and doing releases!

And 2019 will mark [the twentieth anniversary of Krita](https://phabricator.kde.org/R511:3e91e954652b9db5c715b71c717b2a58cfe49bcd)!

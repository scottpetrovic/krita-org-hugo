---
title: "The Inside View: How Krita is Developed"
date: "2019-08-02"
categories: 
  - "news"
---

In this post, I want to share with you how we're developing Krita. Of course, the post's title is already nonsense, since there's no "inside" and "outside" when it comes to Krita. Krita is a free software project, and as open as it can be. If you use Krita, report issues, help people who are using Krita, show off your work, well, you're already part of this community that makes life better for everyone who uses Krita.

That said, you might've been using Krita for years, and still being a bit vague on who develops this application, how that's organized, why people are spending time on it and what resources we have for developing Krita.

### Who are the developers

Until [2005](https://en.wikipedia.org/wiki/Google_Summer_of_Code), all Krita development was done by volunteers, in their spare time. That year, Google started the Google Summer of Code program. Then we had students working full-time on Krita for three months; mentored by the existing volunteer team.

For me, Krita maintainer since 2003, there was nothing more satisfying than working on Krita. In contrast with my day jobs, we actually started [releasing](/about/krita-releases-overview/) in 2004!

But it was clear that there was only so much that could be done by a purely volunteer, unsponsored team. Time is money, money buys development time, so since [2009](https://dot.kde.org/2009/12/02/krita-team-seeking-sponsorship-take-krita-next-level), we've tried to sponsor development beyond Google Summer of Code. Some argued that this would kill the volunteer element in the community, but we've never seen a trace of that.

So, these days, there are four people working full-time on Krita. There is Dmitry, since 2012, sponsored by the [Krita Foundation](/about/krita-foundation/) through donations and fund raisers.

Me, Boudewijn, has been funded working on Krita through a combination of donations, special projects for third-party organizations and, since 2017, the income from the Windows Store. I don't do just coding, but pretty much all project management.

Agata and Ivan started working full-time on Krita this year, and are funded through the income from the Steam Store. Agata is well-known as Tiar and has been supporting other Krita users for ages. Ivan has been around in the Krita community for more than ten years, first producing things like shortcut cheat sheets, and completing a Google Summer of Code project successfully in 2018.

This year, there are [four Google Summer of Code students](/item/our-2019-google-summer-of-code-students/?utm_source=dlvr.it&utm_medium=twitter) working on Krita: Sharaf, Tusooa, Kuntal and Alberto.

Any given week, [there are a dozen people committing](https://github.com/KDE/krita/pulse) to Krita, so only a small part of the development community is funded. There are volunteers from many places in the world, some developing just one feature they need and asking for it to be included in Krita, others providing smaller and bigger features, bug fixes and UX improvements.

The group of volunteers is more or less fleeting: people often come and go, but there are people who have been around for a long time. Wolthera manages our [manual](https://docs.krita.org), with help from Raghukamath. Scott maintains the website and helps out with UX design and GUI polish. Anna codes complicated stuff, like the gamut mask feature or more recently, the hardening of the saving code.   Ahabgraybeard helps other users on the [forum](https://forums.kde.org/krita), Timothee designs icons, Maria makes release videos, Irina handles the bi-weekly artist interviews.

Of course, this is who were are... Developers, manual writers, artists. It's also important to realize what there isn't: there isn't a quality assurance team, so we're counting on our users to test the nightlies and the beta releases to find issues. There isn't a user support team, so we're again counting  on our users to help each other out. We don't have customer support or a marketing department. There isn't an office, and there isn't a legal department.

### How's development organized

Our main communication channel is [irc](/irc/), internet relay chat. Yes, it's old-fashioned compared to something like [Matrix](https://webchat.kde.org/), but it works in a timely and dependable way.

We have a weekly meeting at 14:00 CE(S)T every Monday. The meeting doesn't take more than an hour, and we'll discuss various topics and make a report. The reports are archived on [files.kde.org](https://files.kde.org/krita/krita_meeting_docs/).

New code can be put up for review on KDE's gitlab instance, [invent](https://invent.kde.org/kde/krita/merge_requests). Everyone with a KDE identity account can fork Krita on gitlab and create pull requests.

Right now, all full-time developers are working on fixing bugs for Krita 4.3, but volunteers can choose what they work on to a very large extent. The only limitation is that it must fit within Krita's [vision](/item/kritas-updated-vision/).

And next week we'll have our [2019 Krita Sprint](https://community.kde.org/Krita/Sprint2019). We try to get together at least once a year. Not just the Krita contributors, but we also invite artists to our sprints. The only way to learn how people use our application is by watching them work! Sprints are intense, but also lots of fun.

### What are Krita's resources

Financially, we've got several sources of income and support. The donation page you see after downloading Krita brings in about 2000 to 2700 euros a month; the median donation is 10 euros. This goes to the Krita Foundation. The yearly fundraiser brings in between 20,000 and 40,000 euros, and this also goes to the Krita Foundation. The income from the special projects, like the HDR project, is variable, but that, like the income from the Windows Store and the Steam Store, goes to a separate company for tax reasons. All of this is around 6,000 to 10,000 euros a month, and growing.

As you can see, nobody who is working full-time on Krita is getting filthy rich, but it does make it possible for the four full-time developers to work on a project that's really worth it :-)

Our non-financial resources are provided by the wider [KDE community:](https://www.kde.org)

- continuous integration system ([Jenkins](https://build.kde.org/job/Extragear/job/krita/))
- the binary factory that creates nightly builds for [Windows](https://binary-factory.kde.org/job/Krita_Nightly_Windows_Build/), [Linux](https://binary-factory.kde.org/job/Krita_Nightly_Appimage_Build/) and [macOS](https://binary-factory.kde.org/job/Krita_Nightly_MacOS_Build/) and releases for Windows and Linux
- these websites krita.org and our documentation site docs.krita.org
- [mailing list](https://mail.kde.org/pipermail/kimageshop/) (which doesn't see so much usage anymore, but if you go back to 2003, you'll find many interesting discussions)
- the [forum](https://forum.kde.org/viewforum.php?f=136)
- [bug tracker](https://bugs.kde.org/weekly-bug-summary.cgi)

And of course a broad community full of people who are experts on C++, CMake, Qt and community management. And a [big translator community](https://l10n.kde.org/).

### Future development

While the developers and volunteers communicate mostly online, we occasionally get together in person with sprints. We discuss Krita of course, but we also socialize and just have a fun time! Next week we are meeting in the Netherlands for one of these sprints. We are going to be discussing many topics such as the future of Krita as well as taking a side trip to a [local museum](https://openluchtmuseum.nl/en). Many of our developers are artists as well, so there is sure to be a lot of sketch pads and painting flying around.

if this sounds something you might want to be a part of, we are always welcoming new contributors. There are a lot of different areas that we have people volunteering and developing, not just hardcore programmers. We have a [getting involved section](/get-involved/overview/) that outlines some of the areas such as testing and creating brush resources. We also have a lot of documentation on building krita and being involved with our [updated contributor's manual](https://docs.krita.org/en/contributors_manual/community.html#).

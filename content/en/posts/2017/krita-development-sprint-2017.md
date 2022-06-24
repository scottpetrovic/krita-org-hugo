---
title: "Krita Development Sprint 2017"
date: "2017-11-27"
---

With all the turmoil the project experienced in 2017 it looked for a while as if we wouldn't have a face to face meeting this year. But that's not good for a project working on its fourth major release! We knew we really had to sit together, and finally managed to have a smaller than usual, but very productive, sprint in Deventer, the Netherlands from Thursday 23th to Sunday 26th.

Not having been together since [August 2016](/item/2016-krita-sprint-day-1/), we had an agenda stuffed with a enormous backlog of items. And since we've been working on new code for a long time ago, our [bug tracker](https://bugs.kde.org/buglist.cgi?bug_status=UNCONFIRMED&bug_status=CONFIRMED&bug_status=ASSIGNED&bug_status=REOPENED&list_id=1478186&product=krita&query_format=advanced) was also slowly dying from elephantiasis of the database.

Let's do the bug tracker first: we managed to close over 120 bugs! Not every bug that gets closed gets closed with a fix: the problem is that most bug reports are actually help requests from users, and many of the rest are duplicates, or requests for features that are irrelevant for Krita. Still, while triaging the list of open and unconfirmed bug reports, we managed to fix more than a dozen real bugs.

Here's the proof:

[![](/images/posts/2017/bugs_november_sprint-874x1024.png)](/images/posts/2017/bugs_november_sprint.png)Now let's go to the other topics that were [discussed](https://docs.google.com/document/d/1TnrwAqLPfjPO-0VES2FaJQTgxgQNYSX4UiPPNjAE0aE/edit#heading=h.qum3twq1ypdv)...

### Krita 4.0

We finalized the set of features that we want to complete for 4.0, and came up with a schedule. Originally, we wanted to release 4.0 this year, but that's completely impossible...

We still want to add:

- Lazy brush for easy line art colorization (mostly works, needs some testing and bug fixing)
- Stacked brushes, redux. Our first implementation was ready in 2016, but we discarded it and will have to redo the work in a different way
- The new text tool. This is going to be a massive simplication of our original plans... While Boudewijn is still working on making vertical text work in Qt, that's not going to be ready. The tool itself will be simple, easy to use for the main use-cases for Krita.
- There are some missing bits in features that are mostly done, like the Python plugin manager, or finishing up the brush editor redesign.

We are also still facing some problems on some platforms: on Linux, we don't have a working script to package Python and GStreamer in the appimages, and the way we package G'Mic is wrong. On OSX, we don't have a working G'Mic at all, and no support for PDF import. We _do_ need help with that!

The current release schedule looks like this:

- 31st December: Freeze. No new strings, no new features accepted
- January 3rd: first Beta 1 test builds
- January 10th: Krita 4.0 Beta 1
- From now on, weekly development builds, _if_ we have the resources to automate that.
- From now on, bug fixing, bug fixing, bug fixing.
- March 7th: first Krita 4.0 release candidate
- March 14th: Krita 4.0

Right now, the focus is on releasing Krita 4.0, which means that currently no new Krita 3.3.x bug fix releases are planned, even though there are plenty of fixes that can be backported and should be released.

### HDR Support

We've been approached about supporting HDR screens in Krita, which is different from the existing 10 bits/channel screens that Krita has supported on some systems for a long time. But even though we can get access to the hardware, we don't have the time to work on it, and the API's seem to be exclusively Windows-only.

### Get Hot New Stuff

This was a 2017 Google Summer of Code project. We had an almost working implementation, but something changed server-side which means that right now _nothing works_. It turns out to be pretty hard to figure out what's up, and that means it's unlikely Krita 4.0 with have a dialog for download resources from share.krita.org.

### Python API

Over the summer, we have gained a lot of experience with our Python API, also thanks to our Google Summer of Code student Eliakin. We found some places where the current API needs to be expanded and decided to do just that...

### Google Summer of Code

Krita has participated in all editions of Google Summer of Code, and many of the current developers cut their teeth on Krita's codebase during GSOC. We discussed how we could improve our participation, and how we could attract the kind of students who stay around after the project ends. One problem there is the new rules, which specify that a student can participate only twice. In our experience, it is much better for retention if students can participate during their entire university career.

We also decided to raise the bar a bit. We often see candidates who fulfill the current requirement of three patches with three one-liner patches. We'll create a set of tasks that have a rating (1 to 3), and only candidates who have reached at least 6 points of completed tasks will be acceptable. We will also test the candidates on their ability to navigate the codebase by asking them to make a diagram of a particular subsystem.

### Telemetry

The telemetry Summer of Code project has resulted in working code and a working server, but was not far enough to be mergeable to Krita. We are still interested in learning what we can about the way Krita is actually used, though. The student is interested in doing his bacherlor's thesis on this subject, too.

### Contributor Guide

Currently, information about contributing to Krita is scattered all over our website, our manual, the KDE community wiki, the source code repository and external websites. Jouni has created an [outline for a contributor manual](https://docs.google.com/document/d/1xIhmocYvbNf4FsW6k9LuerFi0ojDrTGiYR6UsXYVVFo/edit?ts=5a16ab20) that should be part of our manual website. We've even already started on some parts, like the [bug tracker howto](https://phabricator.kde.org/T7492)!

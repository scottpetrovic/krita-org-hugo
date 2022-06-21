---
title: "June 2019 Krita Development Update"
date: "2019-06-13"
categories: 
  - "news"
---

Time for another development update. [The last one was in April](/item/april-development-update/). We skipped reporting on May, because doing a [release](/item/krita-4-2-0-is-out/) takes a lot of time and effort and concentration! And then we had to do a [bugfix release](/item/krita-4-2-1-released/) in the first week of June; the next release, Krita 4.2.2, will be out by the end of this month.

We're still fixing bugs like crazy, helped by long-standing community member Ivan Yossi, who started fixing bugs full-time in May, too.

But then, we're also getting a crazy number of bug reports. Honesty compels us to say that many of those reports are not so very valuable: there are many people with broken systems who report problems that we cannot solve in Krita, and many people report bugs without telling us anything at all. Hence we [created a manual page on reporting bugs](https://docs.krita.org/en/untranslatable_pages/reporting_bugs.html)! But there are also many helpful bug reports that give us a chance to improve things.

[![](../images/bug_graph.png)](https://krita.org/wp-content/uploads/2019/06/bug_graph.png)

So, how does Krita's development work these days? Well, there are the many people who work on Krita as volunteers, which has always been the mainstay of Krita development. Then there are this year's four Google Summer of Code students, who are all making good progress in their projects.  Krita has participated in every edition of Google Summer of Code since the beginning.

But these days, there are four people working on Krita full-time, thanks to donations, the development fund (which we're working on to revamp a bit and make it more useful to supporters, too), the Windows Store and the Steam Store. None of us is exactly getting rich, but we're getting by. And we're doing stuff that would otherwise be hard to do: projects that take several weeks or months to complete, fixing lots of bugs all over the place, doing janitorial stuff like fixing warnings and so on.

Since this is a development update, we'll just in passing mention all the great work that's been done on this website, [the manual](https://docs.krita.org), and all the work supporting our users on places like the [forum](https://forums.kde.org/krita) or [reddit](https://reddit.com/r/krita).

We're all hanging out on the Krita IRC channel, which is the main place where contributors to Krita come together to discuss whatever needs to be discussed. We have a weekly meeting every Monday from 14:00 to 15:00 CE(S)T -- which means that if you've got a question about Krita, that's probably not the right time to join the channel.

In August, we'll have another [Krita Sprint](https://community.kde.org/Krita/Sprint2019), a big one, with 25 people attending. Half of the people coming to the Sprint are contributors, half are artists and half are both.

So, that's how our community in general works -- but what did we do specifically, since the release? Since 4.2.0, we released 4.2.1 with a bunch of bug fixes already, and the fixing has not abated. Tiar has finished most of the work on making Krita report back any and all failures when saving an image. Dmitry has been fixing some severe issues in the layer stack, GPU canvas and tool handling, Boudewijn has been fixing bugs all over the place and Ivan has been busy with animated brush tips (that is, [Gimp Image Hose](https://gitlab.gnome.org/GNOME/gimp/blob/master/devel-docs/gih.txt) files).

\[caption id="attachment\_9446" align="aligncenter" width="500"\][![](../images/gih.png)](https://krita.org/wp-content/uploads/2019/06/gih.png) Color is random, left and right hands come one after the other, and hand direction  is dependent on drawing direction. Image by Ivan Yossi.\[/caption\]

Not for 4.2.2, but 4.3 (which should be out in September) are two new features already: the palettize filter by [Carl Olsson](https://twitter.com/not_surt/status/1137609273150623744), still work in progress, but that's fine, 4.3 isn't done yet, and the High Pass filter by Miguel Lopez:

\[caption id="attachment\_9441" align="aligncenter" width="1016"\][![](../images/palettize.jpg)](https://krita.org/wp-content/uploads/2019/06/palettize.jpg) Allows interactively painting in truecolour while viewing matched to palette, with optional pattern-based dithering. Image by Carl Schwan\[/caption\]

At the [Libre Graphics Meeting, which was attended by Boudewijn, Wolthera and Tiar](/item/krita-at-the-2019-libre-graphics-meeting/), several projects presented the history of their project with cool graphs. Well, since Krita officially turned twenty on June 8th (which we completely forgot to celebrate, because of all the release work), we thought it might be interesting to analyze the history of Krita's codebase a bit as well.

[![](../images/first_commit.png)](https://krita.org/wp-content/uploads/2019/06/first_commit.png)

Interestingly, this commit isn't even in Krita's git repository anymore: a lot of history was lost over the years. Krita started out as KImageShop in KDE's CVS repository. Then, after KImageShop had been renamed to Krayon and Krita, the CVS repository was converted to Subversion. Then the subversion repository was converted to git, and the git repository [split](https://lwn.net/Articles/419822/) into a [KOffice](https://cgit.kde.org/koffice.git/), a [Calligra](https://cgit.kde.org/calligra.git/) and a [Calligra-History](https://cgit.kde.org/calligra-history.git/) repository.  And then the [Krita repository](https://invent.kde.org/kde/krita) was extracted from the Calligra repository. Still, let's take a look at what we found out.

We used [theseus-of-git](https://github.com/erikbern/git-of-theseus) to analyze the repository. Here's the number of lines of code written by the top twenty-five developers.

[![](../images/25authors.png)](https://krita.org/wp-content/uploads/2019/06/25authors.png)Another interesting graphic shows how long code survives over the years. Just as in the previous graph, there's a huge peak of code that quickly disappears, and that's when KOffice/Calligra was being developed together with Nokia for the Maemo document viewer application. When Krita was separated from Calligra, all that code was no longer necessary.

[![](../images/25cohorts.png)](https://krita.org/wp-content/uploads/2019/06/25cohorts.png)The type of files in the repository is pretty constant: it's .cpp and .h files, meaning, that Krita is and always has beem mostly C++. The funniest thing is maybe the enormous number of lines of code in .xmi files. That's [Umbrello](https://umbrello.kde.org/)'s file format, and it represents UML diagrams of Krita's codebase. Those had to be updated manually, and at one point, we just deleted them because they had gotten useless.

[![](../images/25exts.png)](https://krita.org/wp-content/uploads/2019/06/25exts.png)

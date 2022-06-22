---
title: "Kicking off 2016 -- the first Krita Sprint"
date: "2016-01-25"
---

This weekend, we had our place full of hackers again. The Calligra Text Layout Sprint coincided with the Krita 2016 Kick-Off Sprint. Over the course of the sprint, which started on Wednesday, we had two newcomers to KDE-related hacking sprints, and during the weekend, we had an unusual situation for free software: actual gender parity.

When asked the Calligra people whether their sprint was a success the answer Camilla gave was an unqualified "Ja!". The main topic was sections and columns. There was also a lot of knowledge transfer and fixing of the okular plugin that's part of Calligra. And Jos gave a sneak preview of his Fosdem presentations, not at all hindered by the noise the Krita hackers were making.

As for Krita, we started on Wednesday already, and first discussed cleaning up our source tree. We recently had a patch by a new contributor, who commented that, compared to some other projects he'd hacked our codebase is an exemplar of clarity... But it can and should be improved, we're still having lots of legacy from the calligra days... So we're moving things around to make the structure more logical.

Next was **OpenGL**. Once of the promises of Qt4 was that QPainter would work on an opengl surface. Back in the Krita 1.x days, the Qt3 days, we already had a QPainter and an OpenGL canvas. Both canvases needed separate code for brush outlines, tool helplines and so on. When we ported to Qt4, we unified that code. Painting the image on the canvas was still different for OpenGL and QPainter canvas, but what we call the tool and canvas decorations, that was all unified.

However, the OpenGL QPainter engine has never been really maintained and got stuck in the OpenGL v2 days. Maybe sufficient for some mobile applications, but not for a desktop application like Krita, which needs several OpenGL 3.2 features to function correctly. That wasn't a problem until we decided to make a serious effort of our port to OSX. The OpenGL QPainter engine, being OpenGL v2, can only work in an OpenGL 3.2 context if the compatibility profile is set: it needs all those deprecated things.

Apple decided that nobody would need _that_, and offers only the Core Profile. That sucks. That means the OpenGL QPainter engine is not available on OSX for applications that need V3.2 Core Profile. Worse, Intel's Windows drivers regularly go through a phase where using V3.2 Compatibility Profile causes black screens.

So... We teased out Qt's OpenGL QPainter engine and started trying to port it to OpenGL v3.2. It's supposed to be possible, but it's likely to be extremely tricky. If we got it working, it would be nice if it could become a part of Qt... But that's likely as challenging as writing the code in the first place.

When, the next day, we started discussing OpenGL in the context of the Qt5 and QtQuick 2 port of Krita Sketch, which Friedrich is working on, we sounded like this:

[![krita-sprint-janurary2016](/images/posts/2016/krita-sprint-janurary2016-1-953x1024.png)](https://krita.org/wp-content/uploads/2016/01/krita-sprint-janurary2016-1.png)

(Image by Wolthera)

After that, on Saturday, we started planning the next Kickstarter, which will have as [its main topics Text and Vector](https://forum.kde.org/viewtopic.php?f=137&t=130747&p=350200#p350200). And we even began to look forward to 2017, when we might want to focus on issues around the creation of comics. Here are [the minutes](https://docs.google.com/document/d/1TWhg7xIx4H1aDwvoN9cE6ucRk-pCKVaA3W5Z1tCKC-I/edit#)!

A nice dinner at our favourite Greek restaurant, Kreta, a quiet evening, and on Sunday...

On Sunday we really went through _all_ the registered Wish bugs in bugzilla. There were 316 of them. A whole bunch we closed for now: wonderful ideas, but not going to happen in the next two years, another bunch turned out to be already implemented and the rest we carefully categorized using the following formula:

- WISHGROUP: Pie-in-the-sky: not going to happen, but it would be really cool
- WISHGROUP: Big Projects: needs more definition, maybe two, three months of work
- WISHGROUP: Stretchgoal : up to a couple of weeks or a month of work
- WISHGROUP: Larger Usability Fixes: maybe a week or two weeks of work
- WISHGROUP: Small Usability Fixes: half a day or a day of work
- WISHGROUP: Out of scope: too far from our current core goals to implement
- WISHGROUP: Needs proposal and design: needs discussion among artists to define scope first

And now the library reorganization is in progress. We also fixed a bunch of bugs, so expect new Windows, OSX and Linux Krita 3.0 development builds later this week! And end of this month, the _last_ Krita 2.9 bugfix release!

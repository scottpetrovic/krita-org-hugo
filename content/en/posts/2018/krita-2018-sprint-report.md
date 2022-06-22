---
title: "Krita 2018 Sprint Report"
date: "2018-05-22"
categories: 
  - "news"
---

This weekend, Krita developers and artists from all around the world came to the sleepy provincial town of Deventer to buy cheese -- er, I mean, to discuss all things Krita related and do some good, hard work! After all, [the best cheese shop](http://www.kaashandel-debrink.nl/) in the Netherlands is located in Deventer. As are the Krita Foundation headquarters! We started on Thursday, and today the last people are leaving.

[![](/images/posts/2018/2018-05_Krita-sprint_Deventer-1024x345.jpg)](https://krita.org/wp-content/uploads/2018/05/2018-05_Krita-sprint_Deventer.jpg) Image by David Revoy

Events like these are very important: bringing people together, not just for serious discussions and hacking, but for lunch and dinner and rambling walks makes interaction much easier when we've gone back to our IRC channel, #krita. We didn't have a big sprint in 2017, the last big sprint was in [2016](/item/2016-krita-sprint-day-1/).

So... What did we do? We first had a [long meeting](https://files.kde.org/krita/krita_meeting_docs/Other%20Meetings/2018%20Krita%20Sprint%20Meeting.odt) where we discussed the following topics:

- **2018 Fund Raiser**. We currently receive about €2000 a month in donations and have about eighty development subscribers. This is pretty awesome, and goes a long way towards funding Dmitry's work. But we still want to go back to having a yearly fund raiser! We aim for September. Fund raisers are always a fun and energizing way to get together with our community. However, Kickstarter is out: it's a bit of tired formula. Instead we want to figure out how to make this more of a festival or a celebration. This time the fund raiser won't have feature development as a target, because...
- **This year's focus**: _zarro bugs._ That's what bugzilla used to tell you if your search didn't find a single bug. Over the past couple of years we've implemented a lot of features, ported Krita to Qt5 and in general produced astonishing amounts of code. But not everything is done, and we've got way too many open bug reports, way too many failing unittests, way too many [embarrassing hits in pvs](https://www.viva64.com/en/b/0569/), way too many features that aren't completely done yet -- so our goal for this year is to work on that.
- [**Unfinished business**](https://phabricator.kde.org/T8758): We identified a number of places where we have unfinished business that we need to get back to. We asked the artists present to rank those topics, and this is the result:
    - Boudewijn will work on:
        - [Fix resource management](https://phabricator.kde.org/T379) (https://phabricator.kde.org/T379).
        - Shortcut and canvas input unification and related bugs
        - Improved G'Mic integration
    - Dmitry will work on:
        - Masks and selections
        - Improving the text layout engine, for OpenType support, vertical text, more SVG2 text features.
        - SVG leftovers: support for filters and patterns, winding mode and grouping
        - Layer styles leftovers
    - Jouni will work on animation left-overs:
        - Frame cycles and cloning
        - Transform mask interpolation curves
    - Wolthera will work on:
        - Collecting information about missing scripting API
        - Color grading filters
- **Releases**. We intend to release Krita 4.1.0 June 20th. We also want to continue doing monthly bug-fix releases. We've asked the KDE system administrators whether we can have nightly builds of the stable branch so people can test the bug fix releases before we actually release them. Krita 4.1 will have lots of animation features, animation cache swapping, session management and the reference images tool -- and more!

We also discussed the resource management fixing plan, worked really hard on making the OpenGL canvas work even smoother, especially on macOS, where it currently isn't that smooth, added ffmpeg to the Windows installer, fixed translation issues, improved autosave reliability, fixed animation related bugs and implemented support for a cross-channel curves filter for color grading. And at the same time, people who weren't present worked on improving OpenEXR file loading (it's multi-threaded now, among other things), fixed issues with the color picker and made that code simpler and added even more improvements to the animation timeline!

And that's not all, because Wolthera, Timothee and Raghukamath also finished porting our manual to Sphinx, so we can generate off-line documentation and support translations of the manual. The manual is over 1000 pages long!

There were three people who hadn't attended a sprint before, artist Raghukamath, ace windows developer Alwin Wong and Valeriy Malov, the maintainer of the KDE Plasma desktop tablet settings utility, who improved support for cintiq-like devices during the weekend.

And of course, there was time for walks, buying cheese, having lunch at our regular place, [De Rode Kater](http://www.derodekater.nu/), and on Sunday the sun even started shining! And now back to coding!

[![](/images/posts/2018/rode_kater-1024x529.jpg)](https://krita.org/wp-content/uploads/2018/05/rode_kater.jpg) Image by David Revoy.

The 2018 Krita sprint was sponsored by KDE e.V. (travel) and the Krita Foundation (accommodation and food).

---
title: "Roadmap"
date: "2018-05-24"
type: "simple-page"
---

Krita has come a long way since it was started -- as KImageShop, the KDE Linux Desktop answer to Photoshop, or GIMP, depending on who you ask. Until [2010,](https://dot.kde.org/2010/03/15/second-krita-sprint-ends-tea) Krita's development roadmap was basically, "do whatever Photoshop does, do whatever Gimp does, don't neglect what Cinepaint offers." Well, that's an exaggeration, of course. In 2010, the Krita community sat down together and defined its vision: Krita was going to be _the_ application for people who wanted to create images from scratch. Photo bashing was banished to the side-lines, only important when it comes to matte painting.

Fair enough! [Two years later](http://www.davidrevoy.com/article114/krita-project-an-old-challenge-won-2-4-very-soon), Krita was becoming a really good painting application. Since 2012, we've gone from strength to strength, focusing on the features, workflow, performance and compatibility that's needed to make it possible to use Krita in a professional setting, while never forgetting the people who want to just paint and sketch for fun.

We always knew what we wanted to achieve, and we have, in a very real way, always engaged with our community to make sure we knew what our users wanted us to achieve. What we never did was write down a high-level overview of where we would like to get with Krita this year, next year, the year after.

Of course, real life has often interfered: KO GmbH went broke for lack of customers, and KO GmbH maintained Krita on Steam. The Krita maintainer had to take second day jobs to finance work on Krita, and broke down. Shit happens, and sometimes it seems that the shit always drops in the same place. But that never really interfered with our focus, or our plans. We just never wrote those down. Until now...

So, here comes: where we want Krita to go, now, and next year and the year after.

### 2016

I know, 2016 has gone and has been buried. But for 2016, we planned to do the last Krita 2.9 releases and the first Krita 3.x releases. We intended to publish the first release with animation support, and we did, with Krita 3.0. Which was also the port to a new version of our development platform, and that sort of thing is _huge_. Let's hope Qt6 is still far away!

We also wanted to go back to the monthly releases we had with Krita 2.9, but failed at that, because of personal circumstances: the lesson from this should be that it shouldn't be the Krita maintainer who makes all binary releases and all binary builds for all platforms.

We also released most of the features for the three kickstarters we've run.

We also released the 2016 Krita Art Book, which however sold very badly, leaving the Krita Foundation with quite a big loss. It was a big success from the point of getting interested artists to contribute, though!

### 2017

This is the 19th year that Krita has been in development. 2017 was another year with some serious setbacks. We lost a lot of time and energy on a tax audit that also had serious repercussions for our financial situation. That's to say, it cost us a third of our yearly income. Our plans for this year were, and are:

- Finish the remaining kickstarter-funded features still open:
    - lazy brush
    - stacked brushes
    - palette manager
    - reference images docker or tool
    - svg vector layers and vector tools,
    - text tool,
    - python scripting
    - svg import/export
- Release Krita 4.0 with Python scripting, SVG support and improved Text tool.
- Release plenty of Krita 3.x releases with bug fixes and new features.
- Release a Pepper and Carrot comic book, as an open culture project.
- Do another fund raiser to fund work to be done in 2018.
- Work on improving multi-core performance for use with Intel and AMD's new cpu's: especially painting, rendering animation and saving
- Restore touch painting
- Restore some form of touch-optimized user interface
- Investigate ports to other platforms such as Android, iOS, ChromeOS or NaCli.
- Implement saving in the background of the application: i.e., no pauses while saving.

Of course, the "planned" work only is part of what is being done in any given year. In 2017, we also got some awesome unplanned work done by people who just want to work on Krita and make it better: Jospin, Eugene, Allan -- making it possible to do calculations in numerical entry fields, improved histograms and a smart patch tool, and a much improved airbrush engine. And the topics of the Google Summer of Code projects fall outside the roadmap, too.

The roadmap is just a general thing, what do we feel is the most important thing to move forward, in a given year.

Well, from 2014 onward, also because of the kickstarter campaigns, we really have driven Krita towards acquiring important features that were missing, that people couldn't work with. There are still features we feel Krita needs -- better G'Mic integration, for instance, improved warnings when saving to any lossy file file format, saving without blocking the UI. All of those are worked on or are done in the current 4.0 pre-alpha development version.

**Our goal for 2017 is: finish up all currently planned features and release Krita 4.0**

### 2018

For 2018, we really feel that -- well, we're torn. We've done a ton of work on performance, and in 2017, we'll also be spending some months on improving the use of multiple cores in Krita, but, honestly, if you suffer from "lag", right now, it's either because of a local misconfiguration/system problem or because you're using brushes with too narrow spacing on too limited a machine. For all normal purposes, performance is fine.

Platform stuff? We can probably postpone worrying about Wayland on Linux for another year.

- We will spend more time on macOS. Even though Apple's support for the technologies Krita needs, like OpenGL, sucks.

What really is needed in 2018 is focus on

- polish
- stability

We have spent three years now adding cool new features to Krita. We also fixed thousands of bugs, but still. After we release Krita 4.0 with SVG vector support and a new and improved text tool, and scripting, it's going to be time to go deep, and use all available tools to find deep-down bugs, on all platforms. We will also want to polish the existing features: both the workflow as well as the inevitable bugs..

We worry that this might be a tough sell: we will need a serious amount of money to fund at least two full-time developers (at the princely wages of 16 euros an hour) to work on this. There won't be new features -- well, we don't plan really big features. But this consolidation is important!

**Our goal for 2018 is: as close to 0 bugs as possible.**

### 2019

It is really time to do some more fun stuff with brush engines. Of course, last year, Dmitry coded up, in his spare time, the Quick Brush. That makes filling an area really fast. But it's time to step outside the box, do fun stuff we haven't really been doing since Lukáš spent a year on brush engines. There's so much fun to be had!

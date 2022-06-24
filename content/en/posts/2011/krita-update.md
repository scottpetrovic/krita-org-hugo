---
title: "Krita Update!"
date: "2011-02-02"
---

Calligra moved to git december 12, 2010. We're in February now, and since then there have been 2222 commits -- not counting various branch merges. There are now 37 active feature branches. Not all of that work is for Krita, but in the onslaught it's getting difficult to actually keep track of all the work!

Lukáš Tvrdý has taken over the job of planning the next Krita sprint from me -- I was just too overloaded to actually do anything. With the team growing, I'm sure this sprint will rock as much as the previous one. Just don't forget the [t-shirt design effort](http://forum.kde.org/viewtopic.php?f=137&t=92453)!

Kubuntiac a.k.a. Bugsbane, webmaster of krita.org is busy working on a [feature overview of Krita.](http://community.kde.org/Krita/v2.3CompleteFeatureList) We need screenshots to show off!  

There's one lovely design by Animtim already, featuring a squirrel. During GCI, Heroid told us in #krita that "kirta" is Albanian for squirrel and asked us what we thought of a painting squirrel as a Krita mascot, the whole team rather fancied the idea.

New Krita user Rachepatty showed [this strong self portrait in the forum gallery](http://forum.kde.org/viewtopic.php?f=138&t=92885):

![](/images/posts/2011/kritaselfportrait1s.jpg)  

### LGM

KDE e.V. has accepted the proposal to send Lukáš, me and Animtim to [LGM](http://www.libregraphicsmeeting.org). Animtim will hold a workshop centered around drawing comics using Krita. Lukáš intends to present the state of the art in Krita, while I want to man a booth with one or computers running the latest Krita, introducing everyone who's interested to Krita in the proposed LGM lab area.

### Code

Not content with fixing bugs, for instance in the experimental paintop and the mirroring feature beloved by Animtim, Deevad and other artists, **Lukáš** (who is now also working profesionally on Calligra for Ixonos) has been having a lot of fun exerimenting with mirroring, in his multihand branch. For now, there is hardcoded symetry mode with the axis point in center with six brushes. Lots of fun to be had!

![](/images/posts/2011/krita_symmetry.jpg)  

**Cyrille Berger** has started work on making it possible to have multiple inputs for every brush preset parameter -- like having both "pressure" and "random" (still called fuzzy, I think) influence the size or opacity of your brush footprint. He improved recording, in repsonse to queries by a user on the forum and made it possible to use gradients or patterns as a color source for painting. Krita 2.3 already feels old now...

**Boudewijn Rempt** has mostly worked on fixing bugs for Krita 2.3.x -- improving memory handling and backporting fixes from git.

**Silvio Heinrich** has been working on implementing new blending modes. Look at this before and after screenshot (the first is with regular Krita, the second with his new blending modes enabled).

before...  

![](/images/posts/2011/composite_modes_before.jpg)

and after...

![](/images/posts/2011/composite_modes_after.jpg)  

(his own artwork, by the way!)  

Silvio has also worked on improving the canvas rotation, mirror and zoom, and on improving the smudge brush.

**Sven Langkamp** has been chipping away at user interaction niggles, imprving the toolbox, moving the mirror options to the brushes toolbar, fixing shortcuts for tools and lots more bugs. And then for kicks and giggles added a channels docker and a basic workspace manager!

**Geoffry** **Song** has improved the assistants -- freely placable guides on the canvas that make painting along lines and shapes much easier -- beyond all recognition.

### Conclusion

While there are some regressions -- and we're on top of those -- and some severe bugs have been discovered after the 2.3 release, Krita really seems to fulfil its promise now; it's really quite stable under most circumstances, the performance is good and the features and improvements keep coming in. So get out your wacom and start painting. We need new entries in the showcase and the forum gallery!

---
title: "Last week in Krita -- week 21"
date: "2010-06-01"
---

### Intro

First of all, our future plans: when Lukáš is done with his exams, he will return for some more months of full-time hacking. It will be more than originally planned, which is made possible by a very generous donation by Silvio Grosso. Silvio's donation, in fact, is so generous that it will be possible to also have the Krita 2.3 manual professionally edited from rough drafts!  
  

### Coding  

Last week, Dmitry and Adam started coding on their Google Summer of Code projects. And Pentalis is starting to write code as we write. Hit by the unfortunate tendency of French universities to disregard any alignment to Google's idea of when the summer starts, Marc Pegon still has to finish his last assignment before he can really start. Cyrille was to busy with, on the one hand, playing with the latest addition to his household: a puppy dog (I wonder what his cat thinks of this competition for the cosy spot in Cyrille's arms), and on the other hand with porting OpenGTL to LLVM 2.7. More on OpenGTL later. Boudewijn picked up work on the PSD import filter. Sven and Vera have been fixing bugs. But we're not yet at the activity level we had in February: hopefully we will surpass that soon when the students get up to speed!

As for bugs, we are still under sixty; and then there are 110 wishes in [bugzilla](http://www.bugs.kde.org). Wishes are a difficult thing. We really like to hear from users, and many wishes are valid. Some don't fit in the vision, and I really should prune bugzilla from wishes that don't fit. On the other hand, we also have a roadmap with an action plan and everything, created by carefully looking into what users tell us they need, what we perceive as useful functionality looking at the way our target users use other applications and finally things that appeal to us -- and those seldom map 1:1 to wishes in bugzilla.  

### Woo-hoo!  

The big news, of course, for last week was the release of [Krita 2.2](http://krita.org/component/content/article/9-krita-updates/45-krita-22-released). This release is the first that I'd say an artist (a tech-savvy artist...) can install and start experimenting with. We're not hyping this release: it's a good piece of reasonably solid work that shows great improvement over 2.1, but it still has too many rough edges. In particular, the integration of the vector/text tools is quite bad and the lack of a "default" button in the brush settings dialog hurts usability. And I am sure that there are some serious bugs in there that we haven't found. And I _do_ hope that anyone testing Krita 2.2 who encounters a bug will report it! There's a wonderful report bug option in the help menu, and the crash window (which, fingers crossed, you won't see...) can send us all the relevant information with a few clicks. Make sure to also install the _debug_ packages if your distribution offers them, that will help us a lot! On to 2.3 now!  

### Libre Graphics Meeting  

This weekend, Lukáš and Boudewijn were at the [Libre Graphics Meeting](http://www.libregraphicsmeeting.org). Lukáš presented his brush engines: you will find a video recording of his presentation at [River Valley TV](http://river-valley.tv/conferences/lgm-2010), as soon as Kaveh and crew are done editing. It'll be well-worth viewing, for people who want to simply use Lukáš' brush engines, since Lukáš gave a lot of good information, but also for the wonderful artwork Lukáš showed. Lukáš' thesis on Krita brush engines, by the way, received a well-deserved full marks. Now Lukáš just has to do his state exams and then he's free to get back to full-time Krita hacking! Libre Graphics Meeting is a wonderful place to meet people. Having Gimp's Brush Dynamics Guru Alexia Death and Krita's Brush Engine Guru Lukáš Tvrdý in the same place was great. We also managed to have a useful OpenRaster bof session and a session with Peter Sikking about the interaction design for the brush settings popups. Read a more extensive report at [valdyas.org](http://www.valdyas.org/fading/index.cgi/urlaub/lgm2010.html).  

### OpenGTL  

Finally, [OpenGTL](http://opengtl.org/). Cyrille has been really busy this week making OpenGTL compatible with LLVM 2.7. OpenGTL is a graphics transformation language library: you can write graphics algorithms in an optimized language (OpenCTL or OpenShiva). The code you write gets compiled (which is where llvm comes in) and then is executed in an optimized way. There are bindings for gegl, and it's used extensively in Krita. OpenCTL is compatible with AmpasCTL (which isn't GPL compatible) and OpenShiva as inspired by Adobe's PixelBender language.

Despite being the work of one (incredibly productive) person, OpenGTL is quite mature and stable and packaged by many Linux distributions, like Fedora, \*buntu and Mandriva, and work is being done to package it for Debian. It's still an optional dependency of Krita, but it's really important since without OpenGTL, no floating-point colorspaces, no OpenEXR, no OpenShiva filters. If you're interested in graphics programming and haven't played with OpenGTL yet, you owe it to yourself to check it out.

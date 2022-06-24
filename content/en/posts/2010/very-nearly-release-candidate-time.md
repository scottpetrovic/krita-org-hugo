---
title: "Very Nearly Release Candidate Time!"
date: "2010-12-01"
---

Towards the First Release Candidate (inches at a time)

You might be feeling that we're twiddling our thumbs in the Krita community -- but nothing could be less true! The last bugs to fix, the last tests to fix before a release (we don't have any unittest failures anymore!), especially an important release like tend to be tricky and time-consuming. Of course, there are also real-life issues that make people busier than usual. Work, a new job, the renaming of the KOffice project, school and university -- all that stuff can't be ignored forever.

Still, it's time for an update.

Next week we hope to release the first release candidate of Krita 2.3. This is the big one, the one that _you_ need to test. Because if nobody tests it, nobody will find the last few bugs and we will release another abst&uumlrzfreudig Krita. I would prefer a hundred bugs found that make us postpone the release to January to a release on time, with a hundred bugs found once Krita appears in distribution's repositories.

And _right now_ we need people to help triage the crash bugs using Krita from subeversion. There are a number of open crash bugs that we cannot reproduce ourselves; and that makes fixing real hard. If other people can reproduce, we might learn more about the circumstances those crashes occur.

### Krita on Meego

Following hot on the heels of FreOffice and KOffice on MeeGo, I made it possible to compile Krita on MeeGo, using the mobile profile of the KDE libraries. Kevin Ottens did most of the work on that profile, with me and Marijn Kruisselbrink helping. Marijn then did the packaging using the MeeGo OBS build system. All that was left to do was to remove all deprecated KDE code from Krita and run!

I have a WeTab at home, which is a fun little device. The hardware looks pretty cool, and after a series of updates the software isn't half bad either. It's fun to finger paint, but frankly, without a pressure-sensitive stylus a tablet is never going to be a great platform for art.

![](/images/posts/2010/wetab_krita.jpg)  

And for keyboard-less tablet usage, Krita's user interface needs a bit of tweaking, to say the least!

### Google Code-In

Krita is part of Google's Code-In program. It's a busy time for our project, so we probably could be more active in mentoring and creating tasks. But there are some very nice results already and I'm very impressed by the people joining us on #krita.

**Matus Talcik** had the first version of the history docker done _before_ Google Code-In actually had started! He's now working on refining it, to show snapshots for every history step in the docker.

**Salma Sultana** has prepared a really nice screencast about Krita 2.3:

Other people are hacking on VBR brush support and other items. What we need, though, is more mentors with more spare time -- and someone to go through our bugs and wishes on bugs.kde.org and select suitable tasks for students.

### Code

No exciting new features, of course! Everyone has been trying to fix the last bugs and unittests that prevent us from delivering a release.

**William Steidtmann** has been fixing bugs in the histogram code; with that done, he's now focussing on fixing the filters that show histograms.

**Boudewijn Rempt** has been replacing deprecated calls to KDE library classes and removing warnings.

**Francisco Fernandes** has started hacking on Krita -- his first patch fixed the usage of the Delete key. It now always clears the selection, no matter the layer type. See his [blog](http://kdepi.wordpress.com/2010/11/25/krita-patch-removing-pixels-and-shapes-with-clear/) for details! Welcome Francisco!

**Dmitry Kazakov** fixed loading, saving and recalculation of clone layers. He also fixed handling the various grids and the grid tool and the convolution code.

**Cyrille Berger** fixed several unittests. He also squashed a very nasty bug where dolphin, plasma or even konsole would hang when starting krita, for instance by clicking on a jpeg image. Cyrille improved the performance of the (ancient) raindrops filter enormously.

**Lukas Tvrdy** fixed the jpeg unittest and several issues in the autobrush unittest.

**Sven Langkamp** cleaned up the paintop settings selection list and fixed a crash in the shape selection. And that fixed another unittest.

And there were many, many more fixes -- too many to enumerate here. Go, update your checkout and test, test, test!

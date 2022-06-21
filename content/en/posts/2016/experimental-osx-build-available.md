---
title: "Experimental OSX Build Available"
date: "2016-09-07"
---

Over the summer, Google Summer of Code student [Julian Thijssen, aka Nimmy,](http://kritadev.blogspot.nl/) has been working hard on making Krita and Qt5 work properly with OpenGL 3.0 Core Profile. The reason for that is that you cannot use OpenGL 3.0 Compatibility profile on some systems, notably OSX systems, and Krita needs 3.0 functionality.

This meant work had to be done to remove all legacay OpenGL code from Qt's OpenGL painting backend. (It turned out that someone had tried to do that before, and failed, but there were confusing code remnants all over the place.).

That work is now done and submitted to the Qt Project: [https://codereview.qt-project.org/#/c/166202/.](https://codereview.qt-project.org/#/c/166202/)

And there was some work modernizing krita as well, and that work is ready to be merged to the main branch and will be in the next release.

_But_ it needs testing first! And for that, we made a special disk image for our OSX users. And we've opened a forum topic where you can first discuss your experience with that disk image before reporting bugs to bugzilla.

Forum: [https://forum.kde.org/viewtopic.php?f=137&t=135853](https://forum.kde.org/viewtopic.php?f=137&t=135853)

**UPDATE: this is a new build which includes all of 3.0.1 and a fix for the broken HUD palette**

Disk image: [http://files.kde.org/krita/3/osx/devbuilds/krita-3.0.1-nimmy2.dmg](http://files.kde.org/krita/3/osx/devbuilds/krita-3.0.1-nimmy2.dmg)

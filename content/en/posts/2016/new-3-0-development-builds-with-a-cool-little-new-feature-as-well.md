---
title: "New 3.0 development builds! (With a cool little new feature as well)"
date: "2016-05-13"
---

Our [kickstarter campaign](http://www.krita.org/2016kickstarter) has been running four days now, and we're only 2000 euros short of being at 50% funded! Of course it's Kickstarter, so it's 100% or nothing, so we've still got work to do!

In the meantime, Dmitry published an [article on Geektimes](https://geektimes.ru/post/275530/#comment_9247098) and one of the comments had a tantalizing suggestion about locking the brush angles that when Wolthera, David Revoy and Raghukamath, resident artists on the Krita chat channel, saw the mockup of, they all cried, we want that!

Since we could implement it without adding new strings, Dmitry took half a day off from bug fixing and added it! And David Revoy let himself be inspired by Cezanna and produced this introduction video:

{{< youtube bbL7qeVAaC8 >}}

And then, among other things, we fixed the application icon on Windows, fixed issues with translations on Windows, fixed issues with the color picker, finished the [Spriter scml export](https://brashmonkey.com/) plugin, worked around some bugs in Qt that made popups and dialogs show on the wrong monitor, made sure author and title info gets saved to PNG images, fixed display artefacts when using Instant Preview, fixed the direction of the fade, distance and time brush engine sensors, fixed reading the random offset parameter in brush engines, improved custom shortcut handling and fixed some crashes. Oh, and we fixed the [Krita Lime repository builds for Ubuntu 16.04](https://launchpad.net/~dimula73/+archive/ubuntu/krita), so you can replace the ancient 2.9.7 build Ubuntu provides with a shiny 2.9.11

Krita 3.0 is getting stabler all the time; a new beta will be released next week, but we feel it's good enough that we've added Bleeding Edge download links to the [download page](http://krita.org/download), too! For your convenience, here are the links to the latest builds:

Windows Shell Extension package by Alvin Wong. Just install it and Windows Explorer will start showing preview and meta information for Krita files. (Disregard any warnings by virus checkers, because this package is built with the NSIS installer maker, some virus checkers always think it's infected, it's not.)

- Installation package: [kritashellex_1.1.0.1_setup.exe](http://files.kde.org/krita/3/windows/kritashellex_1.1.0.1_setup.exe)

**Windows:** Unzip and run the bin/krita.exe executable!

- Zip archive: [krita-3.0-Beta-master-d330a4a-x64.zip (64 bits)](http://files.kde.org/krita/3/windows/devbuilds/krita-3.0-Beta-master-d330a4a-x64.zip)
- Zip archive: [krita-3.0-Beta-master-d330a4a-x86.zip (32 bits)](http://files.kde.org/krita/3/windows/devbuilds/krita-3.0-Beta-master-d330a4a-x86.zip)

**The OSX disk image** still has the known issue that if OpenGL is enabled, the brush outline cursor, grids, guides and so on are not visible. We’re working on that, but don’t expect to have rewritten the canvas before 3.0 will be released.

- Disk Image: [http://files.kde.org/krita/3/osx/devbuilds/krita3-beta1-ad04a1c.dmg](http://files.kde.org/krita/3/osx/devbuilds/krita3-beta1-ad04a1c.dmg)

**The Linux appimage:**After downloading, make the appimage executable and run it. No installation is needed. For CentOS 6 and Ubuntu 12.04, a separate appimage is provided with g'mic built without OpenMP (which makes it much slower)

- AppImage [krita-3.0-Beta-master-562442e-x86_64.appimage](http://files.kde.org/krita/3/linux/devbuilds/krita-3.0-Beta-master-562442e-x86_64.appimage) for modern distributions
- AppImage [krita-3.0-Beta-master-562442e-no-openmp-x86_64.appimage](http://files.kde.org/krita/3/linux/devbuilds/krita-3.0-Beta-master-562442e-no-openmp-x86_64.appimage) for ancient distributions

(As usual, you can use these builds without affecting your 2.9 installation.)

Let's finish up with [cute Kiki!](https://twitter.com/ramskullsart/status/730023741711777792/photo/1)

[![kiki](/images/posts/2016/kiki-782x1024.jpg)](/images/posts/2016/kiki.jpg)

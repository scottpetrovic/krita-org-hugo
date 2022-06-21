---
title: "Krita 3.0 BETA builds out!"
date: "2016-04-27"
---

We have spent the last 20 days making over 80 fixes in Krita since the last Alpha build. We have decided it is time to enter the Beta phase! Furthermore, we've also spent time on improving our [Windows builds](/posts/new-krita-3-0-windows-builds/).  This should fix all the scary G'Mic crashes on Windows.

### Notable Fixes

- G'Mic is fixed so that it uses OpenMP for multi-threading on Linux and Windows! This is a big performance increase from Krita 2.9 which was single-threaded. G'Mic probably is still _broken_ on OSX: no need to report that.
- Mask updating problems have been tackled rigorously!
- So have transform masks and transform bugs!
- Scary saving and loading bugs have been fixed. Remember, if you ever having a saving/loading bug with Krita, come to us immediately!
- The clone and tangent tilt brushes have fixes with crashing and behavior!
- Tons of little UI fixes with theme colors and consistency.
- Several fixes for the shortcuts. They should now be saved and loaded properly.
- Tablet fixes for dealing with animation. This makes duplicating frames easier, as well as using several tools faster.
- Several fixes in the grids and guides.
- And much more... [See the full list of bug fixes](https://community.kde.org/Krita/Krita3dot1releasenotes#3.0_BETA_.2822nd_of_April.29)!
- Linux and Windows builds now should have full access to all translations and all of the menus should be translated.

From here, we will go through another round of bug fixing. We would love it if you could test out the new build and give us feedback in the [chatroom](https://krita.org/irc/) or [bug reporter](https://krita.org/get-involved/report-a-bug/). This testing helps us prevent 'surprise issues' when Krita 3.0 will be released in the coming weeks.

### Kickstarter!

We had intended to get 3.0 ready before the next kickstarter, but we feel its more important to spend another month fixing bugs. We're still going ahead with the next Kickstarter on schedule, so the May Kickstarter will coincide with the May release of Krita 3.0!

### Known Issues

We're fixing bugs like crazy, but there are still a [number of known bugs](https://bugs.kde.org/buglist.cgi?bug_severity=critical&bug_severity=grave&bug_severity=major&bug_severity=crash&bug_severity=normal&bug_severity=minor&bug_status=UNCONFIRMED&bug_status=CONFIRMED&bug_status=ASSIGNED&bug_status=REOPENED&list_id=1348442&product=krita&query_format=advanced). Please help us by testing this beta release and checking whether those bugs are still valid! [Bug triaging](/posts/ways-to-help-krita-bug-triaging/) is an awesome way of becoming part of our community.

### Download

**8 May. UPDATE: we made new builds and updated the links**

We haven't managed to create an MSI installer next to the zip files. But we do have 32 bits builds as well as 64 builds now, and a new setup that makes it really fast and easy to do new builds. These builds also include for the first time the camera raw importer plugin and the PDF import/export plugin.

- Zip archive: [Windows 64-bit dev build 99f6246 (zip)](http://files.kde.org/krita/3/windows/krita-3.0-Beta-master-99f6246-x64.zip)
- Zip archive: [Windows 32-bit dev build 99f6246 (zip)](http://files.kde.org/krita/3/windows/krita-3.0-Beta-master-99f6246-x86.zip)

There are also Windows builds with debug information available, as an experiment from [http://files.kde.org/krita/3/windows](http://files.kde.org/krita/3/windows).

**The OSX disk image** still has the known issue that if OpenGL is enabled, the brush outline cursor, grids, guides and so on are not visible. We're working on that, but don't expect to have rewritten the canvas before 3.0 will be released.

- Disk Image: [OSX dev build 8602b3f](http://files.kde.org/krita/3/osx/krita3-beta1-8602b3f.dmg)

**The Linux appimage** should run on any Linux distribution released since 2012. After downloading, make the appimage executable and run it. No installation is needed.

- AppImage [Linux AppImage dev build 8c5e55e](http://files.kde.org/krita/3/linux/krita-3.0-Beta-master-8c5e55e-x86_64.appimage)
- AppImage [Linux AppImage dev build 8c5e55e without openMP for Ubuntu 12.04 and CentOS 6.5](http://files.kde.org/krita/3/linux/krita-3.0-Beta-master-8c5e55e-no-openmp-x86_64.appimage)

**Source code**:

- [krita\_2.99.90](http://download.kde.org/unstable/krita/2.99.90/)

**Git repository:**

- [https://phabricator.kde.org/diffusion/KRITA/](https://phabricator.kde.org/diffusion/KRITA/)

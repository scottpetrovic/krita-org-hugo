---
title: "Krita 3.0 Release Candidate 1 Released"
date: "2016-05-18"
---

We're getting closer and closer to releasing Krita 3.0, the first version of Krita that includes animation tools, instant preview and which is based on Qt5! Today's release candidate offers many fixes and improvements over the previous beta releases. The Animation and Instant Preview features were funded by last year's [successful Kickstarter](https://www.kickstarter.com/projects/krita/krita-free-paint-app-lets-make-it-faster-than-phot), and right now we're running [our third Kickstarter campaign: this year's main topics are creating a great text and vector toolset](https://www.kickstarter.com/projects/krita/krita-2016-lets-make-text-and-vector-art-awesome). After one week, we're already half-way!

[![support-krita-2016-3](/images/posts/2016/support-krita-2016-3-1024x132.png)](https://www.kickstarter.com/projects/krita/krita-2016-lets-make-text-and-vector-art-awesome)

The biggest new feature is no doubt support for hand-drawn animation. This summer, Jouni Pentikäinen will continue improving the animation tools, but it's already a solid toolset. Here's a video tutorial where Wolthera shows how she created the animated headers for this year's Kickstarter stretch goals:

{{< youtube NnxbhYSLAsE >}}

And here is another demonstration by Wolthera showing off the Instant Preview feature, which makes it possible to use big brushes on big canvases. It may take a bit more memory, but it gives a huge speed boost:

{{< youtube lEXnpwIL45Y >}}

Apart from Instant Preview, Animation, Qt5-support, Krita 3.0 will have a number of Kickstarter stretch goals, like improved layer handling, improved shortcuts, the tangent normal brush, and great colorspace selector, guides, a grids and guides docker, snapping to grids and guides, improved shortcut palette, gradient map filter and much, much, much more. And we'll be sure to fix more issues before we present the final release.

So check out the review prepared by [Nathan Lovato](http://gdquest.com/), while we're preparing the full release announcement:

{{< youtube k51OK2PlTz4 >}}

### Release Candidate 3 Improvements

Compared to the last beta, we've got the following improvements:

- Shortcuts now also work if the cursor is not hovering over the canvas
- Translations are more complete
- The export to PDF dialog shows the page preview
- The advanced color selector is faster
- The vector gradient tool performs petter
- Fill layers are saved and loaded correctly
- Improvements to Instant Preview
- Fix crashes when setting font properties in the text tool.
- Fix handling the mirror axis handle
- Use OpenMP in G'Mic on Windows and Linux, which makes most filters much faster
- Fixes to the file dialog
- The Spriter export plugin was rewritten
- Fix a number of crashes
- Fix the scaling of the toolbox icons
- Add new icons for the pan and zoom tools
- Make it possible to enable HiDPI mode by setting the environment variable KRITA\_HIDPI to ON.
- Fix the fade, distance and time sensors in the brush editor
- Make it possible to open color palettes again
- Add a shortcut for toggling onion skinning
- Fix loading of the onion skin button states
- Add a lock for the brush drawing angle
- Handle positioning popups and dialogs on multi-monitor setups correctly

And a load of smaller things!

### Downloads

**Windows Shell Extension** package by Alvin Wong. Just install it and Windows Explorer will start showing preview and meta information for Krita files. (Disregard any warnings by virus checkers, because this package is built with the NSIS installer maker, some virus checkers always think it’s infected, it’s not.)

- Installation package: [kritashellex\_1.1.0.1\_setup.exe](http://files.kde.org/krita/3/windows/kritashellex_1.1.0.1_setup.exe)

**Windows:** Unzip and run the bin/krita.exe executable! These downloads do not interfere with your existing installation. The configuration file location has been moved from %APPDATA%\\Local\\kritarc to %APPDATA%\\Local\\krita\\kritarc.

- Zip archive: [krita-3.0-RC-1-master-6f75b0f-x64.zip (64 bits)](http://files.kde.org/krita/3/windows/krita-3.0-RC-1-master-6f75b0f-x64.zip)
- Zip archive: [krita-3.0-RC-1-master-6f75b0f-x86.zip (32 bits)](http://files.kde.org/krita/3/windows/krita-3.0-RC-1-master-6f75b0f-x86.zip)

**The OSX disk image** still has the known issue that if OpenGL is enabled, the brush outline cursor, grids, guides and so on are not visible. We’re working on that, but don’t expect to have rewritten the canvas before 3.0 will be released. Disable OpenGL in the preferences dialog to see a cursor outline, grids and guides and so on.

- Disk Image: [krita3-rc1-f345497.dmg](http://files.kde.org/krita/3/osx/krita3-rc1-f345497.dmg)

**The Linux appimage:**After downloading, make the appimage executable and run it. No installation is needed. For CentOS 6 and Ubuntu 12.04, a separate appimage is provided with g’mic built without OpenMP (which makes it much slower)

- AppImage [krita-3.0-RC-1-master-6f75b0f-x86\_64.appimage](http://files.kde.org/krita/3/linux/krita-3.0-RC-1-master-6f75b0f-x86_64.appimage) for modern distributions
- AppImage [krita-3.0-RC-1-master-6f75b0f-no-openmp-x86\_64.appimage](http://files.kde.org/krita/3/linux/krita-3.0-RC-1-master-6f75b0f-no-openmp-x86_64.appimage) for ancient distributions

As usual, you can use these builds without affecting your 2.9 installation.

**Source:** you can find the source here:

- [http://download.kde.org/unstable/krita/2.99.91/](http://download.kde.org/unstable/krita/2.99.91/)

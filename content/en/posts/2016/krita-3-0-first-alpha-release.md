---
title: "Krita 3.0: First Alpha Release"
date: "2016-04-09"
---

On the road to Krita 3.0, we're releasing today the first alpha version. This has all the features that will be in 3.0, and contains the translations, but is still unstable. We're fixing bugs all the time, but there's still plenty to fix! That said, we think we nailed the worst problems and we'd love for you all to give this version a try! The final release is planned for May 1st.

[![Screenshot_20160409_212626](/images/posts/2016/Screenshot_20160409_212626-1024x576.png)](/images/posts/2016/Screenshot_20160409_212626.png)

### What's new?

A short overview of new features compared to Krita 2.9:

- Tools for creating hand-drawn animations
- Instant Preview for working with big brushes and large canvases
- Rulers, guides, grids and snapping
- Revamped layer panel
- loading and saving gimp brushes
- and much, much more...

Krita 3.0 is also based on Qt 5 and the KF5 Framework libraries.

Since the last [development build](/posts/3-0-pre-alpha-3-is-out/), we focused on fixing bugs and improving performance.

There are some changes and improvements that we made outside of the mountain of fixes that were done. This is a list of improvements since the last pre-alpha that was released.

### New Features

- You can now move multiple selected layers at once
- And move masks with Ctrl + PgUp/PgDn
- Updated to G'MIC 1.7 ([see release notes](https://discuss.pixls.us/t/release-of-gmic-1-7-0/835))
- Updated Design templates

We also removed the print and print preview options; printing in Krita has never worked well, and after porting to Qt5 broke completely.

### User Interface and Usability Improvements

- Splash screen shows what area is loading on startup
- Updated Grids and Guides Tool Options UI elements
- Some checkboxes have been replaced with lock icons like the crop and geometry tool options
- Global Input pressure curve now has labels with the axes. ( Settings > Configure Krita > Tablet Settings ).
- Use highlighted color for the selected tool in toolbox (easier to see)
- Resource manager has separate buttons for importing resources now. This improves the stability with this area.

[![Screenshot_20160409_212649](/images/posts/2016/Screenshot_20160409_212649-1024x576.png)](/images/posts/2016/Screenshot_20160409_212649.png)

### Known Issues

We're fixing bugs like crazy, but there are still a [number of known bugs](https://bugs.kde.org/buglist.cgi?bug_severity=critical&bug_severity=grave&bug_severity=major&bug_severity=crash&bug_severity=normal&bug_severity=minor&bug_status=UNCONFIRMED&bug_status=CONFIRMED&bug_status=ASSIGNED&bug_status=REOPENED&list_id=1348442&product=krita&query_format=advanced). Please help us by testing this alpha release and checking whether those bugs are still valid! [Bug triaging](/posts/ways-to-help-krita-bug-triaging/) is an awesome way of becoming part of our community.

### Download

**There are two Windows versions**: an msi installer and a portable zip archive. The MSI installer also contains an explorer shell extension that allows you to see thumbnails of krita files in explorer. The shell extension was written by Alvin Wong.

- Zip archive: [Windows 64-bit Alpha 1 (zip)](#)
- MSI installer: [Windows 64-bit Alpha 1 (msi)](#) **WARNING**: the installer will _replace_ older versions of Krita!

**The OSX disk image** still has the known issue that if OpenGL is enabled, the brush outline cursor, grids, guides and so on are not visible. We're working on that, but don't expect to have rewritten the canvas before 3.0 will be released.

- Disk Image: [OSX Alpha 1](#)

**The Linux appimage** should run on any Linux distribution released since 2012. After downloading, make the appimage executable and run it. No installation is needed.

- AppImage [Linux AppImage Alpha 1](#)

Since this is the first official 3.0 release, we also have source code!

- [krita\_2.99.89](http://download.kde.org/unstable/krita/2.99.89/)

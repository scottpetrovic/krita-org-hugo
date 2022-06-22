---
title: "New Test Builds: changes to Flow and Saving/Loading"
date: "2019-01-25"
categories: 
  - "development-builds"
---

Krita needs you! We've new test builds of what will become Krita 4.2. There are two changes that we really would like everyone to test!

**DO NOT USE THIS FOR REAL WORK. ONLY FOR TESTING.**

**YOU MIGHT LOSE YOUR WORK!**

First, following [two discussions](https://forum.kde.org/viewtopic.php?f=288&t=136165) on [the forum](https://forum.kde.org/viewtopic.php?f=139&t=152017), William Brown created his [very first patch for Krita](https://phabricator.kde.org/D18467). This changes the way flow and opacitiy interact:

\[caption id="attachment\_8897" align="aligncenter" width="1024"\][![](/images/posts/2019/image-1024x768.png)](https://krita.org/wp-content/uploads/2019/01/image.png) Comparison of new and old Flow handling\[/caption\]

Now these changes really touch the core of what Krita does, that is painting, so we'd like all of you to go out, download a test build and play with it.

The second change is even scarier... We swapped out the engine that encodes and decodes Krita files.

Krita's .kra format is actually a simple zip file. And simple zip files have a limit: they cannot be bigger than 4GiB.  And it turns out that people working with animations sometimes do make files bigger than that...

So we are now using a new library, [quazip](https://stachenov.github.io/quazip/), that supports the Zip64 standard. But we use that library now wherever we load and save .kra files, but also [OpenRaster](https://www.openraster.org/) files, resource bundles -- everything that's a zip file. By default, Zip64 is disabled: if you're working on big animations, you need to manually enable Zip64 functionality:

[![](/images/posts/2019/zip64.png)](https://krita.org/wp-content/uploads/2019/01/zip64.png)Note that Zip64 files cannot be loaded in older versions of Krita! But we also need you test whether everything is okay when Zip64 is disabled.

### Feedback

[Please give us feedback](https://docs.google.com/forms/d/1TsmYcfM6Gp9FOAl9ybSPRM5sOdaztwaTvjoboaIq4Ec)!

## Download

### Windows

- 64 bits Windows: [krita-x64-4.2.0-preview2-setup.exe](https://download.kde.org/unstable/krita/4.2.0-preview2/krita-4.2.0-preview2-setup.exe)
- Portable 64 bits Windows: [krita-4.2.0-preview2.zip](https://download.kde.org/unstable/krita/4.2.0-preview2/krita-4.2.0-preview2.zip)

### Linux

- 64 bits Linux: [krita-4.2.0-preview2-x86\_64.appimage](https://download.kde.org/unstable/krita/4.2.0-preview2/krita-4.2.0-preview2.appimage)

(If, for some reason, Firefox thinks it needs to load this as text: to download, right-click on the link.)

### OSX

- OSX disk image: [krita-4.2.0-preview2.dmg](https://download.kde.org/unstable/krita/4.2.0-preview2/krita-4.2.0-preview2.dmg)

## Support Krita

Krita is a free and open source project. Please consider supporting the project with [donations](/support-us/donations/) or by [buying training videos or the artbook!](/support-us/shop) With your support, we can keep the core team working on Krita full-time.

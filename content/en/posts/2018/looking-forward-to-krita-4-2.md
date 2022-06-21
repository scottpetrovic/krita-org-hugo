---
title: "Looking forward to Krita 4.2!"
date: "2018-10-04"
categories: 
  - "development-builds"
  - "news"
---

Everyone is hard at work, and what will become Krita 4.2 is taking shape already. Today we're presenting a preview of Krita 4.2. It's not complete yet, and there **ARE** bugs. More than in the stable release (we'll be doing a 4.1.4 after all next week to clear up some more bugs...), and some might make you lose work.

\[caption id="attachment\_8252" align="aligncenter" width="850"\][![](../images/2018-fundraiser-hero2.png)](https://krita.org) Support Krita! Join the 2018 Fundraiser!\[/caption\]

But experiment with it, test it, check it out! There are lots of new things in there, and we'd love your feedback! There are also quite a few things we're right now working on, that aren't in this preview, but will be in 4.2. And we'll talk about, too!

## What's in there already

**Masks and Selections**. We've done a lot of work on improving working with masks and selections. Some of that work has already landed in Krita 4.1.3, but there's more to come. Ranging from making it easier to paint selections masks, to a new way of moving and transforming selections, to performance improvements all round. The "select opaque" function has received new options.

{{< youtube gWv--Do9L0E >}}

**Gamut masks**. A much-demanded new feature, gamut masks mask out part of the color selector. A [technique described by James Gurney](http://gurneyjourney.blogspot.com/2011/09/part-1-gamut-masking-method.html), this helps you to use color in a harmonious way. You can create new masks and edit existing masks right inside Krita. The masks now work with both the artistic and the advanced color selector. Rotating masks over the color selector is possible as well!

![](../images/gamut-masking.png)

**Improved performance**. We're always working to make Krita perform better, and there will always be room for improvement. This preview contains Andrey Kamakin's Google Summer of Code work on the very core of Krita: the tile engine. That is, the bits where all your layer's pixels are handled. There's still some fixing to do here, so be warned that if you paint with really big brushes, you may experience crashes. At the same time, this preview also contains more of Ivan Yossi's Summer of Code work: the creation of brush masks now uses your CPU's vectorization instructions, and that also increates performance! Dmitry also worked hard on improving the performance of the Layer Styles feature: especially for the Stroke Layer Style. The rendering became more correct at the same time. And fill layers have become much faster, too!

**Keep up to date**! Only on Linux for now, since we're still working on setting up the necessary libraries for encryption on Windows and macOS. The welcome screen can now show the latest news about Krita. It's off by default, since to bring you the news we have to connect to the Krita website.

[![](../images/news_widget-1024x566.png)](https://krita.org/wp-content/uploads/2018/10/news_widget.png)

**Colored Assistants.** It's now possible to give your painting assistants individual colors, and that color is saved and restored when you save and load your .kra project file.

**Activate transform tool on pasting**. When pasting something in Krita a new layer is created. Most of the time you'll want to move the pasted layer around or transform it. There's now a setting in the preferences dialog that, when checked, will make Krita automatically select the transform tool.

**Improved move tool**: undo and redo with the move tool was always a bit wonky... Now it works as expected. Not a big thing, but it should help with everyone's workflow.

**A smoother UI**: 4.2 will have lots of small fixes to improve your workflow. That ranges from making it possible to resize the thumbnails in the layer docker to improved interaction with color palettes to making it possible to translate plugins written in Python. There are also new blending modes, with more coming, and the G'Mic plugin has been updated to the latest version.

\[video width="344" height="502" mp4="https://krita.org/wp-content/uploads/2018/08/resize-thumbnail.mp4"\]\[/video\]

**Lots of bug fixes.** We're already at nearly 200 bug fixes for 4.2, and that number will only increase.

## What we're working on

But we're not done yet! We intend to release Krita 4.2 this year, in December, but we haven't gone into feature freeze. This is a little taste of what may still be coming from 4.2!

This isn't in the preview yet, but here are a couple of things that our UX expert, Scott, is working on. First, the **brush editor** is being redesigned. As you can see from the video, it's being condensed, and that's because we also want to make it possible to dock it as a panel in one of the dock areas of Krita, or have it floating free, possibly on another monitor.

{{< youtube 2hWPzNFPIxY >}}

Then, the **text tool**'s UI is being revamped. While Dmitry is working on making the text tool more reliable, Scott is working on making it nicer to use:

{{< youtube pNsifPZJsjw >}}

Michael's Summer of Code work hasn't been merged yet, but we fully intend to do that before the release. This will improve the stability of working with color palettes and make it possible to save palettes in your .kra Krita project file.

Another area where work is going is **resource management**. That is, loading, working with, tagging, saving and sharing things like brush presets, brush tips, gradients or patterns. This is a big project, but when done Krita will start faster, use less memory and a lot of little niggles and bugs with handling resources will be gone.

### **Downloads**

Have fun with the 4.2 preview!

[![](../images/4.2-preview-1024x693.png)](https://www.krita.org)

## Download

### Windows

- 64 bits Windows: [krita-x64-4.2.0-preview-setup.exe](https://download.kde.org/unstable/krita/4.2.0-preview/krita-x64-4.2.0-preview-setup.exe)
- Portable 64 bits Windows: [krita-x64-4.2.0-preview.zip](https://download.kde.org/unstable/krita/4.2.0-preview/krita-x64-4.2.0-preview.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/unstable/krita/4.2.0-preview/krita-x64-4.2.0-preview-dbg.zip)

- 32 bits Windows: [krita-x86-4.2.0-preview-setup.exe](https://download.kde.org/unstable/krita/4.2.0-preview/krita-x86-4.2.0-preview-setup.exe)
- Portable 32 bits Windows: [krita-x86-4.2.0-preview.zip](https://download.kde.org/unstable/krita/4.2.0-preview/krita-x86-4.2.0-preview.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/unstable/krita/4.2.0-preview/krita-x86-4.2.0-preview-dbg.zip)

### Linux

- 64 bits Linux: [krita-4.2.0-preview-x86\_64.appimage](https://download.kde.org/unstable/krita/4.2.0-preview/krita-4.2.0-preview-x86_64.appimage)
- 64 bits Linux [G'Mic-Qt plugin appimage](https://download.kde.org/unstable/krita/4.2.0-preview/gmic_krita_qt-x86_64.appimage).

(If, for some reason, Firefox thinks it needs to load this as text: to download, right-click on the link.)

### OSX

- OSX disk image: [krita-4.2.0-preview.dmg](https://download.kde.org/unstable/krita/4.2.0-preview/krita-4.2.0-preview.dmg)

Note: the touch docker, gmic-qt and python plugins are not available on OSX.

### Source code

- Source code: [krita-4.2.0-preview.tar.gz](https://download.kde.org/unstable/krita/4.2.0-preview/krita-4.2.0-preview.tar.gz)

### md5sum

For all downloads:

- [md5sum.txt](https://download.kde.org/unstable/krita/4.2.0-preview/md5sum.txt)

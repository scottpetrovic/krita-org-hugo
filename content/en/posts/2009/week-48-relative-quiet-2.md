---
title: "Week 48: Relative Quiet"
date: "2009-11-30"
---

A relatively quiet week, with only 42 commits. This no doubt was because five Krita hackers were travelling to Oslo for a KOffice sprint weekend! Boudewijn, Cyrille, Sven, Lukas and Dmitry met together with about a dozen other KOffice hackers in the Nokia offices, home to the Qt hackers.

Despite a lack of commits, it was a productive weekend in its own right. Oslo being an expensive city, we spend the evenings in the hotel breakfast room drinking tea, munching chocolates (thanks go to Lukas for getting a big bag of all-sorts, and to Dmitry for bringing some excellent chocolate from home) and enjoying some high-bandwidth communication. And still, by Sunday we had managed to bring the bug count for trunk down to 60, but Cyrille then created a new bug... But another got fixed, and at the time of writing, we're still at 60.

Another reason for the quiet might have been the release of Krita (and KOffice) 2.1 this week. The release was generally speak well-received in the press, judging from my bag of google alerts. However, Heise still felt Krita 2.1 to be a rather crash-happy, which was disappointing. Please! Test Krita 2.1 and report any crashes you might encounter. We'll try to fix them for 2.1.1! Any communication medium is okay with me: bugzilla, mail, irc, pigeon, paper letters, texting my n900...

So, what got done last week?

Vera Lukman has been trying to make the popup-palette for quick brush and color selection look nice.  

![](http://krita2d.org/images/stories/krita-feature-images/popup_palette.png)  

Boudewijn Rempt continued trying to get Photoshop files to load. He has discovered another open source project for reading PSD files, [psdparse](http://www.telegraphics.com.au/svn/psdparse), which showed some additional color modes that appear to be present in Photoshop CS and which Krita already supports natively, so conversion should be easy. We're really close to loading our first Photoshop images now: as Cyrille Berger remarked, removing GraphicsMagick has given an enormous impetus to the development of file format filters.

Adrian Page made the brand-new XCF work on Windows, where a standard KDE idiom needs a slightly different twist. Plus there were some issues with the library we are using, [XCFTools](http://henning.makholm.net/software).

Cyrille Berger made Krita compatible with the latest, still unreleased version of OpenGTL. He also fixed the loading of OpenCTL-based color transformations.

Dmitry Kazakov fixed a two bugs in trunk, namely [\[Bug 215180\] Undo in tile engine clears rects](https://bugs.kde.org/show_bug.cgi?id=215180), and [\[Bug 212912\] undoing transform tool actions doesn't update pixels](https://bugs.kde.org/show_bug.cgi?id=212912), making it much easier to work with our (currently still unstable) trunk.

Sven Langkamp fixed [bug 195618](https://bugs.kde.org/show_bug.cgi?id=195618), so when you crop an image that has vector layers, all the vector shapes are now correctly placed again.

Lukáš Tvrdý improved the dyna brush code-wise, but for the user little changed. Then did some more work on the spray brush: you can now load fairly big images and the spray brush will scale them according to the particle size. He demonstrated this in his [blog](http://lukast.mediablog.sk/log/?p=121).

![](http://krita2d.org/images/stories/krita-feature-images/spray-kde-hackers-planet.jpg)

  

Feel free to comment on this article at the [Krita Forums](http://forum.kde.org/viewtopic.php?f=137&t=84201).

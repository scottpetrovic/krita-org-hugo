---
title: "September Development Update"
date: "2021-09-15"
categories: 
  - "development-builds"
  - "news"
---

Not directly development related, but the scammers who registered krita.io, krita.app and getkrita.com for ransomware attacks have lost those domains. Let's hope that also means the scammers decide they have had enough and stop spamming people. It's been quite a chore dealing with all the enquiries, but it's better that people ask than that they blindly go with the flow!

The Krita development fund now has over 150 subscription members -- and about 250 occasional supporters per month. We're still quite far from making it possible to fund more developers from the dev fund instead of -- always fickle -- store sales, so if you aren't a member, please consider joining!

[![](../images/landing-page-banner.png)](https://fund.krita.org)

We have just now released [Krita 5.0 beta 1](/item/first-beta-for-krita-5-0-released/), and now we're working on the second beta. At the same time, there are some exciting developments for Krita 5.1, _and_ we're looking into what we want to focus on after the Krita 5.0 release.

**Halla** and **Wolthera** had the first real life meeting since February 2020, and spent their time triaging and fixing bugs. That resulted in the bug count dropping by about sixty, because in the same week, over forty new bugs were reported. That means that people are really taking testing the first Krita 5.0 beta seriously, which is awesome!

**Wolthera** and **Raghukamath** have been working hard on updating the manual for Krita 5, while **Tyson Tan** and **Windragon** have been digging into the translation of Krita and the manual, finding many places, especially in Krita, where text wasn't translatable yet.

**Windragon** not only worked on translations a whole lot, he also fixed issues with handling touch input when drawing with a stylus, and looked into the use of OpenGL ES on ARM.

**Dmitry** and **Ivan** have worked on a workaround for the slowness of the OpenGL canvas on macOS. **Halla** has been testing their work during a really long inking session, and she reports that there's a huge improvement in performance. The code is still experimental, but we really want this to be in Krita 5.0 Beta 2, that is the _next_ beta, so everyone on macOS can test it. And... It should also improve painting performance on Windows systems with 4K or higher resolution screens.

**Dmitry** and **Amyspark** have been working on improving Krita's performance by updating the compilers Krita can be built with on Windows and Linux. In some cases, this improves Krita's brushes performance by up to sixty percent, but there were a lot of pitfalls along the way, and many bug reports were submitted to compiler developers. **Amyspark** is also working with people from CERN to improve the **Vc** library, which Krita uses for making the brush engines work in parallel.

**Amyspark** has also implemented loading and saving layered tiff files the Photoshop way (Krita has supported the tiff standard way of doing that for more than a decade), refactored our metadata support (exif and so on), away from the really baroque design we implemented back in ... 2005. They also implemented support for metadata in tiff files. Then there were issues with LittleCMS. That now comes with a plugin that makes some calculations a lot faster, but we ran into various bugs. Together with **Matthias**, Amyspark worked with the LittleCMS maintainer, **Marti Maria** to fix those issues, and the results should be visible in today's nightly builds. Fingers crossed! And then Amyspark started looking into a whole lot of legacy OpenGL code with a view to cleaning it up and making it easier to understand.

**Matthias** has also worked on an experiment where even in subwindow mode, there's a tab bar to switch between documents.

**Sharaf** is working on improving Krita on Android and ChromeOS. New Android API's are less than ideal for working with local files, but he's managed to work his way through the problems. He's also been fixing bugs in Krita's vector layer and objects, and issues with Krita's dockers on smaller screens.

**Agata** has been fixing issues found in Beta 1 with the area-limited perspective assistants, as well as the way gradients are shown in the gradient selector.

**Emmet** and **Eoin** have been working both on animation and storyboard bug fixes for Krita 5.0, as well as improving the brand new storyboard feature, which makes its debut in Krita 5.0, but will be even more awesome in Krita 5.1. An experienced storyboard artist is helping them fine-tune the functionality!

---
title: "Krita Dev Fund Campaign -- First Update!"
date: "2021-05-11"
categories: 
  - "news"
---

Here's our first update on how the work for Krita 5 is going!We're bringing you these updates to show what's going on in Krita and why it's a good idea to join [Krita development fund](https://fund.krita.org)! But first a short video by Ramon Miranda showing one the new features in Krita 5: the painting recorder. The painting recorder was created by Shi Yan and improved by Dmitry Utkin. Eoin O'Neill is sponsored to improve the interaction with ffmpeg. Also, looks at the nice new icons created by Timothee Giet!

{{< youtube a0uxM_bQOnU >}}

This is the last month when we can still add new features. From June 1st, it'll be bug fixing only. Not all features start with sponsored developers: many new features are coded by volunteers. Our sponsored developers then work with the volunteers to get the features ready. So here's what got in last week:

- Working together with Dmitry and Emmet, Know Zero completed a new feature: importing animations as frames, like animated gif files or mp4 clips. He also made it possible to export animated gifs with transparent backgrounds.
- Then there's Nabil Magfur Usman's 2 point perspective grid assistant[![](/images/posts/2021/perspective_grid-1024x552.png)](/images/posts/2021/perspective_grid.png)
- Deif Lou added new texture blending modes for brush presets like hard mix, color dodge, color burn, overlay. Here is an [in-depth discussion](https://phabricator.kde.org/T14345). Test image done by Hulmanen: [![](/images/posts/2021/texture_blending-766x1024.jpg)](/images/posts/2021/texture_blending.jpg)
- Agata Cacko was sponsored to work on the MyPaint brush engine. The MyPaint brush engine was created by Ashwin Dhakaita for the 2020 Google Summer of Code program. There were still a few things missing, like support for mirrored painting, and that's what Agata added. Agata also worked on a new resource import dialog, as part of the resource rewrite.
- Sharaf Zaman was sponsored to work on Krita for Android and ChromeOS. He implemented window management for dialog windows in Krita, so the dialogs can be resized and moved around. And he fixed a lot of Android and ChromeOS specific issues as well!
- Ivan Yossi was sponsored to work on Krita on macOS. He fixed the quicklook and finder preview plugins. We'll have to make a Krita 4.4.4 release for this, though. And now he's investigating whether we can finally speed up the GPU canvas on macOS.
- Felipe Lema moved loading the thumbnails for the recent files in the welcome screen to a background thread, which solves the slow startup of Krita if you have ginormous tiff files recently used.
- Dmitry Kazakov was sponsored to work on brush engines. Specifically, he worked on a new [smudge brush engine](https://invent.kde.org/graphics/krita/-/merge_requests/756). He also restored the cumulative undo feature that got broken in 2015. [![](/images/posts/2021/colorsmudge-1024x578.jpg)](/images/posts/2021/colorsmudge.jpg)
- Reinold Rojas has been working on improving the grid brush engine: he added a shortcut for changing the offset of the current grid brush. It's still work in progress!
- Emmet and Eoin have been sponsored to work on changes in the way onion skinning works, so people can use reference frames. That might only land in Krita 5.1, though...
- Wolthera has been sponsored to work on the manual: we want the manual up to date when we launch Krita 5, and there are so many changes, and so many new things to describe.
- Halla has been sponsored to work on making sure that we have a good default brush preset selected when Krita starts for the first time, and on making it possible to create new versions of brush tips.

So, if you like what we're doing, join the development fund!

[![](/images/posts/2021/landing-page-banner.png)](https://fund.krita.org)

---
title: "Krita Dev Fund Campaign: Second Update!"
date: "2021-05-18"
categories: 
  - "news"
---

Here's our second update on the state of Krita 5. We’re bringing you these updates to show what’s going on in Krita and why it’s a good idea to join the [Krita development fund](https://fund.krita.org)!  There are already more than 100 members of the dev fund! But let's have some excitement first. The new smudge brush engine landed in Krita's master branch last week, the culmination of months of work by Dmitry Kazakov and Peter Schatz:

{{< youtube D0Lv5gWvu94 >}}

If you want to give this a try, download one of the [Krita Next nightly builds](/download/krita-desktop/). There's also a [zip file with the presets](https://files.kde.org/krita/extras/RGBA-wet.zip) Ramon created for testing the new engine! Now, take care! These are development builds, so make a backup of [Krita's settings](https://docs.krita.org/en/KritaFAQ.html#resetting-krita-configuration) and of [the resources folder](https://docs.krita.org/en/KritaFAQ.html#where-are-my-resources-stored). Have fun!

Last week was also the week Halla gave a [presentation on funding Krita development during the Linux App Summit](https://www.youtube.com/watch?v=1pFADheIzQk). The video hasn't been cut up in separate videos for each presentation. Her presentation starts at 2:58.

We also [released the results](/item/huion-and-krita-competition-winners/) of the contest we organized together with Huion. That was really fun, and [there were so many awesome submissions](https://krita-artists.org/c/contest-games-collab/four-seasons-journey-of-leon-kiki/30)!

![](/images/posts/2021/competition_1-1024x724.jpg) Watch out Leon!

Now for the work that landed since our last update. It was mostly a bug fix week, where 21 authors have pushed 90 commits to master and 97 commits to all branches -- we have been nicely busy!

- Dmitry spent most of the week finishing the integration of the new color smudge engine. That's in, as you've seen!
- Alvin added console versions of Krita and kritarunner. This means you get a much better experience if you're on Windows and you use Krita's commandline options to convert images, for instance.
- Amyspark was sponsored to work on making Krita build with the Microsoft Visual Studio C++ compiler. This is pretty tricky, because of bugs in that compiler. But we're in touch with the Microsoft compiler team who have told us they all love Krita, so it might be possible to get [these issues](https://developercommunity.visualstudio.com/t/c2027-error-when-using-qts-qshareddatapointer-to-p/1424440) fixed! After that, Amyspark started looking into updating our Python plugin to the latest version of the Python and PyQt, which turns out to be really tricky, especially on Windows.
- Emmet, Halla and Wolthera all have worked on the new animation input feature, adding a warning when you're trying to import too many frames for your system to handle. This was sponsored work.
- Deif Lou fixed color dodge/burn and hard mix for brush masking.
- Sharaf Zaman was sponsored to fix issues for Android -- and issues in general, like the transform tool no longer transforming the selection itself.
- Halla was sponsored to continue working on the resource system rewrite. It's been taking ages, but we're getting results. Importing and creating gradients now works properly again. She also spent a day fixing bugs.
- Agata was sponsored to work on the resource system rewrite as well, and she fixed saving mypaint brush presets into bundles as well as the layout of the tag selection widget. And she fixed showing the individual brushes of ABR (Photoshop) brush collection libraries.
- Reinold Rojas worked on the grid brush engine: he made sure all grid particle types have brush outlines and added a shortcut to change the offset of the grid brushes.
- Eoin and Emmet were sponsored to work on fixing animation related bugs and documentation fo rhte new animation features.
- Wolthera was sponsored to work on the manual for Krita 5/

So, if you like what we're doing, join the development fund!

[![](/images/posts/2021/landing-page-banner.png)](https://fund.krita.org)

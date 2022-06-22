---
title: "Krita 2.9 Animation Edition Beta released!"
date: "2015-11-25"
categories: 
  - "officialrelease"
tags: 
  - "animation"
  - "krita"
  - "release"
coverImage: "kiki2_ann_small.jpg"
---

[![kiki2_ann_small](/images/posts/2015/kiki2_ann_small.jpg)](https://krita.org/wp-content/uploads/2015/11/kiki2_ann_small.jpg)

Today we are happy to announce the long awaited beta-version of Krita with Animation and Instant Preview support! Based on Krita 2.9, you can now try out the implementation of the big 2015 [kickstarter](https://www.kickstarter.com/projects/krita/krita-free-paint-app-lets-make-it-faster-than-phot) features!

What's new in this version? From the user point of view Krita didn't change much. There are three new dockers: **Animation**, **Timeline** and **Onion Skins**, which let you control everything about your animation frames and one new menu item **View->Instant Preview Mode** (previously known as Level of Detail) allowing painting on huge canvases. For both features, you need a system that supports OpenGL 3.0 or higher.

For people who previously installed Krita, to get Instant Preview to show up on the view menu, delete the krita.rc(not kritarc) file in your resource folder(which can be accessed quickly via Settings->Manage Resources->Open Resource Folder) and restart Krita. Or just use the hotkey **Shift**+**L**.

But under these visually tiny changes hides a heap of work done to the Krita kernel code. We almost rewritten it to allow most of the rendering processes run in the background. So now all animated frames and view cache planes are calculated in the moments of time when the user is idle (thinks, or chooses a new awesome brush). Thanks to these changes now it is possible to efficiently work with huge images and play a sequence of complex multi-layered frames in real time (the frames are recalculated in the background and are uploaded to you GPU directly from the cache).

[![krita_animation_1](/images/posts/2015/krita_animation_1-300x205.png)](https://krita.org/wp-content/uploads/2015/11/krita_animation_1.png)

So, finally, welcome Krita 2.9 Animation Edition Beta! (Note the version number! The final release will be based on Krita 3.0, this version is created from the 2.9 stable release, but it is _still_ beta. We welcome your feedback!

#### Video tutorial from Timothee Giet:

A short video introduction into Krita animation features is available [here](http://timotheegiet.com/blog/anim/krita-2-9-animation-edition-beta.html).

#### Packages for Ubuntu:

You can get them through Krita Lime repositories. Just choose 'krita-animation-testing' package:

sudo add-apt-repository ppa:dimula73/krita
sudo apt-get update
sudo apt-get install krita-animation-testing 

#### Packages for Windows:

Two packages are available: 64-bit, 32-bit:

- [64 bits Windows zip file](http://files.kde.org/krita/windows/krita_2.9.9.2ae_beta_x64.zip)
- [32 bits Windows zip file](http://files.kde.org/krita/windows/krita_2.9.9.2ae_beta_x86.zip)

You can download the zip files and just unpack them, for instance on your desktop and run. You might get a warning that the Visual Studio 2012 Runtime DLL is missing: you can download the missing dll [here](https://www.microsoft.com/en-us/download/details.aspx?id=30679). You do not need to uninstall any other version of Krita before giving these packages a try!

#### User manuals and tutorials:

- [Animation User Manual](https://userbase.kde.org/Krita/Manual/Animation)
- [Instant Preview User Manual](https://userbase.kde.org/Krita/Manual/BrushEngines/LODstrokes)

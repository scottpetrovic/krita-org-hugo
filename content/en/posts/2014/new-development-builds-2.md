---
title: "New Development Builds"
date: "2014-10-23"
categories: 
  - "development-builds"
tags: 
  - "krita-2-9"
---

It's been about a month since we last published new development builds... And a lot has happened in the meantime. Now, before everyone starts downloading, a warning:

**THIS BUILD IS REALLY EXPERIMENTAL**

And we mean it. Not only does this build include a month of Dmitry's work, but we also merged in Mohit Goyal's Summer of Code work. That touched a lot of stuff... There is at least one known crash -- the sketch brushes are broken. We're working on fixing, but we need _more_ testing! Please join the [forum](http://forums.kde.org/krita) and report your findings!

Okay, so what's in here?

Let's take Mohit's work first:

1. _Dirty Presets_: Keeps temporary tweaks made to the preset till the session ends. Go to the Brush Editor box. Bottom left -- select "Temporarily save tweaks to presets". Any time you make a change to any setting in the preset -- the textbox will turn pink and a "+" symbol will appear on the icon. The Reload button is used to reset the tweaks for that particular preset.
2. _Locked Settings_: Keeps settings constant across presets In the brush editor box, for any paint option like "Size" on the left, there will be a "link" icon. Right click on that option to Lock the option. Now that particular setting will remain constant across all presets. If you change it in one preset - the changes will reflect across all presets. To unlock any option: right click on a locked option and click on Drop Locked Settings. You can either use these settings in the preset or load the last settings available in the preset.
3. _Cumulative Undo/Redo_ 1. To use this feature, you will have to first have to go to Settings->Dockers->Undo History to activate the docker. 2. Next right click on <empty> or on any stroke in the undo docker and select "Use Cumulative Undo/Redo" 3. This feature merges commands together so the the user doesn't have to undo a particular group one by one and has a much larger undo history than the initial 30 strokes. The feature works on three configurable parameters : Time before merging strokes together: while strokes are made, the code keeps checking for a particular timelapse of T seconds before it merges the groups together Time to group the strokes : According to this parameter -- groups are made. Every stroke is put into the same group till two consecutive strokes have a time gap of more than T seconds. Then a new group is started. Individual strokes to leave at the end : A user may want to keep the ability of Undoing/Redoing his last N strokes. Once N is crossed -- the earlier strokes are merged into the group's first stroke.

Next, Scott Petrovic has been putting a lot of polish on Krita!

1. Keep Eraser size. Now, toggling Erase mode with the 'E' shortcut will save the size of your current preset. That means that if you paint with a small brush, then erase with a big brush, you only have to press 'E'.
2. Saving tool options. Most of the tools now save your settings between sessions: fill, multi-line, gradient, rectangle, ellipse, line, move, text, crop, freehand...
3. And a lot of polish in other places as well -- better defaults, labels for previously unclear sliders, 'C' is crop tool now,  and more.

Dmitry Kazakov has worked on the transform tool. While the cage tool got plenty of fixes, he also implemented a whole new mode: liquify. This needs testing now! Now the transform tool option pane is seriously overloaded...

[![liquify](../images/liquify-300x274.png)](https://krita.org/wp-content/uploads/2014/10/liquify.png)

If you've got a good proposal for a better layout, please share your ideas on the forum! Right now, Dmitry is working on the next part of the Kickstarter feature list: non-destructive transformation masks.

 

Boudewijn Rempt did some more OSX porting work -- the file dialogs should now be native and work correctly -- and started working on loading and saving resource blocks, layer styles and transparency masks in PSD.

And we've got a nice icon clean-up, too, courtesy of Wolthera and Timothée.

Sven Langkamp has worked mostly on the MVC branch, which is where we're trying make Krita open more than one image in a window. He got it stable enough that we could start testing for real, and Wolthera dove in and made [reports](http://lists.kde.org/?l=kde-kimageshop&m=141350643901581&w=2)... There's a lot of work to be done here!

So, here are the new builds:

For Windows, I've added a zip file next to the MSI installer. Unzip the zip file anywhere, go into krita/bin, double-click krita.exe and you can test this build without breaking your real installation. Remember -- this build is not ready for daily work, it's _experimental_.

- [http://files.kde.org/krita/windows/krita\_x64\_2.8.79.21.zip](http://files.kde.org/krita/windows/krita_x64_2.8.79.21.zip)
- [http://files.kde.org/krita/windows/krita\_x64\_2.8.79.21.msi](http://files.kde.org/krita/windows/krita_x64_2.8.79.21.msi)

For OSX, here's a new DMG. Other than the file dialog fix, there's no new OSX specific fixes in here. We're still mulling over ways to [fund a proper OSX port](https://forum.kde.org/viewtopic.php?f=137&t=123362), among other things.

- [http://files.kde.org/krita/osx/krita-2.8.79.21.dmg](http://files.kde.org/krita/osx/krita-2.8.79.21.dmg)

For Linux, Krita Studio users have access to a [package for CentOS 6.5](http://kritastudio.com), and Krita Lime has been updated for Ubuntu users.

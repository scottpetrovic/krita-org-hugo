---
title: "Last week in Krita — weeks 25 & 26"
date: "2014-06-30"
---

This last two weeks have been very exiting with the kickstarter campaign getting closer and closer to the pledge objective. At the time of writing we just crossed 13k! And with the wave of new users, drawn by the great word spreading labor of collaborators and enthusiasts, we have been very busy bringing new functions and building beta versions for you.

And now there's also the first public build for OSX:

[http://www.valdyas.org/~boud/krita\_osx\_2.8.79.0.tgz](http://www.valdyas.org/%7Eboud/krita_osx_2.8.79.0.tgz)

![](../images/kritaosx.jpg)

[It is just a prototype, with stuff missing and rather detailed instructions on getting it to run](https://www.kickstarter.com/projects/krita/krita-open-source-digital-painting-accelerate-deve/posts/894745)... But if you've always wanted to have Krita on OSX, this is your chance to help us make it happen!

Before getting into the new hot stuff in the code I can’t go without mentioning the useful videos from Ramon Miranda. Aiming to improve the common knowledge of Krita features and capabilities as a painting software for those who hear about it for the first time, he has created a short series of video tips: Short video introductions to many functions and fundamentals. Even for the initiated these are a good resource. I wasn’t aware of some depicted functions on the videos. [All tips and info on kickstarter post,](https://www.kickstarter.com/projects/krita/krita-open-source-digital-painting-accelerate-deve/posts/891145) [Ramon youtube channel](https://www.youtube.com/user/TheShockito)

## Week 25 & 26 progress

Amongst the notable changes and develops we can cite the efforts of Boudewijn to create a building environment to eventually allow the creation of an alpha version for **OSX** users. Still in experimental phase, the current steps show steady progress as its now possible to open the program and do minor paintings. Of course this is far from been a version to distribute, but if we remember the Windows humble beginnings, this is a great sign. go krita!

In other news. Somsubhra, developer of Krita Animation spin, has added, aside many bug fixes and tweaks, a first rough animation player. I wanted to make a short video for you, but still the build is very fragile and on my system it crashed after creating the document. You can see the player in action in a video made by Sohsumbra

\[embed\]https://www.youtube.com/watch?v=VEHJ-JIunII\[/embed\]

### This week’s new features:

- Implemented "Delayed Stroke" feature for brush smoothing. (Dmitry Kazakov)
- Edit Selection Mask. (Dmitry Kazakov)
- Add import/export for r8 and r16 heightmaps, extensions .r8 and .r16. (Boudewijn Rempt)
- Add ability to zoom and sync for resource item choosers (Ctrl + Wheel). (Sven Langkamp)
- Brush stabilizer by Juan Luis Boya García. (Juan Luis Boya García)
- Allow activation of the Isolated Mode with Alt+click on a layer. (Dmitry Kazakov)

### This week’s main Bug fixes

- Make ABR brush loading code more robust. (Boudewijn Rempt)
- FIX [#319279](https://bugs.kde.org/show_bug.cgi?id=319279): Drop the full brush image after loading it to save memory. (Boudewijn Rempt)
- Enable the vector shape in Krita. This make possible to show embedded svg images. (Boudewijn Rempt)
- CCBUG [#333451](https://bugs.kde.org/show_bug.cgi?id=333451): Add basic svg support to the vector shape. (Boudewijn Rempt)
- FIX [#335041](https://bugs.kde.org/show_bug.cgi?id=335041): Fix crash when installing a bundle. (Boudewijn Rempt)
- FIX [#33592](https://bugs.kde.org/show_bug.cgi?id=33592): Fix saving the lock status. (Boudewijn Rempt)
- Fix crash when trying to paint in scratchpad. (Dmitry Kazakov)
- Don’t crash if deleting the last layer. (Boudewijn Rempt)
- FIX [#336470](https://bugs.kde.org/show_bug.cgi?id=336470): Fix Lens Blur filter artifacts when used as an Adjustment Layer. (Dmitry Kazakov)
- FIX [#334538](https://bugs.kde.org/show_bug.cgi?id=334538): Fix anisotropy in Color Smudge brush engine. (Dmitry Kazakov)
- FIX [#336478](https://bugs.kde.org/show_bug.cgi?id=336478): Fix convert of clone layers into paint layers and selection masks. (Dmitry Kazakov)
- CCBUG [#285420](https://bugs.kde.org/show_bug.cgi?id=285420): Multilayer selection: implement drag & drop of multiple layers. (Boudewijn Rempt)
- FIX [#336476](https://bugs.kde.org/show_bug.cgi?id=336476): Fix edge duplication in Clone tool. (Dmitry Kazakov)
- FIX [#336473](https://bugs.kde.org/show_bug.cgi?id=336473): Fixed crash when color picking from a group layer. (Dmitry Kazakov)
- FIX [#336115](https://bugs.kde.org/show_bug.cgi?id=336115): Fixed painting and color picking on global selections. (Dmitry Kazakov)
- Fixed moving of the global selection with Move Tool. (Dmitry Kazakov)
- CCBUG [#285420](https://bugs.kde.org/show_bug.cgi?id=285420): Add an action to merge the selected layers. (Boudewijn Rempt)
- CCBUG [#285420](https://bugs.kde.org/show_bug.cgi?id=285420): Layerbox multi-selection. Make it possible to delete multiple layers. (Boudewijn Rempt)
- FIX [#336804](https://bugs.kde.org/show_bug.cgi?id=336804): (Boudewijn Rempt)
- FIX [#336803](https://bugs.kde.org/show_bug.cgi?id=336803): (Boudewijn Rempt)
- FIX [#330479](https://bugs.kde.org/show_bug.cgi?id=330479): Fix memory leak in KoLcmsColorTransformation. (Boudewijn Rempt)
- And many code optimizations, memory leak patching, spelling and translation updates and other fixes.

### Delay stroke and brush stabilizer

A new way of creating smooth controlled lines. The new Stabilizer smooth mode works using both the distance of the stroke and the speed. It uses 3 important options that can be described as follows:

- **Distance:** The less distance the weaker the stabilization force.
- **Delay:** When activated, it adds a halo around the cursor. This area is defined as a "Dead Zone", no stroke is made while the cursor is inside it. Very useful when you need to create a controlled line with explicit angles in it. The Pixel value defines the size of the halo.
- **Finish line:** If switched off, line rendering will stop in the spot it was when the pen lifted. Otherwise, it will draw the missing gap between the current brush position and the cursor last location.

### Multiselection

Developers have been working to re implement working on multiple layers. This time they made possible to select more than one layer to reorganize the stack, merge and delete actions. After selecting multiple layers you can:

- Drag and drop from on location to another
- Drag and drop layers inside a group
- Click the erase layer button to remove all selected layers
- Go to "Layer -> Merge selected layers" to merge.

This first implementation allows a much more faster workflow when dealing with many layers. However it is still necessary to use groups to make some actions, like transform, on multiple layers.

**NEW** :Layer -> Merge selected layers

### Edit selection mask (global selection)

To activate go to Selection menu and turn on "Show global Selection Mask".

When activated all global selections will appear in the layer stacks as local selection do. You can deactivate the selection, hide or edit using any available tool, like transform, brushes or filters.

At the moment it is not possible to see the effect a tool causes on all tools, but you can transform the selection to a painter layer to make finer adjustments.

**NEW** :Selection -> Show Global Selection Mask

### Alt + click isolated layer

Added a new action to toggle isolate layer.

**NEW** :\[ALt\] + \[Click\] over a layer in layer docker.

This actions shows instantly the selected layer hiding all other. It will return to normal mode after another layer is selected, but while the isolated layer mode is on its possible to paint, transform and adjust visualizing only the isolated layer.

---
title: "Last week in Krita — week 20"
date: "2014-05-18"
---

When a feature is proposed there is discussion and feedback before getting into coding and implementation. The debate continues until most devs and artists agree that we need the feature and should be coded. This is done so the coding time is used more effectively. However no new feature is bug free or closed to improvements.

With this in mind I present you the products of this week’s hard work.

## Week 20 progress

#### This week’s new features:

- [Show mirror axis in mirror mode](#show-axis). (Arjen Hiemstra)
- [Add Background color preview to Right Click Palette](#popup-bg). (Iván Yossi)
- Improvements to resource manager. (Boudewijn Rempt)
- [New bundle creator Dialog](#bundle-create). (Boudewijn Rempt)

#### This week’s main Bug fixes:

- Partially fix [#333917](https://bugs.kde.org/show_bug.cgi?id=333917): Added extensive tablet debugging on Windows. (Dmitry Kazakov)
- Worked [#333843](https://bugs.kde.org/show_bug.cgi?id=333843): Added more extensive tablet debugging on X11. (Dmitry Kazakov)
- FIX Linux [#331358](https://bugs.kde.org/show_bug.cgi?id=331358): Fix tablet stylus rotation in Linux. The Windows fix will be worked shortly after. (Dmitry Kazakov)
- FIX [#334204](https://bugs.kde.org/show_bug.cgi?id=334204): Handling tablet events when "Pan/Scroll" mode is assigned to a button. (Dmitry Kazakov)
- Fix crash on open/create file. (Timothée Giet)
- FIX [#332367](https://bugs.kde.org/show_bug.cgi?id=332367): Add actions provided by KisLayerBox to the global action collection. This adds some missing actions to the keyboard configuration list. (Dmitry Kazakov)
- FIX [#334508](https://bugs.kde.org/show_bug.cgi?id=334508): Fix pixel-alignment of the Rectangle and Ellipse tools. (Dmitry Kazakov)
- FIX [#334408](https://bugs.kde.org/show_bug.cgi?id=334408): Fix a triangular brush outline for a 1px brush. (Dmitry Kazakov)

### Show axis in mirror mode

In Mirror mode the axis is now represented by a line. Axis display has two icons, one to show the type of mirror, vertical or horizontal, and a second one to edit the axis position by clicking and dragging.

[![Mirror axis canvas editable](/images/posts/2014/sm_w20_mirror-axis-edit_thumb.jpg)](/images/posts/2014/sm_w20_mirror-axis-edit.jpg)

### Add Background color to Palette

Palette now shows both Foreground and Background colors.

![Palette fg/bg colors](/images/posts/2014/sm_w20_palette-fgbg.jpg)

This work also adjusted the overall size and proportion of the palette elements to allow bigger preset icons, help recognize selected presets and provide more comfortable usage.

### Massive improvements in resource manager

Boudewijn Rempt has been busy providing a better experience on the resource manager. Aside from the many code optimizations and code clean up, boud worked to stabilize the manager to work seamlessly with Krita md5 tags internals. Also he coded a new dialog to make and export resource bundles. A previously manual labor, assembling brush presets, patterns sets, texture packs, brush tips sets; will be automatized with this new feature, making the task of sharing resources a breeze.

[![Bundle creator dialog](/images/posts/2014/sm_w20_bundle-dialog_thumb.jpg)](/images/posts/2014/sm_w20_bundle-dialog_thumb.jpg) [![Resource manager ui tweaks](/images/posts/2014/sm_w20_resource-manager_thumb.jpg)](/images/posts/2014/sm_w20_resource-manager.jpg)

## Krita Sketch and Gemini

Arjen Hiemstra and Dan Leinir Turthra Jensen have been busy fixing bugs and polishing Sketch and Gemini interface mostly. A new feature is the ability to see the mirror axis and adjust it using on screen ui buttons. These controls were also ported to Gemini and main Krita.

- Gemini: FIX [#334381](https://bugs.kde.org/show_bug.cgi?id=334381): Hide the "open existing as new" action. (Arjen Hiemstra)

## Code cleanup and optimizations.

Listing all optimization and cleanups from this week would result in a massive list. Some tasks done include: Remove unused methods and code, standardize code style and naming schemes, add tests cases and checks, close memory leaks, simplify code, rename libraries and many other small code-related tasks. Most optimizations are small but added together make the code not only easier to work with but also faster to run. Special thanks to Boudewijn Rempt for his hard work in this area.

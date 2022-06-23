---
title: "Krita 4.1 Release Notes"
date: "2018-06-13"
---

# Krita 4.1 Release Notes

Krita 4.1 is the second feature release in the Krita 4 series and is released only three months after 4.0. But there is still a heap of interesting new things and improvements to check out!

{{< youtube N6oHLuICrHM >}}

## Note!

We found a bug where activating the transform tool will cause a crash if you had selected the Box filter previously. if you experience a crash when enabling the transform tool in krita 4.1.0, go to your kritarc file ([https://docs.krita.org/en/KritaFAQ.html#where-are-the-configuration-files-stored …](https://docs.krita.org/en/KritaFAQ.html#where-are-the-configuration-files-stored "https://docs.krita.org/en/KritaFAQ.html#where-are-the-configuration-files-stored")) and remove the line that says "filterId=Box" in the \[KisToolTransform\] section. Sorry for the inconvenience. We will bring out a bug fix release as soon as possible.

## Reference images tool

Reference images are back in Krita... Now more powerful and useful than ever! No longer a docker with postage stamp-sized images, this is now a tool in the toolbox. Look for the pin icon in the same group as the assistant and ruler tools. With this tool, you can

- add multiple images at one time
- move one or multiple images around or outside the canvas
- scale and rotate each image
- control the opacity and saturation of each image.
- embed or link the reference images to your KRA file.

Take a look at the video Wolthera made to see the new [reference images tool](https://docs.krita.org/en/reference_manual/tools/reference_images_tool.html) in action:

{{< youtube LWpjlyUlBiA >}}

## Animation Improvements

More frame management options with animation: moving frames, adding frames, copying frames, and setting playback time. All these new actions can be assigned to shortcuts.

### Frame Actions

![](/images/pages/frame-actions.png)

### **Column Actions (affects multiple layers)**

![](/images/pages/column-actions.png)

 

### Improved animation timeline display

The [timeline](https://docs.krita.org/en/reference_manual/dockers/timeline.html) has been improved to better communicate how long a single frame is running, and when a frame is empty or not.

![](/images/pages/improved-animation-timeline.png)

 

### Animation cache swapping and performance setting area

Handle larger animations better by offloading the data to your drive instead of keeping all rendered frames in memory. To further assist playing back large animations, the new cache comes with a 'region of interest' setting. When the region of interest is enabled, Krita will only calculate areas that have changed on within the viewed area instead of the entire canvas. You will need both "Use region of interest" and "Limit cached frame size" enabled [in the performance settings](https://docs.krita.org/en/reference_manual/preferences/performance_settings.html#animation-cache) for it to take effect.

![](/images/pages/animation-options.png)

 

## Better color picking with new blending option

Inspired by how color mixing works in real life, you can now pick a [small amount of color to mix](https://docs.krita.org/en/reference_manual/tools/color_selector.html) with your existing color. Thanks to Emmet and Eoin O'Neill for contributing this patch.

{{< youtube D6_scO-rVgE >}}

## Improved vanishing point assistants and custom colors

Vanishing points can display reference lines where you can control the density. And you can control the [color of each assistant individually](https://docs.krita.org/en/reference_manual/tools/assistant.html#tool-options), while before all painting assistants shared one and the same color.

![](/images/pages/vanishing-point-assistant.png)

## Python 2 Support and updated packages

Jeroen Hoolmans has made it possible to build Krita with python 2, which is necessary for VFX studios that depend on a Python 2 pipeline. Note that the Linux appimage and the Windows builds use Python 3.

#### Updated packaged scripts

- The Krita Script starter got updated.
- The Comic Project Management tools got some major updates: rewritten page viewer for better drag and drop, pot extraction for translating comics, comic viewer improvements, and much better ACBF generation support and much much more. Check the manual in the Plugin Manager for the list of changes.

## Sessions and Window Layouts

Krita already had workspaces, which contained information about the location of dockers. However, those were per-window, and if you work with multiple monitors that is a bit limiting. So Krita 4.1 now introduces ‘[sessions](https://docs.krita.org/en/reference_manual/resource_management/resource_workspace.html#sessions)’ and ‘[window layouts](https://docs.krita.org/en/reference_manual/resource_management/resource_workspace.html#window-layouts)’.

Sessions remember your open windows and documents, allowing you to pick up again where you were previously. Krita can also automatically open your previous session upon startup or show the session manager for you to select one.

Window layouts extend on the idea of workspaces. However, instead of storing just the layout within a window, they can store multiple windows, their layouts, sizes and positions on the screen. They can be especially useful if you work with multiple monitors or changing configurations, such as a laptop and an external monitor.

Window layouts also come with two options to help working with multiple windows:

- ‘Show active image in all windows’. With this enabled any new image you open or switch to will appear in all windows. For example, to can keep an overview of the image on a secondary screen.
- ‘Primary workspace follows focus’. This option keeps your primary workspace on which ever window is currently active, swapping it across as the focus changes.

You can find the session manager via File -> Sessions, and window layouts via the Workspace dropdown on the toolbar.

## More RAW formats supported

Krita now accepts the following RAW formats: bay, bmq, cr2, cs1, dc2, dcr, dng, erf, fff, hdr, mdc, mos, mrw, nef, orf, pxn, raf, raw, rdc, sr2, srf, x3f, 3fr, cine, ia, kc2, mef, nrw, qtk, sti, rwl, srw. Thanks to L.E. Segovia for the patch!

## Faster Brushes: First Google Summer of Code Results

The Circular Gaussian and Soft Brush tips are now up to 10 times faster. Ivan Yossi's project to speed up the Gaussian and Softbrush tips with AVX shows its first results in this release.

## Cross Channel Adjustment Filter and color adjustment improvement

![](/images/pages/cross-channel-adjustment.png)

The [Cross Channel Adjustment filter](https://docs.krita.org/en/reference_manual/filters/adjust.html#cross-channel-color-adjustment) allow you to 'drive' a color adjustment by another channel. What can you do with this? For instance,

- increase the redness of only the lighter pixels
- desaturate everything but a single hue
- shift the hue on the darker pixels.

The Color Adjustment (curves) filter also now has support for Hue and Saturation curves on top of the existing channel, alpha and lightness curves.

## Better Debugging with new tablet tester

To make debugging tablet errors easier, we've copied Drawpile's Tablet Tester. This little dialog is accessible from [settings->configure Krita->tablet->tablet tester](https://docs.krita.org/en/reference_manual/preferences/tablet_settings.html#tablet-tester). It allows you to check if Krita can see your tablet at all. If it can't, you can sure you have a driver problem.

![](/images/pages/tablet-tester.png)

 

Miscellaneous improvements:

- Added context menu (right click) options for transform tool. This makes it easier to change your transform type between perspective, free, warp, etc.
- Added context menu (right click) options for crop. This makes it easier to use without needing the tool options open.
- New Cursor option. Force brush outline to always be shown at 100%
- HEIF file format can now be opened and saved to. Thanks to a patch by Dirk Farin. Note that this is not enabled in the default builds because the libraries needed to build the import/export filter are very new.
- Ask the user what DPI they want their SVG images imported with
- Multibrush tool now accepts decimals for the angle
- Fixes to links for new documentation site
- Fix for animation docker so closing the docker doesn't make the animation stuck on stop
- Improve text describing 8 bits/integer channel depth
- Update g'mic plugin to 2.3.0 (was at 2.2.0)

There are many bug fixes as well, but most of those were already released in the stable releases for Krita 4.0.

---
title: "First Krita 2.5 Beta"
date: "2012-06-23"
---

A milestone in development: this weekend, Cyrille Berger created a branch for Krita 2.5. And that means that 2.5 is around the corner already -- and we've barely recovered from the excitement of the 2.4 release! Still, plenty to be excited about in Krita 2.5.

Krita 2.5 will bring:

- the first version of textured brushes,
- the composition docker,
- the dulling mode in the color smudge brush,
- improved openraster compatility,
- more 32 bit floating point (HDR) colorspaces through lcms2 (and more blending modes and filters for 32 bit float rgba),
- improvements to the transform tool (use alt or meta to enable perspective transform!),
- updated paintop presets, with more presets for the hairy brush,
- support for selecting units in the rulers,
- shortcuts can now be set for tools and will be remembered after closing krita,
- brush rotation now is absolute to the canvas rotation,
- pdf import at high resolution is improved,
- visual improvements in rendering the image both in the normal and in the opengl canvas,
- assistants are saved in .kra files,
- on saving jpeg images with transparent parts, you get to chose which color will be used by default,
- all file filter dialogs remember their settings,
- the collapsed state of layers is saved to .kra,
- the full-screen setting is back and much improved (tab is the shortcut),
- improvements to the recovering of autosave files,
- lots and lots of usability and polish improvements thanks to the reporting by Antoine and Tom Hall,
- improved performance all around
- and much, much more...

Under heavy bug fixing development right now is a new interaction frameworks. Sounds abstract, I know, but it will make a huge difference: interactions like color picking, zooming, panning, rotating, brush resizing will now be uniformly available no matter which tool is selected, whether it's a vector tool or a paint tool. Cool work, done by Arjen Hiemstra and sponsored by KO GmbH.

Time to select a new splash screen!

You will be able to upgrade to 2.5 beta1 using the usual experimental repositories of your distribution. More news when I've got more detailed instructions.

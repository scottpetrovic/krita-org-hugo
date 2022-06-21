---
title: "Krita 2.8.3 Released"
date: "2014-05-15"
---

The third monthly bugfix release for Krita 2.8 is out! [Download your Windows installer](http://kritastudio.com/desktop.html) now, or get your distribution's updated packages! There are quite a few bugfixes and improvements:

- Translation fix in the Multihand tool: Axis -> Axes.
- More precise translations. (bug 333135)
- A fix for the outline of invert selection.
- Krita no longer closes immediately when a file is corrupted but gently warns the user.
- Fix bug: deleting Group-Layer and contents when there are no other layers prevented user from creating new layers (crash). (bug 333496)
- Improved detection of supported image formats.
- Removed a number of resource leaks.
- Add support for selection in GMIC filters. (bug 325771)
- Fix crash when GMIC filter is applied to the layer which was moved. (bug 327980)
- Add search box for filter names of the GMIC plug-in. A text box below the filters tree can now be used to find the GMIC filter by name.
- Select only paint layers when gathering all Krita layers from layer stack.
- Remember the last used preset across sessions.
- Fix invalid recalculation of width and height between units.
- Ensure that the channel flags are always reset when they are set to full, otherwise compositing will not be will work not efficient. (bug 333080)
- Fix painting grid on lower zoom levels. (bug 333234)
- Fix a triangular brush outline for a 1-pixel brush. (bug 334408)
- Fix pixel-alignment of the Rectangle and Ellipse tools, perform alignment exactly how the user expects. (bug 334508)
- Make layer actions such as "Delete the layer or mask" listed in the in Configure Shortcuts dialog. (bug 332367)
- Fix handling a tablet when "Pan/Scroll" mode is assigned to a button. Note: Wacom’s "Pan/Scroll" feature supports only vertical wheel scroll, so using usual Middle-button panning is recommended. (bug 334204)

---
title: "Krita 2.9.5 Released"
date: "2015-06-10"
---

The Kickstarter was a success, but that didn't keep us from adding new features and fixing bugs! We made quite a bit of progress including adding pass-through mode to group layers, allowing inherit alpha to be used on all layer types, better PSD support, and adding an on-canvas preview of the color being picked. We even added a new brush preset history docker! You can see the full release notes below.

**Krita 2.9.5 also fixes a critical bug in 2.9.4.7. Please upgrade if you experience crashes after restarting Krita.**

### New Features:

- Add a lightness curve to the per-channel filter (bug 324332)
- Add a brush preset history docker (bug 322425)
- Add an all-files option to the file-open dialog
- Add global light to the layer styles functionality (bug 348178)
- Allow the user to choose a profile for untagged PNG images (bug 345913, 348014)
- Add a built-in performance logger
- Added a default set of paintop preset tags (these are not deletable yet!)
- Add support for author profiles (default, anonymous, custom) to .kra files
- Add buttons and actions for layer styles to the Layer docker
- Add ctrl-f shortcut for re-applying the previously used filter (bug 348119)
- Warn Intel users that they might have to update their display driver
- Implement loading/saving of layer styles to PSD files
- Add support for loading/saving patterns used in layer styles
- Allow inherit alpha on all types of layers
- Add a pass-through switch for group layers (bug 347746, 185448)
- Implement saving of group layers to PSD
- Add support for WebP (on Linux)
- Add a shortcut (Ctrl-Shift-N) for edit/paste into New Image (bug 344750)
- Add on-canvas preview of the current color when picking colors (bug 338128)
- Add a mypaint-style circle brush outline.
- Split the cursor configuration into outline selection and cursor selection
- Add loading and saving transparancy masks to PSD groups

### Performance improvements:

- Remove delay on stroke start when using Krita with a translation

### Bug fixes:

- Fix view rotation menu by adding rotation actions
- Fix crash when duplicating a global selection mask (bug 348461)
- Improve the GUI for the advanced color selector settings (wrench icon on Advanced color selector)
- Fix resetting the number of favorite presets in the popup (bug 344610)
- Set proper activation flags for the Clear action (bug 34838)
- Fix several bugs handling multiple documents, views and windows (bug 348341, bug 348162)
- Fix the limits for document resolution (bug 348339)
- Fix saving multiple layers with layer styles to .kra files (bug 348178)
- Fix display of 16 bit/channel RGB images (bug 343765)
- Fix the P\_Graphite\_Pencil\_grain.gih brush tip file
- Fix updating the projection when undoing removing a layer (bug 345600)
- Improve handling of command-line arguments
- Fix the autosave recovery dialog on Windows
- Fix creating templates from the current image (bug 348021)
- Fix layer styles and inherit alpha (bug 347120)
- Work around crash in the Oxygen widget style when animations are enabled (bug 347367)
- When loading JPEG files saved by Photoshop, also check the metadata for resolution information (bug 347572)
- Don’t crash when trying to isolate a transform mask (transform masks cannot be painted on) (bug 347622)
- Correctly load Burn, Color Burn blending modes from PSD (bug 333454)
- Allow select-opaque on group layers (bug 347500)
- Fix clone brush to show the outline even if it’s globally hidden (bug 288194)
- Fix saving of gradients to layer styles
- Improve the layout of the sliders in the toolbar
- Fix loading floating point TIFF files (bug 344334)

**Downloads**

- Linux:
    - Distributions are expected to create packages for their bleeding edge repositories.
    - Ubuntu and derivatives can use Krita Lime, as usual: [https://launchpad.net/~dimula73/+archive/ubuntu/krita](https://launchpad.net/%7Edimula73/+archive/ubuntu/krita).
    - OpenSUSE users can the KDE:Extra repo: [http://download.opensuse.org/repositories/KDE:/Extra/](http://download.opensuse.org/repositories/KDE:/Extra/) or Leinir's OBS repositories which have Krita built with support for Vc (which makes painting faster):
        - [http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE\_13.1/](http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_13.1/)
        - [http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE\_13.2/](http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_13.2/)
        - [http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE\_Factory/](http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_Factory/)
- Windows and OSX
    - The [download page](https://krita.org/download/krita-desktop/ "Krita Desktop") has been updated, so check out the new builds.

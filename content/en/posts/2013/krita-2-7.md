---
title: "Krita 2.7 Released!"
date: "2013-08-02"
---

Only 5 months after we released Krita 2.6, we release Krita 2.7 today! There are a lot of cool new features, bug fixes and improvements. Soon to come to a Linux distribution near you.

The "highlights" of Krita 2.7:

- Rewritten and hugely improved transform tool.
- New line smoothing method for inking.
- Greyscale masks and selections.[![kritaSmoothTest](http://kritawebshopblog.files.wordpress.com/2013/07/kritasmoothtest.png?w=266)](http://kritawebshopblog.files.wordpress.com/2013/07/kritasmoothtest.png)

But there are more improvements:

- Brushes: the textured painting option has been added to many brushes, the darken brush option has a larger range, faster experimental brush engine with displacement option, the bug in the healing brush is fixed and we will have a smudge mode for the filter brush.
- Filters: HSL and colorize options are now available in tje HSV filter,  one can apply a curve to the alpha channel with Color Curves filter, a new user interface for an improved " color to alpha" filter that makes it possible to pick colors from the canvas directly
- Files: support for CMYK to PSD export filter, loading resolution for PSD images is fixed, it's now possible to importing a PSD image as a layer into an existing image, QML export (exports a all the top-level layers in the Krita image as image and creates a QML file where all the images are inserted as image objects) and [drag & drop of url’s](http://dimula73.blogspot.nl/2013/05/upcoming-krita-27-updated-drag-drop-and.html).
- Texturing: Image offset tool (for creating seamless textures to Krita).

\[embed\]https://www.youtube.com/watch?v=6DeyjO4JIEw\[/embed\]

- Tools: you can now finally type upper-case characters in the text tool, there are improvements to the move tool. The path tools are improved: the pencil tool integrates better with Krita, shapes can be stroked with a Krita brush, fix the transformation of path strokes.
- Canvas: the performance of the OpenGL canvas on Linux has been improved. For Krita 2.8, OpenGL comes to Windows, too.
- Docker: new composition docker (stack can be browsed with up and down arrow; the compositions can be exported in one go).
- Layer: new file-backed layers, improved transforming of paint and vector layers, it's now possible to mirror all layers in an image.
- Usability and interface:  improved zooming around cursor, two default workspaces (one for painting and one for working with vectors), now you can switch between favorite presets with left and right arrow keys and switch between current and previous shortcut with the / key, systems with multiple tablets and screens (for Cintiqs + classic tablet both connected to dual screen) now work fine, the display of marching ants around selection is improved, you can easily remove blacklisted resources from disk, you can select the most appropriate scale method, The Color button on the Krita toolbar opens the KDE color dialog which allows picking colors in other applications and selecting colors by numbers) and there's a menu action to select all opaque pixels in a layer -- check the right-click menu in the layerbox.

David Revoy has written an extensive Krita 2.7 guide with lots of screenshots and screencasts: [http://www.davidrevoy.com/article178/krita-2-7-a-guide-through-the-new-features](http://www.davidrevoy.com/article178/krita-2-7-a-guide-through-the-new-features)

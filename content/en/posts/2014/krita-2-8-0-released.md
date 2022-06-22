---
title: "Krita 2.8.0 Released"
date: "2014-03-04"
---

Today, the Krita team releases Krita 2.8. Krita 2.8 is a big milestone release, since this is the first release that is ready for end-users on Windows! Krita 2.8 has also many new features, hundreds of bug fixes, performance improvements, usability fixes and look-and-feel improvements. Let's join [David Revoy](http://www.davidrevoy.com) for a tour of...

### What's new in Krita 2.8?

![](/images/posts/2014/Krita_2.8_screenshot_with_its_mascot_Kiki.png)

Krita 2.8 running in [Trisquel GNU/Linux 6.0](http://trisquel.info/), showing the default interface. The character on the canvas is Kiki the Cyber Squirrel, Krita's Mascot.

_Author of screenshot and mascot: Tyson Tan_

### Krita 2.8 highlights:

#### Windows version

Krita 2.8 will be the first stable Krita release for Windows. We have been making experimental builds for Windows for about a year now, and a lot of testers helped us to stabilize it. While this is not really a new feature for the Linux user, the step and the work on it was so huge that it does merit the 1st rank in this feature list! Most work on the Windows port has been done by [KO GmbH](http://kritastudio.com), in cooperation with Intel.

_Development: Dmitry Kazakov, Boudewijn Rempt._

#### Better tablet support:

Krita has relied on Qt's graphics tablet support since Krita 2.0. We consciously dropped our own X11-level code in favour of the cross-platform API that Qt offered. And apart from the lack of support for non-Wacom tablets, this was mostly enough on X11. On Windows, the story was different, and we were confronted by problems with offsets, bad performance, no support for tablets with built-in digitizers like the Lenovo Helix.

So, with leaden shoes, we decided to dive in, and do our own tablet support. This was mostly done by Dmitry Kazakov during a week-long visit to Deventer, sponsored by the Krita Foundation. We now have our own code on X11 and Windows, though still based on Qt's example. Drawing is much, much smoother because we can process much more information and issues with offsets are gone.

![](/images/posts/2014/image14.jpg)

Photo: David Revoy testing Krita with four tablets.

_Development: Dmitry Kazakov, Boudewijn Rempt._

#### New high-quality scaling mode for the OpenGL canvas

Krita was one of the first painting applications with support of OpenGL to render the image. And while OpenGL gave us awesome performance when rotating, panning or zooming, rendering quality was lacking a bit.

That's because by default, OpenGL scales using some fast, but inaccurate algorithms. Basically, the user had the choice between grainy and blurry rendering.

Again, as part of his sponsored work by the Krita Foundation, Dmitry took the lead and implemented a high-quality scaling algorithm on top of the modern, shader-based architecture Boudewijn had originally implemented.

The result? Even at small zoom levels, the high-quality scaling option gives beautiful and fast results.

![](/images/posts/2014/image09.png)

_Image by Timothee Giet_

_Development: Dmitry Kazakov, Boudewijn Rempt._

#### Krita Gemini

On Linux, the Krita Sketch user interface is now bundled with Krita 2.8, and users can switch from one interface to another. Krita Sketch and Krita Gemini were developed by KO GmbH together with Intel. On Windows, Krita Gemini will be available through [Valve's Steam platform](http://steamcommunity.com/sharedfiles/filedetails/?id=225403385).

{{< youtube qiSGuCzRZFk >}}

{{< youtube lLwFJ0jF37s >}}

_Development: Arjen Hiemstra, Dan Leinir Turthra Jensen, Timothée Giet , Boudewijn Rempt_

#### Wrap Around mode

The Wrap Around mode (activate it with the W key, or in View > Wrap around mode) tiles the artwork on the canvas border for easy creation of tiled textures. It is only visualized in OpenGL mode (Settings > Configure Krita > Display).

![](/images/posts/2014/image06.png)

Development: Dmitry Kazakov.

#### New default presets, better tagging system

Krita 2.8 offer a new set of brush presets, with new icons following standards. Here is a screenshot with a sample of them.

Additionally, now It is easier and faster to assign tags to resources -- with a single right click.

![](/images/posts/2014/image11.png)

_Development: Sascha Suelzer_

_Resources: Timothée Giet, Ramon Miranda, Wolthera, David Revoy, and other Krita community artists._

#### Layer-picker

Directly select a layer by pressing the 'R' key and clicking with mouse/stylus on the canvas.

![](/images/posts/2014/image10.png)

_Development: Dmitry Kazakov._

_Icons: David Revoy_

#### Custom transparency checkboxes:

Transparency checkboxes represent the transparent colors. Now the colors and size of the checkboxes are configurable: You can change it in Settings > Preferences > Transparency Checkboxes. Here is a demo with a dark checker theme to show the halo around the Krita 256x256 \*.png logo:

![](/images/posts/2014/image05.jpg)

_Development: Boudewijn Rempt._

#### New palette docker

It’s now easier to switch palettes with the Palette docker. Adding and removing a color can be performed directly on the docker. A set of new palette presets made by talented authors are now also bundled with Krita by default. You can display the Palette docker via: Setting > Docker > Palette.

![](/images/posts/2014/image01.jpg)

_Development: Sven Langkamp_

_Resources: Tim Von Rueden, Spencer Goldade, Richard Fhager, Kim Taylor, David Revoy._

#### Pseudo Infinite canvas

If you scroll the canvas a lot in one direction, you’ll notice a big button appearing with an arrow on it on the border of the screen  A single click on this big button will extend the canvas automatically in this direction.

This feature will help you to focus on drawing and never worry about the drawing surface available.

![](/images/posts/2014/image12.png)

#### Additional options for the crop tool

The crop tool can now ‘grow’ (you can crop a document outside the canvas limit and extend the canvas) and also get decorations (third guidelines, middle crosshair).

![](/images/posts/2014/image02.png)

_Development: Camilla Boemann_

#### Better color pickers

The color pickers get new icons and more options.

- Ctrl + LeftClick --- Pick from merged image to Fg color
- Ctrl + Alt + LeftClick --- Pick from current layer to Fg color
- Ctrl + RightClick --- Pick from merged image to Bg color
- Ctrl + Alt + RightClick --- Pick from current layer to Bg color

You can change the shortcuts (like Alt) for the Color pickers in the Settings > Configure Krita > Canvas Input Settings and unfold ‘Alternate Invocation’.

_Development: Dmitry Kazakov, icons: David Revoy_

#### New Color balance filter

Color balance changes the overall colors of an artwork via sliders and is used for color correction. It’s an ideal filter to give an extra mood to your artwork (warmer, cooler) or enhance black and white studies. You can find the filter here: Filter > Adjust > Color balance (Ctrl+B)

{{< youtube Jos-2j4bgIE >}}

_Development: Sahil Nagpal, Dmitry Kazakov_

#### Initial support for G'mic

Use hundreds of famous Gmic filters directly in Krita. It’s a first implementation, and still experimental and unstable. Also, it does not yet take the selection into account and doesn't show a preview yet.

You can find the feature under the menu: Layer > Apply Gmic actions.

![](/images/posts/2014/image00.jpg)

_Development: Lukáš Tvrdý, David Tschumperlé._

#### Clone array tool

This new feature creates a number of clones of the current layer so you can paint on it as if the tiles were repeated. The feature is convenient for the creation of isometric tiles.

You can find the feature in Layer > Clone Array

Note that, ‘Clone layers’ child can be moved independently from the parent layer with the move tool. You can clone any base layer, and position them to your liking ; they keep the dynamic properties to the live clone.

{{< youtube IFKgqhTmM3w >}}

_Images, test and videos by Paul Geraskin._

Development: Dmitry Kazakov.

#### More custom shortcuts

Krita gets a new panel in the preferences (Setting > Configure Krita > Canvas Input Settings) to offer you the possibility to customize all related canvas shortcuts. That means: all the zoom- and color picker keys are configurable now.

![](/images/posts/2014/image04.jpg)

_Development: Arjen Hiemstra_

#### More compact, better looking

A lot of work was done to make the Krita 2.8 user interface more compact, and dim the saturation of the icons to let the user focus on the canvas.

![](/images/posts/2014/image07.jpg)

#### Other new Features:

- Make it possible to copy the projection of a group layer
- Make it possible to drop images on the startup page
- Isolate layer or mask: right-click on the layer or mask, select "isolate" and temporarily work only on that layer or mask.
- Make it possible to load ACT palette files
- Make the channel docker work on the image, not the individual layer
- Add a wraparound layer move mode

#### Removed Features

- OpenShiva filter and generator scripting language. This is replaced by the G'Mic plugin.

#### Improvements of old features

- Make it possible to end paths and selection paths with Shift-Click, Enter, Esc and clicking on a handle shown over the first point
- Improve the reference images docker
- Make predefined brush tips use a size parameter rather than scale
- Update the default brush presets largely (new icons, new presets, better organization)
- Make the fill layer command obey the alpha lock switch
- Make the PSD import filter ignore malformed resource blocks
- The resource tagging system has been hugely improved
- Implemented anisotropic spacing for the Krita brushes. Now if you change the 'ratio' option of the brush, the horizontal and vertical spacing will be relative to the width and height of the brush correspondingly.
- Added support for 16 bit color depths in Color Balance and Dodge and Burn Filter
- Improve painting of sharp corners with the Drawing Angle sensor enabled ("fan corners feature")
- Improve the UI of the Sobel Filter
- Add support for loading single-layer PSD Grayscale images
- Improve the image docker: displays a color picker when hover over the image in the docker, scale to fit filenames, use the theme highlight for the selected icons
- Use 'size' instead of 'scale' to scale the predefined brushes
- Make the fill tool obey the layer alpha lock state
- Rework the brush outline cursor and add a combined brush outline and dot or crosshair cursor mode. Brush outlines now also behave sensibly with very big and very small brushes.
- add option to hide preset strip and/or scratchpad in the brush editor
- Make it possible to copy the projection of a group layer to the clipboard
- Add the filter name to the filter layer or mask name
- Make it possible to drag and drop an image on the startup window
- Improve rendering of vector layers
- Apply thickness parameter to the hatching brush
- Add a shortcut (shift + Z) to undo points added to paths
- Allow the multibrush to use an angled axis and have an option to show the axis
- Improve mirroring of layers or masks (and make it four times as fast)
- Improve the layout of many dialogs: imagesize, layersize, phong bumpmap, canvas size, modify selection, jpeg and jp2 export
- Cut memory usage of pattern resources in half
- Cut runtime memory usage when switching predefined brushes
- Update the default workspaces, adding versions for high and low res screens
- Pixel and vector selections can be converted to each other
- Updated line smoothing algorithms
- Fix saving compositions
- New erase toggle icon
- Fix a memory leak when using the brightness/contrast curve
- Save resolution info to OpenRaster files
- Make handling custom input profiles more robust, also when updating (this should be the first 2.7.9.x release where you shouldn't need to remove the input settings folder)
- add a reset button to the input profile editor
- Fix wraparound mode for the selection painting tools
- Crop selection masks when activating the wraparound mode
- Fix painting the cursor outline when there is no cursor outline
- Make painting on high bit depth images much faste when the OpenGL canvas is enabled
- Fix updates of the canvas rulers
- Fix moving of a selection out of a layer
- Fix saving indexed PNG files with current versions of libpng
- Update to the latest G'Mic version and enable the G'Mic plugin on windows
- Make the G'Mic dialog resize when selecting a filter (fixes layout issues)
- Add a crash handler for Windows that uploads minidumps (the website that goes with it is not done yet!) and offers a clean restart

#### Optimizations

- Rewrite the OpenGL canvas: it's now much faster and more robust, as well as more extensible.
- Rewrite the tablet support to support non-wacom tablets on Windows and Linux and have better support for Wacom tablets. It is now possible to use multiple tablets (like Cintiq + Intuos) and issues with offsets are gone.
- Freehand lines are now much smoother and more precise
- Load all resources in the background, as soon as possible
- Fix memory leak when downscaling an image
- Fix memory leak when making selections
- Make painting gradients much faster
- Make selections much faster
- Painting with predefined brushes is 20% faster

The Krita 2.8 release has been made possible by:

- the [KDE project and community](http://kde.org/) which provided the infrastructure, the foundations and frameworks Krita has been built on as well as the community we are proud to be part of.
- the [Krita Foundation](http://krita.org/support-krita#general) which, supported by the Krita user community has been able to sponsor Dmitry Kazakov as a full-time developer on Krita during this development period. Consider joining the Develop Fund to make sure Krita's development will continue at its current break-neck pace!
- [KO GmbH](http://www.kritastudio.com), responsible for most of the work of making Krita work on Windows and providing commercial support for Krita users, as well as the Krita on Steam effort.

Many Linux distributions will offer Krita 2.8 in their backports repositories. Windows users can download [Krita 2.8 here](http://kritastudio.com/desktop.html), provided by KO GmbH.

###  Muses Training DVD

The best way to get to know Krita is through the Muses DVD! [Check out the contents](http://krita.org/item/216-muses), or order your copy now!

The regular price is € 32,50 including shipping.

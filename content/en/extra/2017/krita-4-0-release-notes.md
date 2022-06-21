---
title: "Krita 4.0 Release Notes"
date: "2017-07-21"
---

# Krita 4.0 release notes

With a complete rewrite of the vector layer file format, the addition of Python scripting, a new text tool and much more, Krita 4.0 is one of the biggest releases ever. There is so much to explore and enjoy! As a team, we're happy and proud to have reached this milestone and we're looking forward to build on Krita 4 for many releases to come!

Before we begin telling you about all the new and improved things, take a moment to read this warning:

**Krita 4 has a new file format for vector and text objects. Krita 4 tries to import Krita 3 and older files. Krita 3 and older will not be able to read vector and text objects saved by Krita 4. Because the new file format and the old file format are not 100% compatible, images with vector and text objects might look different in Krita 4. We recommend:**

- To _always_ keep a backup of your Krita 3 files before working on them in Krita4!
- In some cases, to convert your vector and text layers to raster layers before working on your old files in Krita 4!

Note that on all platforms it is possible to keep Krita 3 and Krita 4 running side by side. On Windows, use the zip archive downloads, on Linux the appimages and on OSX the disk images, dragged to some other place than Applications. Krita 4 and Krita 3 share settings and resources.

For 4.0, Tyson Tan has again created an awesome Kiki image. The Chinese plum blossoms symbolise overcoming hardship, so it's a very apposite image for the first major release of Krita after 2017's tribulations!

[![](../images/kiki_4.0_sm-1-1024x463.png)](https://krita.org/wp-content/uploads/2018/03/kiki_4.0_sm-1.png)

{{< youtube OXvHHJUyBDg >}}

Video by Owly Owlet

## SVG Format for Vector Tools

Krita 3.0 used the OpenDocument Graphics format (ODG) for vector shapes and paths. This was originally an office document file format and not a format designed for artistic work. ODG does not work well with other applications like [Inkscape](https://www.inkscape.org). We rebuilt our vector tools from the ground up in Krita to use SVG. SVG is a W3C standard that can be opened by many different programs. This is going to allow for more possibilities in the future with working with other applications. Currently, Krita supports most of the SVG 1.1 standard. In the future, SVG 2 will also be supported.

![](../images/vector-tools.gif)

In addition to converting the back-end to SVG we also added the following features:

- The gradient tool has been merged into the default tool for easier editing.
- Import and save SVG objects. KRA files, when opened as a ZIP, will have its vector layers stored in SVG.
- You can now copy-paste shapes from and to Inkscape directly.
- Boolean function to combine and intersect multiple vector objects. These are accessible from the new context menu (right click).
- The conversion to SVG also allowed us to fix a lot of vector object bugs from Krita 3.

## Vector Tools UX Improvements

We did more than just update the technology. We also spent a lot of time researching the workflow for vector artists and made an improved user experience for how the tools work. Scott Petrovic lead the discussion with artists and determined how the tools would look and operate.

One caveat is that we didn't have time to finish the pattern fill and SVG Filters features. We are working on that, though, and hope to have those features ready for Krita 4.1.

See the manual for more information on these changes [Shape Selection Tool Documentation](https://docs.krita.org/Shape_Selection_Tool), [Edit Shapes Tool Documentation](https://docs.krita.org/Edit_Shapes_Tool)

- The organization of the vector tool options has been improved. It is easy to switch between the type of fill, stroke, and transform properties.
- The shape editing tool is now always visible in the toolbox. In Krita 3 it was hard for a lot of people to tell where the shape editing tool was at.
- The shape editing tool has been polished. Parametric shape features are now shown in the tool options of this tool.
- Vector nodes have better visibility and improved visual feedback.
- All drawing tools that could draw on the vector layers now use the active color, brush size and opacity to draw the final shape.
- Vector layers can be directly exported to SVG via Layers → Import/Export → Export Vector Layer to SVG.
- Right-click on the canvas if a vector layer is active, will give a relevant submenu for the vector tools with more options.

![](../images/vector-library.gif)

## New Text Tool

One of the improvements funded by the 2016 kickstarter was a new text tool. With the goal of creating a tool that would be stable, dependable and simple to use, we made a lot of progress in Krita 4.0. External pressure made it impossible to implement everything we wanted for Krita 4.0, and we will be making more updates and adding new things to the text tool as the 4.x releases progress: line wrapping, fine typographic control, vertical text layout for Asian languages, as well as improvements in workflow are all still planned.

Check what is possible in the manual for [the text tool](https://docs.krita.org/Text_Tool).

![](../images/text-editor-features.gif)

Some of the changes and things you can do with the new text tools

- Uses SVG internally
- supports 90% of all SVG 1.1 text features except glyphs and rotation
- edit font size, line height, color, font weight, italics, and more
- The text editor popup supports entering bidirectional text
- The text editor popup has both a rich text editor panel as well as an SVG source editor panel where you can enter any SVG that is valid inside a text element.

## Python Scripting

The BIG stretch goal of last year's Kickstarter! You can now create scripts that create and manipulate images, add dockers and entries to the menu and much more. Note that this is the first release of Krita with scripting, so we're expecting lots of feedback from you all on what can be done with scripting and what not, and which part of the API works, and which part doesn't.

We also are including a large amount of scripts so you can see how it works for examples. In Krita's settings dialog, you can enable or disable Python plugins and check out the script's manual. Krita will need to be restarted for the python scripts to show up or be disabled.

Read this [in-depth overview of python scripting](https://docs.krita.org/Introduction_to_Python_Scripting) and the [Krita Python API documentation](https://api.kde.org/extragear-api/graphics-apidocs/krita/libs/libkis/html/index.html)!

### Python Plugin Manager

Manage which python scripts are active. Located via Settings->Configure Krita->Python Plugin Manager. Activated plugins can be accessed via the tools->scripts.

Note that on Windows 7 and 8 you need to install the Universal C Runtime separately. See the [manual](https://docs.krita.org/Introduction_to_Python_Scripting#Technical_Details).

We've taken several wishes from our forums and community and turned them into python scripts. Hopefully with these samples you can see the types of things you can accomplish with Python scripting. Creating these plugins also allowed us to test our own API. Let's take a look at some of them...

![](../images/python-plugin-manager.png)

### Included Scripts Highlights

![](../images/ten-brushes.jpg) **Ten Brushes** - Assign specific brush presets to shortcuts. You can do this with dragging and dropping the preset into the shortcut slots. Of course you can open the script up and modify how this works to your heart's desire!

![](../images/scripter.png) **Internal Scripting Console** - Run scripts while you are in Krita. Important for when you are testing things, or for when you just want to write a small script. The python editor is equipped with syntax-hightlighting and a small debugger to tell you when your code does not make sense. Created by Eliakin Almeida during his 2017 Summer fo Code project.

![](../images/quick-settings-docker.gif) **Quick Settings Docker** - Quickly change between brush sizes, opacity, and flow values... If you've used some other applications, this'll be familiar to you. Once enabled can be found from Settings > Dockers. Coded by Wolthera.

![](../images/comic-book-manager.png) **Comic Project Management Tools** - A robust plugin used for managing multiple pages for a comic project that Wolthera created. It is a great example for how to handle common tasks in pipeline scripts: opening, saving, cropping, scaling and batch changes. It even has custom exporting formats such as CBZ, EPUB, and ACBF. And the python files are abundantly documented to help you along the way and create your own pipelines!

## Colorize Mask Tool

Simplify coloring intricate line art such as comic art. With the new colorize mask layer, you can fill a line art with a few quick strokes...and have Krita figure out how to fill it in. The normal flow is to make your line art, switch to the Colorize Mask tool in the toolbox, then make some quick strokes in the area.

Press the Update button in the layers toolbox. The layer should update and fill everything in. You can either convert this later to a paint layer, or break it apart into color groups. See how it works in more detail from the manual: [Colorize Mask documentation](https://docs.krita.org/Colorize_Mask).

{{< youtube fIOhd3xXv-A >}}

## Background Saving

No more freezing while you wait while Krita auto-saves every 15 minutes. Not only do we have a background worker for saving documents, but also when exporting animations. This allows you to export a large animation then keep working while Krita keeps exporting the animation in the background. And exporting animations has been made faster by fully using all the cores on your CPU to calculate fames, too!

## New KPL Color Palette Format & Improved Palette Docker

![](../images/krita_4_0_palette.png)

The palette docker in Krita 3 can only handle 8bit sRGB. Our existing GPL color palette format was designed in a time when anything more seemed like decadence. We've taken the plunge and designed a new color palette file format. The KPL fileformat can store any color that Krita can handle. This new file format also allows you to group colors! The file format is made up of a ZIP file with an xml inside. (We are nothing if not consistent!)

The palette docker has also been improved with the following things:

- drag and drop support
- color renaming
- color grouping
- able to load Swatchbooker (SBZ) palettes (patch by L.E. Segovia)
- able to load Scribus XML palettes (patch by L.E. Segovia)

## Brush Editor Editor Improvements and Live Preview

We revamped the brush preset editor significantly to make it easier to use and understand. The brush editor has as preview area for you to see a live update as you are changing settings. This should make creating and editing brushes easier than only using the scratchpad. Note: There are a couple brush engines that do not have a preview because of technical limitations (shape and quick).

![](../images/live-preview.gif)

- Easily rename brushes. Look for the pencil icon in the brush editor
- Overwriting brushes now keeps the current preview image.
- Creating a brush brings up a new dialog that allows you to modify the preset image or load a custom image
- You can collapse/expand the presets, settings, and scratchpad areas. This was added to help people with smaller monitor sizes
- Added a set of curve presets when working with brush editor settings such as S curves. The buttons are underneath the curve area
- The effect of curves can now affect each other in different ways using different algorithms (seen at the bottom of the curve setting).
- When creating brush presets, there is a brush icon library that can be used as a base. These are resources that you can customize in the application's shared area.

## Performance Improvements with Multithreaded brushes

We are always trying to improve Krita's performance in every area. Last year's big performance project was multi-threading the pixel brush engine. Krita is now smart enough to let each of your computer cores calculate the dabs separately, and also have them work together. You can decide how many cores Krita will try to use for this in the performance settings! These changes only affect the pixel brush engine for now, but we can later expand this out to other engines like the color smudge.

Speaking of performance improvements, all brushes now have an "Instant Preview threshold" property. This probably sounds confusing, but this speeds up a lot of smaller brushes where Instant Preview didn't have any performance improvement. Instant Preview will automatically turn on when a brush's size gets big enough. You can right click the "Instant Preview" checkbox in the bottom of the brush settings to change this.

The work on multi-threaded brushes was sponsored by Intel.

## Larger Brush Sizes

![](../images/max-brush-size.png)

In Krita 3, there is a 1,000px brush size limit. In Krita 4, you can lift that limit through the configuration and make it go up to 10,000px! This change requires a restart to take effect. Be careful with the big sizes, as a 10,000 pixel brush is about as heavy as copy-pasting an image of 10kx10k at the bitdepth of the image you are painting on. Make sure your computer can handle that!

## Masked Brushes

![](../images/waterpaint.gif)

Add a mask to your brush tip to create even a greater variety of brushes. This started out as a Kickstarter stretch goal named 'stacked brushes'. Masked brush allows you to select a second brush tip, and define size, rotation, mirroring, scatter, and other properties to decide how it should blend with the main brush. You can also assign blending modes to your mask. The example here is using the Screen blending mode to create a watercolor appearance. See the [manual](https://docs.krita.org/Masked_Brush) for more information!

## Updated Brush Presets

We have updated our brush presets after feedback from a lot of artists. We have spent time trying to improve performance and add a greater variety of brush presets. Some of the new presets show off what the new masked brush properties can achieve like the watercolor brushes. Thanks goes out to David Revoy, Ramon Miranda, Wolthera, Pablo Cazorla, Rad, Scott Petrovic, and Razvan for their contributions. Also for all the people that took our brush presets survey and gave us ideas to make them even better. The final brush preset collection has been curated by David Revoy, whose [brush kit](http://davidrevoy.com/article319/krita-brushkit-v8) was used by more than two-thirds of respondents to the survey.

Krita 3's brushes bundle can be enabled in the resource manager dialog.

![](../images/new-brush-presets.png)

## Pixel grid

![](../images/pixel-grid-example.gif)

Andrew Kamakin added this cool new feature: you can now see a pixel grid when you zoom in past 800% (the zoom percentage and color are configurable). Great for precision art where it is hard to tell where pixels start and end.

The zoom percentage and color can be conigured in the Settings area.

## Isometric grids

Specify the angles and spacing for each axis to help with your isometric artwork. The grid area has an option for either Rectangular or Isometric grid options. There are also a few options for how they will display like color and style. This option is located in the grid docker.

![](../images/isometric-grid.gif)

## Improvements to the pop-up palette

![](../images/popup-palette-improvements.gif)

We have made a few changes to the pop-up palette after feedback

- A quick method for zooming with a slider
- A quick canvas rotation wheel around presets
- quick buttons for mirroring and canvas-only, and resetting zoom to 100%

## Painting Assistant Improvements

We have made the assistants much easier to use

- Improved rendering of the handles so they are easier to use for tablets.
- Ability to change the color and opacity for assistants in the tool options
- Fixes for loading and saving assistants

![](../images/assistants-opacity.gif)

## Filter Improvements

New and updated filters

- A new edge detection filter has been written. It supports multithreading(which means it works with filter layers as well as filter brushes), and has several options to choose between algorithms, strength and even a special toggle to let it be applied to the alpha channel for cool fringe effects. Manual: [Edge-detection](https://docs.krita.org/Edge_Detection)
- A height to normal map filter has been added using the same framework.
- Old edge detection and brightness/contrast curves have been removed.
- The gradient map filter has been changed to create gradients on the fly and now stores this filter properly inside the kra file.

## Resize thumbnails in presets docker and show brush size

![](../images/resize-icons.gif)

Easily resize your brush presets by the new slider. You can also quickly see a brush presets size to the right of a thumbnail now when you are in details mode

## Improved Warnings when Saving without layers

![](../images/krita_4_0_file_information_warning.png)

Often people will save their work to an unsuitable file format, losing layers (when you save as a png image) precision and layers (when saving as a jpg image) or more esoteric features like channel depth or vector objects. For Krita 4. we implemented a warning system that will inform you which features are present in the document but cannot be saved to the chosen file format. To be extra safe, the dialog also allows you to save a simultaneous copy as a native KRA file as well.

## New Darker Theme

![](../images/darker-theme.jpg)

Just in case you wanted Krita even darker

## Bug fixes/changes

 

- Layers

- File layers now can have the location of their reference changed.
- A convert layer to file layer option has been added, that saves out layers and replaces them with a file layer referencing them.
- FEATURE: let toggling SHOW IN TIMELINE for multilayer selection (BUG 377730)
- Fix crash with drag and drop mask with Ctrl key (BUG 389037)
- Show a warning when trying to paint on a clone layer (BUG 389570)
- Do not add imported layers to recent documents (BUG 389879)
- Do an exact match if threshold for color is set to 1 (BUG 385160)
- Fixed bug with selecting layer colors on hover (BUG 389560)
- Improved behavior when copying selection (BUG 389174)
- reorder and rename locks and visibility menu options in layer docker context menu to be more consistent
- Check all changed properties when doing undo/redo actions (BUG 389876)
- Fix crash when selecting multiple masks and pressing the properties button
- fixed resetting Instant Preview cache when changing visibility of layer (T6652)

- Brushes

- FEATURE: Brush Performance Monitoring. You can toggle this on from the settings under Performance.
- Intel GPUs will default to using the ANGLE software rendering. They were creating too many issues with OpenGL turned on.
- Implement kinetic scrolling in resource choosers
- Show brush sizes in the brush presets docker by thumbnail
- Give a notification when the current preset has changed with the next or previous shortcuts (D7454)
- Fixed reference counts with text brushes
- Fixed saving GBR files (BUG 382068)
- fixed selection area when changing between list and details in the brush preset docker.
- Fix erase mode not returning to brush mode when returning to the brush tool (BUG 380340)
- Disable the brush size shortcuts when the brush size slider is disaled (BUG379958)
- Brush preset names that contain an underscore character will display as a space on the UI
- Fix NaN values for bristle brushes (BUG 344437)
- label and visibility UI updates to brush smoothing, magnetism, and assistant tool options.
- Scale the fuzzy dab/stroke with Strength property and HSV options (BUG 387507)
- Set the name and validity of brush when copying it (BUG 388570)
- add a pressure/angle option to the hatching brush engine
- Removed the chalk brush engine. It was the base for other engines and is not needed
- Fixed rounding error in wrap around mode when painting (BUG 367943)

- Files

- Render animation UI has been updated to be easier to understand.
- FEATURE: Can export out different height, width, and FPS when rendering animations
- PSD: implement loading and saving of layer styles for group laters (BUG 387708)
- fixed saving/loading of the currently active node to kra files (T6542)
- fixed with nested auto-saves (T6542)
- Improve feedback when auto-saving document (T6542)
- fixed an issue with saving transparency to png and jpg file
- Fix crash when using Save Incremental or Save Backup (BUG 388927)
- Removed the ODG import feature (BUG 345312)
- Fix a delay before starting a stroke with a huge texture (BUG 386642)
- Fix a hangup when canceling exporting a PNG image (T7194)

- Filters and Blending Modes

- Add a "Hard Mix (Photoshop)" blending mode
- Added a logarithmic scale switch for the color adjustment filter
- Add an invert button to the levels filter
- fix bug with color to alpha filter when creating a mask (BUG 362626)
- Set minimum blur radius for filter to 1 (BUG389313)
- Only allow "apply filter again" when it can actually be done (BUG 389253)
- Do not crash if an export filter does not have a default configuration (BUG 383456)
- Added a reset button for the HSV adjustment dialog
- Added a reset button to the per channel filter
- Improve determining color format with color generator layers (BUG 390033)

- GUI

- Condensed the Configure Krita UI to make it usable for people with smaller monitor screens
- Allow document tabs to be movable/sort able (BUG 388268)
- File size and modified status appears in the title area for each tab
- The "document name" field was moved to the Content tab in the New File dialog
- Fixed a crash when closing one of the main windows showing the same document
- Fixed placeholder position of window title
- Change ruler subdivision display based on zoom level (388247)
- fixed correct set up of the canvas switched
- UI: Make the advanced color selector docker look disabled out if there are no documents open
- Improve how toolbox is resized with dragging and scrolling
- File dialog: check wither the suffix reflects the MIME type (BUG 388738)
- Make the color selectors a bit faster by improving the algorithm of checking IDs
- Splash image template update UI on loading Krita
- Sort the items in the fill layer drop-down box
- fixed workaround for switching subwindow to tabbed mode when one window is always on top
- Some fixes to icons changing when changing themes
- New application icon

- FEATURE: The variables vh and vw have been added to the numerical input, they represent the width and the height.
- Fix division result in the Algebra algorithms (BUG 389034)
- Fix a bug that caused the auto-scroll bars to get stuck on certain tools
- Fix crash when adding group to empty palette (BUG 388841)
- Fix logic for reading the swap file from configuration (BUG 389410)
- theme icons to the file new dialog with the various template types
- Avoid crashing when deleting a shortcut that doesn't exist (BUG 385662)
- Add icons for brush presets to the vector symbol library (T6478)
- attempt to restore OpenGL 2.1 support fo non-OSX systems (BUG 282281, 363770)
- fixed updating the shader when OCIO is activated after being deactivated
- fix a set of OCIO related bugs (BUG 373481)
- Fix leak due to cycling shared pointers
- SSE chipset speed up with handling division (8dc92f7dee7dc4e32e22724843669a25f444fa39)
- Don't set the swap directory to an empty string if the user pressed cancel
- Change the default author profile to Anonymous (T6627)
- Insert author widget at position zero (BUG 389877)
- Take into account multiplication when translating DPI to Krita internals (BUG 390337)
- Handle offset better when cropping image (BUG 390382)
- Fix a regression with delegated tools. (BUG 382690 )
- Reset screen rotation after probling QPA on OpenGL (BUG 390651)
- Add identify for UC-LOGIC based tablets on linux (BUG 363443)
- Windows: set OS and platform when reporting a bug

## Top Contributors

Since 3.0 was released we have had a lot of people helping out making Krita better. Here is a list of the top 10 contributors for Krita for 4.0. Information taken from github during the period from June 2016 through March 2018 sorted by commit count.

![](../images/boudewjin-40-github.png) **#1 Boudewjin Rempt** (IRC: boud)

- Maintainer of Krita
- Project management and finances, release communication
- setup nightly builds for Windows & Appimages
- Programmed text tool, Python support and API
- Programmed Python Scripts: Scripter, Ten Brushes

![](../images/dmitry-40-github.png) **#2 Dmitry Kazakov** (IRC: dmitryK)

- Programmed vector tools, text tools, masked brushes
- Programmed multi-threaded brushes, text tool
- Programmed background saving, Colorize mask

![](../images/wolthera-40-github.png) **#3 Wolthera van Hövell tot Westerflier ** (IRC: wolthera)

★ Volunteer

- Programmed Python scripts: Comics management, Palette Docker, Settings Docker
- Programmed Brush Tip creator, text editor, Python API, edge detection filter
- Documentation on docs.krita.org and forum support

![](../images/scott-40-github.png) **#4 Scott Petrovic** (IRC: scottyp2)

★ Volunteer

- UI design for vector tools, text tools, brush editor improvements, UI Polish
- Programmed brush editor improvements, assistants improvements, new dialog, preferences
- All design and programming for krita.org

![](../images/alvin-40-github.png) **#5 Alvin Wong** (IRC: windragon)

★ Volunteer

- Better tablet support for Windows devices like Surface Pro
- ANGLE support to improve graphics acceleration for low end systems
- Helped a lot of with Windows builds and setting up nightly Windows builds

![](../images/frederick-40-github.png) **#6 Frederic Gladhorn** (IRC: fregl)

★ Volunteer

Did a flurry of pointer fixes to improve memory management

![](../images/timothee-40-github.png) **#7 Timothee Giet** (IRC: animtim)

★ Volunteer

- Updated and added new icons for new dialog, brush engines, warning icons and tools
- cleaned up SVG elements

![](../images/allen-40-github.png) **#8 Allen Marshall**

★ Volunteer

contributed a new airbrush algorithm to give much better results

![](../images/eliakin-40-github.png) **#9 Eliakin Costa** (IRC: eliakincosta)

★ Volunteer

- Google Summer of Code student
- Programmed and improved multiple Python scripts
- Programmed some of Python API

![](../images/david-40-github.png) **#10 David Revoy** (IRC: deevad) Merged his brush presets into 4.0 and polished the existing set

## Artwork Made with Krita

![](../images/mod.png) MarrHero

![](../images/scoiattolottolo1.png) Elena Pollastri

![](../images/Dibujo-N°20.png) graffted1

![](../images/5-20170913-hippo.png) Jeremy Fries

![](../images/summer-A3.png) johan jaccob

![](../images/vampik-copy.jpg) Dorota Krzyżosiak

![](../images/gorillaSCR.png) kitsune09

![](../images/Earth-chan.jpg) Gelpat Lucas

![](../images/robot.png) Tomas Marek

![](../images/PTP09J1.png) Matteo Pescarin

![](../images/kinetics_1015_72dpi_rgb_v2.png) Mauricio Hunt

![](../images/bg1_1_wip6.png) Noitibmar Tibbs

![](../images/tribalFace.jpeg) Rakesh Chakraborty

![](../images/Owl_wide.jpeg) Shannen McMorrighan

![](../images/kiki4x.png) Ramskulls Art

![](../images/153-paint.png) Răzvan Rădulescu

![](../images/DV6fPpfXcAEoJH5.jpg) Rositsa 'roz' Zaharieva

![](../images/waves-storm.png) runend artworks

![](../images/death_sylviaritter_by_sylviaritter-dbqgaeq.png) Sylvia Ritter

![](../images/IMG_0116.jpg) Toby Willsmer

![](../images/carrot-deevad.jpg) David Revoy

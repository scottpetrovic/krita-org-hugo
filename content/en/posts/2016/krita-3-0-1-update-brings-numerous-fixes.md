---
title: "Krita 3.0.1: new features and bug fixes"
date: "2016-09-06"
---

Krita 3.0.1 is the first release after Krita 3.0. With the new release schedule we're trying to release every six weeks, with a combination of new features and bug fixes. This release already contains the first results of the 2016 Google Summer of Code projects, as well as kickstarter-funded features, the work of new contributors Eugene Ingerman, Nishant Rodrigues, Miroslav Talasek and Laurent Jospin and the work from students mentored by Dmitry: Grigory Tantsev and Alexey Kapustin.

{{< youtube 9S_x6koOVBo >}}

[Video by Nathan Lovato.](http://gdquest.com/)

### Tweak Brush settings in the pop-up palette

![oncanvas_brush_editor_3](/images/posts/2016/oncanvas_brush_editor_3.png)

Tweak your brush without having to go into the brush editor. Each brush engine has its own settings to tweak. Use the small arrow icon to toggle this on and off. You can even configure which properties are shown. [Read the documentation for more information](https://docs.krita.org/On_Canvas_Brush_Editor).

### Soft Proofing

![softproofing_gamutwarnings](/images/posts/2016/softproofing_gamutwarnings.png)

See how your artwork will look like when converting to CMYK. There is an additional "out of gamut" display to show you what color data will be getting lost. The first result of Wolthera's Google Summer of Code 2016 work! [Read the documentation](https://docs.krita.org/Soft_Proofing)

### Improved Mirror Tools

![mirror tool enhancements](/images/posts/2016/mirror-tool-enhancements.jpg)

Additional options for the mirror tools. Lock the position so you don't accidently move it. Hide the line so it doesn't get in the way while painting. Move to center if you accidently move it while painting. [See documentation](https://docs.krita.org/Mirror_Tools)

### Threshold and Wavelet Decompose Added

![wavelet_decompose](/images/posts/2016/wavelet_decompose.png)

Added a Threshold filter and a [Wavelet Decompose](https://docs.krita.org/Wavelet_Decompose) plugin. The wavelet decompose plugin was created by Miroslav Talasek.

### Quick Flip and Rotate buttons

![quick flip](/images/posts/2016/quick-flip.jpg)

Quickly flip or rotate your layers and selections with the free transform tool. No more -100% width transformations. Buttons exist for flipping vertical or horizontal, rotating clock wise or counter clock wise rotate.

### Improved Dockers

![histogram docker](/images/posts/2016/Histogram_docker.png)

We moved the Histogram area from the layers menu into its own [Histogram docker](https://docs.krita.org/Histogram_docker) so it always can stay on the screen. Greatly improved the visual quality of the overview docker so it looks better. The channels docker now shows thumbnails as well. This work was done by Eugene Ingerman. Thanks!

## Other New or Improved Features

- [Smarter input boxes that can accept simple maths!](https://docs.krita.org/Maths_input) Unit conversion is still coming! This feature was created by Laurent Jospin.
- Per-stroke fuzziness sensor, called "Fuzzy: Stroke", perfect for all those grassblades that need to be subtly different.
- Added ["Ratio" property](https://docs.krita.org/Parameters#Ratio) to the brush editor. This allows you to map the brush width and height aspect ratio to your pen. This feature was created by Nishant Rodriguez
- Gradient Maps can now be added as filter layers.
- New option to convert a group into an animated layer
- Added showing coordinates when using the Move Tool. Enable this feature from the tool options.
- Added [Japanese animation template](https://docs.krita.org/Japanese_Animation_Template_for_Krita) (by Saisho Kazuki)
- Snap free transform tool with the Shift key
- Improved Pixel 1 Preset
- Improved default onion skin settings to make it easier to use
- Use relative zooming so you zoom based off your cursor instead of the center of the screen
- Add ability to enter groups with PgUp/PgDown shortcuts
- Gray out sliders for disabled onion skin columns
- Added Breeze color themes
- re-organized the layers menu and layer context-click menu so they take up less space
- Improved verbiage for "paste to simple source" dialog. It is now called "Missing Color Profile". Added option to remember your selection.
- Visibility of status bar is now saved
- Show previous color in Advanced Colors Selector docker
- Retired the support for the little-used OpenJPEG export format. (Note: this has _nothing_ to do with JPEG support!)
- There is an optional button available for the toolbars to switch pressure sensitivity off and on (patch by Grigory Tantsevov)

## Fixes

- Fix sharp corners when drawing circles with the stabilizer on Windows
- Fix drag & drop slow down with layers
- Added Full screen functionality back
- Fix crash when dragging and dropping transform mask
- Fix crashes with some tablet manufacturers when you try to paint
- Fix crash when duplicating a file layer
- Fix double dots in the file name when saving
- Fix crash when loading multi layer EXR files
- Fix crash with saving layer group
- Fix: Switch off 'canvas only mode' before closing the main window. It made restarting krita get in an odd state.
- Fix crash when moving a hidden layer with the arrow keys
- Fix Clone tool crash when when using Ctrl + left mouse button
- Fix Onion skin build up issue when changing frames
- OSX: fixed some touchpad issues
- OSX: fix brush freeze with Wacom after lifting stylus from canvas
- OSX: Fixed 100% opacity blobs at the start of a line
- Fix some part of the application not changing to the appropriate language
- Fix crash when editing a macro that contains a filter layer
- Fix memory issue when closing and opening new images
- 3\_texture brush tip has been fixed to use alpha
- Fix assistants so previews can be hidden and shown
- When using the deform transform tool, moving now takes the rotation of the canvas into account
- Fix saving templates
- Fix loading images with uppercase suffix
- Fix HSL/HSV adjustment filter with Colorize displaying wrong hue value
- Fix to make feather selection work again (thanks Spencer Brown)
- Some display issues (black screens) when using assistants on NVida GPU’s have been fixed
- Fix brush preset layout after changing tags and hiding scrollbars
- Fix a crash when the resource selector tries to display a deleted resource
- Fix using the threshold filter as a mask and the threshold filter preview for colorspaces other than 8 bits RGBA
- Fix initializing tool options when Krita starts
- Change range for inner and outer glow layer styles to 1 to 100
- Update the default workspace set
- When saving pixels outside of the layer will be cropped
- Fix incorrect offset when loading first animation frame
- Fix exporting animations to the CSV format
- Brush composite action has name in the toolbar config now
- Uncheck the PNG profile embedding option by default.
- Disable the system monitor check if colord doesn't give us devices
- Make Nearest Neighbour filtering mode work properly
- Add the decoration back for the horizontal and vertical mirror tools
- Don't put 100% pressure blobs at the start of some lines
- Don't allow painters remove the automatically generated gradients: They are special!
- Brush preset tags load again on Windows and OSX

##  Download Links

Visit the [Download page](/download/krita-desktop/) to grab the new builds. While you are downloading the new version, check out this amazing video that Achille made using Krita's animation features.

 

https://twitter.com/\_Achille\_/status/747493119243980802

#### Windows

On Windows, Krita supports Wacom, Huion and Yiynova tablets, as well as the Surface Pro series of tablets. The portable zip file builds can be unzipped and run by double-clicking the krita link.

Krita on Windows is tested on Windows 7, Windows 8 and Windows 10. The x86 Windows builds can be slower than usual because vectorization has been disabled.

**There is a known issue that the default templates do not show up. This will be fixed in a patch release.**

- [krita-3.0.1-x64-setup.exe](http://files.kde.org/krita/3/windows/krita-3.0.1-x64-setup.exe)
- [krita-3.0.1-x86-setup.exe](http://files.kde.org/krita/3/windows/krita-3.0.1-x86-setup.exe)
- [krita-3.0.1-x64.zip](http://files.kde.org/krita/3/windows/krita-3.0.1-x64.zip)
- [krita-3.0.1-x86.zip](http://files.kde.org/krita/3/windows/krita-3.0.1-x86.zip)

#### Linux

For Linux, we offer [AppImages](http://appimage.org/) that should run on any reasonable recent Linux distribution. You can download the appimage, make it executable and run it in place. No installation is needed. At this moment, we only have appimages for 64 bits versions of Linux. This appimage has experimental desktop integration.

- [krita-3.0.1-x86\_64.appimage](http://files.kde.org/krita/3/linux/krita-3.0.1-x86_64.appimage)

You can also get Krita from [Ubuntu’s App Store in snap format](https://uappexplorer.com/app/krita.krita). This version includes the translations for Krita itself. Install with

snap refresh --stable krita (if you've installed the beta)
snap install krita (if not)

#### OSX and MacOS

Krita on OSX will be fully supported with version 3.1. Krita 3.0 for OSX is still missing Instant Preview and High Quality Canvas scaling. There are also some issues with rendering the image — these issues follow from Apple’s decision to drop support for the OpenGL 3.0 compatibility profile in their display drivers and issue with touchpad and tablet support. We are working to reimplement these features using OpenGL 3.0 Core profile. For now, we recommend disabling OpenGL when using Krita on OSX for production work or selecting nearest-neighbour scaling.

Krita for OSX runs on 10.9, 10.10, 10.11 and is reported to work on MacOS too.

**There is a known issue that the default templates do not show up. This will be fixed in a patch release.**

- [krita-3.0.1.dmg](http://files.kde.org/krita/3/osx/krita-3.0.1.dmg)

You can also download the **experimental** build that has the new OpenGL Core Profile code that enables wraparound mode, High Quality Scaling and all other OpenGL features on OSX. It is **not** the official 3.0.1 release and does **not** have any translations:

- [krita-3.0.1-nimmy2.dmg](http://files.kde.org/krita/3/osx/devbuilds/krita-3.0.1-nimmy2.dmg)

See this [post for more information](/item/experimental-osx-build-available/) and how to report your findings.

#### Source

The source tarbal contains all translations.

- [krita-3.0.1.tar.gz](http://files.kde.org/krita/3/source/krita-3.0.1.tar.gz)

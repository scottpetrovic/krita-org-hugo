---
title: "4.0 Development Update"
date: "2017-11-06"
---

And then we realized we hadn't posted news about ongoing Krita development for some time now. The main reason is that we've, well, been really busy doing development. The other reason is that we're stuck making fully-featured preview builds on OSX and Linux. More about that later...

So, what's been going on? Some of the things we've been doing were backported to Krita 3.2 and 3.3, like support for the Windows 8 Pointer API, support for the ANGLE Direct3D display renderer, the new gmic-qt G'Mic plugin, new commandline options, support for touch painting, the new smart patch tool, new brush presets and blending modes... But there is also a lot of other work that simply couldn't be backported to 3.x.

The last time we did a development update with Krita 4.0 was in June 2017: the [first development build for 4.0](/item/first-development-builds-for-krita-4-0/) already had a large number of new features:

- the SVG-based vector layers with improved vector handling tools,
- Allan Marshall's new airbrush system,
- Eugene Ingerman's healing brush,
- a new export system that reports which parts of your image cannot be saved to your chosen file format: and that is **now** **improved: saving now happens in the background**. You can press save, and continue painting. Autosave also doesn't interrupt your painting anymore.
- Wolthera's new and improved palette docker
- A new docker for loading SVG symbol collections, Which now comes with **a new symbol libary with brush preset icons.** Perfect with the new brush editor.
- We added Python scripting (only available in the Windows builds: we need platform maintainers). Eliakin and Wolthera have spent the summer adding great new python-based plugins, extending and improving the scripting API while working:
    - Ten brushes: a script to assign ten favorite brushes to hotkeys
    - Quick settings docker: with brush size, opacity and flow
    - Comic Projects Management tools
    - And much, much more

## What has been recently added to Krita 4.0

### Big performance improvements

After the development build release we sent out a user survey:  In case you didn't see the results of our last survey this was the summary.

![](../images/gripes.png)

The biggest item on the list was lag. Lag can have many meanings, and there will always be brushes or operations that are not instant. But we had the opportunity the past couple of months to work on an outside project to help improve the performance of Krita. While we knew this might delay the release of Krita 4.0, it would be much appreciated by artists. Some of the performance improvements contain the following:

- multi-threaded performance using all your CPUs for pixel brush engines (80% of all the brushes that are made).
- A lot of speed optimizations with dab grouping for all brushes
- more caching to speed up brush rendering across all brushes.

Here's a video of Wolthera using the multithreaded brushes:


{{< youtube wnPUtYo2Y9Y >}}

### Performance Benchmarking

We also added performance benchmarking. We can see much more accurately how brushes are performing and make our brushes better/optimized in the future:

![](../images/performance-benchmarking.gif)

 

 

### Pixel Grid

Andrey Kamakin added an option to show a thin grid around pixels if you zoom in enough:

![](../images/pixel-grid-example.gif)

### Live Brush Preview

Scott Petrovic has been working with a number of artists to rework the brush editor. There have been many things changed including renaming brushes and  better saving options.  There's also a live stroke preview now to see what happens when you change settings. Parts of the editor can be shown or hidden to accommodate for smaller monitors.

![](../images/live-preview.gif)

### Isometric Grid

The grid now has a new Isometric option. This can be controlled and modified through the grid docker:

[![](../images/isometric-1024x715.png)](https://krita.org/wp-content/uploads/2017/11/isometric.png)

## Filters

- A new edge detection filter
- Height to normal map filter
- Improved gradient map filter
- A new ASC-CDL color balance filter with slope, offset and power parameters

### Layers

- File layers now can have the location of their reference changed.
- A convert layer to file layer option has been added that saves out layers and replaces them with a file layer referencing them.

### Dockers

- A new docker for use on touch screens: big buttons in a layout that resembles the button row of a Wacom tablet.

### More

And there's of course a lot of bug fixes, UI polish, performance improvements, small feature improvements. The list is too long to keep here, so we're working on a [separate release notes page](/krita-4-0-release-notes/). These notes, like this Krita 4.0 build, are very much a work in progress!

### Features currently working on

There are still a number of features we want to have done before we release Krita 4.0:

- a new text tool (we have started the ground work for this, but it still needs a lot more work)
- a faster colorize mask tool (we need to make this much faster as it is currently too slow)
- stacked brushes where you can have multiple brush tips similar to other applications.

And then there are no doubt things missing from the big new features, like SVG vector layers and Python scripting that need to be implemented, there will be bugs that need to be fixed. We've made packages for you to download and test, but be warned, there are bugs. And:

_**This is pre-alpha code. It will crash. It will do weird things. It might even destroy your images on saving!**_

_**AND: DOCUMENTS WITH VECTOR LAYERS SAVED IN KRITA 4.0 CANNOT BE EDITED IN KRITA 3.x!**_

You can have both Krita 3 and Krita 4 on the same system. They will use the same configuration (for now, that might change), which means that either Krita 3 or Krita 4 can get confused. They will use the same resources folder, so brush presets and so on are shared.

### Downloads

Right now, all releases and builds, except for the Lime PPA, are created by the project maintainer, Boudewijn Rempt. This is not sustainable! Only for the Windows build, a third person is helping out by maintaining the scripts needed to build and package Krita. We really do need people to step up and help maintain the Linux and macOS/OSX builds. This means that:

- The **Linux AppImage** is missing **Python scripting** and **sound** **playback**. It may be missing the QML-based touch docker. We haven't managed to figure out how to add those features to the appimage! The appimage build script is also seriously outdated, and Boudewijn doesn't have time to improve it, next to all the other things that need to be done and managed and, especially, coded. **We need a platform maintainer for Linux!**
- The **OSX/macOS DM****G** is missing Python scripting as well as PDF import and G'Mic integration. Boudewijn simply does not have the in-depth knowledge of OSX/macOS needed to figure out how to add that properly to the OSX/macOS build and packages. Development on OSX is picking up, thanks to Bernhard Liebl, but **we need a platform maintainer for macOS/OSX!**

#### Windows Download

Note for Windows users: if you encounter crashes, please follow [these instructions](https://docs.krita.org/Dr._Mingw_debugger) to use the debug symbols so we can figure out where Krita crashes.

There are no 32 bits Windows builds yet. There is no installer.

- Portable 64 bits Windows: [krita-4.0.0-prealpha.2c.zip](https://download.kde.org/unstable/krita/4.0.0-prealpha.2/krita-4.0.0-prealpha.2c.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/unstable/krita/4.0.0-prealpha.2/krita-4.0.0-prealpha.2c-dbg.zip)

#### Linux Download

- 64 bits Linux: [krita-4.0.0-pre-alpha-x86\_64.appimage](https://download.kde.org/unstable/krita/4.0.0-prealpha.2/krita-4.0.0-pre-alpha-x86_64.appimage)

(If, for some reason, Firefox thinks it needs to load this as text: to download, right-click on the link.)

#### OSX Download

- OSX disk image: [krita-4.0.0-prealpha.2b.dmg](https://download.kde.org/unstable/krita/4.0.0-prealpha.2/krita-4.0.0-prealpha.2b.dmg)

Note: the gmic-qt and pdf plugins are not available on OSX.

### Source code

- Source code: [krita-4.0.0-prealpha.2.tar.gz](https://download.kde.org/unstable/krita/4.0.0-prealpha.2/krita-4.0.0-prealpha.2.tar.gz)

#### md5sums

For all downloads:

- [md5sums.txt](https://download.kde.org/unstable/krita/4.0.0-prealpha.2/md5sums.txt)

#### Key

The Linux appimage and the source tarball are signed. You can retrieve the public key over https here: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8). The signatures are [here](http://download.kde.org/unstable/krita/4.0.0-prealpha.2/).

#### Support Krita

Krita is a free and open source project. Please consider supporting the project with [donations](/support-us/donations/) or by [buying training videos or the artbook!](/support-us/shop) With your support, we can keep the core team working on Krita full-time.

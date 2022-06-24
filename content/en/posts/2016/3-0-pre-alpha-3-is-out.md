---
title: "3.0 Pre-alpha 3 is out!"
date: "2016-03-14"
---

Today was an important day for the Krita project! We entered _feature freeze_! That means that from now on until the release of Krita 3.0, which is planned for April 27th, we won't be working on adding new features, but we'll be fixing bugs, fixing bugs and fixing more bugs! If you want to help us identify and triage bugs, read this article: "[Ways to Help Krita: Bug Triaging](/posts/ways-to-help-krita-bug-triaging/)". It's the first of what's intended to be a series of reference articles on ways to help Krita grow and become better and better.

Since Krita 3.0 is frozen, we know exactly which Kickstarter and Stretch Goal features will be in this release, and which features will be in the 3.1 and following releases. Krita 3.0 will have: Instant Preview, Animation Support, Rulers and Guides, Grid Docker, layer multi-selection handling improvements, loading and saving Gimp brushes as images, and a completely revamped layer management panel! As an extra, originally not part of the Kickstarter Stretch Goals, snapping to guides and grids has also been implemented! Work has already started on the on-canvas brush settings editor (HUD), stacked brushes brush engine and the lazy brush or (anime coloring) tool.

And additionally, Krita 3.0 has been ported to Qt5, which was in itself a huge task, much bigger than we had even imagined. We intend to make Krita 3 fully supported on OSX, too, but that still needs a lot of work. And there are a ton of features that weren't part of the Kickstarter, of course. Volunteers from all over the world have been adding cool new stuff. We're really dreading writing the full release announcement for April!

Anyway... Here are the highlights compared to the last [pre-alpha build](/posts/krita-2-9-11-and-the-second-3-0-alpha-build/):

### Improved Layer Docker

A stupendous amount of work has gone into the layer docker's new load, one of the 2015 Kickstarter stretch goals!

- More condensed and clean looking to make it easier to use.
- Layers can have colors be associated with them. You can later filter the layers by color.
- A lot of new shortcuts for grouping, moving, and working with multiple layers.
- Ctrl+Alt+G now quick ungroups layers! (Not in the video below)

See Nathan Lovato's overview for all the features: 

<iframe src="https://www.youtube.com/embed/uGiucAklXXc" width="560" height="315" frameborder="0" allowfullscreen="allowfullscreen"></iframe>

### Updated Grid Handling

We removed the Grid Tool... And created a new grid docker that exposes all the grid and guide settings. This makes it much easier and logic to work with and edit your grids. Krita's grid handling has been streamlined by removing the perspective grid tool (you can find a much more powerful perspective grid in the assistants) and the snap settings docker is gone...

 

[![gridsguidessnapping](/images/posts/2016/gridsguidessnapping-1024x569.png)](/images/posts/2016/gridsguidessnapping.png) ... To be replaced by the Snap Settings pop-up(on shift+S)!

### Snapping

Snapping to grids and guides wasn't part of the original plan, and we were even considering making it a 2016 Kickstarter stretch goal, but we implemented snapping for all vector, selection and raster tools! Well, with the exception of the distance measurement tool and the freehand tools, like the freehand brush tool, multibrush, dynabrush, and freehand path tools.

## Export filters

There are two new export filters:

- A [Spriter](https://brashmonkey.com/) exporter! We've worked together with BrashMonkey to create a new export filter to create sprite maps from Krita images. Based on the Photoshop plugin, this filter is still in its early stages. Plenty of known bugs, but very promising.
- Compatible with TV-Paint, Fazek created a new export filter that can generated CSV-based layered animation projects

### Gradient Map Filter

Turn your greyscale artwork into color with a gradient map filter.  This wasn't planned to be done, but we had a surprise special guest hacker Spencer Brown who submitted this feature out of the blue! Thank you Spencer! For the future, we want to make it possible to use the Gradient Map filter as a filter layer, but that isn't possible yet.

![gradientmapfilter](/images/posts/2016/gradientmapfilter-1024x635.png)

### The "Greater" Blending Mode

[![greaterblendmode](/images/posts/2016/greaterblendmode.gif)](/images/posts/2016/greaterblendmode.gif) Nicolas Guttenberg implemented the "Greater" blending mode to make it easier to create semi-transparent strokes.

### Move Tool

There are still known bugs in the move tool, but it also got a really nice additional feature: Move Increment Multipliers for the Move Tool. (Accessible with shift+arrow keys)

### Other Tools

The Crop tool, Assistant editing tool and the Straight line tool got an improved user interface, and the Straight line tool's on-canvas preview has been improved as well.

[![Screenshot from 2016-03-12 18-15-58](/images/posts/2016/Screenshot-from-2016-03-12-18-15-58-1024x691.png)](/images/posts/2016/Screenshot-from-2016-03-12-18-15-58.png)

### More...

And there are more and more improvements

- Shortcut settings have been moved to sit with the other settings
- The steps for the lighter/darker and similar hotkeys can now be configured in the settings.
- The HSY selector's Gamma can be configured in the settings!
- New cursor options: single pixel black and white, for those who REALLY need precision.
- Pixel art brush presets
- And many, many, many bugsfixes!

### Next

The next time we release, we'll call it a Real Alpha Release! We also intend to make development builds available every week. They'll end up in [files.kde.org/krita/3/](http://files.kde.org/krita/3), with weird version numbers including git hashes for extra confusion, that is, to make it easier to figure out what exactly went into the build. And we'll try to package the brand new [Krita Shell Extension](https://github.com/alvinhochun/KritaShellExtension) by Alvin Wong for Windows. Finally your .kra files will have thumbnails in Explorer. And we'll fix bugs. And fix bugs. And fix some more bugs!

### Downloads

(If you're wondering about the version numbering... This is Krita 3, it's pre-alpha, so it's not even alpha yet, but a development build. It's the third pre-alpha we make available (and the last) and the weird string of numbers and letters makes it possible to figure out exactly which version of the source code we built.)

**Windows**

- [krita3-prealpha3-de0d43d.zip](http://files.kde.org/krita/3/windows/krita3-prealpha3-de0d43d.zip)

Download the zip file. [Unzip the zip file where you want to put Krita.](http://windows.microsoft.com/en-us/windows-10/zip-and-unzip-files#v1h=tab02).

Run the vcredist\_x64.exe installer to install Microsoft’s Visual Studio runtime. (You only need to do this once.)

Then double-click the krita link.

Known issues on Windows:

- The issue where Krita would show a black window if OpenGL is enabled on certain Intel GPU + driver combinations should be fixed now.
- The spriter export plugin may not be found.

**OSX**

- [krita3-prealpha3-de0d43d.dmg](http://files.kde.org/krita/3/osx/krita3-prealpha3-de0d43d.dmg)

Download the DMG file and open it. Then drag the krita app bundle to the Applications folder, or any other location you might prefer. Double-click to start Krita.

Known issues on OSX:

- We built Krita on El Capitan. The bundle is tested to work on a mid 2011 Mac Mini running Mavericks. It looks like you will need hardware that is capable of running El Capitan to run this build, but you _do not have to have_ El Capitan, you can try running on an earlier version of OSX.
- You will **_not_** see a brush outline cursor or any other tool that draws on the canvas, for instance the gradient tool. This is known, we’re working on it, it needs the same fix as the black screen you can get with some Intel drivers on Windows. Basically, we need to port a core chunk of Qt functionality to a new version of OpenGL because Apple refuses to implement the OpenGL compatibility profile in their drivers.

**Linux**

- [krita3-prealpha3-de0d43d-x86\_64.appimage](http://files.kde.org/krita/3/linux/krita3-prealpha3-de0d43d-x86_64.appimage)

For the Linux builds we now have AppImages! These are completely distribution-independent. To use the AppImage, download it, and make it an executable in your terminal or using the file properties dialog of your file manager. Another change is that configuration and custom resources are now stored in the .config/krita.org/kritarc and .local/share/krita.org/ folders of the user home folder, instead of .kde or .kde4.

Known issues on Linux:

- Your distribution needs to have Fuse enabled
- On some distributions or installations, you can only run an AppImage as root because the Fuse system is locked down. Since an AppImage is a simple iso, you can still mount it as a loopback device and execute Krita directly using the AppRun executable in the top folder.

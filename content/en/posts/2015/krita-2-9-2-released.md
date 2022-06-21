---
title: "Krita 2.9.2 Released"
date: "2015-04-02"
---

It's April! We've got another bug-fix and polish release of Krita! Here are the improvements:

- Make the eraser end of the stylus erase by default
- Make krita remember the presets chosen for each stylus and stylus end
- Don't show the zoom level on-canvas message while loading
- Fix initialization of the multi-brush axis
- Add some more kickstarter backers to the about box
- Fix memory leak when loading presets (and a bunch more memory leaks)
- Fix crashes related to progress reporting when running a g'mic action
- Add a toggle button to hide/show the filter selection tree in the filter dialog
- Fix a focus bug that made it hard to edit e.g. layer names when activating the editor in the docker with a tablet stylus
- Fix geometry of the toolbox on startup in some cases
- Fix lock proportions in the free transform tool when locking aspect ratio
- Add an option to hide the docker titlebars
- Update the resource manager lists after loading a resource bundle
- Make the resource manager look for bundles by default
- Make Krita start faster by only loading images for the references docker when the references docker is visible
- Fix a crash in the g'mic docker when there's no preview widget selected
- On switching images, show the selected layer in the layer box, not the bottom one
- Show the selected monitor profile in the color management settings page instead of the default one
- Make the Image Split dialog select the right export file type.
- Fix saving and loading masks for file layers
- Make the default MDI background darker
- Fix loading some older .kra files that contained an image name with a number after a /
- Don't crash if the linux colord colormanager cannot find a color-managed output device
- Clean the code following a number of PVS studio code analyzer warnings
- Add tooltips to the presets in the popup palette
- Fix a problem where brush presets in the popup palette were sometimes misaligned
- Fix loading most types of images in the reference docker on Windows

Most work in the past month has gone into the Qt 5 port (Krita now starts, yay! But it doesn't work yet...) and most of all the Photoshop-style Layerstyle feature. We've got most of the effects implemented, most of the dialog box, too -- only the contour selector, the style library selector and the blending mode page is still missing. Loading and saving is still to be done.

But here's a _teaser_ screenshot of of a layer style on a _vector_ layer (layer styles work on all types of layers, paint layers, vector, group, clone, file...)

 

[![layerstyle](images/layerstyle-1024x314.png)](https://krita.org/wp-content/uploads/2015/04/layerstyle.png)

We hope the loading and saving will be ready in time for 2.9.3!

**Note on G’Mic on Windows**: Lukas, David and Boudewijn are trying to figure out how to make G’Mic stable on Windows. The 32 bits 2.9.1 Windows build doesn’t include G’Mic at all. The 64 bits build does, and on a large enough system, most of the filters are stable. We’re currently trying different compilers because it seems that most problems are causes by Microsoft Visual Studio 2012 generating buggy code. We’re working like crazy to figure out how to fix this, but please, for now, on 64 bits Windows treat G’Mic as entirely experimental. We still haven't managed to find a combination of compilers that will let us build Krita and G'Mic and make it work reliable.

If you've got experience cross-compiling from Linux to Windows and want to help out: that's about the last thing we haven't done. I've tried to create a cross-compilation setup, but got stuck on making Qt build with OpenGL support for Windows on Linux. **If you can help, please join us on #krita**.

**Note for Windows users with an Intel GPU**: If krita shows a **black screen** after opening an image, you need to update your Intel graphics drivers. This isn’t a bug in Krita, but in Intel’s OpenGL support. Update to 10.18.14 or later. Most Ultrabooks and the Cintiq Companion can suffer from outdated drivers.

**Note on OSX**: Krita on OSX is still experimental and not suitable for real work. Many features are still missing. Krita will only work on Mavericks and up.

**Downloads**

- Linux:
    - Distributions are expected to create packages for their bleeding edge repositories.
    - Ubuntu and derivatives can use Krita Lime, as usual: [https://launchpad.net/~dimula73/+archive/ubuntu/krita](https://launchpad.net/%7Edimula73/+archive/ubuntu/krita).
    - OpenSUSE users can the KDE:Extra repo: [http://download.opensuse.org/repositories/KDE:/Extra/](http://download.opensuse.org/repositories/KDE:/Extra/) or Leinir's OBS repositories which have Krita built with support for Vc (which makes painting faster):
        - [http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE\_13.1/](http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_13.1/)
        - [http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE\_13.2/](http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_13.2/)
        - [http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE\_Factory/](http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_Factory/)
- Windows. From Vista and up, Windows 7 and up is recommended. There is **no** Windows XP build. If you have a 64 bits version of Windows, don’t use the 32 bits build! The zip files do not need installing, just unpacking, but do not come with the Visual Studio C runtime that is included in the msi installer.
    - 32 bits Windows: [http://files.kde.org/krita/windows/krita\_x86\_2.9.2.0.msi](http://files.kde.org/krita/windows/krita_x86_2.9.2.0.msi) or [http://files.kde.org/krita/windows/krita\_x86\_2.9.2.0.zip](http://files.kde.org/krita/windows/krita_x86_2.9.2.0.zip) (This version does not include a working G’Mic.)
    - 64 bits Windows: [http://files.kde.org/krita/windows/krita\_x64\_2.9.2.0.msi](http://files.kde.org/krita/windows/krita_x64_2.9.2.0.msi) or [http://files.kde.org/krita/windows/krita\_x64\_2.9.2.0.zip](http://files.kde.org/krita/windows/krita_x64_2.9.2.0.zip)

OSX:

- [http://files.kde.org/krita/osx/krita-2.9.2.0.dmg](http://files.kde.org/krita/osx/krita-2.9.2.0.dmg)

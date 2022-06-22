---
title: "Second stretchgoal reached and new builds!"
date: "2015-05-22"
---

We've got our second stretchgoal through both [Kickstarter](https://www.kickstarter.com/projects/krita/krita-free-paint-app-lets-make-it-faster-than-phot) and the [Paypal](https://krita.org/2015-kickstarter/) donations! We hope we can get many more so that you, our users, get to choose more ways for us to improve Krita. And we have got half a third stretch goal actually implemented: modifier keys for selections!

Oh -- and check out [Wolthera's updated brush packs](https://forum.kde.org/viewtopic.php?f=274&t=125125)! There are brush packs for inking, painting, filters (with a new heal brush!), washes, flow-normal maps, doodle brushes, experimental brushes and the awesome lace brush in the SFX brush pack!

We've had a really busy week. We already gave you an idea of our latest test-build on Monday, but we had to hold back because of the revived crash file recovery wizard on windows... that liked to crash. But it's fixed now, and we've got new builds for you!

So what is exactly new in this build? Especially interesting are all the improvements to PSD import/export support. Yesterday [we learned that Katarzyna uses PSD as her working format when working with Krita](/posts/krita-comes-to-discworld/) \-- we still don't recommend that, but it's easier now!

[![Check the pass-through switch in the group layer entry in the layerbox!](/images/posts/2015/passthtrough.png)](https://krita.org/wp-content/uploads/2015/05/passthtrough.png) Check the pass-through switch in the group layer entry in the layerbox!

- Dmitry implemented Pass-Through mode for group layers. Note: filter, transform and transparency masks and pass-through mode don't work together yet, but loading and saving groups from and to PSD now does! Pass-through is _not_ a fake blending mode as in Photoshop: it is a switch on the group layer. See the screenshot!
- We now can load and save layerstyles, with patterns from PSD files! Get out your dusty PSDs for testing!
- Use the right Krita blending mode when a PSD image contains Color Burn.
- Add Lighter Color and Darker Color blending modes and load them from PSD.
- When using Krita with a translation active on windows, the delay on starting a stroke is a bit less, but we're still working on eliminating that delay completely.
- The color picker cursor now shows the currently picked and previous color.
- Layer styles can now be used with inherit-alpha
- Fix some issues with finding templates.
- Work around an issue in the oxygen widget style on Linux that would crash the OpenGL-based canvas due to double initialization
- Don't toggle the layer options when right-clicking on a layer icon to get the context menu (patch by Victor Wåhlström)
- Update the Window menu when a subwindow closes
- Load newer Photoshop-generated JPG files correctly by reading the resolution information from the TIFF tags as well. (Yes, JPG resolution is marked in the exiv metadata using TFF tags if you save from Photoshop...)
- Show the image name in the window menu if it hasn't been saved yet.
- Don't crash when trying to apply isolate-layer on a transform mask
- Add webp support (at least on Linux, untested on Windows)
- Add a shortcut to edit/paste into a new image. Patch by Tiffany!
- Fix the autosave recovery dialog on Windows for unnamed autosaves!
- Added a warning for intel users who may still be dealing with the broken driver. If Krita works fine for you, just click okay. If not, update your drivers!

New builds for Linux are being created at the moment and will be available through the usual channels.

### Linux:

- Users of Ubuntu and derivatives can use Krita Lime, as usual: [https://launchpad.net/~dimula73/+archive/ubuntu/krita](https://launchpad.net/%7Edimula73/+archive/ubuntu/krita). Currently rebuilding: builds will be ready later today!
- OpenSUSE users can use Leinir's OBS repositories which have Krita built with support for Vc (which makes painting faster):
    - [http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE\_13.1/](http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_13.1/)
    - [http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE\_13.2/](http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_13.2/)
    - [http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE\_Factory/](http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_Factory/)

### Windows:

From Vista and up, Windows 7 and up is recommended. There is **no** Windows XP build. If you have a 64 bits version of Windows, don’t use the 32 bits build! The zip files do not need installing, just unpacking, but do not come with the Visual Studio C runtime that is included in the msi installer.

- 32 bits Windows: [http://files.kde.org/krita/windows/krita\_x86\_2.9.4.6.msi](http://files.kde.org/krita/windows/krita_x86_2.9.4.6.msi) or [http://files.kde.org/krita/windows/krita\_x86\_2.9.4.6.zip](http://files.kde.org/krita/windows/krita_x86_2.9.4.6.zip) (This version does not include a working G’Mic.)
- 64 bits Windows: [http://files.kde.org/krita/windows/krita\_x64\_2.9.4.6.msi](http://files.kde.org/krita/windows/krita_x64_2.9.4.6.msi) or [http://files.kde.org/krita/windows/krita\_x64\_2.9.4.6.zip](http://files.kde.org/krita/windows/krita_x64_2.9.4.6.zip) (Not all G'Mic filters work on Windows, some may even crash Krita.)

### OSX:

(Please keep in mind that these builds are unstable and experimental. Stuff is expected not to work. We make them so we know we're not introducting build problems and to invite hackers to help us with Krita on OSX.)

- [http://files.kde.org/krita/osx/krita-2.9.4.5.dmg](http://files.kde.org/krita/osx/krita-2.9.4.5.dmg)

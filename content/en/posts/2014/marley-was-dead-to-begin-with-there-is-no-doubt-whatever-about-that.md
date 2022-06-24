---
title: "Marley was dead: to begin with. There is no doubt whatever about that."
date: "2014-12-21"
---

Well, [Marley might be dead](http://www.gutenberg.org/ebooks/46), but Krita ain't! So, here's what'll be the last beta build of Krita before the festive season really breaks lose. Apart from building, the Krita hackers have had a _pretty_ good week, with lots of deep discussions on animation and coding safety, too.

Oh -- and there's a [seasonal surprise](http://www.patreon.com/davidrevoy) for you, if you start one of these builds!

In the new builds, not quite beta 2 yet, just another build in between the last beta and the next beta, there are the following fixes:

- Stefano Bonicatti fixed a bunch of memory issues, and is tracking more and more of them -- also threading issues, and issues with AMD graphics cards.
- Boudewijn added a new option to use Krita to convert images: **krita bla.png --export --export-filename bla.jpg** will convert bla.png to bla.jpg. This replaces the calligraconverter utility.
- The 'hairy brush' is now called the 'bristle brush'
- PDF export has been fixed to export landscape as landscape and portrait as portrait, instead of everything as portrait, when using any paper size except A4. (A4 already worked fine).
- The filter dialog (filters, filter layers, filter masks) no longer show a big thumbnail. The thumbnail was getting in the way of the filter's name, and frequently didn't get rendered correctly/.
- Deleting the last node (layer or mask) in a group would lead Krita to having no node selected, causing crashes in filters. That got fixed, too.
- On loading or creating the first image, the default tool is once again the freehand brush, and besides, the tool options are now shown.
- Select-all is back
- In tab-mode, the tabs now keep the right caption
- A crash when flattening layers was fixed
- Jouni Pentikäinen fixed the outline cursor preview of a rotating brush
- Selecting a document size specified in anything but pixels was broken; that works now, too. Thanks to Joe for the detailed bug report!
- Every open subwindow can now have its own exposure and gamma settings, when a HDR image is  loaded an OpenColorIO is active
- A bunch of fixes to the tablet subsystem were committed by Dmitry. Painting should be much smoother now -- and we've also figured out why some n-trig devices do weird stuff. They tell us their maximum pressure is 255, but then send us tablet strokes with pressure in the 0 to 1024 range!
- Wolthera fixed an issue with darkening around the color smudge brush's radius
- Dmitry made it possible to drag & drop layers from one subwindow to another.
- And made it possible again to drag & drop images from web-browsers
- The locked status of docking panels now is kept properly
- (But on Windows, the minimum width of the toolbox now is three icons -- investgations are ongoing)
- Scott cleaned up the precision setting in the brush editor
- Lukáš worked like a beaver on the G'Mic plugin and updated it to the latest version, added proper layer synchronization -- and, tada! -- on Linux/X11 enabled the interactive filter feature. Interactive Colorize now works on Linux, from within Krita. Press Space for the best effect!
- Sven and Stefano fixed a crash when opening one image after closing another and changing the OpenGL settings in between.
- Timothée Giet updated all color-smudge brush presets
- Dmitry fixed a crash in the duplicate brush engine when using a tablet device
- Sven fixed loading brush presets from bundles

And that ties in with a lot of work Wolthera has done. Building on Victor Lafon's work earlier this year to make it possible to package resources -- brushes, gradients, patterns, everything -- in bundles, she's hit her stride and figured out what was broken and what needs to be added. But... It's already possible to load a bundle into Krita, and use the resources!

[![resources](/images/posts/2014/resources-300x204.png)](/images/posts/2014/resources.png)

And here's the [first bundle, with inking brushes](https://www.dropbox.com/s/4nj8t4538f5wx2s/Wolthera_Inking_Pack.bundle?dl=0)! If you want to get into the game, remember, this is still barely ripe. Also check the [brush preset guidelines](https://community.kde.org/Krita/Brushes_Preset_Preview)!

### Downloads

There are still  [230 bugs](https://bugs.kde.org/buglist.cgi?bug_severity=critical&bug_severity=grave&bug_severity=major&bug_severity=crash&bug_severity=normal&bug_severity=minor&bug_status=UNCONFIRMED&bug_status=CONFIRMED&bug_status=ASSIGNED&bug_status=REOPENED&list_id=1167792&product=krita&query_format=advanced) at the moment, down from 234, even though we fixed more than thirty bugs! Some of these bugs might cause dataloss, so users are recommended to use the beta builds for testing, not for critical work!

For Linux users, Krita Lime will be updated on Monday. Remember that launchpad is very strict about the versions of Ubuntu it supports. So the update is only available for 14.04 and up.

OpenSUSE users can use the new OBS repositories created by Leinir:

- [http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE\_13.1/](http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_13.1/)
- [http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE\_13.2/](http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_13.2/)
- [http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE\_Factory/](http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_Factory/)

Windows users can choose between an installer and the zip file. You can unzip the zip file anywhere and start Krita by executing bin/krita.exe: this only works if you have the right Microsoft Visual Studio C runtime library. Otherwise, use the MSI file. We only have 64 bits Windows builds at the moment, we’re working on fixing a problem with the 32 bits build.

- [http://files.kde.org/krita/windows/krita\_x64\_2.8.90.2.zip](http://files.kde.org/krita/windows/krita_x64_2.8.90.2.zip)
- [http://files.kde.org/krita/windows/krita\_x64\_2.8.90.2.msi](http://files.kde.org/krita/windows/krita_x64_2.8.90.2.msi)

OSX users can open the dmg and copy krita.app where they want. Note that OSX still is _not_ supported. There are OSX-specific bugs and some features are missing.

- [http://files.kde.org/krita/osx/krita-2.8.80.2.dmg](http://files.kde.org/krita/osx/krita-2.8.80.2.dmg)

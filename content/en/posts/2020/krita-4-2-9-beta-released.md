---
title: "Krita 4.2.9 beta released!"
date: "2020-03-09"
categories: 
  - "development-builds"
---

Much later than we wanted to, we've finally gotten the beta ready for Krita 4.2.9! One of the reasons it took so long is that an update to [Python 3.8 broke scripting on Windows](https://valdyas.org/fading/software/python-3-8-woes/). When we finally had figured out that the reason wasn't just that Python no longer looks for libraries in all the usual places, but also that the bindings to Qt, PyQt cannot be built in parallel, it was already February. And then, of course, Apple changed the way applications are notarized... And then we updated to a newer version of some of the libraries we build Krita on, and that broke all kinds of things. In short, we have had months of trying to get our builds working again!

On the other hand, we have _also_ worked like crazy to make this the most stable release of Krita ever, with countless bugs fixed -- and there are even some fun new features:

- Dmitry improved the brush outline: it no longer flickers when you hover over the canvas: \[video width="960" height="540" mp4="/images/posts/2020/2020-02-11_comparing-outline.mp4"\]\[/video\]
- He also added "Airbrush" and "Airbrush Rate" to the Color Smudge brush, and a new Ratio setting, also for the Color Smudge brush, which allows making the shape of the brush flatter using the different sensors. Ramón Miranda has even made a video demonstrating these features: 
    
    <iframe src="https://www.youtube.com/embed/fyc8-qgxAww" width="560" height="315" frameborder="0" allowfullscreen="allowfullscreen"></iframe>
    
- New contributor Saurabh Kumar added a "Split Layer into Selection Mask" feature:[![Layer Split Dialog](/images/posts/2020/Screenshot_20200225_140252.png)](/images/posts/2020/Screenshot_20200225_140252.png)

As for the bugfixes...

- Fix transparency checkers looked white on HDR display [bug 406698](https://bugs.kde.org/show_bug.cgi?id=406698)
- Several fixes to file dialogs for overwriting and jpg files [bug 412651](https://bugs.kde.org/show_bug.cgi?id=412651)
- Fix Grow Selection expanding in one direction [bug 414647](https://bugs.kde.org/show_bug.cgi?id=414647)
- Fix crash using onion skins on non-animated layers [bug 414668](https://bugs.kde.org/show_bug.cgi?id=414668)
- Increase the limit in Layer Offset to 100k [bug 414625](https://bugs.kde.org/show_bug.cgi?id=414625)
- Fix crash opening .kra with incorrect clone source (related to [bug 414699</a)](https://bugs.kde.org/show_bug.cgi?id=414699)
- Prevent crash on addition of color to deleted palette with colorpicker [bug 413548](https://bugs.kde.org/show_bug.cgi?id=413548)
- Make Add subbrush off on changing multibrush tool's type from Copy Translate [bug 415651](https://bugs.kde.org/show_bug.cgi?id=415651)
- Improve rendering of predefined default Rect dab
- Set the default location for restored files to QStandardPaths::PicturesLocation [bug 415810](https://bugs.kde.org/show_bug.cgi?id=415810)
- Don't crash if remoteArguments is called when there isn't a mainwindow [bug 415794](https://bugs.kde.org/show_bug.cgi?id=415794)
- On Android, default to TouchGesture for Kinetic Scrolling
- Delay initialization of brush paintop widget state [bug 415033](https://bugs.kde.org/show_bug.cgi?id=415033)
- Reenable breeze: with the latest release, the bug with comboboxes has been fixed
- Show the hand cursor if there is no colorize mask yet [bug 415935](https://bugs.kde.org/show_bug.cgi?id=415935)
- Fix logic for enabling/disabling options in stroke selection dialog [bug 415896](https://bugs.kde.org/show_bug.cgi?id=415896)
- ORA export, write entire layers instead of cropping them
- Fix endless recursion in when assigning a profile[bug 414818](https://bugs.kde.org/show_bug.cgi?id=414818)
- Fix a crash when cancelling Transform Tool action [bug 414672](https://bugs.kde.org/show_bug.cgi?id=414672)
- Fix an obviously wrong assert in the gradients [bug 414550](https://bugs.kde.org/show_bug.cgi?id=414550)
- Fix 1px brush offset in line tool [bug 407405](https://bugs.kde.org/show_bug.cgi?id=407405)
- Fix Layer Filter Combobox with Breeze theme [bug 406595](https://bugs.kde.org/show_bug.cgi?id=406595)
- Fix comparison of double spin box
- Fix PaletteDocker not showing palettes [bug 414890](https://bugs.kde.org/show_bug.cgi?id=414890)
- Fix undo of replacing vector selection [bug 412808](https://bugs.kde.org/show_bug.cgi?id=412808)
- Separate krita log dialog from system information
- Resource bundle: turn assert into check [bug 399008](https://bugs.kde.org/show_bug.cgi?id=399008)
- Fix the python Canvas.setRotation method [bug 416126](https://bugs.kde.org/show_bug.cgi?id=416126)
- Store and restore the geometry of the svg editor window [bug 416097](https://bugs.kde.org/show_bug.cgi?id=416097)
- Fix number of asserts with continued transform [bug 415625](https://bugs.kde.org/show_bug.cgi?id=415625)
- Fix Touch Docker save button not working on new files [bug 407905](https://bugs.kde.org/show_bug.cgi?id=407905)
- Fix blur Filter inconsistencies [bug 416241](https://bugs.kde.org/show_bug.cgi?id=416241)
- Fix border artifacts in layer styles [bug 414582](https://bugs.kde.org/show_bug.cgi?id=414582)
- Use Qt::Popup for color selectors popup widgets [bug 410959](https://bugs.kde.org/show_bug.cgi?id=410959)
- Always show color popup below the cursor [bug 394139](https://bugs.kde.org/show_bug.cgi?id=394139)
- Remove the strength compatibility with older paintop presets [bug 416335](https://bugs.kde.org/show_bug.cgi?id=416335)
- Fixed unneeded error message in Render Animation. [bug 412599](https://bugs.kde.org/show_bug.cgi?id=412599)
- Fix canvas offset calculation [bug 416352](https://bugs.kde.org/show_bug.cgi?id=416352)
- Layers with alpha channel disabled correctly export as "svg:src-atop" for ORA
- Add icon to Close button of "About Krita" dialog box
- Fix memory leak in preset history docker
- Warn that Krita needs to be restarted after enabling/disabling plugins [bug 416575](https://bugs.kde.org/show_bug.cgi?id=416575)
- Workaround Qt 5.14's colormanagement preventing png files from being saved [bug 416515](https://bugs.kde.org/show_bug.cgi?id=416515)
- Fixes with last used filter command. [bug 416706](https://bugs.kde.org/show_bug.cgi?id=416706)
- Fix Increase/Decrease Brush Size and Switch To Previous Preset buttons
- Fix Warp and Cage transform in master [bug 416505](https://bugs.kde.org/show_bug.cgi?id=416505)
- Fix crazy snapping when resizing shapes [bug 414336](https://bugs.kde.org/show_bug.cgi?id=414336)
- Fix hiccups when doing canvas actions [bug 414576](https://bugs.kde.org/show_bug.cgi?id=414576), [415773](https://bugs.kde.org/show_bug.cgi?id=415773)
- Fix animation rendering problem on small images (< 100px in size) [bug 415367](https://bugs.kde.org/show_bug.cgi?id=415367)
- Fix display of vector shapes when transformed with transform tool [bug 417016](https://bugs.kde.org/show_bug.cgi?id=417016)
- Fix hangup when loading image with generator/file layers [bug 415891](https://bugs.kde.org/show_bug.cgi?id=415891)
- Fix slowdown associated with the quick hide function of Shift+click on layer visibility icons
- Fix canvas border color issue
- Fix issue when saving preferences
- Hide SubWindow decoration on macOS
- A number of fixes with L\*A\*B\* and CMYK thanks to L.E Segovia's Season of KDE work
- Android: Make it possible to select opengles
- Set setRedirectPolicy as per discussion on KDE mailing lists
- Fix crash when loading asl with tdta OSType
- Make "Save Incremental Version" update recently used files
- Correct logic for determining whether there are multiple backups requested [bug 417914](https://bugs.kde.org/show_bug.cgi?id=417914)
- Fix incorrect common curve in very old presets [bug 417748](https://bugs.kde.org/show_bug.cgi?id=417748)
- Fix layout issue in the history docker
- Fix strobbing of the brush outline because of subpixel precision [bug 374551](https://bugs.kde.org/show_bug.cgi?id=374551)
- Make local selection outline visible on layer converted to selection mask
- Fix freeze on vector layers [bug 412746](https://bugs.kde.org/show_bug.cgi?id=412746)
- Fix artifacts on filter masks applied to adjustment layers [bug 417673](https://bugs.kde.org/show_bug.cgi?id=417673)
- Fix ratio option on lower precision brushes
- Fix opening Appimages [bug 418230](https://bugs.kde.org/show_bug.cgi?id=418230)
- Set image as modified after a legacy action (fix Channels docker not updating in some cases) [bug 417992](https://bugs.kde.org/show_bug.cgi?id=417992)

Now it's up to you all to beta-test this release and help us make sure we've caught all regressions (that is, new bugs for things that used to work) and all release blockers. We are currently investigating how we can make testing more robust, so this beta has no survey, please report all bugs you find to bugs.kde.org under the product Krita. Note that the Krita Lime PPA currently only has the beta and not the current stable.

## Download

### Windows

For the beta, you should only only use the portable zip files. Just open the zip file in Explorer and drag the folder somewhere convenient, then double-click on the krita icon in the folder. This will not impact an installed version of Krita, though it will share your settings and custom resources with your regular installed version of Krita. For reporting crashes, also get the debug symbols folder.

- 64 bits Windows Installer: [krita-x64-4.2.9-beta1-setup.exe](https://download.kde.org/unstable/krita/4.2.9-beta1/krita-x64-4.2.9-beta1-setup.exe)
- Portable 64 bits Windows: [krita-x64-4.2.9-beta1.zip](https://download.kde.org/unstable/krita/4.2.9-beta1/krita-x64-4.2.9-beta1.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/unstable/krita/4.2.9-beta1/krita-x64-4.2.9-beta1-dbg.zip)

- 32 bits Windows Installer: [krita-x86-4.2.9-beta1-setup.exe](https://download.kde.org/unstable/krita/4.2.9-beta1/krita-x86-4.2.9-beta1-setup.exe)
- Portable 32 bits Windows: [krita-x86-4.2.9-beta1.zip](https://download.kde.org/unstable/krita/4.2.9-beta1/krita-x86-4.2.9-beta1.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/unstable/krita/4.2.9-beta1/krita-x86-4.2.9-beta1-dbg.zip)

### Linux

- 64 bits Linux: [krita-4.2.9-beta1-x86_64.appimage](https://download.kde.org/unstable/krita/4.2.9-beta1/krita-4.2.9-beta-x86_64.appimage)
- 64 bits Linux [G'Mic-Qt plugin appimage](https://download.kde.org/unstable/krita/4.2.9-beta1/gmic_krita_qt-x86_64.appimage)

(If, for some reason, Firefox thinks it needs to load this as text: to download, right-click on the link.)

### OSX

- OSX disk image: [krita-4.2.9-beta1.dmg](https://download.kde.org/unstable/krita/4.2.9-beta1/krita-4.2.9-beta1.dmg)

Note: the gmic-qt is not available on OSX.

### Source code

- [krita-4.2.9-beta1.tar.gz](https://download.kde.org/unstable/krita/4.2.9-beta1/krita-4.2.9-beta1.tar.gz)
- [krita-4.2.9-beta1.tar.xz](https://download.kde.org/unstable/krita/4.2.9-beta1/krita-4.2.9-beta1.tar.xz)

### md5sum

For all downloads:

- [md5sum.txt](https://download.kde.org/unstable/krita/4.2.9-beta1/md5sum.txt)

### Key

The Linux appimage and the source .tar.gz and .tar.xz tarballs are signed. You can retrieve the public key over https here: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8). The signatures are [here](https://download.kde.org/unstable/krita/4.2.9-beta1/) (filenames ending in .sig).

## Support Krita

Krita is a free and open source project. Please consider supporting the project with [donations](/support-us/donations/) or by [buying training videos!](/support-us/shop) With your support, we can keep the core team working on Krita full-time.

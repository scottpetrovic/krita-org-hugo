---
title: "Krita 4.0.1 Released"
date: "2018-04-11"
categories: 
  - "news"
  - "officialrelease"
---

Today the Krita team releases Krita 4.0.1, a bug fix release of Krita 4.0.0. We fixed more than fifty bugs since the Krita 4.0.0 release! See below for the full list of fixed isses. Translations work again with the appimage and the macOS build. Please note that:

- The reference image docker has been removed. Krita 4.1.0 will have a new reference images tool. You can test the code-in-progress by downloading the nightly builds for Windows and Linux
- There is no scripting available on macOS. We had it almost working when the one macbook the project has received a broken update, which undid all our work. G'Mic is also not available on macOS.
- The lock and collapse icons on the docker titlebars are removed: too many people were too confused by them.

If you find a new issue, please consult this [draft document on reporting bugs](https://phabricator.kde.org/T7492), before reporting an issue. After the 4.0 release, more than 150 bugs were reported, but most of those reports were duplicates, requests for help or just not useful at all. This puts a heavy strain on the developers, and makes it harder to actually find time to improve Krita. Please be helpful!

[![](../images/kiki_4.0_sm-1-1024x463.png)](https://krita.org/wp-content/uploads/2018/03/kiki_4.0_sm-1.png)

## Improvements

### Windows

- Patch QSaveFile so working on images stored in synchronized folders (dropbox, google drive) is safe

### Shortcuts

- Fix duplicate shortcut on Photoshop scheme
- Alphabetize shortcut to make the diffs easier to read when doing changes

### UI

- Make the triangles larger on the categorized list view so they are more visible
- Disable the macro recorder and playback plugin
- Remove the docker titlebar lock and collapse buttons. [BUG:385238](https://bugs.kde.org/show_bug.cgi?id=385238) [BUG:392235](https://bugs.kde.org/show_bug.cgi?id=392235)
- Set the pixel grid to show up at 2400% zoom by default. [BUG:392161](https://bugs.kde.org/show_bug.cgi?id=392161)
- Improve the layout of the palette docker
- Disable drag and drop in the palette view: moving swatches around did not actually change the palette. [BUG:392349](https://bugs.kde.org/show_bug.cgi?id=392349)
- Fix selecting the last used template in the new document dialog when using appimages. [BUG:391973](https://bugs.kde.org/show_bug.cgi?id=391973)
- Fix canvas lockup when using Guides at the top of the image. [BUG:391098](https://bugs.kde.org/show_bug.cgi?id=391098)
- Do not reset redo history when changing layer's visibility. [BUG:390581](https://bugs.kde.org/show_bug.cgi?id=390581)
- Fix shifting the pan position after using the popup widget rotation circle. [BUG:391921](https://bugs.kde.org/show_bug.cgi?id=391921)
- Fix height map to normal map in wraparound mode. [BUG:392191](https://bugs.kde.org/show_bug.cgi?id=392191)

### Text

- Make it possible to edit the font size in the svg text tool. [BUG:392714](https://bugs.kde.org/show_bug.cgi?id=392714)
- Let Text Shape have empty lines. [BUG:392471](https://bugs.kde.org/show_bug.cgi?id=392471)
- Fix updates of undo/redo actions. [BUG:392257](https://bugs.kde.org/show_bug.cgi?id=392257)
- Implement "Convert text into path" function. [BUG:391294](https://bugs.kde.org/show_bug.cgi?id=391294)
- Fix a crash in SvgTextTool when deleting hovered/selected shape. [BUG:392128](https://bugs.kde.org/show_bug.cgi?id=392128)
- Make the text editor window application modal. [BUG:392248](https://bugs.kde.org/show_bug.cgi?id=392248)
- Fix alignment of RTL text. [BUG:392065](https://bugs.kde.org/show_bug.cgi?id=392065) [BUG:392064](https://bugs.kde.org/show_bug.cgi?id=392064)
- Fix painting parts of text outside the bounding box on the canvas. [BUG:392068](https://bugs.kde.org/show_bug.cgi?id=392068)
- Fix rendering of the text with relative offsets. [BUG:391160](https://bugs.kde.org/show_bug.cgi?id=391160)
- Fix crash when transforming text with Transform Tool twice. [BUG:392127](https://bugs.kde.org/show_bug.cgi?id=392127)

### Animation

- Fix handling of keyframes when saving. [BUG:392233](https://bugs.kde.org/show_bug.cgi?id=392233) [BUG:392559](https://bugs.kde.org/show_bug.cgi?id=392559)
- Keep show in timeline and onion skin options when merging layers. [BUG:377358](https://bugs.kde.org/show_bug.cgi?id=377358)
- Keep keyframe color labels when merging layers. [BUG:388913](https://bugs.kde.org/show_bug.cgi?id=388913)
- Fix exporting out audio with video formats MKV and OGV.

### File handling

- Do not load/save layer channel flags anymore (channel flags were removed from the UI in Krita 2.9). [BUG:392504](https://bugs.kde.org/show_bug.cgi?id=392504)
- Fix saving of Transform Mask into rendered formats. [BUG:392229](https://bugs.kde.org/show_bug.cgi?id=392229)
- Fix reporting errors when loading fails. [BUG:392413](https://bugs.kde.org/show_bug.cgi?id=392413)
- Fix a memory leak when loading file layers
- Fix loading a krita file with a loop in the clone layers setup. [BUG:384587](https://bugs.kde.org/show_bug.cgi?id=394587)
- Fix showing a wait cursor after loading a PNG image. [BUG:392249](https://bugs.kde.org/show_bug.cgi?id=392249)
- Make bundle loading feedback a bit clearer regarding the bundle.

### Vector bugs

- Fix crash when creating a vector selection. [BUG:391292](https://bugs.kde.org/show_bug.cgi?id=391292)
- Fix crash when doing right-click on the gradient fill stop opacity input box of a vector [BUG:392726](https://bugs.kde.org/show_bug.cgi?id=392726)
- Fix setting the aspect ratio of vector shapes. [BUG:391911](https://bugs.kde.org/show_bug.cgi?id=391911)
- Fix a crash if a certain shape is not valid when writing SVG. [BUG:392240](https://bugs.kde.org/show_bug.cgi?id=392240)
- Fix hidden stroke and fill widgets not to track current shape selection BUG:391990

### Painting and brush engines

- Fix crash when creating a new spray preset. [BUG:392869](https://bugs.kde.org/show_bug.cgi?id=392869)
- Fix rounding of the the pressure curve
- Fix painting with colorsmudge brushes on transparency masks. [BUG:391268](https://bugs.kde.org/show_bug.cgi?id=391268)
- Fix uninitialized distance info for KisHairyPaintOp [BUG:391940](https://bugs.kde.org/show_bug.cgi?id=391940)
- Fix rounding of intermediate pressure values
- Fix the colorsmudge brush when painting in wraparound mode. [BUG:392312](https://bugs.kde.org/show_bug.cgi?id=392312)

### Layers and masks

- Fix flattening of group layers with Inherit Alpha property set. [BUG:390095](https://bugs.kde.org/show_bug.cgi?id=390095)
- Fix a crash when using a transformation mask on a file layer. [BUG:391270](https://bugs.kde.org/show_bug.cgi?id=391270)
- Improve performance of the transformation mask

## Download

### Windows

Note for Windows users: if you encounter crashes, please follow [these instructions](https://docs.krita.org/Dr._Mingw_debugger) to use the debug symbols so we can figure out where Krita crashes.

- 64 bits Windows: [krita-x64-4.0.1-setup.exe](https://download.kde.org/stable/krita/4.0.1/krita-x64-4.0.1-setup.exe)
- Portable 64 bits Windows: [krita-x64-4.0.1.zip](https://download.kde.org/stable/krita/4.0.1/krita-x64-4.0.1.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.0.1/krita-x64-4.0.1-dbg.zip)

- 32 bits Windows: [krita-4.0.1-x86-setup.exe](https://download.kde.org/stable/krita/4.0.1/krita-x86-4.0.1-setup.exe)
- Portable 32 bits Windows: [krita-x86-4.0.1.zip](https://download.kde.org/stable/krita/4.0.1/krita-x86-4.0.1.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.0.1/krita-x86-4.0.1-dbg.zip)

### Linux

- 64 bits Linux: [krita-4.0.1-x86\_64.appimage](https://download.kde.org/stable/krita/4.0.1/krita-4.0.1-x86_64.appimage)

(If, for some reason, Firefox thinks it needs to load this as text: to download, right-click on the link.)

When it is updated, you can also use the [Krita Lime PPA](https://launchpad.net/%7Ekritalime/+archive/ubuntu/ppa) to install Krita 4.0.1 on Ubuntu and derivatives. We are working on an updated snap.

### OSX

- OSX disk image: [krita-4.0.1.dmg](https://download.kde.org/stable/krita/4.0.1/krita-4.0.1.dmg)

Note: the gmic-qt and python plugins are not available on OSX.

### Source code

- Source code: [krita-4.0.1.tar.gz](https://download.kde.org/stable/krita/4.0.1/krita-4.0.1.tar.gz)

### md5sum

For all downloads:

- [md5sum.txt](https://download.kde.org/stable/krita/4.0.1/md5sum.txt)

### Key

The Linux appimage and the source tarball are signed. You can retrieve the public key over https here: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8). The signatures are [here](http://download.kde.org/stable/krita/4.0.1/) (filenames ending in .sig).

## Support Krita

Krita is a free and open source project. Please consider supporting the project with [donations](https://krita.org/en/support-us/donations/) or by [buying training videos or the artbook!](https://krita.org/en/support-us/shop) With your support, we can keep the core team working on Krita full-time.

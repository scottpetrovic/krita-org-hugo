---
title: "Krita 4.1.3 Released"
date: "2018-09-27"
categories: 
  - "news"
  - "officialrelease"
---

Today we're releasing the latest version of Krita! In the middle of our [2018 fundraiser campaign](https://www.krita.org), we've found the time to prepare Krita 4.1.3. There are about a hundred fixes, so it's a pretty important release and we urge everyone to update! Please join the 2018 fundraiser as well, so we can continue to fix bugs!

[![](../images/2018-fundraiser-hero2.png)](https://krita.org)

Now you might be wondering where Krita 4.1.2 went to... The answer is that we had 4.1.2 prepared, but the Windows builds were broken because of a change in the build infrastructure. While we were fixing that, Dmitry made a couple of bug fixes we really wanted to release immediately, like an issue where multiline centered text would be squashed into a single line when you'd edit the text. So we went and created a new version, 4.1.3!

[![](../images/text_tool-1024x577.jpg)](https://krita.org/wp-content/uploads/2018/09/text_tool.jpg)

Krita 4.1.3 is a bug fix release, so that's the most important thing, but there are also some new things as well.

The first of these is the new welcome screen, by Scott Petrovic. You get some handy links, a list of recently used files, a link to create or open a file and a hint that you can also drag and drop images in the empty window to open them.

[![](../images/welcome_page-1024x781.png)](https://krita.org/wp-content/uploads/2018/09/welcome_page.png)

Dmitry Kazakov has worked like crazy fixing bugs and improving Krita in the past couple of weeks. One of the things he did was improve Instant Preview mode. Originally funded by our 2015 Kickstarter, Instant Preview works by computing a scaled-down version of the image and displaying that. But with some brushes, it would cause a little delay at the end of a stroke, or some flickering on the canvas: [BUG:361448](https://bugs.kde.org/show_bug.cgi?id=361448). That's fixed now, and painting really feels smoother! And for added smoothness, most of [Ivan Yossi's Google Summer of Code work](https://colorathis.wordpress.com/tag/kde/) is also included in this release.

We've also done work on improving working with selections. Krita's selections can be defined as vectors or as a pixel mask. If you're working on a vector selection, using the figure tools, like rectangle or ellipse now add a vector to the selection, instead of rasterizing the vector selection.

The move tool has been improved so it's possible to undo the steps you've set with the move tool, instead of undo immediately placing back the layer where it originally came from. See [BUG:392014](https://bugs.kde.org/show_bug.cgi?id=392014).

The bezier curve tools have been improved: there is an auto-smoothing option. If you select auto-smoothing, the created curve will be not a polygon, but a smooth curve with the type of all the points set to "smooth". [BUG:351787](https://bugs.kde.org/show_bug.cgi?id=351787)

[![](../images/bezier_smoothing-1024x726.png)](https://krita.org/wp-content/uploads/2018/09/bezier_smoothing.png)

The final new feature is round corners for the rectangle tool. Whether you're working on a pixel or a vector layer, you have an ability to set round corners for the resulting shape. [BUG:335568](https://bugs.kde.org/show_bug.cgi?id=335568). You could, of course, already round vector rectangles by editing the shape, but this is easier.

[![](../images/rounded_rectangles-1024x726.png)](https://krita.org/wp-content/uploads/2018/09/rounded_rectangles.png)

The Comics Project manager, a Python plugin created by Wolthera van Hövell tot Westerflier has seen a ton of improvements, especially when it comes to generating standard-compliant epub and acbf files. On a related note, check out [Peruse, the KDE Comic Book Reader](https://peruse.kde.org/). It's a long list of improvements:

- Add improved navigation to generated epubs. This adds...
    - Region navigation for panels and balloons, as per epub spec.
    - Navigation that uses the "acbf\_title" keyword to create a TOC in both nav.xhtml and ncx
    - A Pagelist in both nav.xhtml and ncx.
- Ensure generated EPUBs pass EPUB check validation. This invoved ensuring that the mimetype gets added first to the zip, as well as as some fixes with the author metadata and the NCX pagelist.
- Fix language nonsense.
- Fix several issues with the EPUB metadata export.
    - Add MARC-relators for use with the 'refines'.
    - Add UUID sharing between acbf and epub.
    - Add a modiied and proper date stuff.
- Implement "epub\_spread", the primary color ahl meta and more. This also...
    - Makes the balloon localisation more robust.
    - Names all balloons text-areas as that is a bit more accurate
    - Set a sequence on author
    - Adds a ton of documentation everywhere.
- Make the generated EPUB 3 files pre-paginated. This'll allow comics to be rendered as part of a spread which should have a nice result.
- Move Epub to use QDomDocument for generation, split out ncx/opf. This is necessary so we have nicer looking xml files, as well. as having a bit more room to do proper generation for epub 2/3/3+
- Update ComicBookInfo and ComicRack generators.

[![](../images/Screenshot_20180828_155852-1024x797.png)](https://krita.org/wp-content/uploads/2018/09/Screenshot_20180828_155852.png)

And here's the full list of fixed bugs:

**Animation**

- Add a workaround for loading broken files with negative frame ids. [BUG:395378](https://bugs.kde.org/show_bug.cgi?id=395378)
- Delete existing frame files only within exported range [BUG:377354](https://bugs.kde.org/show_bug.cgi?id=377354)
- Fix a problem of Insert Hold Frames action. We should also "offset" empty cell to make sure the expanding works correctly. [BUG:396848](https://bugs.kde.org/show_bug.cgi?id=396848)
- Fix an assert when trying to export a PNG image sequence [BUG:398608](https://bugs.kde.org/show_bug.cgi?id=398608)
- Fix updates when switching frame on a layer with scalar channel
- Use user-selected color label for the auto-created animation frames [BUG:394072](https://bugs.kde.org/show_bug.cgi?id=394072)
- saving of the multiple frames insertion/removal options to the config

**Improvements to support for various file formats**

- Fix an assert if an imported SVG file links to non-existent color profile [BUG:398576](https://bugs.kde.org/show_bug.cgi?id=398576)
- Fix backward compatibility of adjustment curves. Older versions supported fewer adjustable channels, so we can no longer assume the count in configuration data to matches exactly. [BUG:396625](https://bugs.kde.org/show_bug.cgi?id=396635)
- Fix saving layers with layer styles [BUG:396224](https://bugs.kde.org/show_bug.cgi?id=396224)
- Let Krita save all the kinds of layers into PSD (in rasterized way) [BUG:399002](https://bugs.kde.org/show_bug.cgi?id=399002)
- PNG Export: convert to rgb, if the image isn't rgb or gray [BUG:398241](https://bugs.kde.org/show_bug.cgi?id=398241)
- Remove fax-related tiff options. In fax mode tiff can store only 1 bit per channel images, which Krita doesn't support. So just remove these options from the GUI [BUG:398548](https://bugs.kde.org/show_bug.cgi?id=398548)

**Filters**

- Add a shortcut for the threshold filter [BUG:383818](https://bugs.kde.org/show_bug.cgi?id=383818)
- Fix Burn filter to work in 16-bit color space [BUG:387102](https://bugs.kde.org/show_bug.cgi?id=387102)
- Make color difference threshold for color labels higher
- Restore the shortcut for the invert filters.

**Painting**

- Remove hardcoded brush size limit for the Quick Brush [BUG:376085](https://bugs.kde.org/show_bug.cgi?id=376085)
- Fix rotation direction when the transformed piece is mirrored. [BUG:398928](https://bugs.kde.org/show_bug.cgi?id=398928)
- Make Stamp brush preview be scaled correctly [CCBUG:399065](https://bugs.kde.org/show_bug.cgi?id=399065)

**Tablets**

- Add a workaround for tablets not reporting tablet events in hover mode [BUG:363284](https://bugs.kde.org/show_bug.cgi?id=363284)

**Text**

- Do not reset text style when selecting something in text editor
- Fix saving line breaks when the text is not left aligned [BUG:395769](https://bugs.kde.org/show_bug.cgi?id=395769)

**Reference images tool**

- Fix reference image cache update conditions [BUG:397208](https://bugs.kde.org/show_bug.cgi?id=397208)

**build system**

- Fix build with dcraw 0.19

**Canvas**

- Disable pixel grid action if opengl is disabled [BUG:388903](https://bugs.kde.org/show_bug.cgi?id=388903) Patch by Shingo Ohtsuka, thanks!
- Fix painting of selection decoration over grids [BUG:362662](https://bugs.kde.org/show_bug.cgi?id=362662)

**Fixes to Krita's Core**

- Fix saving to a dropbox or google driver folder on Windows temporary workaround until [QTBUG-57299](https://bugreports.qt.io/browse/QTBUG-57299): QSaveFile should be disabled on Windows.
- Fix to/fromLab16/Rgb16 methods of the Alpha color space
- Fix undo in the cloned KisDocument [BUG:398730](https://bugs.kde.org/show_bug.cgi?id=398730)

**Layers**

- Automatically avoid conflicts between color labels and system colors
- Fix cursor jumps in the Layer Properties dialog [BUG:398958](https://bugs.kde.org/show_bug.cgi?id=398958)
- Fix resetting active tool when moving layers above vector layers [BUG:398095](https://bugs.kde.org/show_bug.cgi?id=398095)
- Fix selecting of the layer after undoing Flatten Image [BUG:398814](https://bugs.kde.org/show_bug.cgi?id=398814)
- Fix showing two nodes when converting to a Filter Mask 1) When a filter mask we should first remove the source layer, and only after that show the filter selection dialog 2) Also make sure that the operation is rolled back when the user presses Cancel button
- Fix updates of Clone Layers when the nodes are updated with subtree walker
- a spurious assert in layer cloning [BUG:398788](https://bugs.kde.org/show_bug.cgi?id=398788)

**Metadata handling**

- Fix a memory access problem in KisExifIO
- Fix memory access problems in KisExifIo
- Show metadata in the dublin core page of the metadata editor. The editor plugin is still broken, with dates not working, bools not working, but now at least a string one has entered is shown again. [CCBUG:396672](https://bugs.kde.org/show_bug.cgi?id=396672)

**Python scripting**

- SegFault in LibKis Node mergeDown [BUG:397043](https://bugs.kde.org/show_bug.cgi?id=397043)
- apidox for Node.position() [BUG:393035](https://bugs.kde.org/show_bug.cgi?id=393035)
- Add modified() getter to the Document class [BUG:397320](https://bugs.kde.org/show_bug.cgi?id=397320)
- Add resetCache() Python API to FileLayer [BUG:398740](https://bugs.kde.org/show_bug.cgi?id=398740)
- Fix memory management of the Filter's InfoObject [BUG:392183](https://bugs.kde.org/show_bug.cgi?id=392183)
- Fix setting file path of the file layer through python API [BUG:398740](https://bugs.kde.org/show_bug.cgi?id=398740)
- Make sure we wait for the filter to be done

**Resource handling**

- Fix saving a fixed bundle under the original name

**Selections**

- Fix "stroke selection" to work with local selections [BUG:398007](https://bugs.kde.org/show_bug.cgi?id=398007)
- Fix a crash when moving a vector shape selection when it is an overlay
- Fix crash when converting a shape selection shape into a shape selection
- Fix crash when undoing removing of a selection mask
- Fix rounded rectangular selection to actually work [BUG:397806](https://bugs.kde.org/show_bug.cgi?id=397806)
- Fix selection default bounds when loading old type of adjustment layers
- Stroke Selection: don't try to add a shape just because a layer doesn't have a paint device [BUG:398015](https://bugs.kde.org/show_bug.cgi?id=398015)

**Other tools**

- Fix color picking from reference images. Desaturation now affects the picked color, and reference images are ignored for picking if hidden.
- Fix connection points on cage transform [BUG:396788](https://bugs.kde.org/show_bug.cgi?id=396788)
- Fix minor UIX issues in the move tool: 1) adds an explicit frame when the move stroke is in progress; 2) Ctrl+Z now cancels the stroke if there is nothing to undo [BUG:392014](https://bugs.kde.org/show_bug.cgi?id=392014)
- Fix offset in Move Tool in the end of the drag
- Fix shift modifier in Curve Selection Tool. The modifier of the point clicked the last should define the selection mode. For selection tools we just disable shift+click "path-close" shortcut of the base path tool. [BUG:397932](https://bugs.kde.org/show_bug.cgi?id=397932)
- Move tool crops the bounding area by exact bounds
- Reduce aliasing in reference images [BUG:396257](https://bugs.kde.org/show_bug.cgi?id=396257)

**Papercuts and UI issues**

- Add the default shortcut for the close action: when opening Krita with an image, the close document shortcut was not available.
- FEATURE: Add a hidden config option to lock all dockers in place
- Fix KMainWindow saving incorrect widget settings
- Fix broken buddy: Scale to New Size's Alt-F points to Alt-T [BUG:396948](https://bugs.kde.org/show_bug.cgi?id=396948)
- Fix http link color in KritaBlender.colors: The link are now visible on the startup page of Krita and were dark blue, exact same value as the background making the frame hard to read. Switching them to bright cyan improves the situation.
- Fix loading the template icons
- Fix the offset dialog giving inaccurate offsets. [BUG:397218](https://bugs.kde.org/show_bug.cgi?id=397218)
- Make color label selector handle mouse release events [CCBUG:394072](https://bugs.kde.org/show_bug.cgi?id=394072)
- Remember the last opened settings page in the preferences dialog
- Remember the last used filter bookmark
- Remove the shortcut for wraparound mode: It's still available from the menu and could be put on the toolbar, or people could assign a shortcut, but having it on by default makes life too hard for people who are trying to support our users.
- Remove the shortcuts from the mdi window's system menu's actions. The Close Window action can now have a custom shortcut, and there are no conflicts with hidden actions any more. [BUG:398729](https://bugs.kde.org/show_bug.cgi?id=398729) [BUG:375524](https://bugs.kde.org/show_bug.cgi?id=375524) [BUG:352205](https://bugs.kde.org/show_bug.cgi?id=352205)
- Set color scheme hint for compositor. This is picked up by KWin and sets the palette on the decoration and window frame, ensuring a unified look.
- Show a canvas message when entering wraparound mode
- Show the zoom widget when switching documents [BUG:398099](https://bugs.kde.org/show_bug.cgi?id=398099)
- Use KSqueezedTextLabel for the pattern name in the pattern docker and brush editor [BUG:398958](https://bugs.kde.org/show_bug.cgi?id=398958)
- sort the colorspace depth combobox

## Download

### Windows

Note for Windows users: if you encounter crashes, please follow [these instructions](https://docs.krita.org/en/reference_manual/dr_minw_debugger.html#dr-minw) to use the debug symbols so we can figure out where Krita crashes.

- 64 bits Windows: [krita-x64-4.1.3-setup.exe](https://download.kde.org/stable/krita/4.1.3/krita-x64-4.1.3-setup.exe)
- Portable 64 bits Windows: [krita-x64-4.1.3.zip](https://download.kde.org/stable/krita/4.1.3/krita-x64-4.1.3.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.1.3/krita-x64-4.1.3-dbg.zip)

- 32 bits Windows: [krita-x86-4.1.3-setup.exe](https://download.kde.org/stable/krita/4.1.3/krita-x86-4.1.3-setup.exe)
- Portable 32 bits Windows: [krita-x86-4.1.3.zip](https://download.kde.org/stable/krita/4.1.3/krita-x86-4.1.3.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.1.3/krita-x86-4.1.3-dbg.zip)

### Linux

- 64 bits Linux: [krita-4.1.3-x86\_64.appimage](https://download.kde.org/stable/krita/4.1.3/krita-4.1.3-x86_64.appimage)
- 64 bits Linux [G'Mic-Qt plugin appimage](https://download.kde.org/stable/krita/4.1.3/gmic_krita_qt-x86_64.appimage).

(If, for some reason, Firefox thinks it needs to load this as text: to download, right-click on the link.)

When it is updated, you can also use the [Krita Lime PPA](https://launchpad.net/%7Ekritalime/+archive/ubuntu/ppa) to install Krita 4.1.3 on Ubuntu and derivatives. We are working on an updated snap.

### OSX

- OSX disk image: [krita-4.1.3.dmg](https://download.kde.org/stable/krita/4.1.3/krita-4.1.3.dmg)

Note: the touch docker, gmic-qt and python plugins are not available on OSX.

### Source code

- Source code: [krita-4.1.3.tar.gz](https://download.kde.org/stable/krita/4.1.3/krita-4.1.3.tar.gz)

### md5sum

For all downloads:

- [md5sum.txt](https://download.kde.org/stable/krita/4.1.3/md5sum.txt)

### Key

The Linux appimage and the source tarball are signed. You can retrieve the public key over https here: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8). The signatures are [here](http://download.kde.org/stable/krita/4.1.3/) (filenames ending in .sig).

## Support Krita

Krita is a free and open source project. Please consider supporting the project with [donations](https://krita.org/en/support-us/donations/) or by [buying training videos or the artbook!](https://krita.org/en/support-us/shop) With your support, we can keep the core team working on Krita full-time.

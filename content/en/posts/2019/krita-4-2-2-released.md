---
title: "Krita 4.2.2 Released"
date: "2019-06-27"
categories: 
  - "officialrelease"
---

Within a month of Krita 4.2.1, we're releasing Krita 4.2.2. This is another bug fix release. We intend to have monthly bug fix releases of Krita 4.2 until it's time to release 4.3, which will have new features as well. Here's the list of bug fixes:

- Text editor: make sure the background color is the one set in the settings ([BUG:408344](https://bugs.kde.org/show_bug.cgi?id=408344))
- Fix a crash when creating a text shape ([BUG:407554](https://bugs.kde.org/show_bug.cgi?id=407554))
- Make sure the text style is not reset when removing the last character in the text editor ([BUG:408441](https://bugs.kde.org/show_bug.cgi?id=408441))
- Fix an issue on macOS where some libraries could not be loaded (BUG:408343)
- Use a highlighted tool button in the selection tool option dockers so it's easier to see which selection action is active
- Fix the nearest neighbour transform algorithm ([BUG:408182](https://bugs.kde.org/show_bug.cgi?id=408182))
- Fix a styling issue in the filter layers properties dialog ([BUG:408171](https://bugs.kde.org/show_bug.cgi?id=408171))
- Fix an issue where if Krita was set to use a language other than English, vector strokes were drawn wrongly
- Fix selecting colors from the combobox in the palette docker
- Fix a crash when loading a broken KPL file ([BUG:408447](https://bugs.kde.org/show_bug.cgi?id=408447))
- Fix an issue where a transparent pattern fill loader was loaded incorrectly ([BUG:408169](https://bugs.kde.org/show_bug.cgi?id=408169))
- Make it possible to make the onion skin docker smaller ([BUG:407646](https://bugs.kde.org/show_bug.cgi?id=407646))
- Improve loading GPL palettefiles with thousands of columns
- Fix the slider widget to make it impossible to get negative values
- Improve the tiff import/export filter ([BUG:408177](https://bugs.kde.org/show_bug.cgi?id=408177))
- Fix loading the scripter Python plugin when using a language other than English
- Improve the reference image tool and optimize loading images from clipboard
- Make the camera raw import filter honor batch mode
- Fix rendering of clone layers if the source layer is not visible ([BUG:408167](https://bugs.kde.org/show_bug.cgi?id=408167), [BUG:405536](https://bugs.kde.org/show_bug.cgi?id=405536))
- Fix move and transform tools after a quick layer duplication ([BUG:408593](https://bugs.kde.org/show_bug.cgi?id=408593))
- Fix a crash when selecting the opaque pixels on a transform mask ([BUG:408618](https://bugs.kde.org/show_bug.cgi?id=408618))
- Fix loading sRGB EXR files ([BUG:408485](https://bugs.kde.org/show_bug.cgi?id=408485))
- Make the new image dialog choose the last used option even when the user's language has changed
- Fix the "Enforce Palette Colors" feature ([BUG:408256](https://bugs.kde.org/show_bug.cgi?id=408256))
- Update the brush preview on every brush stamp creation ([BUG:389432](https://bugs.kde.org/show_bug.cgi?id=389432))
- Make it possible to edit vector shapes on duplicated vector layers ([BUG:408028](https://bugs.kde.org/show_bug.cgi?id=408028))
- Hide the color picker button in the vector object properties docker, it's unimplemented
- Fix color as mask export in GIH and GBR brush tip export ([BUG:389928](https://bugs.kde.org/show_bug.cgi?id=389928))
- Restore the default favorite blending modes
- Add a header to all right-click menus on the canvas so the first thing under the cursor isn't something dangerous, like 'cut' ([BUG:408696](https://bugs.kde.org/show_bug.cgi?id=408696))
- Fix an incorrect condition when rendering animations where Krita would complain to be out of memory
- Keep the community links in the welcome screen visible when changing theme ([BUG:408686](https://bugs.kde.org/show_bug.cgi?id=408686))
- Check after saving whether the saved file can be opened and has correct contents
- Improve the import/export error handling and reporting
- Make sure the filter dialog shows up in front of Krita's main window ([BUG:408867](https://bugs.kde.org/show_bug.cgi?id=408867))
- Make sure that the contiguous selection tool provides the antialiasing switch ([BUG:408733](https://bugs.kde.org/show_bug.cgi?id=408733))
- Fix the fuzziness setting in the contiguous selection tool
- Fix putting the text shape behind every other shape on a vector layer after editing text ([BUG:408693](https://bugs.kde.org/show_bug.cgi?id=408693))
- Fix switching the pointer type by stylus tip ([BUG:408454](https://bugs.kde.org/show_bug.cgi?id=408454), [BUG:405747](https://bugs.kde.org/show_bug.cgi?id=405747))
- Fix an issue on Linux where switching from pen to mouse would prevent the mouse from drawing on the canvas ([BUG:407595](https://bugs.kde.org/show_bug.cgi?id=407595))
- Fix a crash when the user undoes creating layers too quickly ([BUG:408484](https://bugs.kde.org/show_bug.cgi?id=408484))
- Fix using .KRA and .ORA files as file layers ([BUG:408087](https://bugs.kde.org/show_bug.cgi?id=408087))
- Clear all points in the outline selection on clicking ([BUG:408439](https://bugs.kde.org/show_bug.cgi?id=408439))
- Fix a crash when using the fill tool in fast mode on a pixel selection mask
- Fix merging layers with inactive selection masks ([BUG:402070](https://bugs.kde.org/show_bug.cgi?id=402070))
- Remove default actions from the Reference Image tool that were inappropriate ([BUG:408427](https://bugs.kde.org/show_bug.cgi?id=408427))
- Fix undo/redo not restoring the document to unmodified ([BUG:402263](https://bugs.kde.org/show_bug.cgi?id=402263))
- Fix the deform tool leaving darkish traces when scrubbing a lot on a 16 bit canvas ([BUG:290383](https://bugs.kde.org/show_bug.cgi?id=290383))
- Updated Qt to 5.12.4

**Warning**: on some Windows systems, we see that Krita 4.2.x doesn't start. We haven't found a system where we could reproduce this issue, and it seems it mostly has to do with those systems not having a working OpenGL or Direct3D driver. We're working on a solution.

## Download

### Windows

Note for Windows users: if you encounter crashes, please follow [these instructions](https://docs.krita.org/en/reference_manual/dr_minw_debugger.html#dr-minw) to use the debug symbols so we can figure out where Krita crashes.

- 64 bits Windows: [krita-x64-4.2.2-setup.exe](https://download.kde.org/stable/krita/4.2.2/krita-x64-4.2.2-setup.exe)
- Portable 64 bits Windows: [krita-x64-4.2.2.zip](https://download.kde.org/stable/krita/4.2.2/krita-x64-4.2.2.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.2.2/krita-x64-4.2.2-dbg.zip)

- 32 bits Windows: [krita-x86-4.2.2-setup.exe](https://download.kde.org/stable/krita/4.2.2/krita-x86-4.2.2-setup.exe)
- Portable 32 bits Windows: [krita-x86-4.2.2.zip](https://download.kde.org/stable/krita/4.2.2/krita-x86-4.2.2.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.2.2/krita-x86-4.2.2-dbg.zip)

### Linux

- 64 bits Linux: [krita-4.2.2-x86\_64.appimage](https://download.kde.org/stable/krita/4.2.2/krita-4.2.2-x86_64.appimage)
- 64 bits Linux [G'Mic-Qt plugin appimage](https://download.kde.org/stable/krita/4.2.2/gmic_krita_qt-x86_64.appimage).

(If, for some reason, Firefox thinks it needs to load this as text: to download, right-click on the link.)

### OSX

- OSX disk image: [krita-4.2.2.3.dmg](https://download.kde.org/stable/krita/4.2.2/krita-4.2.2.3.dmg)

Note: the gmic-qt is not available on OSX.

### Source code

- [krita-4.2.2.tar.gz](https://download.kde.org/stable/krita/4.2.2/krita-4.2.2.tar.gz)
- [krita-4.2.2.tar.xz](https://download.kde.org/stable/krita/4.2.2/krita-4.2.2.tar.xz)

### md5sum

For all downloads:

- [md5sum.txt](https://download.kde.org/stable/krita/4.2.2/md5sum.txt)

### Key

The Linux appimage and the source tarball are signed. You can retrieve the public key over https here: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8). The signatures are [here](http://download.kde.org/unstable/krita/4.2.0-beta2/) (filenames ending in .sig).

## Support Krita

Krita is a free and open source project. Please consider supporting the project with [donations](https://krita.org/en/support-us/donations/) or by [buying training videos or the artbook!](https://krita.org/en/support-us/shop) With your support, we can keep the core team working on Krita full-time.

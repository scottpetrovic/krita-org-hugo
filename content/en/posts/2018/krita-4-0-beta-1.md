---
title: "Krita 4.0 Beta 1"
date: "2018-01-11"
---

We've officially gone into String Freeze mode now! That's developer speak for "No New Features, Honest". Everything that's going into Krita 4.0 now is in, and the only thing left to do is fixing bugs and refining stuff.

Given how much has changed between Krita 3 and Krita 4, that's an important part of the job! Let us here repeat a very serious warning.

_**THE FILE FORMAT FOR VECTOR LAYERS HAS CHANGED. IF YOU SAVE AN IMAGE WITH KRITA 4.0 THAT HAS VECTOR LAYERS, KRITA 3 CANNOT OPEN IT. IF YOU OPEN A KRITA 3 FILE WITH VECTOR LAYERS IN KRITA 4, THE VECTOR LAYERS MIGHT GET MESSED UP. BEFORE WORKING ON SUCH FILES IN KRITA 4, MAKE A BACKUP.**_

This _doubles_ for files that contain _text_. Text in krita 3 is based on the ODT standard, text in Krita 4 is implemented using SVG. This beta is the first release that contains the new text tool. Here's the low-down on the new text tool:

- It's not the text tool we wanted to create, and you could consider it as a stop-gap measure. Because of all the tax office worries, we simply didn't have the time to create the fully-capable opentype-integrated text tool that we wanted to do.
- But we couldn't keep the old text tools either: they were broken, and based on ODT. We needed to have something that could replace those tools and that would would be functional enough for the simplest of use-cases, like text balloons in a comic.
- So, what we've got is simple. There's no vertical text for Chinese or Japanese yet, there's no OpenType tweaking, there's no fine typographic control.
- The user interface is not final yet, and there are quite a few things that need polishing and fixing, and that we're working on, but Krita 4's text tool will be mostly what we've got now.

### Apart from that...

This beta contains pretty much everything... We started working on some of these features, like the export feedback in 2016. Here's a short list:

- SVG vector system, with improved tools and workflow
- New text tool
- Python scripting
- SVG import/export
- Improved palette docker
- Bigger brush sizes
- Improved brush editor
- Refactored saving and exporting: saving happens in the background, and export shows warnings when your file contains features that cannot be saved to a given file format
- A fast colorize brush
- The default pixel brush is much faster on systems with many cores
- Lots of user interface polish

And there's much more, but please download the builds, or build Krita and see for yourself!

One thing that is still in progress is updating the set of default brush presets: those aren't in the beta yet, but they are in the nightly builds.

### Platform Notes

#### Windows

- There is only a 64 bits build. We haven't decided whether we want to provide 32 bits builds at all on Windows yet.
- There are now [nightly Windows builds available as well](https://binary-factory.kde.org/job/Krita_Nightly_Build/).

#### Linux

- The AppImage does not contain support for audio in animations
- The AppImage does not have Python scripting
- The AppImage does include the latest gmic-qt release

#### OSX

- The app bundle does not contain gmic-qt
- The app bundle does not contain Python scripting
- The app bundle does not have support for importing PDF files

### Download

#### Windows

Note for Windows users: if you encounter crashes, please follow [these instructions](https://docs.krita.org/Dr._Mingw_debugger) to use the debug symbols so we can figure out where Krita crashes.

- 64 bits Windows: [krita-x64-4.0.0.51-setup.exe](https://download.kde.org/unstable/krita/4.0.0.51/krita-x64-4.0.0.51-setup.exe)
- Portable 64 bits Windows: [krita-x64-4.0.0.51.zip](https://download.kde.org/unstable/krita/4.0.0.51/krita-x64-4.0.0.51.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/unstable/krita/4.0.0.51/krita-x64-4.0.0.51-dbg.zip)

#### Linux

- 64 bits Linux: [krita-4.0.0-beta.1-x86_64.appimage](https://download.kde.org/unstable/krita/4.0.0.51/krita-4.0.0-beta1.1-x86_64.appimage)

(If, for some reason, Firefox thinks it needs to load this as text: to download, right-click on the link.)

When it is updated, you can also use the [Krita Lime PPA](https://launchpad.net/%7Ekritalime/+archive/ubuntu/ppa) to install Krita 4.0 beta 1 on Ubuntu and derivatives.

#### OSX

- OSX disk image: [krita-4.0.0-beta.1.dmg](https://download.kde.org/unstable/krita/4.0.0.51/krita-4.0.0-beta.1.dmg)

Note: the gmic-qt and pdf plugins are not available on OSX.

### Source code

- Source code: [krita-4.0.0.51.1.tar.gz](https://download.kde.org/unstable/krita/4.0.0.51/krita-4.0.0.51.tar.gz)

#### md5sums

For all downloads:

- [md5sum.txt](https://download.kde.org/unstable/krita/4.0.0.51/md5sum.txt)

#### Key

The Linux appimage and the source tarball are signed. You can retrieve the public key over https here: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8). The signatures are [here](http://download.kde.org/unstable/krita/4.0.0.51/).

#### Support Krita

Krita is a free and open source project. Please consider supporting the project with [donations](/support-us/donations/) or by [buying training videos or the artbook!](/support-us/shop) With your support, we can keep the core team working on Krita full-time.

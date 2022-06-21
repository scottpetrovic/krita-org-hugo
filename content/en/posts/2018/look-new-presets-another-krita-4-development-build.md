---
title: "Look, new presets! Another Krita 4 development build!"
date: "2018-02-17"
---

We've been focusing like crazy on the Krita 4 release. We managed to close some 150 bugs in the past month, and Krita 4 is getting stable enough for many people to use day in, day out. There's still more to be done, of course! So we'll continue fixing issues and applying polish for at least another four weeks.

One of the things we're doing as well is redesigning the set of default brush presets and brush tips that come with Krita. Brush tips are the little images one can paint with, and brush presets are the brushes you can select in the brush palette or brush popup. The combination of a tip, some settings and a smart bit of coding!

Our old set was fine, but it was based on [David Revoy](https://www.davidrevoy.com)'s earliest Krita brush bundles, and for Krita 4 we are revamping the entire set. We've added many new options to the brushes since then! So, many artists are working together to create a good-looking, useful and interesting brushes for Krita 4.

[![](../images/brushj_presets-1024x529.png)](https://krita.org/wp-content/uploads/2018/02/brushj_presets.png)

It's still work in progress! But we want your feedback. So... Download the new Krita 4 development builds, and start doodling, sketching, painting, rendering... And then tell us what you think:

[Do the brush preset survey](https://goo.gl/forms/xRbDIZRnRX005ZOt2)!

Apart from the new brushes, and the bug fixes, there's also news for Linux users: we updated our AppImage build scripts, and the new appimage includes Python scripting and the Touch UI docker. Note: by default all scripts are disabled, so you need to go to Settings/Configure Krita/Python scripts and enable the scripts you want to use.

#### Help with the release!

We're having our hands full with tasks like coding, bug fixing, manual updating... More than full! One task that looks like it's going to slip is creating a cool what-new-in-4 release video. So: if you're good at creating videos and want to help the team, please join us on #krita on irc.freenode.net and help us out!

#### Windows

Note for Windows users: if you encounter crashes, please follow [these instructions](https://docs.krita.org/Dr._Mingw_debugger) to use the debug symbols so we can figure out where Krita crashes. On Windows, gmic-qt is included.

- 64 bits Windows: [krita-nightly-x64-v4.0.0.51-325-g2126cec79f-setup.exe](https://download.kde.org/unstable/krita/4.0.0.52/krita-nightly-x64-v4.0.0.51-325-g2126cec79f-setup.exe)
- Portable 64 bits Windows: [krita-nightly-x64-v4.0.0.51-325-g2126cec79f.zip](https://download.kde.org/unstable/krita/4.0.0.52/krita-nightly-x64-v4.0.0.51-325-g2126cec79f.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/unstable/krita/4.0.0.52/krita-nightly-x64-v4.0.0.51-325-g2126cec79f-dbg.zip)

#### Linux

On Linux, you need to download the gmic-qt appimage separately. You can configure the location of gmic-qt in Krita's settings. Krita requires the "XDG\_DATA\_DIRS" environment variable to be set. Most distributions do this, but if yours doesn't, set "XDG\_DATA\_DIRS" to "/usr/local/share/:/usr/share/" as a workaround. Next build Krita will do this by itself.

- 64 bits Linux: [krita-4.0.0-beta1-b322ae6-x86\_64.appimage](https://download.kde.org/unstable/krita/4.0.0.52/krita-4.0.0-beta1-b322ae6-x86_64.appimage)
- AppImage: [gmic\_krita\_qt-x86\_64-2.2.0.appimage](https://download.kde.org/unstable/krita/4.0.0.52/gmic_krita_qt-x86_64-2.2.0.appimage)

(If, for some reason, Firefox thinks it needs to load this as text: to download, right-click on the link.)

#### OSX/macOS

The minimum version of OSX/macOS is 10.11

- OSX disk image: [https://download.kde.org/unstable/krita/4.0.0.52/krita-4.0.0-g2126cec79f.dmg](https://download.kde.org/unstable/krita/4.0.0.52/krita-4.0.0-g2126cec79f.dmg)

Note: the python, gmic-qt and pdf plugins are not available on OSX.

#### md5sums

For all downloads:

- [md5sum.txt](https://download.kde.org/unstable/krita/4.0.0.52/md5sum.txt)

#### Support Krita

Krita is a free and open source project. Please consider supporting the project with [donations](/support-us/donations/) or by [buying training videos or the artbook!](/support-us/shop) With your support, we can keep the core team working on Krita full-time.

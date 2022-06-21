---
title: "Krita 3.1.2 released!"
date: "2017-02-01"
---

Krita 3.1.2, released on February 1st 2017, is the first bugfix release in the 3.1 release series. But there are a few extra new features thrown in for good measure!

### Audio Support for Animations

<iframe src="https://www.youtube.com/embed/s08oHOjxo84" width="100%" height="450" frameborder="0" allowfullscreen="allowfullscreen"></iframe>

Import audio files to help with syncing voices and music. In the demo on the left, Timothée Giet shows how scrubbing and playback work when working with audio.

- Available audio formats are WAV, MP3, OGG, and FLAC
- A checkbox was added in the Render animation dialog to include the audio while exporting
- [See the documentation](https://docs.krita.org/Audio_for_Animation) for more information on how to set it up and use the audio import feature.

Audio is not yet available in the Linux appimages. It is an experimental feature, with no guarantee that it works correctly yet -- we need your feedback!

### Other New Features

- Ctrl key continue mode for Outline Selection tool: if you press ctrl while drawing an outline selection, the selection isn't completed when you lift the stylus from the tablet. You can continue drawing the selection from an arbitrary point.
- Allow deselection by clicking with a selection tool: you can now deselect with a single click with any selection tool.
- Added a checkbox for enabling HiDPI to the settings dialog.
- remove the export to PDF functionality. It is having too many issues right now. ([BUG:372439](https://bugs.kde.org/show_bug.cgi?id=372439))

There are also a lot of bug fixes. Check the [full release notes](https://krita.org/en/release-notes-for-3-1-2/)!

### Get the Book!

If you want to see what others can do with Krita, get [**Made with Krita 2016**](https://krita.org/en/item/made-with-krita-2016-the-krita-artbook/), the first Krita artbook, now available for pre-order!

\[caption id="attachment\_4645" align="alignleft" width="217"\][![Made with Krita 2016](images/cover_small-217x300.png)](https://krita.org/wp-content/uploads/2016/12/cover_small.png) Made with Krita 2016\[/caption\]

### Give us your feedback!

Almost 1000 people have already filled in the 2017 Krita Survey! [Tell us how you use Krita, on what hardware and what you like and don't like!](https://goo.gl/forms/9SUIE7xwszu2T7RB3)

#### Windows

Note for Windows users: if you encounter crashes, please follow [these instructions](https://docs.krita.org/Dr._Mingw_debugger) to use the debug symbols so we can figure out where Krita crashes.

- 32 bits Windows: [krita-3.1.2.2-x86-setup.exe](http://download.kde.org/stable/krita/3.1.2/krita-3.1.2.2-x86-setup.exe)
- Portable 32 bits Windows: [krita-3.1.2.2-x86.zip](http://download.kde.org/stable/krita/3.1.2/krita-3.1.2.2-x86.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](http://download.kde.org/stable/krita/3.1.2/krita-3.1.2.2-x86-dbg.zip)

- 64 bits Windows: [krita-3.1.2.1-x64-setup.exe](http://download.kde.org/stable/krita/3.1.2/krita-3.1.2.1-x64-setup.exe)
- Portable 64 bits Windows: [krita-3.1.2.1-x64.zip](http://download.kde.org/stable/krita/3.1.2/krita-3.1.2.1-x64.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](http://download.kde.org/stable/krita/3.1.2/krita-3.1.2.1-x64-dbg.zip)

#### Linux

- 64 bits Linux: [krita-3.1.2-x86\_64.appimage](http://download.kde.org/stable/krita/3.1.2/krita-3.1.2-x86_64.appimage)

A snap image for the Ubuntu App Store will be available soon. You can also use the [Krita Lime PPA](https://launchpad.net/~kritalime/+archive/ubuntu/ppa) to install Krita 3.1.2 on Ubuntu and derivatives.

#### OSX

- OSX disk image: [krita-3.1.2.0.dmg](http://download.kde.org/stable/krita/3.1.2/krita-3.1.2.0.dmg)

### Source code

- Source code: [krita-3.1.2.1.tar.gz](http://download.kde.org/stable/krita/3.1.2/krita-3.1.2.1.tar.gz)

#### md5sums

For all downloads:

- [md5sums.txt](http://download.kde.org/stable/krita/3.1.2/md5sums.txt)

#### Key

The Linux appimage and the source tarbal are signed. You can retrieve the public key over https here: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8). The signatures are [here](http://download.kde.org/stable/krita/3.1.2).

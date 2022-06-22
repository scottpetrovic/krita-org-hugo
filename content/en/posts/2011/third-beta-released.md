---
title: "Third Beta Released!"
date: "2011-10-26"
---

Today the Krita team together with the [Calligra](http://www.calligra-suite.org) team have released the third and hopefully final beta of Krita 2.4! This beta incorporates the strokes framework developed by Dmitry Kazakov during his Google Summer of Code project as well as the first results of Siddharth Sharma's Photoshop import filter project. We really need a good hammering of this beta to make sure we're in excellent shape for the final release!

The Krita team is organizing a bug day where the team will be on irc from early in the morning until late at night across a selection of time zones to help everyone get the latest version of Krita up and running and to help you test Krita and triage bugs. Help us by finding new bugs and confirming existing bugs!

Join us all on #krita on irc.freenode.net on Saturday November 5th!

![](/images/posts/2011/swordman_sm.png)

The Swordman of the Apocalypse by Alvaro Dopazo -- featured on the beta 3 splash screen, to inspire all developers and everyone else. He is ready to slash some bugs. Are you?

### New Features in this beta

The strokes framework is a new design for handling your painting. All painting is done in the background, so Krita is always ready for your next action. This means that even if you're giving Krita and your computer a hard time, for instance by painting with enormous brushes on a ginormous canvas, Krita won't drop any subtleties in your stroke. To test this all you need to do is paint, paint, paint and paint some more. And then of course show of the result in our gallery forum!

Krita now also has preliminary support for 8 and 16 bits RGB Photoshop files. Support for other colorspaces is being worked on. We have a fairly limited selection of test files, so we would love it if people started testing this feature and if they have a file that fails, sending it to [us](mailto:boud@kde.org) so we can improve the psd support!

Geoffry Song has implemented a new kind of autobrush mask, "gaussian", which has much smoother results that the other options ("Default" and "Soft brush"). However, it is also a bit slower, and best suited for smaller brush sizes, compared to the other two options.

The default order of tools in the toolbox has changed. Now we first have the generic vector shape manipulation tool and the text tool, then the krita specific tools and finally the other vector tools.

Srikanth Tiyyagura has made it possible to share ICC profiles using Get Hot New Stuff. However, dynamically loading a new profile is still broken and can lead to crashes.

Ramon Miranda's [Gimp Paint Studio](http://code.google.com/p/gps-gimp-paint-studio/) set of resources has been integrated: the brush tips, patterns, palettes and gradients from Gimp Paint Studio now form the default resource set. We are still working on a set of improved brush presets.

There's a new cursor type: a tiny circle, designed by David Revoy, for precise work.

Bug fixes: loading and saving of clone layers if there are layers with the same name in the stack, the color preview is now grayscale if the image is grayscale, the pixellize filter is fixed. The fill and select-by-color tools should be quite a bit faster now, as is the default canvas. The location of the swapfile is now configurable with the "swaplocation" key in Krita's configuration file. And many more!

Check out the [Visual Tour](http://krita.org/component/content/article/8-press-releases/94-krita-24-beta-release-visual-tour) for more information!

### Known issues in this beta

We still have more than one hundred open bugs, so there's plenty to do before we're ready for a Release Candidate. These are the most important caveats

- Some operations crash the OpenGL canvas. See [bug 28447](https://bugs.kde.org/show_bug.cgi?id=284457): we have a fix in some instances, but need thorough testing of the OpenGL canvas.
- Exchanging brush presets using GHNS is broken.
- The selection/transparency/filter mask painting system still only uses opacity, instead of the gray value. This means that you need to enable Eraser mode if you want to remove parts of a selection using a brush.
- The canvas still is centered wrongly after operations like zoom, crop or resizeis
- We are still working on a new set of default brush presets, so currently no full set of presets is preinstalled.

### Other News

Timothee Giet will visit Deventer in the weekend of November 5th to dedicate the comic + dvd packs and help them send out

![](/images/posts/2011/comics-with-krita-dvd-cover.jpg)

But there are still some copies left, so you can order yours if you haven't done so!

And don't forget to vote for Krita in the  2011 [Packt Open Source Awards](http://www.packtpub.com/open-source-awards-home?utm_source=updated_banner&utm_medium=homepage_banner&utm_campaign=unique_banner). Any proceeds will go towards more bug squashing! You can vote until October 31st!

### To Conclude

_"Just got a mind-blowing demo of #krita by @davidrevoy. Awesome stuff! Once released, that will be "da bomb", to quote him."_ -- Sebastian König on Twitter.

See for yourself, and install our third beta, now available from these fine Linux distributions:

### Source

The source code of the third beta is available for download: [calligra-2.3.83.tar.bz2](http://download.kde.org/download.php?url=unstable/calligra-2.3.83/calligra-2.3.83.tar.bz2)

### Debian

Debian currently hosts the Calligra beta packages in the http://qt-kde.debian.net/ project. To try Calligra, add the following to your /etc/apt/sources.list:

deb http://qt-kde.debian.net/debian experimental-snapshots main
deb-src http://qt-kde.debian.net/debian experimental-snapshots main

In order to get repository key, install the pkg-kde-archive-keyring

package:

aptitude install pkg-kde-archive-keyring

then you can install calligra with :

apt-get install krita

Then apt-get update will update Krita when the new betas are packaged.

### Ubuntu

Users of Ubuntu and Kubuntu are urged to try the daily snapshots prepared by [Project Neon](https://launchpad.net/project-neon). Paste the following in a terminal window and you'll find Calligra installed in /opt:

sudo add-apt-repository ppa:neon/ppa  && sudo apt-get update && sudo apt-get install project-neon-base     project-neon-calligra     project-neon-calligra-dbg

You can run these packages by adding /opt/project-neon/bin to your PATH.

Official Kubuntu packages are also expected soon.

### Arch Linux

Arch Linux provides Krita packages in the \[kde-unstable\] repository.

### Fedora

Fedora is working on packages and expects them to be available soon

### OpenSuse

There are OpenSUSE Krita packages in the [unstable playground repository](https://build.opensuse.org/project/show?project=KDE%3AUnstable%3APlayground).

### Gentoo

Gentoo has Krita packaged in Portage, tagged as unstable.

### FreeBSD

Krita ports will soon be available in [Area51](http://freebsd.kde.org/area51.php).

---
title: "Krita 2.4 Bug Day!"
date: "2011-11-02"
---

Next Saturday, November 5th, the world-wide Krita team will be all ready and preset in #krita on freenode for the Grand Annual Krita Bug Day (well, it's not really annual, at least not intentionally so). We're getting closer and closer to the final release of Krita 2.4, and we want it to be Good (that's Good with the capital E of Excellent). And for that, we need your help. Please install Krita from git or the latest beta from packages, and either try to reproduce the Krita bugs in [http://bugs.kde.org](http://bugs.kde.org) and tell us whether they are still valid, or just try to find new bugs. Try to break Krita!

The only thing worse than finding we need extra time to fix all the bugs you find is to release Krita with bugs we haven't discovered -- so help us out. Since the last [announcement](http://krita.org/component/content/article/10-news/97-third-beta-released), there are some updates on the packaging front for Gentoo, \*buntu and Debian:

First came [Andreas Huettel for Gentoo](http://dilfridge.blogspot.com/2011/10/towards-calligra-24.html). He says:

> I've just committed the ebuild for [Calligra 2.4 beta 3](http://www.calligra-suite.org/news/announcements/calligra-2-4-beta-3/), i.e. in Gentoo [app-office/calligra-2.3.83](http://packages.gentoo.org/package/app-office/calligra), to the portage tree. If all goes well this is going to be the last beta version before Calligra 2.4

Gentoo users rejoice!

Then Jonathan Riddel told me that Paolo Dias has packaged the latest beta for \*buntu -- \*buntu users now have a choice between project Neon (follows git master) and the official releases of the Calligra and Krita teams. This is the ppa:

https://edge.launchpad.net/~paulo-miguel-dias/+archive/peppa/+packages

It's experimental of course, but very, very welcome!

Finally, for Debian users there's great news: the [qt-kde debian project](http://qt-kde.debian.net/) has packages available as well now, thanks to Adrien. Right now it's beta2, but when Adrien returns from his well-earned vacation, he will update it to beta 3. Just follow these instructions:

According to the webpage (http://qt-kde.debian.net/), You have to add the following to your /etc/apt/sources.list:

deb http://qt-kde.debian.net/debian experimental-snapshots main deb-src http://qt-kde.debian.net/debian experimental-snapshots main

In order to get repository key, install the pkg-kde-archive-keyring package:

aptitude install pkg-kde-archive-keyring

then you can install calligra with :

apt-get install calligra

Help make Krita as good as possible by finding bugs for us to slash!

For yours truly and for Timothee Giet, the weekend will be doubly busy, since we'll also be sending out the first batch of dedicated training dvd+comic book packs! If you order now, you could get your copy dedicated -- but it's the last chance, after that, only boring, undedicated copies will be available!

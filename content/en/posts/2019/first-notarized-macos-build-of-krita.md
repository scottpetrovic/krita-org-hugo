---
title: "First Notarized macOS Build of Krita"
date: "2019-11-05"
categories: 
  - "development-builds"
---

Apple having decided it wants to deep inspect any application you might want to run on your Apple computer, has made what it calls "notarization" mandatory with macOS Catalina. Inevitably, Apple's documentation on the subject is highly defective, like [most developer documentation Apple provides](https://nooverviewavailable.com/).

We figured it out, in the end. It adds about half an hour to an hour, depending on how busy Apple's computers are, to the build and release process.

What happens is this: we build Krita, then we create an app bundle. Then we zip up the krita.app bundle and transfer the zip file to Apple, which then checks whether Krita uses any forbidden API's or contains its own html rendering engine and other such things that are highly dangerous for the well-being of the computers it allows its customers to use. Then we get a long string of numbers and letters back, which we can use to periodically check whether Apple is done checking. This can take ages, or happen relatively quickly. Then we need to execute a command to "staple" Apple's imprimatur to the app bundle.

Then we package the app bundle in a disk image, and... Upload that to Apple, which does the checking once again. We wondered whether it would be enough to "notarize" only the disk image, or only the app bundle, but after booting into Catalina, it appears that both need to be "notarized". We might still be mistaken, of course, and there might be ways to only upload Krita once to Apple. In any case, once more we wait for Apple to finish rooting around in the disk image, and if we get Apple's blessing, we once more go through the stapling thing, and we can upload the disk image for you to download.

We did that for our last stable build:

- [krita-4.2.7.1.dmg](https://download.kde.org/stable/krita/4.2.7.1/b/krita-4.2.7.1.dmg)

_**Note: you will have to make sure that the "Native File Dialogs" option is disabled, otherwise you cannot save files!**_

Weird but true, the checking for saving permissions seems built into the file dialog, not in the file system, so we still have to figure that out. Also be aware that notarized applications take a long time to start for the first time.

Another option could be to drop Apple and macOS as supported platforms for Krita, which wouldn't be too bad a thing, what with broken OpenGL drivers, the push for proprietary API's, interference with what application developers are allowed to do and broken-by-design hardware.

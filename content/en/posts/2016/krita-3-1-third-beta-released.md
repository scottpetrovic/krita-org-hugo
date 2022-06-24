---
title: "Krita 3.1: third beta released"
date: "2016-11-07"
---

Here is the third Krita 3.1 beta! From the Krita 3.1 on, Krita will officially support OSX. All OSX users are urged to use this version instead of earlier "stable" versions for OSX.

[![krita_animation_3_0_2](/images/posts/2016/krita_animation_3_0_2-1024x826.gif)](/images/posts/2016/krita_animation_3_0_2.gif)

Note one important change in this beta: saving no longer waits until the image is done rendering. This means that if Krita is still busy and you want to save, you will be warned that the saved file might be incomplete. We're still working on this, so it isn't the final solution for the saving problem, and if you want to to be sure to not lose data, save your work often...

These are the most important fixes:

- Several crash bugs were fixed
- Don't merge onion skins when merging two layers
- Make mirror mode hav different a axis center for each open image
- Load png's with a broken resolution tag
- Restore the shear cursor in the transform tool
- Update the splash image
- Fix loading the swatch names in ACO files
- Fix loading the photoshop shortcut theme (if you have empty menu entries in the previous beta, well, this beta fixes that)

Note: the beta still contains the colorize mask/lazy brush plugin. We will probably remove that feature in the final release because the current algorithm is too slow to be usable, and we're still looking for and experimenting with new algorithms. With the current beta you will get a preview of how the user interface will work, but keep in mind that the we _know_ that it's too slow to be usable and are working on fixing that

The third beta is also much more stable and usable than the first and second beta (3.0.1.90), and we'd like to ask everyone to try to use this version in production and help us find bugs and issues!

### Windows

- 32 bits Windows: [krita-3.0.92-x86-setup.exe](http://download.kde.org/unstable/krita/3.0.92/krita-3.0.92-x86-setup.exe) (MD5 Hash: 092d30cbb158b7ebdc027ddba4ae768d)
- Portable 32 bits Windows: [krita-3.0.92-x86.zip](http://download.kde.org/unstable/krita/3.0.92/krita-3.0.92-x86.zip) (MD5 Hash: 78de5fb91b81b6b2c2f08711be5b9a57)
- [Debug symbols. (Unpack in the Krita installation folder) (MD5 Hash: 634630de985522f6b9f88b5f07d30c65)](http://download.kde.org/unstable/krita/3.0.92/krita-3.0.92-x86-dbg.zip)

- 64 bits Windows: [krita-3.0.92-x64-setup.exe](http://download.kde.org/unstable/krita/3.0.92/krita-3.0.92-x64-setup.exe) (MD5 Hash: 37ae1e819948abeefb2b50497bd01993)
- Portable 64 bits Windows: [krita-3.0.92-x64.zip](http://download.kde.org/unstable/krita/3.0.92/krita-3.0.92-x64.zip) (MD5 Hash: 74f15723011b8429c6431aba65d77e1a)
- [Debug symbols. (Unpack in the Krita installation folder) (MD5 Hash: 7d958532d84e73d1d3eaeb29a7ae17b8)](http://download.kde.org/unstable/krita/3.0.92/krita-3.0.92-x64-dbg.zip)

### Linux

- 64 bits Linux: [krita-3.0.92-x86\_64.appimage](http://download.kde.org/unstable/krita/3.0.92/krita-3.0.92-x86_64.appimage) (MD5 Hash: 2437a99ca375fcf79647147680714076)

There is also a snap image available in the Ubuntu App Store, in the beta channel.

### OSX

- OSX disk image: [krita-3.0.92.dmg](http://download.kde.org/unstable/krita/3.0.92/krita-3.0.92.dmg) (MD5 Hash: 4a938af31688f321d75285825a19d902)

### Source code

- Source code: [krita-3.0.92.tar.gz](http://download.kde.org/unstable/krita/3.0.92/krita-3.0.92.tar.gz) (MD5 Hash: 1a794cd2758e1bf1c63354ae829b0947)

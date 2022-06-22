---
title: "Second Beta for Krita 3.1 Available"
date: "2016-10-22"
---

We're still fixing bugs like madmen... And working on some cool new features as well, but that's for a later release. In any case, here is the second Krita 3.1 beta! Yes, you're reading that correctly. Originally, we had planned to use 3.0.2 as the version for this release, but there is so much news in it that it merits a bigger version bump. Plus, with the acceptance of [Julian Thijssens' Google Summer of Code](https://codereview.qt-project.org/#/c/166202) work by the Qt Project, we're reaching a really big milestone:

From the next release on, Krita will officially support OSX.

[![krita3osx](/images/posts/2016/krita3osx-1024x793.jpg)](https://krita.org/wp-content/uploads/2016/10/krita3osx.jpg)

 

That means that the OpenGL canvas works fully and that we're committed to fixing OSX-specific bugs, just like we're fixing bugs on Windows and Linux. It means we're confident that you can use Krita 3.1 on OSX and be productive, instead of experimenting. So, please test this beta, and help us find bugs and issues!

Of course, Krita 3.1 will have much more new stuff. A new brush engine that supports really big brushes, Jouni's Google Summer of Code work on adding new features to animation, Wolthera's Google Summer of Code work that adds color managed high-channel depth color selectors and soft proofing to Krita, a stop-based gradient editor, [ffmpeg](http://ffmpeg.org/)\-based export to animated gif and video formats. And much more.

Note: the beta still contains the colorize mask/lazy brush plugin. We will probably remove that feature in the final release because the current algorithm is too slow to be usable, and we're still looking for and experimenting with new algorithms. With the current beta you will get a preview of how the user interface will work, but keep in mind that the we _know_ that it's too slow to be usable and are working on fixing that

The second beta is also much more stable and usable than the first beta (3.0.1.90), and we'd like to ask everyone to try to use this version in production and help us find bugs and issues!

### Windows

- 32 bits Windows: [krita-3.0.91-x86-setup.exe](http://download.kde.org/unstable/krita/3.0.91/krita-3.0.91-x86-setup.exe) (MD5 Hash: ead6024307112f5dd98b3c8c91547a85)
- Portable 32 bits Windows: [krita-3.0.91-x86.zip](http://download.kde.org/unstable/krita/3.0.91/krita-3.0.91-x86.zip) (MD5 Hash: 4d36a3648f55137b39c4fe9238b1b5d4)

- 64 bits Windows: [krita-3.0.91-x64-setup.exe](http://download.kde.org/unstable/krita/3.0.91/krita-3.0.91-x64-setup.exe) (MD5 Hash: 56522b839bc04d36730518f2d42ed541)

- Portable 64 bits Windows: [krita-3.0.91-x64.zip](http://download.k
    de.org/unstable/krita/3.0.91/krita-3.0.91-x64.zip) (MD5 Hash: 56e88e68a6f113e77e0b58d6fc313a8c)

### Linux

- 64 bits Linux: [krita-3.0.91-x86\_64.appimage](http://download.kde.org/unstable/krita/3.0.91/krita-3.0.91-x86_64.appimage) (MD5 Hash: 4531ee79eb67d4959b7e4ff91db25681)

There is also a snap image available in the Ubuntu App Store, in the beta channel.

### OSX

- OSX disk image: [krita-3.0.91.dmg](http://download.kde.org/unstable/krita/3.0.91/krita-3.0.91.dmg) (MD5 Hash: 6bd801060b189af0c6efc823a3ac41f4)

### Source code

- Source code: [krita-3.0.91.tar.gz](http://download.kde.org/unstable/krita/3.0.91/krita-3.0.91.tar.gz) (MD5 Hash: 936d256c7e889485ed4722113b2f2bcd)

---
title: "Windows Installer Ready for Testing"
date: "2011-12-21"
---

It is with a certain amount of trepidation that I hereby announce and unveil the first Calligra installer package for Windows. It includes Krita... Thanks to the generous sponsorship by [NLNet](http://nlnet.nl) and [KO GmbH](http://www.kogmbh.com)! The foundation for the work was laid by the [KDE-Windows](http://windows.kde.org/) people. The package also includes other Calligra applications. A dedicated Krita-only will be prepared later on.  

Now before everything else please note: this is experimental. Very experimental. There definitely are problems. I have managed to paint for about half an hour on Windows and didn't experience a crash or a lock-up. But Krita on Windows still uses LCMS1, not LCMS2 which does mean there will be problems with filters. There might also be performance problems because of this. Krita on windows also misses support for floating point colorspaces because [OpenGTL](http://opengtl.org) hasn't been ported yet.  

Please do report any bugs you find in [bugs.kde.org](http://bugs.kde.org)!

You can download the installer from [www.kogmbh.com/download.html](http://www.kogmbh.com/download.html) -- have fun testing and report back your findings!  

![](/images/posts/2011/krita_windows.png)

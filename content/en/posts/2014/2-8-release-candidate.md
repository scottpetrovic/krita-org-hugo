---
title: "2.8 Release Candidate"
date: "2014-02-27"
---

Still labelled as 2.8 beta3, the 2.7.9.12 is pretty close that what we hope to release next Wednesday. Compared to the .11 build, there are the following improvements:  
  
[http://heap.kogmbh.net/downloads/krita_x64_2.7.9.12.msi](http://heap.kogmbh.net/downloads/krita_x64_2.7.9.12.msi)  
[http://heap.kogmbh.net/downloads/krita_x86_2.7.9.12.msi](http://heap.kogmbh.net/downloads/krita_x86_2.7.9.12.msi)  
  
The XP package is being built and will be available later on.

There is also an Ubuntu package available in the [Krita Lime repository](https://launchpad.net/~dimula73/+archive/krita). [Read all about it on Dmitry's blog](http://dimula73.blogspot.ru/2014/02/krita-28-beta3-is-now-in-krita-lime.html)!  

- Fix saving compositions (BUG:331310)
- New erase toggle icon
- Fix a memory leak when using the brightness/contrast curve (BUG:330479)
- Save resolution info to OpenRaster files (BUG:321106)
- Make handling custom input profiles more robust, also when updating (this should be the first 2.7.9.x release where you shouldn't need to remove the input settings folder)
- add a reset button to the input profile editor
- Fix wraparound mode for the selection painting tools
- Crop selection masks when activating the wraparound mode (BUG:330372)
- Fix painting the cursor outline when there is no cursor outline (BUG:330570)
- Make painting on high bit depth images much faste when the OpenGL canvas is enabled (BUG:331347)
- Fix updates of the canvas rulers (BUG:330129)
- Fix moving of a selection out of a layer (BUG:324373)
- Fix saving indexed PNG files with current versions of libpng
- Update to the latest G'Mic version and enable the G'Mic plugin on windows
- Make the G'Mic dialog resize when selecting a filter (fixes layout issues)
- Add a crash handler for Windows that uploads minidumps (the website that goes with it is not done yet!) and offers a clean restart

The final release is expected for next Wednesday.

* * *

And if you're new to Krita, don't forget that the [Muses Training DVD by Ramon Miranda](http://krita.org/item/216-muses) is shipping _now_!![](/images/posts/2014/pixel.gif)

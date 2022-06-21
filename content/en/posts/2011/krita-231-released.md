---
title: "Krita 2.3.1 Released"
date: "2011-01-19"
---

Today Krita 2.3.1 has been released. Your favourite Linux distribution might already have it available! This is a bugfix release, mainly focusing on some problems with working with large images, from 50 megapixels onwards. Note that for large images, you still need a lot of real memory.  

The following issues were fixed:  

- limit size of custom patterns to fit 1000x1000 -- avoid memory problems
- fix error in memory handling. This means really large images are more feasible now
- disable the tile pooler, saving memory for really large images
- fix crash when editing a brightness contrast filter in the action editor
- Do not crash on startup when loading the tutorial if always start with template is checked (bugs 261911, 261940)

Not yet fixed are the upscaling problem Ico-dY reported (this problem only happens intermittently, but we've been able to reproduce it and are working on it) and the broken swapfile. We're also working on that, so there definitely will be a 2.3.2.

---
title: "Looking Forward"
date: "2016-12-16"
---

We have just [released Krita 3.1](/item/krita-3-1-released-and-looking-forward/), but we are already deep into coding again! We will continue releasing bug fix versions of Krita 3.1.x until it's time to release 3.2 (or maybe 4.0...). And, as with 2.9, some bug fix releases might even contain new features, if they're small and safe enough. But we'll also start making development builds soon, and there's also the  [daily build for Windows](https://ci.appveyor.com/project/alvinhochun/krita-packaging/build/artifacts).

**For the 2015 kickstarter features, we're working on the following items:**

- Lazy Brush: the interactive colorizing tool. We spent a lot of time to get this to work, and it _does_ work and can be enabled in 3.1 (add **disableColorizeMaskFeature=false** to the kritarc file). The algorithm we implemented is simply too slow to be useful. We will keep the existing user interface for it, but will work on a faster algorithm.
- Improved palette handling: we've started work on adding support for two new palette formats that can handle color correctly already. We intend to rewrite the palette editor in Python, and for that we need 2016's Python scripting to be done. That is moving along quite nicely! More information on that below.
- Stacked brushes: This functionally works and is pretty innovative, even! But it is difficult to configure stacked brushes with the existing brush editor UI design. We've started re-working the brush editor already to make way for this feature. When that work is done this feature can land. The new brush editor UI is still being refined:

[![screenshot_20161213_143102](/images/posts/2016/Screenshot_20161213_143102-300x180.png)](https://krita.org/wp-content/uploads/2016/12/Screenshot_20161213_143102.png)

**For the 2016 Kickstarter features, we're working on the following items:**

- SVG Support: We've started on the vector file format rewrite. We're now at a stage where Krita can load and save the SVG format instead of ODG -- though a bit of work remains to be done. We can then start hooking up the functionality to the redesigned tools on the UI.
- Python Scripting: The API has been defined on what it will do. Everything builds and works. Most of the API still needs to be hooked up for things to work still, but you an already iterate through the layers and masks in an image and save them.  There is also a separate command-line utility to run scripts, without needing to start the entire gui. But we need to figure out how to build and bundle Python on OSX and Windows! And Eliakin Costa, a Season of KDE student is working on a gui to create, run and save scripts from within the gui.
- Text Tools: We have had some discussion about what features will be included and how it will fit into the application's UI design -- but no coding done yet. The text tools will be using SVG, so we need to wait until that is done before we start digging too deep into this.
- Reference Images Docker: we're also considering rewriting this docker completely, in Python.

And of course this is just what we've _planned_. With outside people making code changes and new people joining, it will be an adventure to see what actually happens. There will no doubt be more exciting features coming along the way in 2017!

---
title: "First Target Reached!"
date: "2015-05-18"
---

On Sunday, we made the base target for our Kickstarter! Unless too many backers decide to cancel their pledges, funding for making Krita really, really fast and animation support is secure! Now, of course, is not the time to fold the hands and lean back: it would be a pity if we don't manage to reach a handful or even more stretch goals!

But having reached this milestone, it's time to make it easy to back the project through paypal:

- **[https://krita.org/2015-kickstarter/](https://krita.org/2015-kickstarter/)**

You can choose your reward level in the comment, and from 15 euros you'll get your stretch goal voting rights, of course!

Talking about stretch goals... Michael Abrahams surprised us all by submitting a [patch on reviewboard](https://git.reviewboard.kde.org/r/123833/) that implemented most of the selection tools improvement stretch goal! Shift, alt, shift all, ctrl have been implemented for the polygonal, elliptical and rectangular selection tools. The rest is still todo, so it's not ready for a build yet.

We've been busy working on fixing other issues as well:

- Dmitry implemented Pass-Through mode for group layers (note: filter, transform and transparency masks and pass-through mode don't work together yet, but loading and saving from and to PSD does!
- When using Krita with a translation active on windows, the delay on starting a stroke is a bit less, but we're still working on eliminating that delay completely
- The color picker cursor now shows the currently picked and previous color.
- We now can load layerstyles (with some limitations) from PSD files. Saving is coming next!
- Layer styles can now be used with inherit-alpha
- Fix some issues with finding templates
- Work around an issue in the oxygen widget style that would crash the OpenGL-based canvas due to double initialization
- Don't toggle the layer options when right-clicking on a layer icon to get the context menu (patch by Victor Wåhlström)
- Update the Window menu when a subwindow closes
- Load newer PSD-generated JPG files correctly by reading the resolution information from the TIFF tags as well. (Yes, JPG resolution is marked in the exiv metadata using TFF tags...)
- Show the image name in the window menu if it hasn't been saved yet.
- Don't crash when trying to apply isolate-layer on a transform mask
- Add webp support (at least on Linux, untested on Windows)
- Use the right Krita blending mode when a PSD image contains Color Burn.
- Add Lighter Color and Darker Color blending modes and load them from PSD.
- Add a shortcut to edit/paste into a new image. Patch by Tiffany!
- Fix the autosave recovery dialog on Windows for unnamed autosaves

Unfortunately, all this has left our codebase in a _slightly_ unstable state...  We tried to make new builds, but they just aren't good enough yet to share! Working on that, though, and hopefully we'll get there by Wednesday!

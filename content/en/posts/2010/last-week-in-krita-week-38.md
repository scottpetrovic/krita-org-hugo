---
title: "Last week in Krita -- week 38"
date: "2010-09-25"
---

### Release

So... Where do we stand with our release preparations. There are still quite a few hurdles to take: we are at 68 bugs now, of which there is 1 **critical**, 5 are major (and thus release blockers) and 14 crashes. And it goes without saying that there are some bugs we really want solved among the rest as well. Krita gets a lot of testing these days (though more is always welcome!) and that means that while we're resolving lots of issues, we're finding new ones as well. There are still a number of unittests that fail -- one of them has been tracked down to a difference between version 0.6 and 0.8 of the jpeg library, but there are others. Those need to be solved before we can release as well. Finally, we might need to do some more work on the way our tools queue their actions. It's too early to say whether this means the release date will have to slip or not, but if it has to, then we will slip.

Still, we're getting close to about a hundred commits a week so the pace is pretty fast!

Another thing is user documentation. I'm still working on the updated manual, but I've also created something new: a Krita image that will show on the very first run and has a numbe rof layer groups, with every group explaining something cool about Krita. Unfortunately, this is only in English and I haven't found a good way to make translated versions. Especially since the file is rather big. We might end up only loading it when Krita run in an English locale.

![](/images/posts/2010/first_run.png)  

Erm... We might want to go into the look of this a bit with some qualified artist...

### Code

Everyone is really busy fixing bugs, so there are no exciting new features to report on. Still, bear with me for a report on what got fixed and what got broken!

**Adam Celarek** fixed the display of the soft-brush curve and fade sliders. He fixed a crash that occurred when switching paintops while the canvas was being updated, fixed the autoupdate for the image colors in the new color selector and optimized the speed of updating. A small new feature, in the KOffice-essen branch (which is the feature branch we open during trunk freeze): a template for new docker plugins, which was then used as the base for a docker for presets. Adam also beatified the transform/warp tool option pane. And -- and this is _really_ nice -- fixed the scratchpad in the brush designer to work correctly in wash mode.

**Boudewijn Rempt** did some cleanup, fixed the gradient, fill and transform tool to lock the current layer while a long-running task is running, added the comic-book templates Animtim created, created the first-run picture and make it show up. Krita now also warns when you are running with a version of Qt earlier than Qt 4.6.3 -- below that, you will not be able to use your tablet. In response to a requirement from Lukas, he implemented a white-list mechanism for blending modes: some brush engines, like the pixel brush can't do anything useful with, for instance, the COPY blending mode, while others, like deform or smudge, absolutely need those. Finally, Boudewijn made sure the quick-access palette has some default content and fixed a number of memory leaks.

**Cyrille Berger** sneaked off to present his wife to his family in Normandy -- all the while thinking hard on a rounding problem in Krita's integer maths. He also fixed the display of the rotation feature in the pixel brush. And he painted a tree in Krita:

![](/images/posts/2010/datree.png)  

**Dmitry Kazakov** in his first month of sponsored part-time development (thanks to **Silvio Grosso**!) moved the pan and color picking feature of the freehand tool down the tool hierarchy: all tools support pan on middle-click now, and all painting tools can also pick a color from the canvas. He fixed the brush outline updating on the QPainter-based canvas and made sure the tool decorations are also shown on the canvas outside the image boundaries. Finally, he fixed the application of masks and filters when there is a selection.

**Jonathan Riddell** proposed a patch by **Emmet Hikory** from Ubuntu to make it possible to compile Krita on ARM processors. This got reviewed, ported by Boudewijn, updated by Emett and then committed by Jonathan. Of course, we are heavily dependent on distributions for patches of this kind --  **Ana Beatriz Guerrero López** from Debian is a regualar in this blog for fixing Krita to compile on ARM.  

**José Luis Vergara** spent a lot of time fixing the smudge paintop, together with Cyrille and Lukas. The problem here is that Krita is way more flexible with smudgiing than any other application: we support various blending modes for smudge, as well a variable size of the smudge area depending on tablet pressure.

**Lukas Tvrdy** made it possible to test the dynabrush brush engine in the scratchpad, fixed the slow performance of the spray, hairy and chalk brush on CMYK images (but please remember this: _the best colorspace to paint on is 16 bit RGBA with a linear-light profile_! Try it -- the difference is amazing!). When working with the duplicate brush editor the scratchpad is now disabled (there's nothing to duplicate from, so it didn't make sense). Lukas fixed a number of memory leaks as well. He fixed the outline of the dyna tool, got a job with Ixonos, improved the dynabrush brush engine even more and fixed a crash. Lukas spent a lot of time investigating the remaining issues with our smudge brush as well.

**Marc Pegon** spent time polishing the transform/warp tool: he fixed the tool handles to make them visible on dark images, a number of crashes, fixed the perspective feature and made some fixes to the warp feature.

**Sven Langkamp**, in between exams at university, fixed a total of _nine_ bugs in one week, and found time for a lot of fixes that weren't in bugzilla yet. Among other things, the filter dialog now is a lot faster, the convolution code got fixed, fixed a nasty bug with the move tool where a new layer would be created on every mouse-click, improved the locking of nodes by the tools, fixed the updating of previews in the layer box, and fixed a number of memory leaks.

### Conclusion

There are still plenty of changes, so we're not near the Release Candidate. Please help us find more bugs by testing Krita -- and if you like some nice coding, why not join the team? Lots of nice bug fixing to be done!

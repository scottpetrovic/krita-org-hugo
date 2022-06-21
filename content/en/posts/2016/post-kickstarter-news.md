---
title: "Post-Kickstarter News"
date: "2016-06-25"
---

The campaign season is over, and we're slowly recovering and getting back into a productive groove of coding, coding, coding and more. Kickstarter has transferred €34,594.37 to our bank account, and we've started planning the next releases. Time for an update!

### Kickstarter Surveys

The survey replies have been streaming in! We've already contacted a dozen artists and commissioned artwork for the rewards. For Kickstarter rewards, we're paying for the work, as promised! The backers who wanted character sketches have been put in touch with the artists who wanted to do those! Only the art book will feature work for the exposure. Check out the [call for submissions](/item/call-for-submissions-for-the-2016-art-of-krita-book/)! (We're working on getting an icc proofing profile from the printer because... See below!)

With the majority of surveys returned, we can be pretty sure of the final stretch goal ranking. Python is No. 1 and SVG import/export is No 2! And with those goals reached, the other stretch goals have to wait until next year (or be implemented by a fearless volunteer -- like [**16\. Numerical Input Widget**](https://phabricator.kde.org/D1875). That looks like it might get into 3.1 after all!

Here's the full vote breakdown:

1. **Goal 24. Python Scripting Plugin: 587 votes**
2. **Goal 8. SVG Import/Export: 544**
3. Goal 1. Transform from pivot point: 258
4. Goal 21. Flipbook/Sketchbook: 251
5. Goal 2. Composition Guides: 239
6. Goal 7. Vector Layers as Mask: 182
7. Goal 15. Smoother Gradients: 175
8. Goal 13. Arrange Layers: 167
9. Goal 23. Audio Import: 164
10. Goal 19. Improve Calligraphy Tool Drastically: 152
11. Goal 6. Reference Images Docker: 134
12. Goal 5. Export a tag as a bundle: 123
13. Goal 17. Stroke Paths with Brushes: 113
14. Goal 3. Global Texture for Texture Brush: 110
15. Goal 4. Make bundles smarter to get a more usable interface: 101
16. Goal 11. Convert Height Map to Normal Map: 100
17. Goal 20. Stop-based gradient editor: 87
18. Goal 22. Rotatable, Scalable Patterns: 71
19. Goal 18. Objects Outliner: 62
20. Goal 16. Numerical Input Widget: 45
21. Goal 12. LUT Baking: 34
22. Goal 9. Move Assistants to a Separate Layer Type: 32
23. Goal 14. On-Canvas Layer Tooltips with Layer Selection Tools: 31
24. Goal 10. Convert Vector Shape to Assistant: 28

With Python clearly in the lead, we already started on implementing a Python scripting plugin, in the hope that we can use that to implement some of the remaining 2015 stretch goals, like the improved palette/color swatches docker. It already somewhat works: you can create Krita plugins in Python that add dockers or menu items, and there's a Python plugin that makes it possible to run Python scripts from Krita with access to the Krita Python API. Which is currently limited to counting the number of open windows, but still!

[![scripter](../images/scripter-1024x582.png)](https://krita.org/wp-content/uploads/2016/06/scripter.png)

### Google Summer of Code

It's mid-term time already for our Google Summer of Code students! All of them passed, fortunately, because all of them are doing great work. Wolthera is nearly finished with implementing soft-proofing. She even already wrote a [manual page](https://docs.krita.org/Soft_Proofing) for the feature, and it's currently being tested extensively. If all is fine, and it's looking good, soft-proofing will land in Krita 3.0.1, which would make Krita once again one of the first projects participating in Google Summer of Code to release the results to the world! Soft-proofing includes configurable gamut alarms and white-point adaptation slider that can be used to check the effect of paper on your image. Krita will save the proofing profile with your image, instead of relying on a global setup, which means you can create templates for particular printers, for instance. And you can have a proofed and an unproofed view of your image _at the same time_.

[![gamut_alarms_fast](../images/gamut_alarms_fast-1024x553.png)](https://krita.org/wp-content/uploads/2016/06/gamut_alarms_fast.png)

Julian Thijsen is hard at work on fixing the OpenGL QPainter engine. Check out [his series of blog posts,](http://kritadev.blogspot.nl/) detailing the paths his adventure takes him on. There's a lot of work to do here, but progress is brisk! And in the end, his work will be submitted for inclusion in Qt, which means everyone will benefit. Right now, the goal is to fix Qt's OpenGL backend for the QPainter class so it can render all of Krita's tools -- that's things like cursors, or the assistants, or the line that the gradient tool draws.

[![Working_01](../images/Working_01.png)](https://krita.org/wp-content/uploads/2016/06/Working_01.png)

Jouni Pentikainen is busy working on interpolation curves so we can automatically and smoothly animated changes in, for example, opacity. He's also working on making it possible to animate transformation masks between frames -- and that's something that'll give animators enormous freedom! Check out his [blog for more information](http://kritaanimation.blogspot.nl/). This is a mockup, created during the discussions about the flow of interaction and user experience design:

[![interpolation-mockup](../images/interpolation-mockup.png)](https://krita.org/wp-content/uploads/2016/06/interpolation-mockup.png)

### Releases

We've made a new release schedule: 3.0.1 will be released July 15th. Apart from a lot of bug fixes, for instance [for tablets with broken drivers](https://krita.org/item/anatomy-of-a-bug-fix/), onion skinning, drag & drop of layers on Windows, there will be a host of goodies. Michael Abrahams managed to restore the full-screen mode on Windows, Eugene Ingerman has improved the look and feel of the histogram dialog (and is working on a histogram docker and improved thumbnails for the channel and layer docker and improved rendering for the overview docker). If all goes well with what is a big refactoring, you'll be able to render an animation to [animated gif and several other video formats directly from Krita (2015 stretch goal)](https://phabricator.kde.org/T116). The [2015 Fuzzy Strokes stretch goal](https://phabricator.kde.org/T166) is in! And we might get soft-proofing, too.

And after the release of Krita 3.0, the animation edition, [Saisho Kazuki](https://twitter.com/motoaki_saisho), a professional Japanese animator adopted Krita as one of his tools. He readily agreed to our request to contribute a template he made for his work to us. His templateis based on true steps of animation which are used in Japanese Anime Studios -- and that will also be in Krita 3.0.1:

[![animation_template](../images/animation_template-1024x577.png)](https://krita.org/wp-content/uploads/2016/06/animation_template.png)

For a zero-dot-one release, this is going to be pretty exciting!

We intend to release new version in the 3.0 series every month until 3.1 is released with all 2015 stretch goals included -- and probably the first version of the Python scripting plugin, if it turns out we can use that to implement some more stretch goals. That should be done somewhere between end of August and end of October. It's too early to have a hard-and-fast date for it!

### Sprint

Every other year or so, Krita developers and artists get together in sunny Deventer, the Netherlands, to discuss the project's direction and goals, to hack together and basically to touch base with each other. These sprints are really productive. The [last one was in 2014](https://dot.kde.org/2014/06/04/2014-krita-sprint-deventer-netherlands), so it's time for another sprint! This will happen end of August. Travel is sponsored by our umbrella community, KDE. KDE is running a fund raiser right now to fund sprints like ours -- so don't hesitate [to click here and chip in](https://www.kde.org/fundraisers/randameetings2016/)! The Krita Foundation is sponsoring accommodation -- we try to fit as many people as possible in the Foundation HQ, but this time we're going to need more beds!

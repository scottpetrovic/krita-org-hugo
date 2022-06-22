---
title: "Last week in Krita — week 21&22"
date: "2014-06-02"
---

Last weekend we celebrated a Krita sprint in Deventer, an event that reunites Krita’s developers to talk about, coordinate and if possible code the next steps in Krita’s roadmap. The discussion themes where varied and went from Krita foundation status to specific software features such as OpenGL default setting. Other topics included:

- _2.9 main features_ and code emphasis and 3.0 roadmap priorities. In general we laid out a plan on how to code all the plans needed for a successful 2.9 release and a solid 3.0 version with the new powerful qt 5.0
- _Multiple documents View_. An informative session on the current code status of the branch and discussion on the technical complexities of making it happen.
- _Text and vector tools_ enhancement was a big topic on the table. Big changes and improvements are now set to happen from 3.0 building slowly towards the future.
- _Translation:_ We established the work that needs to be done to standardize all translatable strings and make internationalization consistent across languages.
- Discover-ability of features within the app and tool tips. A decision was made about this: create a simple system to allow the user to submit a help tool tip for the community.
- _OpenGL default settings:_ Krita has two painting engines, while both work okay. The non-GL engine is very slow on Windows. It was decided to turn the OpenGL engine on by default and, if not supported, fall-back to the CPU based one.

### This week’s new features:

- Index colors filter. (Manuel Riecke)
- Allow to lock docker state. (Boudewijn Rempt)
- Improved gradient editor: save rename edit. (Sven Langkamp)
- Show a floating message when rotating, mirroring and zooming the canvas. (Dmitry Kazakov)

#### Index colors filter

This filter allows you to reduce the number of colors displayed using a color ramp’s map.

![Filter: Index Colors dialog](/images/posts/2014/w_indexed_d01.jpg)

![Filter: Index Colors variants](/images/posts/2014/w_indexed_01.jpg)

Some uses for the filter include HD index painting as in the video below.

{{< youtube v1Z__mSfo8s >}}

#### Lock docker state

It’s now possible to lock the dockers in position to avoid any modification. This solves the problem of accidentally moving the dockers while adjusting layers and options.

![Dock lock position](/images/posts/2014/w_lock-state.jpg)

#### Improved gradient editor

The gradient editor received necessary improvements. This makes creating gradients a lot easier and gives the option to rename and edit. It's now much faster to get exactly the gradient you are building.

![Gradient Editor](/images/posts/2014/w_gradient_ed.jpg)

#### Floating messages

Rotating, Zooming and Mirroring canvas will now trigger a nice message at the top of the screen with the current degree, zoom level or ON/OFF states. The message will stay for a second before fading out. Neat!

![Floating messages](/images/posts/2014/w_floating_s.jpg)

### General bug fix and features

- FIX [#335438](https://bugs.kde.org/show_bug.cgi?id=335438): Fix saving on tags for brushes. (Sven Langkamp)
- Fix crash in imagesplit dialog. (Boudewijn Rempt)
- FIX [#335382](https://bugs.kde.org/show_bug.cgi?id=335382): Fix segfault in image docker on ARM. (Patch: Supersayonin)
- Improved gradient editor. Create segmented gradients, edit, rename. (Sven Langkamp)
- Show the current brush in the statusbar, CCBUG:[#332801](https://bugs.kde.org/show_bug.cgi?id=332801). (Boudewijn Rempt)
- Disable the lock button if the docker is set to float. (Boudewijn Rempt)
- Do not miss the dot when appending the extension. (Patch: Tobias Hintze)
- FIX [#335298](https://bugs.kde.org/show_bug.cgi?id=335298): Fix cut and paste error. (Boudewijn Rempt)
- Implement internet updates for [G'MIC](http://gmic.sourceforge.net/) (Compile G’MIC with zlib dependency). (Lukáš Tvrdý)
- FIX [#331358](https://bugs.kde.org/show_bug.cgi?id=331358): Fixed rotation tablet sensor on Windows and make rotation on Linux be consistent with rotation on Windows. (Dmitry Kazakov)
- FIX [#331694](https://bugs.kde.org/show_bug.cgi?id=331694): Add another exr mimetype "x-application/x-extension-exr", to make the exr system more robust. (Boudewijn Rempt)
- FIX [#316859](https://bugs.kde.org/show_bug.cgi?id=316859): Fix Chalk brush paint wrong colors on saturation ink depletion. (Dmitry Kazakov)
- Index Colors Filter: Add option to reduce the color count. (Manuel Riecke)
- Fix "modifier + key" canvas input shortcuts not working. (Arjen Hiemstra)
- FIX [#325928](https://bugs.kde.org/show_bug.cgi?id=325928): Allow to lock the state of the dockers. (Boudewijn Rempt)
- Reduce size of mirror handles and other minor tweaks to the mirror axis handles. (Arjen Hiemstra)
- Let the user select a 1px brush with a shortcut. (Dmitry Kazakov)
- FIX [#325295](https://bugs.kde.org/show_bug.cgi?id=325295): Make changing the brush size with the shortcuts more consistent. (Dmitry Kazakov)
- FIX [#334982](https://bugs.kde.org/show_bug.cgi?id=334982): Fix a hang-up when opening the filter dialog twice. (Dmitry Kazakov)
- Enable opengl by default. (Boudewijn Rempt)
- FIX [#334371](https://bugs.kde.org/show_bug.cgi?id=334371). (Boudewijn Rempt)
- Add rename composition to the right click menu. (Sven Langkamp)
- FIX [#334826](https://bugs.kde.org/show_bug.cgi?id=334826): Fix loading ABR brushes. (Boudewijn Rempt)
- Add ability to update a composition CCBUG:[#322159](https://bugs.kde.org/show_bug.cgi?id=322159). (Sven Langkamp)
- Activate compositions with double click. (Sven Langkamp)

### Code cleanup and optimizations.

Following previous week’s efforts, Boudewijn Rempt kept improving the code efficiency on many aspects of the code. With the hard work of Dmitry Kazakov, Stuart Dickson, Lukáš Tvrdý and Sven Langkamp the code is kept evolving, from ensuring compilation on systems with QT 4.7 or disabling some portions of QT if the version is too old (to make Krita work in many distros), updating [G'MIC](http://gmic.sourceforge.net/) version to 1.5.9.0, improving OpenGL crash detection, and renaming brushes to "brush tips" to avoid user confusion between presets and brushes, now brush tips.

### Krita Sketch and Gemini

This week in sketch an Gemini. Dan Leinir Turthra Jensen added support for templates and a small foldout in brush tool to allow selecting predefined sizes. Stuart Dickson fixed minor UI inconsistencies re-ordering the display of new documents window, updating mirror tool bar actions and expanding template categories. Dmitry Kazakov fixed color space realted problems. Arjen Hiemstra tweaked the size of mirror mode handles to make them more comfortable to use and made other enhancements to the general UI look and feel. Bug fixes are as follow:

- Fix hsvF -> hsv. This cause crash when loading sketch and gemini. (Dmitry Kazakov)
- FIX [#332864](https://bugs.kde.org/show_bug.cgi?id=332864): Use a lighter colour for the x in the unchecked checkbox. (Arjen Hiemstra)
- FIX [#332860](https://bugs.kde.org/show_bug.cgi?id=332860): Cleanup the Tool panel and tool config pages. (Arjen Hiemstra)

![Krita Gemini/Sketch with templates](/images/posts/2014/w_sketch-template.jpg)

### Animation branch

Sohsumbra’s work preview can be seen in the following video, working animation with layers.

{{< youtube 3VKcvJT8rQ8 >}}

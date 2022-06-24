---
title: "Krita 4.4.0 Release Notes"
date: "2020-08-10"
---

# Krita 4.4.0 Release Notes

If we had to give a theme to this release, it would be textures and patterns. This was half by coincidence, one of our GSoC students this year focused on getting SeExpr integration going, one of the mentors decided to work in the same area, and two volunteer contributors also came up with pattern and texture related features.

## Fill Layers

This release brings a lot of updates and changes to fill layers.

### Multi-threading for fill layers

Fill layers can now make use of multi-threading. This means that if your computer has multiple cores, Krita can subdivide the calculation work for making fill layers between them. This makes fill layers a lot faster.

### Transformations for the pattern fill

[![](/images/pages/krita_4_4_texture_example.png)](/images/posts/2020/krita_4_4_texture_example.png)

The different pattern transforms possible now.

The [patterns of fill layers](https://docs.krita.org/en/reference_manual/layers_and_masks/fill_layer_generators/pattern_fill.html) can now be transformed, allowing you to amongst others, rotate the patterns. This has also been implemented for the shape drawing tools and the bucket fill, and had been long on the to-do list.

### Screentone

[![](/images/pages/fill_layer_screentone_postprocessing.png)](/images/posts/2020/fill_layer_screentone_postprocessing.png)

[A new fill layer option](https://docs.krita.org/en/reference_manual/layers_and_masks/fill_layer_generators/screentone.html) specialized in filling the whole screen with dots, squares, lines, waves or more. This fill layer allows you to quickly generate the simple pattern you need on the fly, which is very useful for those doing comic book illustration or similar highly graphics styles.

### Multigrid

[![](/images/pages/multigrid-color-examples.png)](/images/posts/2020/multigrid-color-examples.png)

[A fill layer that generates](https://docs.krita.org/en/reference_manual/layers_and_masks/fill_layer_generators/multigrid.html), among others, [Penrose tilings](https://en.wikipedia.org/wiki/Penrose_tiling), as well as Quasicrystal structures. The results are rotationally symmetric, but aperiodic, meaning these rhomb patterns don't repeat themselves.

This filter was inspired by the next item on the list...

### SeExpr

[![](/images/pages/1096px-SeExpr_manual_1.jpg)](/images/posts/2020/1096px-SeExpr_manual_1.jpg)

SeExpr Manual

Amyspark's Google Summer of Code project, the integration of Disney Animation's [SeExpr](https://docs.krita.org/en/reference_manual/layers_and_masks/fill_layer_generators/seexpr.html) expression language. SeExpr is in effect a tiny shader language that is used by Walt Disney Animation Studios itself to generate textures and materials on the fly for their animations. Within Krita, this allows you to code your own fill layers. We've also tried to come up with a good set of defaults to work off from and included them.

## Brushes

Following the addition of the lightness mode in 4.3, this release sees another round of features for the brush engines.

[![](/images/pages/flowers_gradients_lightness.png)](/images/posts/2020/flowers_gradients_lightness.png)

Top stroke: using a combination of the new lightness parameter with the mix parameter. Bottom stroke: using the texture strength parameter to mix gradient mapped brush tips and textures.

### Gradient Map mode for Brush-tips

If lightness mode is not subtle enough for you, you can now also use the global [gradient to color a brush tip](https://docs.krita.org/en/reference_manual/brushes/brush_settings/brush_tips.html). Especially useful with small repeating objects like flowers and leaves.

### Lightness and Gradient modes for brush textures

Brushes now have the ability to use [lightness and the gradients for textures](https://docs.krita.org/en/reference_manual/brushes/brush_settings/texture.html) as well.

### Diagonal selection lines in MyPaint color selector (Shift+M)

Diagonal lines allow modifying _lightness and saturation_ of the currently active color at the same time.

[![Diagonal lines in MyPaint Color Selector (Shift+M)](/images/pages/mypaint_selector_diagonal.png)](/images/posts/2020/mypaint_selector_diagonal.png)

Diagonal lines in MyPaint Color Selector (Shift+M)

## Support for dynamic use of currently selected colors in gradients.

While Krita had support for the GIMP Gradient format, we never supported the dynamic changing of [gradients](https://docs.krita.org/en/reference_manual/resource_management/resource_gradients.html) based on the current fore and background colors. Nor did we do so for the layer styles. This has now been added. Several of the bundled presets use the foreground color to easily create sparks, haze and other effects.

[![](/images/pages/fg_changing_gradients_for_sparkles.png)](/images/posts/2020/fg_changing_gradients_for_sparkles.png)

 

Little sparkles added with the 'GPS glare' default, different colors are a different foreground color.

## Animation

While most of the animation work is happening in master and will be in the next big Krita release, some choice features have made it to 4.4:

- [Audio Support](https://docs.krita.org/en/reference_manual/audio_for_animation.html) within an AppImage.
- WebM/VP9 preset for [Animation Rendering](https://docs.krita.org/en/reference_manual/render_animation.html) - Based on a request for a web friendly rendering preset.
- [Compositions Docker](https://docs.krita.org/en/reference_manual/dockers/compositions.html) now allows for the exporting of Animations - Requested by animators, the compositions docker allows for saving and loading layer visibility configurations. This adds the ability to setup animation renders for these configurations.

## Python

### GDQUEST Batch Exporter add-on

An exporter for batch exporting the layers and positions from Krita. Made by the folks over at Game Design Quest:

{{< youtube jJE5iqE8Q7c >}}

### Python plugin Channels to Layers

By Gwendal Blanchard, this plugin allows you to quickly separate the image channels into layers.

### API changes

- Return list of available dockers for application in python
- add signal to notify when theme changed
- Add signal when active view changes in python
- Add showFloatingMessage to View API
- New widget bindings: [scratchpad](https://api.kde.org/appscomplete-api/krita-apidocs/libs/libkis/html/classScratchpad.html). See an example of a [scratchpad docker built using python.](https://invent.kde.org/scottpetrovic/krita-scratchpad-docker)

### New Python scripting website

![](/images/pages/scripting-school-1024x387.png)

To learn about the new scripting APIs, or learn how to script with Krita in general, [a new website was made](https://scripting.krita.org/) to assist. It is broken apart into various sections of what scripting can do.

## Other

- Make Ctrl+C/X/V shortcut work with layers when there is nothing else to copy - Krita can copy pixel data, vector objects and whole layers with blending modes, frames, child layers and other properties. Previously, Krita would only try to copy pixel and vector objects if these were selected and otherwise not copy anything. Now, Krita will copy (or cut) the selected layer if nothing is selected, making it a lot easier to copy and paste layers between files.
- Basic Reapply Filter with Prompt. We already had 'Reapply Filter', but some filters have configuration dialogs that you might wish to change. This function allows for exactly that, and can have a hotkey assigned for quick access.
- Update default layer name to show type - Krita used to give layers names like 'layer 1', 'layer 2', regardless of layer type. Based on artist feedback, we've now added the layer type to make it easier to tell what kind of layer was made.
- Add 'selection as a border' option to the [Fill Tool](https://docs.krita.org/en/reference_manual/tools/fill.html) - In some graphics software, the fill tool will treat separately selected areas as separate areas to fill. We've added an option to the fill tool that allows this in Krita. It is a little slower, and therefore off by default.

## Bugfixes

- Fix undo breakage after converting a pixel selecion into a vector one ([Bug 411394](https://bugs.kde.org/show_bug.cgi?id=411394))
- Add a workaround for boolean operations on shapes ([Bug 411056](https://bugs.kde.org/show_bug.cgi?id=411056))
- Fix Move Tool to work correctly with Instant Preview ([Bug 400484](https://bugs.kde.org/show_bug.cgi?id=400484))
- Add antialias to the gradients in the cases they showed jagged borders (Thanks, Deif Lou)
- Make the color labels combobox nicer in Tool Options
- Fix layer's bounds extending when painting outside the selected area ([Bug 394439](https://bugs.kde.org/show_bug.cgi?id=394439))
- Disable doing bitBlt outside extent when alpha channel is locked ([Bug 394439](https://bugs.kde.org/show_bug.cgi?id=394439))
- Fix moving local selection mask created from global selection ([Bug 411802](https://bugs.kde.org/show_bug.cgi?id=411802))
- Fix the \_other\_ place where the lorem text was used([Bug 421663](https://bugs.kde.org/show_bug.cgi?id=421663))
- Bugfix: Recent documents don't open ([Bug 422412](https://bugs.kde.org/show_bug.cgi?id=422412))
- Fix resource icon aspect ratio on 1 column display
- Fix artifacts when moving a layer with layer styles
- Fix leftover artifacts when moving shapes under layer styles ([Bug 414581](https://bugs.kde.org/show_bug.cgi?id=414581))
- Let Select Opaque deselect the selection when the layer is empty ([Bug 418028](https://bugs.kde.org/show_bug.cgi?id=418028))
- Fix converting multile shapes into a vector selection ([Bug 414262](https://bugs.kde.org/show_bug.cgi?id=414262))
- Don't start move-selection stroke if selection is empty ([Bug 407160](https://bugs.kde.org/show_bug.cgi?id=407160))
- Fix move-selection action after using locked-alpha painting ([Bug 402770](https://bugs.kde.org/show_bug.cgi?id=402770))
- Fix conversion of masks into a paint layer
- Recover active node when the user toggles "Edit Global Selection" ([Bug 409944](https://bugs.kde.org/show_bug.cgi?id=409944))
- Created a shader for drawing brush tool outline. ([Bug 415772](https://bugs.kde.org/show_bug.cgi?id=415772))
- Fixed OpenGL canvas rendering for High-DPI displays.
- Make Angle preferred renderer on Windows
- Remove old workaround for popup palette hiding ([Bug 415106](https://bugs.kde.org/show_bug.cgi?id=415106))
- Add context to the "Original" label ([Bug 422706](https://bugs.kde.org/show_bug.cgi?id=422706))
- Fix the plugins/tool action files ([Bug 422729](https://bugs.kde.org/show_bug.cgi?id=422729))
- Fix loading ASL gradients with only one stop ([Bug 422320](https://bugs.kde.org/show_bug.cgi?id=422320))
- Fix updates of masks when changing visibility ([Bug 422804](https://bugs.kde.org/show_bug.cgi?id=422804))
- Fix Liquify Transform to avoid changing the image when no transform done ([Bug 416471](https://bugs.kde.org/show_bug.cgi?id=416471))
- Fix jumping of shapes when Orthogonal Snap is enabled ([Bug 414336](https://bugs.kde.org/show_bug.cgi?id=414336))
- Fixes the problem of calculating threshold of flood fill tools. ([Bug 416892](https://bugs.kde.org/show_bug.cgi?id=416892))
- Fix applying invert filter on transparency masks ([Bug 422805](https://bugs.kde.org/show_bug.cgi?id=422805))
- Make Smart Patch Tool consider active selection ([Bug 420219](https://bugs.kde.org/show_bug.cgi?id=420219))
- Lens blur: Map between translated and untranslated strings in filter config ([Bug 422999](https://bugs.kde.org/show_bug.cgi?id=422999))
- Fix "Shrink from image border" wrapping ([Bug 402196](https://bugs.kde.org/show_bug.cgi?id=402196))
- Fix border selection to generate non-fuzzy edges ([Bug 395673](https://bugs.kde.org/show_bug.cgi?id=395673))
- Fix Screen Fetch Logic Crash in KoToolBox that was triggered by vertical monitors.
- Parent the resource manager window ([Bug 423097](https://bugs.kde.org/show_bug.cgi?id=423097))
- Fix KoZoomTool on rotated and mirrored canvas ([Bug 386704](https://bugs.kde.org/show_bug.cgi?id=386704))
- Fix canvas FBO object to work ocrrectly in fractional display scaling mode (qt 5.14.0)
- Fix handling of Control modifier in the Zoom Tool ([Bug 411507](https://bugs.kde.org/show_bug.cgi?id=411507))
- Fix the aspect ration of the gradient selector popup
- No need to abort when this assert fails ([Bug 423303](https://bugs.kde.org/show_bug.cgi?id=423303))
- Remove the jpef/jfif mime subtype
- Fix exporting ORA files ([Bug 423088](https://bugs.kde.org/show_bug.cgi?id=423088))
- Add a small executable to print the version ([Bug 423285](https://bugs.kde.org/show_bug.cgi?id=423285))
- Save and load assistant side handles in .kra and .paintingassistant files (Thanks, Nabil Maghfur Usman)
- Add a warning label in file layer dialog ([Bug 413594](https://bugs.kde.org/show_bug.cgi?id=413594)) (Thanks, Matt Coudert)
- Show floating message of activated preset in Ten Brushes
- Disambiguate the filter categories ([Bug 423388](https://bugs.kde.org/show_bug.cgi?id=423388))
- Fill layers: Keep the config around when switching generators ([Bug 422885](https://bugs.kde.org/show_bug.cgi?id=422885))
- Fix contiguous selection tool working on projection ([Bug 423336](https://bugs.kde.org/show_bug.cgi?id=423336), [Bug 423237](https://bugs.kde.org/show_bug.cgi?id=423237))
- Fix ffmpeg argument construct for GIF save ([Bug 420215](https://bugs.kde.org/show_bug.cgi?id=420215), [Bug 423439](https://bugs.kde.org/show_bug.cgi?id=423439))
- Update the waterc brushes so they work with mice, too
- Fix use-after-free in the resource server ([Bug 419140](https://bugs.kde.org/show_bug.cgi?id=419140))
- Fix cloning of a stroke layers style with "center" position ([Bug 423150](https://bugs.kde.org/show_bug.cgi?id=423150))
- Fix crash when using Fill Tool without a selection ([Bug 423470](https://bugs.kde.org/show_bug.cgi?id=423470))
- Add cancellation of assistant creation with escape ([Bug 415172](https://bugs.kde.org/show_bug.cgi?id=415172))
- Fix destination atop rendering ([Bug 423465](https://bugs.kde.org/show_bug.cgi?id=423465))
- Add a workaround for too big brushes generated by Masking Brush option ([Bug 423572](https://bugs.kde.org/show_bug.cgi?id=423572)) (Thanks Defresne for draft patch)
- Fix saving broken .ora file in case of empty layer ([Bug 423741](https://bugs.kde.org/show_bug.cgi?id=423741))
- Don't save x and y of groups in .ora files ([Bug 423088](https://bugs.kde.org/show_bug.cgi?id=423088))
- Don't save reference images in .ora files ([Bug 423741](https://bugs.kde.org/show_bug.cgi?id=423741))
- Allow shift snapping when placing and dragging assistant handles ([Bug 406204](https://bugs.kde.org/show_bug.cgi?id=406204))
- Don't hide global assistant color when no assistant is selected
- Fix broken shortcuts when user uses Space key as a modifier ([Bug 409613](https://bugs.kde.org/show_bug.cgi?id=409613))
- Fix Crash on Frame Priority Caching when Graphics Acceleration is Disabled. ([Bug 424037](https://bugs.kde.org/show_bug.cgi?id=424037))
- Fix the aspect ratio of the palette chooser ([Bug 424227](https://bugs.kde.org/show_bug.cgi?id=424227))
- Fix crash on curve adjustment filter in CMYK document ([Bug 424187](https://bugs.kde.org/show_bug.cgi?id=424187))
- Snap: Fix file chooser icons. Add jpeg 2000, gif, raw, TIFF, HEIF
- Make assistant guidelines follow brush during stroke ([Bug 415208](https://bugs.kde.org/show_bug.cgi?id=415208)) (Thanks, Frans Slothouber)
- Fixup: Canvas No Longer Soft-Locks When Changing Graphics Acceleration Setting ([Bug 423840](https://bugs.kde.org/show_bug.cgi?id=423840))
- Fix deform brush slowly turning the canvas transparent ([Bug 290383](https://bugs.kde.org/show_bug.cgi?id=290383))
- Add missing header QList (Henry Lee)
- Fix painting with colorsmudge brush when a selection is active (394439)
- Fix KRA Saving Failure When Audio File is Missing ([Bug 422890](https://bugs.kde.org/show_bug.cgi?id=422890))
- Fix Rendering Fail on First Render After Switching to video/ogg Container Type. ([Bug 421658](https://bugs.kde.org/show_bug.cgi?id=421658))
- Fix Loading Group Node Opacity Keyframes. ([Bug 424539](https://bugs.kde.org/show_bug.cgi?id=424539))
- Some "Render Animation" dialog settings init to document settings. ([Bug 395230](https://bugs.kde.org/show_bug.cgi?id=395230))
- Fix: Properly Maintain Selection of Keyframes When Inserting / Removing Hold Frames. ([Bug 404519](https://bugs.kde.org/show_bug.cgi?id=404519), [Bug 388779](https://bugs.kde.org/show_bug.cgi?id=388779))
- Fix canvas crashing on closing when having more than one document open. ([Bug 424787](https://bugs.kde.org/show_bug.cgi?id=424787))
- Fix Overview Docker resetting Instant Preview caches ([Bug 366024](https://bugs.kde.org/show_bug.cgi?id=366024))
- Fix layer index generation algorithm ([Bug 420033](https://bugs.kde.org/show_bug.cgi?id=420033))
- Fix update of file layers created via "Convert to" menu ([Bug 411790](https://bugs.kde.org/show_bug.cgi?id=411790))
- Fix canvas freeze on closing the second document in Angle mode
- Correctly flush cache after layer > resize operations. ([Bug 424111](https://bugs.kde.org/show_bug.cgi?id=424111))
- Fix z-order saving for reference images. ([Bug 403974](https://bugs.kde.org/show_bug.cgi?id=403974))
- Fix setting z-index for reference images when loading or adding to a document. ([Bug 424793](https://bugs.kde.org/show_bug.cgi?id=424793))
- Add signal compressor in the reference image tool to prevent freezes. ([Bug 411457](https://bugs.kde.org/show_bug.cgi?id=411457))
- Fix skipping over fake nodes for composition visibility. ([Bug 417911](https://bugs.kde.org/show_bug.cgi?id=417911))
- Elide very long brush names. ([Bug 424601](https://bugs.kde.org/show_bug.cgi?id=424601))
- Enable antialiasing properly for rectangle select. ([Bug 410567](https://bugs.kde.org/show_bug.cgi?id=410567))
- Fix "Fill Entire Selection" action not to multiply opacity twice
- Remove the version number from the caption ([Bug 425158](https://bugs.kde.org/show_bug.cgi?id=425158))
- Fix loading colorize masks with custom profiles ([Bug 416607](https://bugs.kde.org/show_bug.cgi?id=416607))
- Fix first redo() after paint device color space conversion ([Bug 416584](https://bugs.kde.org/show_bug.cgi?id=416584))
- Fix ellipsis sign in some user actions
- Fix halos around strokes in "Inherit Alpha" layers with transparency ([Bug 424797](https://bugs.kde.org/show_bug.cgi?id=424797))
- Fix Local Selection being collapsed right after addition ([Bug 422909](https://bugs.kde.org/show_bug.cgi?id=422909))
- Fix extra frames not being added for hidden animation layers ([Bug 422525](https://bugs.kde.org/show_bug.cgi?id=422525))
- Fix scaling of file layers with transparent background ([Bug 396131](https://bugs.kde.org/show_bug.cgi?id=396131)) (May change old files)
- Fix the color label of the layers when doing merge-down ([Bug 421744](https://bugs.kde.org/show_bug.cgi?id=421744))
- Fix artifacts when using Move Tool in WrapAround mode ([Bug 424233](https://bugs.kde.org/show_bug.cgi?id=424233))
- Fix painting with colorsmudge brush on a alpha-locked layer ([Bug 425152](https://bugs.kde.org/show_bug.cgi?id=425152))
- Fix shotcut conflict in "Protoshop Compatible" profile ([Bug 409754](https://bugs.kde.org/show_bug.cgi?id=409754))
- Fix setting a proper color profile in RAW import plugin ([Bug 425325](https://bugs.kde.org/show_bug.cgi?id=425325))
- Fix flatten/merge down/merge multiple action handle locked groups correctly ([Bug 406697](https://bugs.kde.org/show_bug.cgi?id=406697))
- Remove global/document import question for palettes. ([Bug 424959](https://bugs.kde.org/show_bug.cgi?id=424959))
- Align quickbrush dabs to outline. ([Bug 412309](https://bugs.kde.org/show_bug.cgi?id=412309))
- New shortcut: Resize brush in full pixel increments ([Bug 361814](https://bugs.kde.org/show_bug.cgi?id=361814)) (Thanks, Santiago A M Rodriguez)
- Fix actions not to modify locked layers ([Bug 425412](https://bugs.kde.org/show_bug.cgi?id=425412), [Bug 406697](https://bugs.kde.org/show_bug.cgi?id=406697))
- Fix drop indicator rendering for the layers ([Bug 410970](https://bugs.kde.org/show_bug.cgi?id=410970))
- Fix jumps in composite op combobox when using mouse wheel or keyboard ([Bug 410312](https://bugs.kde.org/show_bug.cgi?id=410312))
- Fix color space when saving EXR with Gray channels ([Bug 425379](https://bugs.kde.org/show_bug.cgi?id=425379))
- Fix temporary wrongly selected layer when merging down huge layers ([Bug 418922](https://bugs.kde.org/show_bug.cgi?id=418922))
- Try once more to fix the window captions ([Bug 425529](https://bugs.kde.org/show_bug.cgi?id=425529))
- Fix update of layers with Destination Atop blendign mode ([Bug 423533](https://bugs.kde.org/show_bug.cgi?id=423533))
- Limit the size of the warning icon in the Blending Mode combobox ([Bug 415673](https://bugs.kde.org/show_bug.cgi?id=415673))
- Fix layers docker not updating blendmode availability on image cs change ([Bug 374386](https://bugs.kde.org/show_bug.cgi?id=374386))
- Fix errorneously set background color in EXR loading code ([Bug 425588](https://bugs.kde.org/show_bug.cgi?id=425588))
- Switch radio buttons to combobox to reduce the size of the predefined brushes. ([Bug 424284](https://bugs.kde.org/show_bug.cgi?id=424284))
- Fix crash on particular LCMS profiles ([Bug 423685](https://bugs.kde.org/show_bug.cgi?id=423685))
- Fix selecting a font in the font combobox by being less agressive in activating slots. ([Bug 425322](https://bugs.kde.org/show_bug.cgi?id=425322))
- Fix convertions of font-weight between qt and svg (Thanks, Pietro Carrara)
- Add reload preset button to brush HUD in popup palette
- Add a warning message when changing profile of a multilayered image ([Bug 356303](https://bugs.kde.org/show_bug.cgi?id=356303))
- Fix a bug in KisConvolutionWorkerFFTW ([Bug 413317](https://bugs.kde.org/show_bug.cgi?id=413317))
- Make LCMS init() crash-proof ([Bug 423685](https://bugs.kde.org/show_bug.cgi?id=423685))
- \`pixelDataAtTime\` Implementation Correction ([Bug 409414](https://bugs.kde.org/show_bug.cgi?id=409414))
- Don't let transform tool use non-affine transforms on vector layers ([Bug 420919](https://bugs.kde.org/show_bug.cgi?id=420919), [Bug 419758](https://bugs.kde.org/show_bug.cgi?id=419758))
- Add \* to the tab caption for modified documents ([Bug 425812](https://bugs.kde.org/show_bug.cgi?id=425812))
- Make Opacity/BlendingMode/InheritAlpha changes compressible
- Fix updates when changing visibility of a layer
- Fix bug with brushes that can't find brushtip ([Bug 425784](https://bugs.kde.org/show_bug.cgi?id=425784))
- Select last reference image whenever adding a reference image. ([Bug 414691](https://bugs.kde.org/show_bug.cgi?id=414691))
- Fix saving/loading colorized masks after cropping them ([Bug 425831](https://bugs.kde.org/show_bug.cgi?id=425831))
- Fix duplication of default tags ([Bug 425845](https://bugs.kde.org/show_bug.cgi?id=425845))
- Fix loading visibility of colorize masks ([Bug 425830](https://bugs.kde.org/show_bug.cgi?id=425830))
- Fix crash when trying to export Transform Mask ([Bug 422391](https://bugs.kde.org/show_bug.cgi?id=422391))
- Fix artifacts when using Masking Brush in Subtract mode in FP color space ([Bug 424210](https://bugs.kde.org/show_bug.cgi?id=424210))
- Fix comma at the end of "Blur," filter category
- Fix artifacts when doing Split Alpha after Gaussian Blur filter ([Bug 420013](https://bugs.kde.org/show_bug.cgi?id=420013))
- Make "Use Selection As Boundary" create new selection when clicking outside selection ([Bug 425524](https://bugs.kde.org/show_bug.cgi?id=425524))
- Fix Divide, Vivid Light and Parallel blending modes handle negative layer colors ([Bug 353204](https://bugs.kde.org/show_bug.cgi?id=353204))
- Show shortcuts in native format where applicable ([Bug 425118](https://bugs.kde.org/show_bug.cgi?id=425118))
- Link to krita-artists.org instead of the forum
- Fix WinTab protocol handling on convertible Yoga C940
- Fix initialization of WinInk if wintab.dll is not found
- Fix switching Krita settings to WinInk when the driver doesn't support WinTab
- Frame Drag and Drop No Longer Accepted on Uneditable Layers ([Bug 425286](https://bugs.kde.org/show_bug.cgi?id=425286))
- Frame Drag and Drop Default Pixel Correction ([Bug 425288](https://bugs.kde.org/show_bug.cgi?id=425288))
- Fix crash when D&D a reference image as an external URL ([Bug 426172](https://bugs.kde.org/show_bug.cgi?id=426172))
- Fix blending mode shortcuts when using non-English locale ([Bug 422919](https://bugs.kde.org/show_bug.cgi?id=422919))
- Reenable Next/Prev Blendign Mode shortcuts([Bug 343655](https://bugs.kde.org/show_bug.cgi?id=343655))
- Fix full-pressure blobs when using floating dockers ([Bug 417040](https://bugs.kde.org/show_bug.cgi?id=417040))
- Add Up/Down buttons to compositions docker ([Bug 400618](https://bugs.kde.org/show_bug.cgi?id=400618))
- Fix small images and pixel art in Overview docker ([Bug 408143](https://bugs.kde.org/show_bug.cgi?id=408143))
- Fix Image->Convert Color Space for layers with a different color space
- Fix bad rendering of text shapes ([Bug 418141](https://bugs.kde.org/show_bug.cgi?id=418141))
- Fix jumping when editing vector path
- Fix crash when redoing creation of a colorize mask ([Bug 424829](https://bugs.kde.org/show_bug.cgi?id=424829))
- Fix erratic assert in ToolTransformArgs ([Bug 424030](https://bugs.kde.org/show_bug.cgi?id=424030))
- Add a translators tab to the aboutbox ([Bug 422156](https://bugs.kde.org/show_bug.cgi?id=422156))
- Fix crash after pasting a shape layer into a different document([Bug 423752](https://bugs.kde.org/show_bug.cgi?id=423752))
- Fix crash in ColorSmudge paintop with animated GIH brushes ([Bug 425875](https://bugs.kde.org/show_bug.cgi?id=425875))
- Fix a crash when recoverng the assistants via snapshots ([Bug 424697](https://bugs.kde.org/show_bug.cgi?id=424697))
- Fix font options after clearing the rich text editor ([Bug 411393](https://bugs.kde.org/show_bug.cgi?id=411393))
- Refactor a logic that enables FBO rendering for the brush outline
- Fix brush outline rendering on openGL 3.0
- Fix partial updates in Reference Images tool ([Bug 396209](https://bugs.kde.org/show_bug.cgi?id=396209))
- Fix rendering (bounding box) of fancy fonts ([Bug 420408](https://bugs.kde.org/show_bug.cgi?id=420408))
- Fix text marked modified when Text Editor is opened ([Bug 411393](https://bugs.kde.org/show_bug.cgi?id=411393))
- Fix several python API functions to be synchronous ([Bug 426349](https://bugs.kde.org/show_bug.cgi?id=426349))
- Fix mapping of Alt key on Windows ([Bug 424319](https://bugs.kde.org/show_bug.cgi?id=424319))
- Add diagonal lines to MyPaint Shade Selector ([Bug 349534](https://bugs.kde.org/show_bug.cgi?id=349534))
- Fix crash when loading a file with reference images ([Bug 426839](https://bugs.kde.org/show_bug.cgi?id=426839))
- Fix lightness strength option for smudge engine ([Bug 426874](https://bugs.kde.org/show_bug.cgi?id=426874))
- Fix Cutoff Pattern option [Bug 426874](https://bugs.kde.org/show_bug.cgi?id=426874)
- Android: Vector/references don't get rendered ([Bug 422312](https://bugs.kde.org/show_bug.cgi?id=422312))
- Fix updates of color picker's preview ([Bug 426867](https://bugs.kde.org/show_bug.cgi?id=426867))
- Also copy the other two .lnk files for Krita animation and Krita minimal, these are shortcuts that will open up Krita in a specific workspace.
- Fix crash when undoing Rectangle Selection and doing redo after
- Fix a crash when moving local selection mask ([Bug 426816](https://bugs.kde.org/show_bug.cgi?id=426816))
- Fix shortcut for Polygonal Selection Tool ([Bug 426916](https://bugs.kde.org/show_bug.cgi?id=426916))
- Fix update of color preview in MyPaint Color Selector on mouse click
- SeExpr: assert isDirty on the correct preset instance ([Bug 426911](https://bugs.kde.org/show_bug.cgi?id=426911))
- Fix snapping decorations in Create Path Tool ([Bug 426514](https://bugs.kde.org/show_bug.cgi?id=426514))
- Android: Use Storage Access Framework for all file operations ([Bug 424541](https://bugs.kde.org/show_bug.cgi?id=424541), [Bug 423670](https://bugs.kde.org/show_bug.cgi?id=423670))
- Android: show recent files on Welcome widget
- Android: Fix problem with loading/saving file layer
- Android: Fix saving for files with no extension
- Android: Fix saving with selections
- Android: Fix saving usage logging ([Bug 427043](https://bugs.kde.org/show_bug.cgi?id=427043))
- Do not install Krita 3 bundle on android so the apk is small enough.
- Fix missing translated menu entries by letting Krita recognise the context properly ([Bug 426992](https://bugs.kde.org/show_bug.cgi?id=426992))
- Fix pop-up palette not showing brushes on Android ([Bug 425344](https://bugs.kde.org/show_bug.cgi?id=425344))
- Fix incorrect conversion in artistic color selector for HSL mode.
- Android: fix move tool not moving the layer ([Bug 423196](https://bugs.kde.org/show_bug.cgi?id=423196))
- Android: fix opening autosave files.
- Fix a crash caused by multithreading ([Bug 427199](https://bugs.kde.org/show_bug.cgi?id=427199))
- Fix textured mode for patterns with transparency ([Bug 427153](https://bugs.kde.org/show_bug.cgi?id=427153))
- Fix pasting as reference image on Android ([Bug 427402](https://bugs.kde.org/show_bug.cgi?id=427402))
- Fix second color preview in MyPaint shade selector.
- Android: activate kinetic scrolling by default ([Bug 423279](https://bugs.kde.org/show_bug.cgi?id=423279), [Bug 421997](https://bugs.kde.org/show_bug.cgi?id=421997))
- Fix canvas updates in wraparound mode ([Bug 427427](https://bugs.kde.org/show_bug.cgi?id=427427))
- Fix link to Krita artists.
- Fix memory leak.
- Fix crash caused by pasting as reference image when there was no clipboard data ([Bug 427466](https://bugs.kde.org/show_bug.cgi?id=427466))
- Fix finding quazip ([Bug 427511](https://bugs.kde.org/show_bug.cgi?id=427511))
- Fix a crash when loading a file with a pattern fill layer ([BUG:427866](https://bugs.kde.org/show_bug.cgi?id=427866))
- Fix loading masks with vector selections ([BUG:428332](https://bugs.kde.org/show_bug.cgi?id=428332))
- Fix a crash in the text tool when opening the editor by double-clicking the text ([BUG:427858](https://bugs.kde.org/show_bug.cgi?id=427858))
- Fix a crash when using the move tool on a pixel selection ([BUG:428260](https://bugs.kde.org/show_bug.cgi?id=428260))
- Android: Use SDK version 29, which means Krita doesn't need permissions to run anymore and can access external files more easily. Krita is also updated to use NDK 20 or better
- Android: Fix the color picker ([BUG:423254](https://bugs.kde.org/show_bug.cgi?id=423254))
- Android: Fix problems with events reaching the canvas if a popup message was shown
- Android: Use the device's locale, so the translations can be used ([BUG:427692](https://bugs.kde.org/show_bug.cgi?id=427692))
- Android: Fix copy and paste on Android ([BUG:423199](https://bugs.kde.org/show_bug.cgi?id=423199))

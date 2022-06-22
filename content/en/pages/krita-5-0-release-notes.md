---
title: "Krita 5.0 Release Notes"
date: "2021-02-08"
---

.row-spacer { margin-top: 2rem; } .post.page img { margin-top: 0; } h2 { margin-top: 3rem; } .videoWrapper { position: relative; height: 0; padding-bottom: 50%; padding-top: 25px; height: 0; margin-bottom: 1rem; } .videoWrapper iframe { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }

# Krita 5.0 Release Notes

**Note on File Compatibility with Krita 4.x and Krita 3.x files:**

- Krita 5.0 is a major release of Krita. Krita 5.0 cannot load vector layers created before Krita 3.0 and has a completely reworked resource system.
- Krita 5.0 has an updated brush preset file format (.kpp). Krita 4 and earlier cannot use brush presets created in Krita 5.
- Krita 5.0 fixed [an issue with text size in documents](#text_size_dpi_issue_fix). However, opening files created with earlier versions of Krita may require [changing a setting](https://docs.krita.org/en/reference_manual/preferences/general_settings.html#miscellaneous) to get the originally expected text size.

 

It has certainly been a long time coming and a lot of hard work, but Krita 5 is here at last! I can say with a measure of pride (and a whole helping of relief for the development team) that 5.0 is up there among the largest and most significant updates that Krita has ever seen, affecting and improving almost every aspect of the program in a variety of ways, big and small. And of course, there's a ton of cool new features that we can't wait for our community of artists to start working with, but before we dig into the details...

**Hey, wait! Don't skip this part... Krita really needs your support!**

One of the main things that makes Krita stand out from its rivals is its _non-profit, open source and community-driven development model_. Krita is made by a global team of programmers and artists, some working professionally and others passionately contributing their talents when they can, with the shared mission of creating a powerful and expressive tool for artists everywhere. Moreover, we all believe that artists should own and control their tools, and that digital art should be just as accessible as putting a pencil to paper.

What a concept, eh? But here's the rub: our grassroots development model means, well... _grassroots funding_.

![](/images/pages/2021-11-16_kiki-piggy-bank_krita5.png)The Krita community is the lifeblood of the project, and without ongoing support from members like you progress would grind to a screeching halt. Thanks to our many contributors over the years Krita has come a long way from its humble beginnings and we don't take that for granted, but in order for us to realize our goal of funding 10 full-time developers to bring Krita to the next level, we seriously need your help. **So, if you can afford to chip in, please consider stepping up to become a member of the Krita Development Fund, join the discussion and get involved.** There's no limit to the Krita we can build together, but we just can't do it without you--it's as simple as that!

[**Support our mission by joining the Krita Development Fund today!**](https://fund.krita.org/)

 

\[video width="1920" height="1080" mp4="/images/pages/Video-for-store\_final-30fps.mp4"\]\[/video\]

Music provided to us by [Irene Fariña](https://www.instagram.com/irerakmusic/).

 

## Faster & More Flexible Resource System

We have fully rewritten [Krita's handling of resources](https://docs.krita.org/en/reference_manual/resource_management.html) like brush presets, gradients, palettes and more. Before we had a fragile system of models, where we should have been using a proper database, and thus, we are now using an SQLite database as the core of our resource handling. This fixes many bugs with tagging and loading resources as well as a handful of UI problems. It also makes our resource system faster and leaner. Because we are now not loading all resources at once, Krita will now start up quicker, and take up less working memory (from our tests, Krita 5.0 took up 200 mb less RAM!).

![](/images/pages/bundle-manager.png)

#### New bundle manager and configurable resource locations.

Krita's resource folder used to be hardcoded. Not any more! You can now configure which folder is the resource folder and where the cache is located. Those of us who'd like to have their resource folder on a USB stick will now be able to do so.

As well, we now support more resource libraries. We already had our own resource bundle format, but now we also support photoshop layer style libraries and brush libraries. Documents can now also be seen as a place to store resources, and though we only use it for palettes right now, we hope to extend this in the future.

[![Screenshot of the new resource manager.](/images/pages/Manageresources.png)](https://krita.org/wp-content/uploads/2021/07/Manageresources.png)

#### New Resource Manager

This new manager allows you to mass-tag brushes as well as delete and undelete resources at will (Krita will deactivate these). It comes with nice little UI features, like a tagging widget that shows all the current tags on a resource in one quick glance.

#### Layer styles are now resources

This allows tagging and searching amongst layer styles, as well as sharing them, or loading several layer styles at once from a downloaded ASL file.

## Smoother Gradients & Improved Gradient Tools

#### Dithered gradients ([MR 668](https://invent.kde.org/graphics/krita/-/merge_requests/668))

Gradients are an excellent way to quickly setup the main color swatches of your image, for example, a quick linear gradient for the horizon, or several radial gradients for light sources. However, if you used subtle gradients, you would sometimes see banding, caused by there being too few colors available in 8 bit images for a smooth gradient. We have [implemented dithering for gradients](https://docs.krita.org/en/reference_manual/tools/gradient_draw.html) in 8 bit images, which involves using a blue noise pattern to create a little bit of offset in the boundary between colors. This way, even 8 bit images which don't always have enough colors to trick the human eye that something is smooth, can have the illusion of smoothness in these gradients.

There was a [Libre Graphics Meeting talk](https://conf.tube/videos/watch/b7b9f48e-606b-42a6-9dae-8def47551970) discussing the technical details.

#### Wide gamut and unbounded gradients ([MR 668](https://invent.kde.org/graphics/krita/-/merge_requests/668) , [MR 675](https://invent.kde.org/graphics/krita/-/merge_requests/675)).

But not only the 8 bit images got love. For images in 16 and 32 bit, the gradients Krita generates will now be able to use the full scale available. Furthermore, we've made it possible to store wide gamut and unbounded colors using [SVG 1.1 icc-color definitions](https://developer.mozilla.org/en-US/docs/Web/SVG/Attribute/stop-color), meaning that you can now have radial gradients that contain rec2020 green, or whites that would only be possible in HDR images, bringing the conveniences of the gradient tool to people who work in these higher bit depths. We hope to support CSS 4 color definitions for the stop gradients when [it's draft](https://www.w3.org/TR/css-color-4/) has been completed.

![Comparison of dithered and non-dithered gradients](/images/pages/krita_gradient_dither.png) Comparison of gradients with and without dither, with an extra set of examples with increased contrast to display the difference.

#### Gradient Editors got an overhaul ([MR 857](https://invent.kde.org/graphics/krita/-/merge_requests/857)).

They are now more cohesive, compact and convenient, with small options left and right to make [creating gradients easier than before](https://docs.krita.org/en/reference_manual/resource_management/resource_gradients.html).

- Easier option on UI to delete stops
- New tear drop display of stops
- New color sorting options
- Cycle through stops with left and right arrows

![](/images/pages/new-gradient-editor-web.png)

#### Faster color management with fast float plugin ([MR 726](https://invent.kde.org/graphics/krita/-/merge_requests/726))

With the [fast float plugin](https://www.littlecms.com/plugin/), the speed of color management improves drastically, especially with 32bit float. This is enabled by default. Color management via LittleCMS enables us to display colors accurately, and is also necessary for professional features like soft proofing and color model support, and is always applied to Krita's view of the image.

![](/images/pages/little-cms-logo.png)

Work by artists using Krita:

[![A longtail bird sitting on a tree branch.](/images/pages/birdweek-sketch1longtailedtit.png)](/images/pages/birdweek-sketch1longtailedtit.png) by [Christine Garner](https://thimblefolio.com) (CC-BY-NC-ND 4.0)

\[caption id="attachment\_12837" align="aligncenter" width="800"\][![A sphinx cat, the lighting making for an intimate scene](/images/pages/m_coudert_202108010.png)](/images/pages/m_coudert_202108010.png) [\*Matthieu COUDERT (MaKo)\* Designer graphique](https://www.makomatt.com/) (CC-BY)

[![A teenage girl in a sailor school girl uniform sitting on a concrete wall, enjoying the sunset. She's joined by a tiny white creature wearing a sailor hat.](/images/pages/negeon_renj_20210401test.png)](/images/pages/negeon_renj_20210401test.png) By Negeon Renj (CC-BY-SA)

## Faster Smudge Brushes & New MyPaint Brush Engine

{{< youtube D0Lv5gWvu94 >}}

#### Rewritten Color Smudge engine ([MR 765](https://invent.kde.org/graphics/krita/-/merge_requests/756))

With the pixel brush now capable of lightness and gradient mapped brush tips, the color smudge engine was to follow. This required a [full rewrite of how the engine works](https://docs.krita.org/en/reference_manual/brushes/brush_engines/color_smudge_engine.html), and often requested features like separation of color rate and color smudge have been added into the mix as well, plus optimization improvements!

#### MyPaint Brush engine ([MR 464](https://invent.kde.org/graphics/krita/-/merge_requests/464), [MR 582](https://invent.kde.org/graphics/krita/-/merge_requests/582))

[MyPaint's brush engine](https://github.com/mypaint/libmypaint) is known for its interesting experiments in how to think of brushes. Krita had some support for it in the distant past, but we had to remove that plugin. Now, Ashwin has created a new [integration of this engine](https://docs.krita.org/en/reference_manual/brushes/brush_engines/mypaint_engine.html), allowing for MyPaint 1.2 brushes to be loaded into Krita and used for your artworks.

![](/images/pages/new-texture-modes.png)

#### New modes for textured brushes ([MR 806](https://invent.kde.org/graphics/krita/-/merge_requests/806)).

Deif Lou has added a variety of new modes for [the texture option](https://docs.krita.org/en/reference_manual/brushes/brush_settings/texture.html). Hard Mix, Color Dodge, Color Burn, Overlay, Height, Linear Height and more will now be available for all engines supporting them, and the Hard Mix Softer mode is also available for the [Masked Brush](https://docs.krita.org/en/reference_manual/brushes/brush_settings/masked_brush.html) blending. These are accessed through the brush editor with pixel engine brushes. Go to Texture group > Pattern > Options tab. The new modes have been added to the Texturing Mode drop-down.

## Animation Overhaul

[Our Timeline Docker](https://docs.krita.org/en/reference_manual/dockers/animation_timeline.html) has a new look and a variety of improvements. We've removed the old Animation Docker and moved its core functionality directly onto the Timeline. Also, animations can be paused at any time, pinning layers has been made easier, playback range automatically adapts as key frames are added, and a number of other changes have been made to improve visual clarity and the overall feel of navigation, transport and editing. ([MR 311](https://invent.kde.org/graphics/krita/-/merge_requests/311) [MR 317](https://invent.kde.org/graphics/krita/-/merge_requests/317))

![](/images/pages/animation-50-ui.png)

#### Redesigned Animation Curves Docker ([MR 601](https://invent.kde.org/graphics/krita/-/merge_requests/601))

Like the Timeline Docker, [Krita's Curves Docker](https://docs.krita.org/en/reference_manual/dockers/animation_curves.html) has also been updated with an emphasis on improving the overall look and feel of navigation and editing. Value key frames are now easier to edit thanks to the improved mouse controls with axis snapping, and a box for reading and writing the specific value of the selected key frame. The visibility of individual channels can be hidden or soloed. And, new navigation options like zoomable scrollbars as well as "fit to curve" and "fit to channel" buttons make it much easier to move around the new, dynamic graph view.

![](/images/pages/animation-curves-50.png)

#### Clone Frames ([MR 469](https://invent.kde.org/graphics/krita/-/merge_requests/469))

Krita 5 now supports Clone Frames, a much requested feature that allows animators to reuse the exact same key frame at multiple times throughout their animation. Clone frames are great for building looping animations and finding clever other ways to save yourself time while animating. Just remember that editing one clone edits them all!

\[video width="1920" height="1028" webm="https://krita.org/wp-content/uploads/2021/05/krita\_anim-clones-direct.webm"\]\[/video\]

#### Transform Mask Animation ([MR 493](https://invent.kde.org/graphics/krita/-/merge_requests/493))

What good is a shiny Curves Docker without some new things to animate? Along with layer opacity, Krita 5 also brings the ability to animate the position, rotation, scale and shear of any layer through animated Transform Masks. Sometimes referred to as "tweening" in other software, this feature should help with animations that are difficult or inconvenient to do through drawing alone. With animated transform masks, moving a walking figure as shown in the video will be a piece of cake.

\[video width="1920" height="1028" webm="https://krita.org/wp-content/uploads/2021/05/krita\_anim-tform-direct.webm"\]\[/video\]

#### Import Videos as Animations ([MR 778](https://invent.kde.org/graphics/krita/-/merge_requests/778))

Community contributor **"KnowZero"** has iterated on **Scott Petrovic**'s feature which allows for [importing videos and animated images](https://docs.krita.org/en/reference_manual/import_animation.html) as Krita animations. This improved importer can be used with an existing document or to create a new document, works with a wider range of formats, and also decreases disk overhead. It's great for studying and rotoscoping! Thank you both!

![The video import dialog.](/images/pages/import_video.png)

#### Even More Animation Improvements!

#### New Options for Exporting GIF, APNG and WEBP ([MR 734](https://invent.kde.org/graphics/krita/-/merge_requests/734))

Another useful patch from "**KnowZero**" allows animated images to set configuration options while exporting, just like their video counterparts. This should make it much easier to work with animated image formats.

#### Improved Render Settings Behavior

Animation export paths are now stored directly in each Krita document and settings like render FPS are automatically set to match your timeline setting.

#### Crop Active Frame

It's now possible to crop only the contents of the current frame by setting "Applies to: Frame" in the Tool Options menu while the Crop Tool is active.

#### Apply a filter on all selected frames ([MR 665](https://invent.kde.org/graphics/krita/-/merge_requests/665))

There's a toggle for applying a filter on all selected frames, or just a single one.

#### Render Animation from composition docker ([MR 407](https://invent.kde.org/graphics/krita/-/merge_requests/407))

Another feature request. The composition docker allows for storing the state of visibility in the layer docker, while this new feature is a bit of convenience for animators to render the current animation with a given stored composition. Useful for situations where you only need a few layers rendered.

#### AutoKey Blank Mode

We've added a new "AutoKey Blank" mode. This mode should help speed up your animation workflow by creating a new blank key frame each time you draw on an empty frame. You can find this setting by clicking on the arrow next to the AutoKey button within the Timeline's settings menu.

#### Select Matching Key Frame

For those of you who organize your key frames with color labels, Krita now has an action for selecting the previous or next key frame of the same color. This can be found by searching for "matching" in Krita's "Keyboard Shortcuts" configuration menu.

#### Improved Animation Backend and Caching

We've also made a lot of changes to how our animation system works under the hood that will hopefully add up to further improved stability and cache reliability for Krita animators.

#### New Animation Workspace

We've put together an updated animation workspace that takes advantage of our more space-efficient dockers.

Work by artists using Krita:

[![A turn table of a catgirl](/images/pages/loentar_kuro-tt_003.gif)](/images/pages/loentar_kuro-tt_003.gif) by Dmitrii Utkin

[![Profile portrait of a horse, painted in a very textured manner.](/images/pages/ramon_horse_power-1024x790.jpg)](/images/pages/ramon_horse_power.jpg) by Ramón Miranda

[![An anthromorphic cat named Olivia with a yellow-orange dress.](/images/pages/simon_rollins_olivia_s_fall_dress-702x1024.png)](/images/pages/simon_rollins_olivia_s_fall_dress.png) By Simon Rollins (CC-BY-NC-SA)

## New Storyboarding Tools and Workflow

Thanks to the help of one of our 2020 Google Summer of Code students, **Saurabh "Confifu" Kumar**, Krita now has a Storyboard Docker that can be used to plan the shots and storytelling of complex shorts or films. ([MR 392](https://invent.kde.org/graphics/krita/-/merge_requests/392)). This docker does not just allow you to collect and annotate scenes, but also a wide variety of export options, such as PDF and SVG. There are multiple views you can switch between (screenshot showing the row view).

[![](/images/pages/Storyboard_row_mode.png)](https://krita.org/wp-content/uploads/2020/09/Storyboard_row_mode.png)

#### Flexible storyboard export templating

Krita's new storyboard docker has a lot of options for exporting your boards, including the ability to use SVG file data to specify a completely custom layout. This advanced feature means that, with a little work, storyboards that you make in Krita can always be made to fit your project's needs or match existing storyboard paper.

[![Krita default svg storyboard export template](/images/pages/storyboard_export_template-214x300.png)](https://krita.org/wp-content/uploads/2021/11/storyboard_export_template.png)

## User Interface Improvements

[![Krita in the old oxygen style](/images/pages/krita-style-change-1024x533.png)](https://krita.org/wp-content/uploads/2021/08/krita-style-change.png)

Our icons were last refreshed for 2.9, and over the years a few hiccups had emerged. **Timothée Giet** was hired to give the icon set a good scrubbing, and the UI overall had all sorts of little tweaks done by **Raghavendra Kamath**, **Pedro Reis**, **Scott Petrovic**, **Tom Tom**, **Simon Repp**, **Paul Franz**, **Andrei Rudenko**, **Daniel (Sxnic)**, and **Alvin Wong**.

#### Detach the brush editor from the toolbar

You now have the option to make the brush editor detach to its own window, or stay as a pop-up from the toolbar. A detached brush editor can be great for brush creators that make frequent tweaks to their brushes and want to see the result. No more having to constantly show the brush editor every time you want to make a change.

![](/images/pages/detach-brush-editor.png)

#### Add option to auto hide controls in overview docker ([MR 739](https://invent.kde.org/graphics/krita/-/merge_requests/739))

This makes it so the view controls hide in the overview docker when not in use, giving the maximum room to the overview itself.

#### Support for user-installed themes on Linux and widget style selection ([MR 557](https://invent.kde.org/graphics/krita/-/merge_requests/557), [MR 354](https://invent.kde.org/graphics/krita/-/merge_requests/354))

Krita's looks can be modified with both theme and widget style. You could already choose the theme, but now it's also possible to change the widget style on the fly, allowing users to switch between all widget styles available for your platform.

#### Docker locks have returned ([MR 623](https://invent.kde.org/graphics/krita/-/merge_requests/623))

Locking dockers is helpful for those with sensitive tablet stylii, as sometimes a subtle stroke can undock a docker.

#### Color Selector Uses Theme Color for Background ([MR 365](https://invent.kde.org/graphics/krita/-/merge_requests/365))

This was mid-grey to give an unbiased understanding of the color, but it can now be turned off for extra consistency.

## New File Formats with AVIF & WebP

[![Image of a sunset](/images/pages/avif_import_cosmos-1024x425.png)](https://krita.org/wp-content/uploads/2021/08/avif_import_cosmos.png)

This avif is a frame from Cosmos Laundromat, encoded in rec 2100 pq. Krita opens files like these as 32bit float linear images, making them ready to be used with the LUT docker.

#### Heif plugin update and Avif support ([MR 530](https://invent.kde.org/graphics/krita/-/merge_requests/530)).

Heif and Avif are the new formats being used by mobile phone cameras, with Avif in particular being slated as a new image format for websites. Krita now supports loading and saving for both RGB and monochrome, 8 bit, 10 bit and 12 bit to these [two file formats](https://docs.krita.org/en/general_concepts/file_formats/file_heif.html). Color space encoding is fully supported, including the HDR options such as Rec 2100 PQ and Rec 2100 HLG. The official binaries will also ship rav1e and dav1d for speedy encoding and decoding of Avif.

#### Improved Tiff support ([MR 907](https://invent.kde.org/graphics/krita/-/merge_requests/907), [MR 929](https://invent.kde.org/graphics/krita/-/merge_requests/929), [MR 962](https://invent.kde.org/graphics/krita/-/merge_requests/962))

Many improvements have come to the venerable tiff plugin: It now supports signed integer formats (as opposed to only unsigned), floating point formats and premultiplied alpha. The UI has been improved with the fax option removed. There is also a patch in the works for 5.1 to get support for Photoshop style tiffs, which should greatly improve interoperability.

#### WebP plugin improvements ([MR 891](https://invent.kde.org/graphics/krita/-/merge_requests/891))

We've now got a plugin based on the official libwebp codec. Where before the webp options were limited to compression, this new plugin contains all possible configuration options available to libwebp. Including the presets!

#### krz archival kra file format

A feature request granted, Krita can now save to KRZ, which is a [KRA file](https://docs.krita.org/en/general_concepts/file_formats/file_kra.html) with the preview removed and compression added. This is useful for archiving.

#### Resize image when exporting ([MR 710](https://invent.kde.org/graphics/krita/-/merge_requests/710))

**Sachin Jindal** added the option to crop and resize an image before export. When exporting images, you'll often want to crop and resize them before export. Some artists had however made the mistake of accidentally saving over their working file with their export file. With the new advanced export, you can avoid this problem. This can be accessed from the **File > Export Advanced** main menu option.

Work by artists using Krita:

[![A study of wasps and other insects.](/images/pages/m_coudert_202107015.png)](/images/pages/m_coudert_202107015.png) [\*Matthieu COUDERT (MaKo)\* Designer graphique](https://www.makomatt.com/) (CC-BY)

[![A mermaid like creature gathering pearls with their tentacles](/images/pages/marina_moroz_The_Gatherer.png)](/images/pages/marina_moroz_The_Gatherer.png) By Marina Moroz (CC BY SA)

[![Page two and three depicting a younth reading a magic tome in a forest, but getting distracted by a deer.](/images/pages/alex_sabo_Dragon_Caller_Page_02-03.png)](/images/pages/alex_sabo_Dragon_Caller_Page_02-03.png) _Dragon Caller_ Page 2 and 3, Concept and Story by Daniel Rizea Art by Alexandru Sabo

## New Tools & Improvements

{{< youtube a0uxM_bQOnU >}}

#### Record your next painting session ([MR 522](https://invent.kde.org/graphics/krita/-/merge_requests/522), [MR 180](https://invent.kde.org/graphics/krita/-/merge_requests/180)).

Thanks to community contributor **Dmitrii Utkin**, Krita artists can now record a time-lapse video of their creative sessions with the [new Recorder Docker](https://docs.krita.org/en/reference_manual/dockers/recorder_docker.html)! (Also, a quick shout out to another community contributor, **Shi Yan**, for their good work on this feature. Thank you both for your contributions.)

\[video width="1920" height="1080" mp4="https://krita.org/wp-content/uploads/2021/09/local-assistants-50.mp4"\]\[/video\]

The two point perspective assistant is a quick and convenient way to set up what before required two vanishing points and a parallel assistant. Combined with the area limiter, this tool should prove very useful for comics and concept art.

#### 2-Point Perspective Assistant ([MR 390](https://invent.kde.org/graphics/krita/-/merge_requests/390))

Another community contributor, **Nabil Maghfur Usman**, has added a brand new 2 Point Perspective assistant. This assistant keeps vanishing points reasonably spaced and on the horizon line, draws a grid to help visualize perspective distortion, and is great for adding solidity and depth to your drawings.

#### Limit Area feature for Assistants ([MR 850](https://invent.kde.org/graphics/krita/-/merge_requests/850)).

The two-point and vanishing point assistants are designed so their previews and areas you can snap to draw over the whole image. With limit area, two extra handles are added so you can limit the area in which the assistant is effective, which is very useful for comic pages.

![video of candle stick being transformed](/images/pages/instack_transform.gif)

#### In-stack transform preview

Our transform tool preview is now composited into the layer stack. Before, Krita's transform preview was always hovering above all the layers in the canvas, meaning that you could not see if something aligned correctly, or what the effect would be with blending modes and filters applied.

With in-stack transform, the blending modes and overlapping layers are composited on top of the transform preview. This was a feature funded by the Blender Institute.

![Video showing several ellipse being drawn and rotated.](/images/pages/rotate_ellipse.gif)

#### Rotation ability in the Rectangle and Ellipse Tools ([MR 768](https://invent.kde.org/graphics/krita/-/merge_requests/768))

Where before rotated rectangles and ellipses required an additional transform after the fact, you can now directly draw them with their tools, using Ctrl+Alt during drawing.

Ellipses and rectangles can now be rotated as you draw them.

#### Pop-up palette Improvements ([MR 838](https://invent.kde.org/graphics/krita/-/merge_requests/838), [MR 922](https://invent.kde.org/graphics/krita/-/merge_requests/922))

As per tradition, another update to the pop-up palette, courtesy of **Mathias Wein** and **Alan North**. Maximum brush presets are increased from 30 to 45, pop-up size can be configured, as well as the visibility of the color history and rotation rings and other navigation options. Furthermore, it was already possible to switch between the simple triangle and wide gamut selector since 3.0, but only as a hidden option. Now this toggle and other features have gotten their own section in the user settings.

#### Extra options for temporary tool invocations ([MR 693](https://invent.kde.org/graphics/krita/-/merge_requests/693))

Previous versions of Krita allowed briefly switching to the line tool by holding 'V' and would switch back when released. Thanks to Tom Tom, it is now possible to configure similar actions in the Canvas Input Settings for Ellipse, Rectangle, Move, Fill, Gradient, Measure and several of the selection tools.

#### Crop Canvas option in the crop tool ([MR 800](https://invent.kde.org/graphics/krita/-/merge_requests/800))

Much like the frame crop, you can now also crop the canvas alone with the crop tool, which will leave the layers and the frames alone.

#### Improvements to the similar color selector tool ([MR 587](https://invent.kde.org/graphics/krita/-/merge_requests/587))

The [similar color selector](https://docs.krita.org/en/reference_manual/tools/similar_select.html) can now, like the contiguous selector, select only from layers with color labels. Furthermore, it's been sped up through multi-threading.

#### Color Selector/Picker has been renamed to Color Sampler ([MR 647](https://invent.kde.org/graphics/krita/-/merge_requests/647)).

This was done to distinguish it from the color selection dockers.

## Layers Improvements

#### Drag and drop colors onto the canvas and layer tree ([MR 703](https://invent.kde.org/graphics/krita/-/merge_requests/703))

Colors can now be dragged and dropped from the Palette Docker to the canvas or Layers Docker. While dropping a color onto the canvas causes the selected area to be filled that that color, dropping a color onto the Layers Docker will create a new [Fill Layer](https://docs.krita.org/en/reference_manual/layers_and_masks/fill_layers.html) containing that color.

![](/images/pages/drop-palette-on-canvas.gif)

#### Filter Layers by Name ([MR 292](https://invent.kde.org/graphics/krita/-/merge_requests/292))

Our new [layer filter widget](https://docs.krita.org/en/reference_manual/dockers/layers.html) allows you to filter layers by name, on top of color label.

![Layer search in Krita](/images/pages/krita_layer_search.png)

#### Isolate Active Group ([MR 310](https://invent.kde.org/graphics/krita/-/merge_requests/310))

We've also added a new "Isolate Active Group" isolation mode. Found in the context menu when right-clicking on a layer, this mode temporarily makes the current group that you're working on the only thing that's visible.

#### Paste Into Layer ([MR 732](https://invent.kde.org/graphics/krita/-/merge_requests/732))

Community contributor **Paolo Amadini** has added the ability to paste directly into the active layer, as well as the active frame of an animated layer.

#### Non-destructive layer soloing ([MR 335](https://invent.kde.org/graphics/krita/-/merge_requests/335))

A perhaps little-known feature, "soloing" a layer by shift-clicking on its eye icon can now be exited without permanently changing layer visibility.

## Python Plugins Added/Improvements

{{< youtube jJE5iqE8Q7c >}}

#### GDQuest Batch Exporter Add-On ([MR 116](https://invent.kde.org/graphics/krita/-/merge_requests/116))

Contributed by the **GDQuest Team**, this plugin is designed for the game asset pipeline, allow you to plan and batch export files with the click of a button.

{{< youtube QX9jwhfpB_8 >}}

#### Photobash python plugin ([MR 402](https://invent.kde.org/graphics/krita/-/merge_requests/402))

A plugin by **Pedro Reis** that helps you manage your photo bashing resources and import them quickly into Krita.

#### Support for SIP 5 bindings ([MR 869](https://invent.kde.org/graphics/krita/-/merge_requests/869))

Part of keeping Krita and it's dependencies modern, we now have support for SIP 5 for our Python bindings.

#### Import Python Plugin from Web ([MR 612](https://invent.kde.org/graphics/krita/-/merge_requests/612))

A feature contributed by **Rebecca Breu**, this lets you paste a URL from which to download and import the plugin.

Work by artists using Krita:

[![Landscape of a road running parallel to a river, with a line of trees separating them. The setting sun shines through the tree leaves.](/images/pages/Landscape-raghu.png)](/images/pages/Landscape-raghu.png) Study by Raghukamath (CC-BY-SA-4.0)

[![City-scape showing the front of an apartment, surrounded by plants](/images/pages/wojtryb_cozy_tenement-690x1024.png)](/images/pages/wojtryb_cozy_tenement.png) by [wojtryb](https://www.artstation.com/wojtryb) (CC-BY)

[![Depicted are a raccoon dog girl, as well as a set of comic pages where she is the protagonist.](/images/pages/Victor-Ide-Scopacasa-Tanuki-Manga.png)](/images/pages/Victor-Ide-Scopacasa-Tanuki-Manga.png) by Victor Ide Scopacasa

## ...And More!

![](/images/pages/action-menu.gif)

#### Search all Actions pop-up

Pressing CTRL + Enter while the Krita window is in focus will now give a pop-up search bar where you can search for a given action. This will help new users more easily find features, and old user to quickly get to a given feature. Command search bars are becoming more common in intricate programs like Krita, amongst which [Kate](https://kate-editor.org/post/2021/2021-01-24-kate-january-2021/), whose implementation we were able to reuse.

With Search Actions (on CTRL+Enter), you will be able to search and access any action in Krita.

#### Text size issues have been resolved ([MR716](https://invent.kde.org/graphics/krita/-/merge_requests/716))

In Krita 4.x the size of the text rendered in the document could depend on the resolution of the screen Krita runs on. In Krita 5 this bug has been fixed and now the text is rendered with the same size whatever hardware Krita runs on. That has an important consequence: when loading a .kra file, Krita 5 now converts the font size into the correct value and this new value will be saved into the .kra file later. It means that this file will _no longer be compatible with older versions of Krita_.

[A setting has been added](https://docs.krita.org/en/reference_manual/preferences/general_settings.html#miscellaneous) to allow specifying the text resolution to be used when opening old files.

#### Refactored sliders ([MR 697](https://invent.kde.org/graphics/krita/-/merge_requests/697))

**Deif Lou** reworked the spinbox sliders we use throughout Krita. Now in addition to right click to enter a number, you can also use click-hold and enter while focused. Shift key can be used while dragging to make smaller changes, and the Ctrl key for snapping to predefined values. Last but not least, the dragging in the spinbox sliders is now sensitive to the vertical mouse distance, similar to the angle rotation widget. There are even more subtle features to the new sliders as mentioned in the MR, such as support for very large ranges and more!

#### Pluginification of G'MIC ([MR 581](https://invent.kde.org/graphics/krita/-/merge_requests/581))

G'MIC has been moved to a build-in plugin again, which should improve the G'MIC situation on MacOS.

#### Brush Preset History improvements ([MR 424](https://invent.kde.org/graphics/krita/-/merge_requests/424))

A context menu has been added with several options to control the history, with three new options for history behavior, and the ability to remove a single preset or clear the list, added by **Mathias Wein**.

#### Four finger tap gesture for canvas only mode ([MR 681](https://invent.kde.org/graphics/krita/-/merge_requests/681))

Useful for Android devices, you can now switch in and out of Canvas-Only mode with a four-finger tap.

#### Apply Filter Again (Re-prompt) ([MR 408](https://invent.kde.org/graphics/krita/-/merge_requests/408))

There's a new option for applying the last-used image filter again that also prompts for settings changes.

#### Single Finger Panning ([MR 970](https://invent.kde.org/graphics/krita/-/merge_requests/970))

For years we've had three finger panning. Thanks to **Anunay Jain**, when "finger painting" is disabled in the settings, you will be able to use a single finger to pan.

#### Automatically select an appropriate scaling filter ([MR 103](https://invent.kde.org/graphics/krita/-/merge_requests/103))

If you aren't sure which image scaling filter to use, you can now select "Auto" to have Krita decide for you based on your scaling parameters. It will try to pick the best scaling filter for your image and even automatically applies nearest neighbor filtering to super low resolution pixel art enlargements.

#### Convert Colorize Mask to Paint Layer before splitting layers ([MR 894](https://invent.kde.org/graphics/krita/-/merge_requests/894))

A bit of convenience implemented by **Srirupa Datta**, this feature allows you to apply layer split directly on a colorize mask without converting to a paint layer first.

#### Improved Brush Smoothing ([MR 859](https://invent.kde.org/graphics/krita/-/merge_requests/859))

Our smoothing options make heavy use of the time stamps that belong with tablet stylus movement. Thanks to **Victor Moraes**, You can now switch between the old timer based method, or the new driver based method. Which of these is the best depends on your operating system, driver, and tablet model.

#### Filters use sliders more consistently ([MR 652](https://invent.kde.org/graphics/krita/-/merge_requests/652))

**Sachin Jindal** took the time to update all the filters with these new sliders, giving more consistency throughout Krita.

## Special Thanks

Krita is a community project, with people all over the world working on Krita, and every release we see old and new contributors. Thanks to the [development fund](https://fund.krita.org/), we can invest more time into onboarding and guiding contributors, but one thing is certain: Without these people, Krita would not be possible:

#### Halla Rempt

(irc: halla) The Krita maintainer, and the primary programmer behind the resource rewrite. She also spent a lot of time on getting builds going for the new generation of Macs, with the M1 added to the the KDE building system.

#### Wolthera van Hövell tot Westerflier

(irc: wolthera\_laptop) As the Manual Maintainer, Wolthera has been typing her fingers raw for this release (and these release notes, hi!). In addition to this, she did a lot of work on the resource management, as well as handling color management topics all over Krita. Avif and Heif's many color spaces as well as color spaces in video formats have become near invisible to the user thanks to her work, as well as the writing and parsing of SVG 1.1 icc colors.

#### Ivan Yossi

(irc: ivanyossi) Ivan spend countless hours on getting Krita compiled on the new generation of ARM based Macs, which involved getting all the dependancies to build, as well as many smaller bugs to be fixed.

#### Emmet O'Neill & Eoin O'Neill

(irc: emmetpdx & eoinoneill) Passionate for animation, Emmet and Eoin are largely responsible for the slew of animation improvements, which were selected after extensive discussion with animators. They've also been directing the new storyboarding workflow as well as managing Krita on Steam.

#### L. E. Segovia

(irc: amyspark) Amyspark has not just brought us dithered and unbounded gradients, but also many improvements in file formats and the new handling of G'Mic. They also did a lot of smaller cleanups and maintaince tasks, such as updating the dependancies, refactoring older code and has been working on MSVC support. They are also the maintainer of the KDE fork of SeExpr, KSeExpr, which is used in the fill layers.

#### Ramon Miranda

Created the regular Krita videos for the Krita channel, as well as many special brush preset collections.

#### Carl Schwan

Did a lot of work on fund.krita.org.

#### Saurabh "Confifu" Kumar

GSOC student that brought us the storyboard docker.

#### Nabil Maghfur Usman

Updated the assistant tools with the 2-point perspective assistant.

#### Anna Medanosova

Small android fixes, amongst which the new 4-finger gesture.

#### KnowZero

Created video import.

#### Alan North

Worked on the pop-up palette.

#### Srirupa Datta

Several export and smaller layer bugfixes.

#### Dmitrii Utkin

Worked on the recorder docker.

#### Pedro Reis

Did many smaller fixes, contributed the photobash python plugin, as well as UI fixes.

#### Rebecca Breu

Contributed a python plugin import assistant.

#### GDQuest Team

Contributed the batch exporter plugin.

#### Daniel Doran

Added new cropping options.

#### Dmitry Kazakov

(irc: dmitryK) Core Programmer, Dmitry has been overseeing many MR that got into this release, amongst which collaborating on the Color Smudge rewrite, the in-stack transform preview, and many many more. Recently, he's been investigating compiler optimizations and benchmarking Krita on different platforms.

#### Agata Cacko

(irc: tiar) Hired initially to fix bugs, Agata has been the second driving force behind the resource rewrite. Many elements of the tagging and resource UX has been tested to death by her, as well as handling all the bundles and other resource libraries, such as ASL and ABR. She also worked on improving the selection tools, the fill tool and improving the UX of the assistant tools.

#### Sharaf Zaman

(irc: sha\_zam) Our Android man, Sharaf has not just been working continuously on improving Krita on Android, but also has been tackling many obscure bugs throughout the year.

#### Timothée Giet

(irc: animtim) Hired to refresh the icons, Animtim is a long time KDE contributor and under his careful watch Krita's icons got updated while still in line with the rest of KDE.

#### Raghavendra Kamath

(irc: raghukamath) Handles many tasks with the manual, not least of which is reviewing and handling updated screenshots. Raghu has also started up the Krita-artists.org forum, which aims to bring together Krita users, and which has helped a lot with regards to testing complex features such as the color smudge.

#### Mathias Wein

(irc: lynx3d) Thanks to Lynx3d, we now have optimizations in the blending modes without which the color smudge rewrite would not have been possible. He also updated the pop-up palette, and has been responsible for many smaller fixes.

#### Alvin Wong

(irc: windragon) Has done many bugfixes on windows, and improved many parts of Krita for translation.

#### Tyson Tan

(irc: tyson\_tan) Blessed us with yet another splash screen, and improved a lot of the translatable strings.

#### David Revoy

(irc: deevad) Has updated the brush packs this time to include MyPaint brushes.

#### Deif Lou

(irc: Deif\_Lou) Contributed many improvements to the filter and fill layers, as well as the gradients, on top of introducing the modes for the texture option in the brush tips.

#### Peter Schatz

(irc: voronwe) Spent an extraordinary amount of time on researching and implementing new modes for the brush tips, and the driving force behind the new color smudge algorithm.

#### Scott Pretrovic

(irc: scottyp) Handled many of the website issues we got over the years, such as a better download page as well as handling things like the look for fund.krita.org.

#### Simon Repp

Contributed consistency and usability fixes.

#### Paul Franz

Contributed UX fixes.

#### Tom Tom

Bugfixes and UX improvements left and right.

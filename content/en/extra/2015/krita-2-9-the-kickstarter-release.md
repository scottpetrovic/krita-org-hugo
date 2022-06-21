---
title: "Krita 2.9: The Kickstarter Release"
date: "2015-02-21"
---

[![krita_2_9_splash](../images/krita_2_9_splash.png)](https://krita.org/wp-content/uploads/2015/02/krita_2_9_splash.png)The culmination of over eight months of work, Krita 2.9, is the biggest Krita release until now! It's so big, we can't just do the release announcement in only one page, we've had to split it up into separate pages! Last year, 2014, was a huge year for Krita. We published Krita on Steam, we showed off Krita at SIGGRAPH, we got Krita reviewed in ImagineFX, gaining the Artist's choice accolade --  and we got our first Kickstarter campaign more than funded, too! This meant that more work has gone into Krita than ever before.

And it shows: here are the results. Dozens of new features, improved functions, fixed bugs, spit and polish all over the place.  The initial port to OSX. Some of the new features took more than two years to implement, and others are a direct result of your support!

Without that support, whether through direct donations, Steam sales, the Kickstarter campaign, the work of testers and bug reporters and documentation, tutorial, translation and code contributors, Krita would never have gotten this far! So, thanks and hugs all around!

And now, stay with us for a whirlwind tour of Krita 2.9's new major features:

\[caption id="attachment\_1643" align="aligncenter" width="300"\][![Speedpaint landscape by  Raghavendra Kamath](../images/raghukamath_landscape-300x212.png)](https://krita.org/wp-content/uploads/2015/02/raghukamath_landscape.png) Speedpaint landscape by Raghavendra Kamath\[/caption\]

\[caption id="attachment\_1644" align="aligncenter" width="225"\][![Pirate by Comhorse (http://www.comhorse.com)](../images/comhorse_image2-225x300.jpg)](https://krita.org/wp-content/uploads/2015/02/comhorse_image2.jpg) Pirate by Comhorse  
(http://www.comhorse.com)\[/caption\]

\[caption id="attachment\_1647" align="aligncenter" width="300"\][!["Between Worlds" by Mira-Maia Kyyrö (http://neko-maya.fi/)](../images/betweenworlds_nekomaya-300x190.png)](https://krita.org/wp-content/uploads/2015/02/betweenworlds_nekomaya.png) "Between Worlds" by Mira-Maia Kyyrö (http://neko-maya.fi/)\[/caption\]

\[caption id="attachment\_1659" align="aligncenter" width="300"\][!["Fairies" by Elias Silveira (http://www.flickr.com/photos/elias_ilustracao_design)](../images/Krita_Fairy01-300x212.jpeg)](https://krita.org/wp-content/uploads/2015/02/Krita_Fairy01.jpeg) "Fairies" by Elias Silveira (http://www.flickr.com/photos/elias\_ilustracao\_design)\[/caption\]

### View your images in a new perspective with multiple documents!

[![krita_texture_bg](../images/krita_texture_bg-1024x564.jpg)](https://krita.org/wp-content/uploads/2015/01/krita_texture_bg.jpg)

You can now open multiple documents in Krita.There are two ways you can display documents now: _Tabbed_ and _Subwindow_. The tabbed mode is the default, but can be changed in the settings. If using subwindows, the windows can be automatically arranged with cascading and tiling. You can also have several views of the same document. This can be helpful when looking at images at different zoom levels or while mirrored.

Finally, you can customize Krita's background by adding an image or color. This can be configured in the general settings area under _Configure Krita._

### Transform your illustrations to perfection!

<iframe style="box-shadow: 0px 0px 13px 5px #DDD; margin-left: 1em;" src="https://www.youtube.com/embed/2jvTOe6oi_E" width="100%" height="315" frameborder="0" allowfullscreen="allowfullscreen"></iframe>

 

<iframe style="box-shadow: 0px 0px 13px 5px #DDD; margin-left: 1em;" src="https://www.youtube.com/embed/1J9s7dNuSe4" width="100%" height="315" frameborder="0" allowfullscreen="allowfullscreen"></iframe>

 

<iframe style="box-shadow: 0px 0px 13px 5px #DDD; margin-left: 1em;" src="https://www.youtube.com/embed/7m92IHTrL2w" width="100%" height="315" frameborder="0" allowfullscreen="allowfullscreen"></iframe>

 ![](../images/liquify-example.png)

![](../images/kickstarter-logo.png) The new transformation modes and masks will allow you greater flexibility and control when editing and manipulating your artwork. The new transformation masks give you the freedom to work non-destructively - enabling you to make creative choices.

- **Perspective** - A simple, but powerful, cousin to the regular transform, with a vanishing point to precisely get the perspective right.
- **Cage** and **Liquify** — Based on the same principles, and with the same precision (4px is the highest precision) can now be used to do intricate deformation where warp just doesn't cut it.
- **Warp Improvements** — Improvements to the quality have been made. Both warp and cage transformations now allow _multi-point selection_ with the ctrl shortcut. The transform tool's UI has also completely updated to make it easier to use. The tool options have been rearranged for maximum efficiency.
- **Transform Masks** - These allow for non-destructive transformation and await more improvements in the near future. Perspective and regular transform update instantly when you paint on them, but warp, cage and liquify will take 3 seconds pause before changes to the original update the transform. This is so that your CPU doesn't get overworked, burns out, buys a Harley, leaves for a trip around the world and replaces you with a younger, blonder model.

### Paint in colors beyond the normal with HDR painting!

<iframe style="box-shadow: 0px 0px 13px 5px #DDD; margin-left: 1em;" src="https://www.youtube.com/embed/o7AF302wdrM" width="100%" height="315" frameborder="0" allowfullscreen="allowfullscreen"></iframe>

[![colorsliders](../images/colorsliders.png)](https://krita.org/wp-content/uploads/2014/09/colorsliders.png)

The color selectors got some love in the form of **HDR color selection**. This is useful for any kind of scene-referred image painting, such as making environments for 3d scenes, or vfx work.

HDR painting is still in need of some further support and workflow polish, but you can use 'Y' to quickly turn the exposure up or down. Furthermore, you can use the LUT management docker to control OCIO, allowing you to quickly switch between colour renderings of all kinds.

The improved advanced colour selector now allows you to work in **HSI** (where intensity is measured by summing the values of R, G and B) and **HSY'** (where Luma is calculated using the configurable luma coefficients). These allow you to keep the relative lightness more similar while changing hue and saturation. This is also an option for the MyPaint shade selector, and the new experimental Color Slider docker.

The Experimental **Color Slider docker** was a heeded request for HSV sliders in Krita. Set by default to HSL, you can configure it to have any combination of HSV/HSL/HSI/HSY' sliders.

### Painting and Workflow Improvements

![improved_popup](../images/improved_popup.png)![flow-opacity-demo](../images/flow-opacity-demo.png)

**![](../images/kickstarter-logo.png)Better blending** — The mix brush is a little slower, but the blending is artefact-less now.

 **![](../images/kickstarter-logo.png) Anti-aliased brush-tips** - You can now make the brush-mask extra smooth, useful for line work and fine details. Furthermore, the new auto-spacing really allows you to speed up your bigger brushes.

**Improved Pop-up palette** - Use tags to quickly switch your pop-up palette brushes. You can also change the amount of slices that are available in your pop-up palette (available in the preferences).

**Overview Docker** - Navigate and zoom the canvas quickly.

**Auto Brush-tip** - Smoothen Line and Autospacing to help you make more beautiful sharp lines.

**Separate eraser size** - Choose to have a separate brush size from an eraser size. (in the brush editor)

**Smudge radius** - A request for a feature also found in MyPaint, the smudge radius allows you sample the underlying colour from a larger range. The colour picker too, has had it's range increased to 900px.

**Opacity & Flow separation** - Now you can finally separate opacity and flow, which leads to finer control over both.

**Locked brush settings** -> [Read more.](https://krita.org/item/introducing-dirty-presets-locked-brush-settings-and-cumulative-undo-in-krita-2-9/)

**Dirty Presets** -> [Read more.](https://krita.org/item/introducing-dirty-presets-locked-brush-settings-and-cumulative-undo-in-krita-2-9/)

### Selection Improvements

[![krita_29_selection_ovelay](../images/krita_29_selection_ovelay.png)](https://krita.org/wp-content/uploads/2015/02/krita_29_selection_ovelay.png)

![](../images/kickstarter-logo.png) Direct painting and transforming on the **global selection mask**. The Brush selection tool was removed because painting on the Global Selection Mask is much more versatile. -> [Read more](https://krita.org/item/how-to-select-areas-with-the-paintbrush-in-krita-2-9/)

![](../images/kickstarter-logo.png) **Colored overlay display option**. -> [Read more .](https://krita.org/item/how-to-select-areas-with-the-paintbrush-in-krita-2-9/).

 **![](../images/kickstarter-logo.png) Transparency Mask Improvements** - You can now separate out alpha channels into transparency masks.

**Save and load masks** - For re-using later, or for importing seperately into a different program, like a game engine.

### New Assistants and Tool Improvements

[![29release_Aliciane_assistants_casting_shadows](../images/29release_Aliciane_assistants_casting_shadows.png)](https://krita.org/wp-content/uploads/2015/02/29release_Aliciane_assistants_casting_shadows.png)

**Line Tool Improvements** - Now accepts stylus sensors. You can also hold down 'v' to activate while on the freehand brush tool.

**New assistants** - Parallel, infinite and vanishing point lines. Improve your perspective drawings. Assistants also have toggle-able previews.

**Stabilizer Smoothing** — This allows you to pull lines that will definitely end at the cursor. Unless you have delay active of course. Then a dead-zone, similar to lazy-mouse smoothing, appears around the cursor, which is good for controlling sharp corners.

**Fill Tool Improvements** - The algorithm is improved, and for even faster filled there's the new Fast Mode

**Ruler Assistant Improvements** - You can now temporarily deactivate an assistant.

**Grid Tool Improvements** - Krita will now ask you whether to toggle the grid with enter, instead of doing so automatically.

### Filter and Layer Improvements

<iframe style="box-shadow: 0px 0px 13px 5px #DDD; margin-left: 1em;" src="https://www.youtube.com/embed/YigbVY9s6gU" width="100%" height="315" frameborder="0" allowfullscreen="allowfullscreen"></iframe>

 

<iframe style="box-shadow: 0px 0px 13px 5px #DDD; margin-left: 1em;" src="https://www.youtube.com/embed/1hv3yRUof-c" width="100%" height="315" frameborder="0" allowfullscreen="allowfullscreen"></iframe>

**G'MIC Improvements** Updated version. Previews and access to [Colorize\[Interactive\]](http://www.davidrevoy.com/article247/krita-2-9-comic-coloring-tutorial).

**Split Layer** - Separate all flat colours on a layer to new layers. Pressing 'R' will let you pick the layer you want to paint on.

**Posterize filter** - This filter allows you to reduce the amount of colours per channel

**Index Colors Filter** - Helpful with HD pixel painting

**Auto Levels** - Let Krita determine what the best settings should be for adjusting levels.

**Split Layer** - Allows you to separate out all individual colors into different layers.

**![](../images/kickstarter-logo.png)Improved Vector Object Resolution ** - Now the vector pixel values are actual pixels instead of reliant on the DPI being 72.

### 3d Texturing and Image Support

<iframe style="box-shadow: 0px 0px 13px 5px #DDD; margin-left: 1em;" src="https://www.youtube.com/embed/HkoWF6UKMcY" width="100%" height="315" frameborder="0" allowfullscreen="allowfullscreen"></iframe>

 [![krita_2_9_pixelart_workflow](../images/krita_2_9_pixelart_workflow.png)](https://krita.org/wp-content/uploads/2015/02/krita_2_9_pixelart_workflow.png)

 **![](../images/kickstarter-logo.png) Shaped Gradients** - simplify making bumpmaps.

**PSD Compatibility Improvements** - Resource blocks are round-tripped. All, but four, PSD blending modes are now supported. Krita can load some CS6 PSD files. PSD Layer groups load. Support for 16 bit multi-layer files improved. Krita vector layers are saved (as raster layers) to PSD.

**Random Texture Offset** - For even stronger wilder textured effects, this allows you to randomise the offset.

**Save Merged Images** - allows you to speed up your work flow.

**OpenEXR Improvements** - The OpenEXR filter can now load and save a single-channel grayscale EXR files. Loading images with very small alpha values has been fixed as well as images with zero alpha but non-zero color values.

**RAW Support** - You can now import RAW files.

**Export Fixes and Additions** - Save 16-bit grayscale images to tiff, jpeg and ppm. r16 and r8 heightmaps are supported.

\[caption id="attachment\_1582" align="aligncenter" width="300"\][![by Tou Omiya](../images/14157847317_6d6a562a2d_k-300x249.jpg)](https://krita.org/wp-content/uploads/2015/02/14157847317_6d6a562a2d_k.jpg) by Tou Omiya\[/caption\]

\[caption id="attachment\_1576" align="aligncenter" width="216" class=" "\][![Flourish by Oksana Kharitionova](../images/flourish_v2_2500-216x300.png)](https://krita.org/wp-content/uploads/2015/02/flourish_v2_2500.png) _Flourish_ by Oksana Kharitionova\[/caption\]

\[caption id="attachment\_1642" align="aligncenter" width="300"\][![Wasteland Magic by Kateryna Herasymenko](../images/Wasteland-magic-300x212.jpeg)](https://krita.org/wp-content/uploads/2015/02/Wasteland-magic.jpeg) Wasteland Magic by Kateryna Herasymenko\[/caption\]

\[caption id="attachment\_1580" align="aligncenter" width="238"\][![Firebird by Wolthera(http://wolthera.info)](../images/firebird-238x300.png)](https://krita.org/wp-content/uploads/2015/02/firebird.png) _Firebird_ by Wolthera(http://wolthera.info)\[/caption\]

### Everything Else

### Dockers

Advanced Color Selector - Now with HSI and HSY' selectors in the main shape as well as the MyPaint shade selector. A cleaned up UI, and HDR functionality! Compositions docker - Polished to include updating and renaming compositions. Layer Docker - You can now select multiple layers with CTRL or SHIFT, or isolate a layer with ALT+left mouse click. Palette Docker - You can now add palettes and change the swatch size with CTRL+scroll. Undo history docker - Cumulative undo was one of the fruits from Mohit's Google Summer of Code. -> [Read more.](https://krita.org/item/introducing-dirty-presets-locked-brush-settings-and-cumulative-undo-in-krita-2-9/)

### Miscellaneous

Image - Change the image background color. Resource Manager - Allow quick importing and handling of large amounts of resources. new 'bundle' format to help keep everything together. View - There's fancy new canvas rulers added! Resource subtab has been moved to settings. Oceania - Eurasia is our ally. We've always been at war with Eastasia. Gradients - Editing has been improved.

### Preferences

Display - You can now turn off layer hover preview, and change the colour of the selection overlay. Color Management - You can now have unique icc profiles PER display on Linux. Krita supports using colord directly. Canvas-input settings - Line Tool, as well as Exposure and Gamma controls have been added.

\[caption id="attachment\_1573" align="aligncenter" style="margin:0px; margin-left:3em;" width="300" class=" "\][![Humphrey Boghart Caricature by Daniel Pinheiro Lima (http://prenudos.com/)](../images/humprey-300x291.jpg)](https://krita.org/wp-content/uploads/2015/02/humprey.jpg) _Humphrey Bogart Caricature_ by Daniel Pinheiro Lima (http://prenudos.com/)\[/caption\]

\[caption id="attachment\_1575" align="aligncenter" width="212" class=" "\][![by  Sioni Lopez](../images/coldoutside-212x300.jpeg)](https://krita.org/wp-content/uploads/2015/02/coldoutside.jpeg) _Cold Outside_ by Sioni Lopez\[/caption\]

\[caption id="attachment\_1574" align="aligncenter" width="225" class=" "\][![by  Andrei Rudenko](../images/tch_8-225x300.jpg)](https://krita.org/wp-content/uploads/2015/02/tch_8.jpg) by Andrei Rudenko\[/caption\]

\[caption id="attachment\_1572" align="aligncenter" width="248" class=" "\][![Wraith Queen by Marty Kulma (http://kynlo.deviantart.com/gallery/51532782/Krita)](../images/wraith_queen-248x300.jpg)](https://krita.org/wp-content/uploads/2015/02/wraith_queen.jpg) _Wraith Queen_ by Marty Kulma (http://kynlo.deviantart.com/gallery/51532782/Krita)\[/caption\]

## Next...

So, what's next? Well, lots of awesome art made with Krita 2.9, of course. Monthly bug-fix releases. We'll also be finishing the Photoshop-like layer styles feature and push it in one of those releases. Work has started, and the preliminary results are promising, but we needed more time to finish it up properly. Then there'll be an update of platform, from Qt4 to Qt5, followed by... Our next crowdfunding campaign. We're going to try and make Krita even better, make it work smoother, faster and slicker, and we want to add great animation support, too!

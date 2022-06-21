---
title: "Krita Features"
date: "2009-12-24"
---

Krita is an application for image creation and image manipulation. We focus on painting, illustration, concept art and other creative work. This is a short an incomplete list of the most important features Krita provides. 

Krita provides an OpenGL based canvas in addition to an unaccelerated canvas. Krita's filters, histogram computation and image recomposion are multi-threaded and make use of multiple cores if available. The effect of filters is previewed on-canvas.

Scripting and recording are works in progress.

## File Formats

Krita has support for a variety of file formats. Not all file formats are supported equally well, and for some there is only import, not export. Krita supports metadata for kra, ora, tiff, jpeg and png file formats.

- bmp: export only
- jp2: export, import
- jpeg: export, import
- ora: export, import
- pdf: import only
- png: export, import
- ppm: export, import
- raw: import only (based on dcraw)
- tiff: export, import
- xcf: import only

In preparation are support for gif, psd (only up to Photoshop 7) and eps.

## Color models

Krita does not support indexed color models. In general, Krita does not support color models without an alpha channel. Krita supports different channel depths, from 8 bits integer to 32 bits floating point per channel.

- RGB: 8, 16 bits integer, 16, 32 bits floating point
- CMYK: 8, 16 bits integer
- Grayscale: 8, 16 bits integer
- La\*b\*: 16 bits integer
- YCbCr: 8, 16 bits integer
- XYZ: 16 bits integer, 16, 32 bits floating point
- Painterly colorspaces: colorspaces that represent 3-10 wavelength channels in 16/32 bits floating

## Layer types

Krita supports the both layers and masks. Masks are associated with a single layer, while layers are grouped in a hierarchy.

- group layer: groups layers toegether in a hierarchy
- paint layer: contains raster image data
- filter layer: non-destructively filters all the layers underneath the filter layer in the current group
- clone layer: puts a duplicate of the original layer in a different place in the layer stack
- vector layer: contains vector data, such as vectors, text or complex objecs such as charts
- transparency mask: mask out parts of the associated layer
- filter mask: non-destructively filter parts of the associated layer
- local selection mask: make parts of the associated layer uneditable without masking those parts out

## Tools

There are several types of tools: vector tools, raster tools, guidance tools, canvas tools and selection tools. Note some types of content are not implement as tools but as "shapes" that can be inserted, for instance richt text, text-on-a-path or geometric shapes.

### Vector tools

- object manipulation tool
- connection tool
- path tool
- freehand path tool
- pattern tool
- vector shape filter tool
- calligraphy tool
- gradient tool
- zoom tool
- pan tool

### Raster Tools

- freehand paint
- line
- rectangle
- ellipse
- polygon
- polyline
- start
- stroked path (non-editable)
- dynatool
- fill with pattern or color  
    color selector  
    gradient

### Canvas Tools

- crop
- move layer
- transform tool
- distance calculation

### Guidance Tools

- ruler assistant
- perspective grid
- grid

### Selection Tools

- rectangle select
- elliptical select
- polygon select
- outline select
- fill select
- select similar colors
- path select

(There is no magnetic outline selection tool at the moment)

## Brush engines

Krita is different from other applications in that it supports brush engine plugins. These brush engines are used in the pixel tools to stroke your painting.

- pixel brush: compatible with Gimp's .gbr and .gih brushes, as well as custom brush tips and text
- duplicate: duplicate pixels from the current or another layer
- deform: deform existing pixels
- dyna: paint with movement strength
- spray: spray pixels or images
- filter: paint with a filter
- sumi-e: model a hairy brush
- airbrush: deposit color at a rate
- smudge: smudge existing pixels
- eraser: erase pixels
- grid: paint a grid of pixels
- mixing: mix colors on the canvas
- curve: random jitter and curving along the stroke
- chalk: model drawing with chalk
- pencil: draw aliased lines

In preparation is a brush engine plugin that is compatible with MyPaint's brush definitions.

## Filters

Krita provides filters that can be used directly, i.e. destructively on the pixels of a layer, when painting, or dynamically as a filter layer or filter mask.

- dodge, burn
- levels
- color adjustment curves
- brightness contrast curves
- desaturate
- invert
- autocontrast
- hsv adjust
- cubism
- pixelize
- raindrops
- oilpaint
- blur, gaussian blur
- color to alpha
- color transfer
- minimize, maximize channel
- top, left, bottom, right, sobel edge detection
- sharpen, mean removal, unsharp mask, gaussian and wavelet noise reducer
- various emboss
- small tiles
- bumpmap
- wave
- random noise
- lens correction
- random pick
- random
- OpenShiva-based filters

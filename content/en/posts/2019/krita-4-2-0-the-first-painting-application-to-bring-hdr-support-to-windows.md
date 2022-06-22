---
title: "Krita 4.2.0: the First Painting Application to bring HDR Support to Windows"
date: "2019-03-14"
categories: 
  - "news"
---

We're deep in bug fixing mode now, because in May we want to release the next major version of Krita: Krita 4.2.0. While there will be a host of new features, a plethora of bug fixes and performance improvements, one thing is unique: support for painting in HDR mode. Krita is the very first application, open source or proprietary, that offers this!

So, today we release a preview version of Krita 4.2.0 with HDR support baked in, so you can give the new functionality a try!

Of course, at this moment, only [Windows 10 supports HDR](https://support.microsoft.com/en-us/help/4040263/windows-10-hdr-advanced-color-settings) monitors, and only with some very specific hardware. Your CPU and GPU need to be new enough, and you need to have a [monitor that supports HDR](https://displayhdr.org/certified-products/). We know that the brave folks at Intel are working on HDR support for Linux, though!

### What is HDR?

HDR stands for High Dynamic Range. The opposite is, of course, Low Dynamic Range.

Now, many people when hearing the word "HDR" will think of the HDR mode of their phone's cameras. Those cameras map together images taken at different exposure levels in one image to create, within the small dynamic range of a normal image, the illusion of a high dynamic range image, with often quite unnatural results.

This is not that! Tone-mapping is old-hat. These days, manufacturers are bringing out new monitors that can go much brighter than traditional monitors, up to a 1000 nits (a standard for brightness), or even brighter for professional monitors. And modern systems, Intel 7th generation Core CPU's, support these monitors.

And it's not just brightness, these days most normal monitors are manufactured to display the [sRGB](https://en.wikipedia.org/wiki/SRGB) gamut. This is fairly limited, and lacks quite a bit of greens (some profession monitors have a wider gamut, of course). HDR monitors use a far wider gamut, with the [Rec. 2020](https://en.wikipedia.org/wiki/Rec._2020) colorspace. And instead of using traditional exponential gamma correction, they use [Perceptual Quantizer (PQ)](https://en.wikipedia.org/wiki/High-dynamic-range_video#Perceptual_Quantizer), which not just extends the dynamic range to sun-bright values, but also allows to encode very dark areas, not available in usual sRGB.

[![](/images/posts/2019/image3.png)](https://krita.org/wp-content/uploads/2019/03/image3.png)

And finally, many laptop panels only support 6 bits per channel; most monitors only 8 bits, monitors for graphics professionals 10 bits per channel -- but HDR monitors support from 10 to 16 bits per channel. This means much nicer gradations.

It's early days, though, and from a developers' point of view, the current situation is messy. It's hard to understand how everything fits together, and we'll surely have to update Krita in the future when things straighten out, or if we discover we've misunderstood something.

So... The only platform that supports HDR is Windows 10 via DirectX. Linux, nope, OpenGL, nah, macOS, not likely. Since Krita speaks OpenGL, not DirectX, we had to hack the OpenGL to DirectX compatibility layer, Angle, to support the extensions needed to work in HDR. Then we had to hack Qt to make it possible to convert the UI (things like buttons and panels) from sRGB to p2020-pq, while keeping the main canvas unconverted. We had to add, of course, a HDR capable color selector. All in all, quite a few months of hard work.

That's just the technical bit: the important bit is how people actually can create new HDR images.

### So, why is this cool?

You've got a wider range of colors to work with. You've got a wider range of dark to light to work with: you can actually paint with pure light, if you want to. What you're doing when creating an HDR image is, in a way, not painting something as it should be shown on a display, but as the light falls on a scene. There's so much new flexibility here that we'll be discovering new ways to make use of it for quite some time!

If you'd have a HDR compatible set-up, and a browser that would support HDR, well, this video could be in HDR:

{{< youtube 4O1kxEL9naw >}}

(Image by Wolthera van Hövell tot Westerflier)

### And how do I use it?

Assuming you have a HDR capable monitor, a DisplayPort 1.4 or HDMI 2.0**a** (the 'a' is important!) or higher cable, the latest version of Windows 10 with WDDM 2.4 drivers and a CPU and GPU that supports hits, this is how it works:

You have to [switch the display to HDR mode manually, in the Windows settings utility](https://support.microsoft.com/en-us/help/4040263/windows-10-hdr-advanced-color-settings). Now Windows will start talking to the display in p2020-pq mode. To make sure that you don't freak out because everything looks weird, you'll have to select a default SDR brightness level.

[![](/images/posts/2019/hdr_settings.png)](https://krita.org/wp-content/uploads/2019/03/hdr_settings.png)

You have to configure Krita to support HDR. In the _Settings → Configure Krita → Display_ settings panel you need to select your preferred surface. You'll also want to select the HDR-capable **small color selector** from the _Settings → Dockers_ menu.

[![](/images/posts/2019/hdr_krita_settings.png)](https://krita.org/wp-content/uploads/2019/03/hdr_krita_settings.png)

To create a proper HDR image, you will need to make a canvas using a profile with the rec 2020 gamut and a linear tone-response-curve: "Rec2020-elle-V4-g10.icc" is the profile you need to choose. HDR images are standardized to use the Rec2020 gamut, and the PQ trc. However, a linear TRC is easier to edit images in, so we don't convert to PQ until we're satisfied with our image.

Krita's native .kra file format can save HDR images just fine. You should use that as your working format. For sharing with other image editors, you should use the OpenEXR format. For sharing on the Web, you can use the expanded PNG format. Since all this is so new, there's not much support for that standard yet.

You can also make HDR animations... Which is pretty cool! And you can export your animations to mp4 and H.265. You need a version of [FFMpeg](https://trac.ffmpeg.org/wiki/Encode/H.265) that supports H.265. And after telling Krita where to find that, it's simply a matter of:

- Have an animation open.
- Select File → Render Animation
- Select Video
- Select Render as MPEG-4 video or Matroska
- Press the configure button next to the fileformat dropdown.
- Select at the top 'H.265, MPEG-H Part 2 (HEVC)'
- Select for the Profile: 'main10'.
- The HDR Mode checkbox should now be enabled: toggle it.
- Click 'HDR Metadata' to configure the HDR metadata
- Finally, when done, click 'render'.

If you have a CPU of 7th gen Core or later with intel Graphics integrated you can take advantage of HW accelerated encode to save time in the export stage: ffmpeg does that for you.

### Download

Sorry, this version of Krita is _only_ useful for Windows users. Linux graphics developers, get a move on!

### Windows

- 64 bits Windows: [krita-x64-4.2.0-HDR-setup.exe](https://download.kde.org/unstable/krita/4.2.0-HDR/krita-x64-4.2.0-HDR-setup.exe)
- Portable 64 bits Windows: [krita-4.2.0-HDR.zip](https://download.kde.org/unstable/krita/4.2.0-HDR/krita-x64-4.2.0-HDR.zip)

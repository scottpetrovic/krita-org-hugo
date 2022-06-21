---
title: "New in Krita: Painting with Exposure and Gamma"
date: "2014-06-13"
---

Running a [kickstarter campaign can be quite exhausting](https://www.kickstarter.com/projects/krita/krita-open-source-digital-painting-accelerate-deve)! But that doesn't mean that coding stops -- here is one new Krita 2.9 feature that we prepared earlier: painting with exposure and gamma on HDR images. [HDR (high-dynamic-range) images](https://en.wikipedia.org/wiki/High-dynamic-range_imaging) have greater dynamic range of light than ordinary images. If you make one with your camera, you'll combine a set of images made from the same subject at different exposures. If you want to create a HDR image from scratch, you can create one in Krita by selecting the 16 or 32 bit float RGB colorspace.

HDR images are rendered on your decidedly non-HDR monitor by picking an exposure level and checking what would be visible at that level. That's something Krita has been able to do since 2005! With Krita 2.7, Krita started supporting the VFX industry's standard library, OpenColorIO. But it was always hard to select a color for a particular exposure. Not anymore!

Check out this video by Timothee Giet showing off painting with exposure and gamma in Krita:

\[embed\]https://www.youtube.com/watch?v=esSzKzXVWQE\[/embed\]

Here's how it works, technically:

Krita has two methods of rendering the image on screen: internal and using Open Color IO.

1. Internal. In this mode the image data is converted into the display profile that the user configured in Settings->Color Management dialog. It ensures that all the colors of the image color space are displayed correctly on screen.  To use this mode you need to:
    1. Generate an icc profile for your monitor using any hardware device available on market
    2. Load the "Video Card Gamma Table" part of the generated profile (vcgt icc tag) into the LUT of your video card. You can use ‘xcalib’ to do that.
    3. Choose the profile in Settings->Color Management dialog
2. Open Color IO mode. In this mode Krita does not do any internal color correction for the displayed image. Instead it passes raw image data to the OCIO engine, which handles the color conversions and color proofing itself. To configure OCIO pipeline one should either:
    1. Get the [configuration here](http://opencolorio.org/configurations/index.html).
    2. Set the $OCIO environment variable to the path of your config directory
    3. Select the path to the configuration in the Krita docker manually

![](../images/smoking_common.png)

Smoking Figure by Timothée Giet

![](../images/field_common.png)

Landscape by Wolthera van Hövell tot Westerflier

### Using Exposure and Gamma for painting

Now when using Open Color IO engine (even in "Internal" mode) one can paint on the image, switching the exposure levels on the fly. Just press ‘Y’ key and drag your mouse upward or downward and the amount of light will either increase or decrease! Creation of High Dynamic Range images never have been so easy! This feature can be used for prototyping the scenes that are going to have dynamic light, for example:

A bomb has been blown. The scene becomes filled with light! surely enough, the shadow areas are now becoming well-lightened areas with lots of details!

The characters are in a room. Suddenly the light goes out and the viewer can see only eyes, fire and cigarettes glowing here and there. The highlight areas are now well-detailed.

### Color Selectors and Open Color IO

The good news! The color selectors in Krita now know not only about your monitor profile, but also about Exposure, Gamma and Open Color IO proofing settings! So it will show you the color exactly as it will look on the canvas!

Internally, it works with HSV values which you are expected to see on screen. It takes these values, applies exposure and gamma correction, executes color management routines and displays them on screen. It allows you not to think about current exposure value or color space constraints. You will always see the color exactly as it will be painted on canvas!

That is not all! After you chose any color as active, changing exposure will not alter its visual representation.

### Giving it a try

[Krita Lime packages](https://launchpad.net/~dimula73/+archive/krita) for Saucy and Trusty contain this feature (older versions of Ubuntu Linux do not have OpenColorIO). Windows users can get the latest Krita build: [http://heap.kogmbh.net/downloads/krita\_x64\_2.8.79.4.msi](http://heap.kogmbh.net/downloads/krita_x64_2.8.79.4.msi). Take care! These builds are made directly from the development branch and may contain features (like the resource manager) that are not done yet. Not everything will be working, though development builds are usually stable enough for daily work.

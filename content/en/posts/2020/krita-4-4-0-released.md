---
title: "Krita 4.4.0 released!"
date: "2020-10-13"
categories: 
  - "officialrelease"
---

Today, we're releasing Krita 4.4.0!

Only a little later than we had planned, this is the next feature release of Krita! With a whole slew of new fill layer types, including the really versatile SeExpr based scriptable fill layer type, exciting new options for Krita's brushes like the gradient map mode for brushes, lightness and gradient modes for brush textures, support for dynamic use of colors in gradients, webm export for animations, new scripting features -- and of course, hundreds of bug fixes that make this version of Krita better than ever. Especially exciting are all the fixes we made for Krita on ChromeOS and Android!

Here's an extract from the [full release notes](/krita-4-4-0-release-notes/):

## Fill Layers

This release brings a lot of updates and changes to fill layers.

### Multi-threading for fill layers

Fill layers can now make use of multi-threading. This means that if your computer has multiple cores, Krita can subdivide the calculation work for making fill layers between them. This makes fill layers a lot faster.

### Transformations for the pattern fill

[![](/images/posts/2020/krita_4_4_texture_example.png)](/images/posts/2020/krita_4_4_texture_example.png)

The different pattern transforms possible now.

The [patterns of fill layers](https://docs.krita.org/en/reference_manual/layers_and_masks/fill_layer_generators/pattern_fill.html) can now be transformed, allowing you to amongst others, rotate the patterns. This has also been implemented for the shape drawing tools and the bucket fill, and had been long on the to-do list.

### Screentone

[![](/images/posts/2020/fill_layer_screentone_postprocessing.png)](/images/posts/2020/fill_layer_screentone_postprocessing.png)

[A new fill layer option](https://docs.krita.org/en/reference_manual/layers_and_masks/fill_layer_generators/screentone.html) specialized in filling the whole screen with dots, squares, lines, waves or more. This fill layer allows you to quickly generate the simple pattern you need on the fly, which is very useful for those doing comic book illustration or similar highly graphics styles.

### Multigrid

[![](/images/posts/2020/multigrid-color-examples.png)](/images/posts/2020/multigrid-color-examples.png)

[A fill layer that generates](https://docs.krita.org/en/reference_manual/layers_and_masks/fill_layer_generators/multigrid.html), among others, [Penrose tilings](https://en.wikipedia.org/wiki/Penrose_tiling), as well as Quasicrystal structures. The results are rotationally symmetric, but aperiodic, meaning these rhomb patterns don’t repeat themselves.

This filter was inspired by the next item on the list…

### SeExpr

[![](/images/posts/2020/1096px-SeExpr_manual_1.jpg)](/images/posts/2020/1096px-SeExpr_manual_1.jpg) SeExpr Manual

Amyspark’s Google Summer of Code project, the integration of Disney Animation’s [SeExpr](https://docs.krita.org/en/reference_manual/layers_and_masks/fill_layer_generators/seexpr.html) expression language. SeExpr is in effect a tiny shader language that is used by Walt Disney Animation Studios itself to generate textures and materials on the fly for their animations. Within Krita, this allows you to code your own fill layers. We’ve also tried to come up with a good set of defaults to work off from and included them.

## Brushes

Following the addition of the lightness mode in 4.3, this release sees another round of features for the brush engines.

[![](/images/posts/2020/flowers_gradients_lightness.png)](/images/posts/2020/flowers_gradients_lightness.png)

Top stroke: using a combination of the new lightness parameter with the mix parameter. Bottom stroke: using the texture strength parameter to mix gradient mapped brush tips and textures.

### Diagonal selection lines in MyPaint color selector (Shift+M)

Diagonal lines allow modifying _lightness and saturation_ of the currently active color at the same time.

[![Diagonal lines in MyPaint Color Selector (Shift+M)](/images/posts/2020/mypaint_selector_diagonal.png)](/images/posts/2020/mypaint_selector_diagonal.png) Diagonal lines in MyPaint Color Selector (Shift+M)

## Support for dynamic use of currently selected colors in gradients.

While Krita had support for the GIMP Gradient format, we never supported the dynamic changing of [gradients](https://docs.krita.org/en/reference_manual/resource_management/resource_gradients.html) based on the current fore and background colors. Nor did we do so for the layer styles. This has now been added. Several of the bundled presets use the foreground color to easily create sparks, haze and other effects.

[![](/images/posts/2020/fg_changing_gradients_for_sparkles.png)](/images/posts/2020/fg_changing_gradients_for_sparkles.png)

Little sparkles added with the ‘GPS glare’ default, different colors are a different foreground color.

## Download

### Windows

If you're using the portable zip files, just open the zip file in Explorer and drag the folder somewhere convenient, then double-click on the krita icon in the folder. This will not impact an installed version of Krita, though it will share your settings and custom resources with your regular installed version of Krita. For reporting crashes, also get the debug symbols folder.

**NOTE for Windows Users: Microsoft has changed the way applications signed with certificates are handled. Only Digicert certificates are automatically trusted, other certificates will only be trusted if enough people bypass smartscreen to run the signed application. Our builds are absolutely safe, so you can safely do that.** **If you see the "Windows protected your PC" screen, press "More Info", then select "Run anyway".**

- 64 bits Windows Installer: [krita-x64-4.4.0-setup.exe](https://download.kde.org/stable/krita/4.4.0/krita-x64-4.4.0-setup.exe)
- Portable 64 bits Windows: [krita-x64-4.4.0.zip](https://download.kde.org/stable/krita/4.4.0/krita-x64-4.4.0.zip)
- [Debug symbols. (Unpack in the Krita installation bfolder)](https://download.kde.org/stable/krita/4.4.0/krita-x64-4.4.0-dbg.zip)

- 32 bits Windows Installer: [krita-x86-4.4.0-setup.exe](https://download.kde.org/stable/krita/4.4.0/krita-x86-4.4.0-setup.exe)
- Portable 32 bits Windows: [krita-x86-4.4.0.zip](https://download.kde.org/stable/krita/4.4.0/krita-x86-4.4.0.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/stable/krita/4.4.0/krita-x86-4.4.0-dbg.zip)

### Linux

- 64 bits Linux: [krita-4.4.0-x86_64.appimage](https://download.kde.org/stable/krita/4.4.0/krita-4.4.0-x86_64.appimage)
- 64 bits Linux [G'Mic-Qt plugin appimage](https://download.kde.org/stable/krita/4.4.0/gmic_krita_qt-x86_64.appimage)

(If, for some reason, Firefox thinks it needs to load this as text: to download, right-click on the link.)

### OSX

- OSX disk image: [krita-4.4.0.1.dmg](https://download.kde.org/stable/krita/4.4.0/krita-4.4.0.dmg)

Note: the gmic-qt is not available on OSX.

### ChromeOS and Android Beta

This time, the Android releases are made from the release tarball, so there are translations. We consider Krita on ChromeOS and Android still **_beta_**. There are many things that don't work and other things that are impossible without a real keyboard.

- [64 bits Intel CPU APK](https://download.kde.org/stable/krita/4.4.0/krita-x86_64-4.4.0-release.apk)
- [32 bits Intel CPU APK](https://download.kde.org/stable/krita/4.4.0/krita-x86-4.4.0-release.apk)
- [64 bits Arm CPU APK](https://download.kde.org/stable/krita/4.4.0/krita-arm64-4.4.0-release.apk)
- [32 bits Arm CPU APK](https://download.kde.org/stable/krita/4.4.0/krita-arm32-4.4.0-release.apk)

### Source code

- [krita-4.4.0.tar.gz](https://download.kde.org/stable/krita/4.4.0/krita-4.4.0.tar.gz)
- [krita-4.4.0.tar.xz](https://download.kde.org/stable/krita/4.4.0/krita-4.4.0.tar.xz)

### md5sum

For all downloads:

- [md5sum.txt](https://download.kde.org/stable/krita/4.4.0/md5sum.txt)

## Support Krita

Krita is a free and open source project. Please consider supporting the project with [donations](/support-us/donations/) or by [buying training videos!](/shop/) With your support, we can keep the core team working on Krita full-time.

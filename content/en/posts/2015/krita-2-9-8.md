---
title: "Krita 2.9.8"
date: "2015-10-14"
---

The eighth bug-fix release of Krita 2.9! We're still fixing bugs and adding improvements, but a lot of work has gone into the kickstarter goals and the Krita 3.0 porting work, too. Ubuntu Linux users can use the " krita-lod-unstable" packages from the [Krita Lime repository](https://launchpad.net/~dimula73/+archive/ubuntu/krita) to test-drive the first version of the animation support and the "LOD" performance improvements. Check the LOD option in the View menu, and many brushes and other features will be perform much better on large images!

But for day to day work, please update to Krita 2.9.8! There are some important fixes to the Photoshop-style Layer Styles feature, to the OpenEXR, TIFF, PNG and JPEG import/export filters.

- Improve performance when adding new layers. (A blank new layer doesn't need to make Krita update the entire image)
- Fix the pass-through icons so there's dark and light variants and make some other icons smaller
- BUG:353261: Make rotation terminology consistent in the rotate image and rotate layer plugin
- BUG:353248: Prevent a crash when using some types of graphics tablets
- BUG:352916: Fix a crash in the cage transform worker
- Improve rendering speed when some layers are invisible
- Fix a crash when using shape/vector layers
- BUG:352734: Fix saving single-layer EXR files
- BUG:352983: Load the layers in a multi-layer EXR file in the right order
- BUG:352734: Support loading and saving EXR files that have both layers and top-level channgels
- BUG:310359: Fix loading and saving of L\*a\*b TIFF images
- Add a Save Profile checkbox to the TIFF and JPG export filters: you can now save TIFF, JPG and PNG images without an embedded profile.
- BUG:352845: Store the smoothing options only once
- Fix Photoshop-style layer styles that use the random noise
- Improve the performance of Photoshop-style Layer styles.

### Download

- Linux:
    - Distributions are expected to create packages for their bleeding edge repositories.
    - Ubuntu and derivatives can use Krita Lime, as usual: [https://launchpad.net/~dimula73/+archive/ubuntu/krita](https://launchpad.net/%7Edimula73/+archive/ubuntu/krita).
    - OpenSUSE users can use the KDE:Extra repo: [http://download.opensuse.org/repositories/KDE:/Extra/](http://download.opensuse.org/repositories/KDE:/Extra/) or Leinir’s OBS repositories which have Krita built with support for Vc (which makes painting faster):
        - [http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE\_13.1/](http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_13.1/)
        - [http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE\_13.2/](http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_13.2/)
        - [http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE\_Factory/](http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_Factory/)
- Windows and OSX
    - The [download page](https://krita.org/download/krita-desktop/ "Krita Desktop") has been updated, so check out the new builds. If you don’t want to use the MSI installer, go to [files.kde.org](http://files.kde.org/krita) for the portable zip-file based version of Krita for Windows.
    - You can also get the latest version of [Krita on Steam](http://store.steampowered.com/app/280680), using the “Desktop29″ option in the Beta channel! Steam users get updates automatically.

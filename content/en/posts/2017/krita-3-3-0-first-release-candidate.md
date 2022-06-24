---
title: "Krita 3.3.0 - first release candidate"
date: "2017-09-21"
---

Less than a month after Krita 3.2.1, we're getting ready to release Krita 3.3.0. We're bumping the version because there are some important changes for Windows users in this version!

Alvin Wong has implemented support for the Windows 8 event API, which means that Krita now supports the n-trig pen in the Surface line of laptops (and similar laptops from Dell, HP and Acer) natively. This is still very new, so you have to enable this in the tablet settings:

[![](/images/posts/2017/tablet_support-300x278.png)](/images/posts/2017/tablet_support.png)

And he also refactored Krita's hardware-accelerated display functionality to optionally use Angle on Windows instead of native OpenGL. That means that many problems with Intel display chips and broken driver versions are worked around because Krita now indirectly uses Direct3D.

There are more changes in this release, of course:

- Some visual glitches when using hi-dpi screens are fixed (remember: on Windows and Linux, you need to enable this in the settings dialog).
- If you create a new image from clipboard, the image will have a title
- Favorite blending modes and favorite brush presets are now loaded correctly on startup
- GMIC
    - the plugin has been updated to the latest version for Windows and Linux.
    - the configuration for setting the path to the plugin has been removed. Krita looks for the plugin in the folder where the krita executable is, and optionally inside a folder with a name that starts with 'gmic' next to the krita executable.
    - there are several fixes for handling layers and communication between Krita and the plugin
- Some websites save jpeg images with a .png extension: that used to confuse Krita, but Krita now first looks inside the file to see what kind of file it really is.
- PNG:
    - 16 and 32 bit floating point images are now converted to 16 bit integer when saving the images as PNG.
    - It's now possible to save the alpha channel to PNG images even if there are no (semi-) transparent pixels in the image
- When hardware accelerated display is disabled, the color picker mode of the brush tool showed a broken cursor; this has been fixed.
- The Reference Images docker now only starts loading images when it is visible, instead on Krita startup. **Note:** the reference images docker uses Qt's imageio plugins to load images. If you are running on Linux, remove all Deepin desktop components. Deepin comes with severely broken qimageio plugins that will crash any Qt application that tries to display images.
- File layers now correctly reload on change again
- Add several new commandline options:
    - \--nosplash to start Krita without showing the splash screen
    - \--canvasonly to start Krita in canvas-only mode
    - \--fullscreen to start Krita full-screen
    - \--workspace Workspace to start Krita with the given workspace
- Selections
    - The Select All action now first clears the selection before selecting the entire image
    - It is now possible to extend selections outside the canvas boundary
- Performance improvements: in several places superfluous reads from the settings were eliminated, which makes generating a layer thumbnail faster and improves painting if display acceleration is turned off.
- The smart number input boxes now use the current locale to follow desktop settings for numbers
- The system information dialog for bug reports is improved
- macOS/OSX specific changes:
    - Bernhard Liebl has improved the tablet/stylus accuracy. The problem with circles having straight line segments is much improved, though it's not perfect yet.
    - On macOS/OSX systems with and AMD gpu, support for hardware accelerated display is disabled because saving to PNG and JPG hangs Krita otherwise.

### Download

#### Windows

Note for Windows users: if you encounter crashes, please follow [these instructions](https://docs.krita.org/Dr._Mingw_debugger) to use the debug symbols so we can figure out where Krita crashes. There are no 32 bits packages at this point, but there will be for the final release.

- 64 bits Windows: [krita-3.3.0-rc.1-x64-setup.exe](https://download.kde.org/unstable/krita/3.3.0-rc.1/1/krita-3.3.0-rc.1-x64-setup.exe)
- Portable 64 bits Windows: [krita-3.3.0-rc.1-x64.zip](https://download.kde.org/unstable/krita/3.3.0-rc.1/1/krita-3.3.0-rc.1-x64.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/unstable/krita/3.3.0-rc.1/1/krita-3.3.0-rc.1-x64-dbg.zip)

- Explorer Shell extension: [kritashellex-1.2.4.0-setup.exe](https://download.kde.org/stable/krita/KritaShellExtension-v1.2.4-setup.exe)

#### Linux

- 64 bits Linux: [krita-3.3.0-rc1-x86\_64.appimage](https://download.kde.org/unstable/krita/3.3.0-rc.1/krita-3.3.0-rc1-x86_64.appimage)

(If, for some reason, Firefox thinks it needs to load this as text: to download, right-click on the link.)

When it is updated, you can also use the [Krita Lime PPA](https://launchpad.net/%7Ekritalime/+archive/ubuntu/ppa) to install Krita 3.3.0-rc.1 on Ubuntu and derivatives.

#### OSX

- OSX disk image: [krita-3.3.0-rc.1.dmg](https://download.kde.org/unstable/krita/3.3.0-rc.1/krita-3.3.0-rc.1.dmg)

Note: the gmic-qt and pdf plugins are not available on OSX.

### Source code

- Source code: [krita-3.3.0-rc.1.tar.gz](https://download.kde.org/unstable/krita/3.3.0-rc.1/krita-3.3.0-rc.1.tar.gz)

#### md5sums

For all downloads:

- [md5sums.txt](https://download.kde.org/unstable/krita/3.3.0-rc.1/md5sums.txt)

#### Key

The Linux appimage and the source tarball are signed. You can retrieve the public key over https here: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8). The signatures are [here](http://download.kde.org/unstable/krita/3.3.0-rc.1/).

#### Support Krita

Krita is a free and open source project. Please consider supporting the project with [donations](/support-us/donations/) or by [buying training videos or the artbook!](/support-us/shop) With your support, we can keep the core team working on Krita full-time.

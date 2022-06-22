---
title: "Krita 2.9.11 and the second 3.0 alpha build!"
date: "2016-02-04"
---

Today, we're releasing the eleventh bugfix release for Krita 2.9 and the second development preview release of Krita 3.0! We are not planning more bug fix releases for 2.9, though it is possible that we'll collect enough fixes to warrant one release more, because there are some problems with Windows 10 that we might be able to work around. So, please check closely if you use Krita on Windows 10:

- **You get a black screen**: please go to settings/configure krita/display and disable opengl. It turns out that recent Windows updates install new Intel GPU drivers that do not implement all the functionality Krita need.
- **Pressure sensitivity stops working**: a recent update of Windows 10 breaks pressure sensitivity for some people. Please check whether reinstalling the tablet drivers fixes the issue. If not, please close Krita, navigate to your user's AppData\\Roaming folder and rename the krita folder to krita\_old. If Krita now shows pressure sensitivity again, please zip up your krita\_old folder and send to foundation@krita.org.

And now for the fixes in 2.9.11!

### 2.9.11 Changelog

- Fix a memory leak when images are copied to the clipboard
- Ask the user to wait or break off a long-running operation before saving a document
- Update to G'Mic 1.6.9-pre
- Fix rendering of layer styles
- Fix a possible issue when loading files with clone layers
- Do not crash if there are monitors with negative numbers
- Make sure the crop tool always uses the correct image size
- Fix a crash on closing images while a long-running operation is still working
- Link to the right JPEG library
- Fix the application icon
- Fix switching colors with X after using V to temporarily enable the line tool
- Fix the unreadable close button on the splash screen when using a light theme
- Fix the Pencil 2B preset
- Fix the 16f grayscale colorspace to use the right channel positions
- Add shortcuts to lower/raise the current layer

Go to the [download page to get your updated Krita](https://krita.org/download/krita-desktop/)!

### 3.0 pre-alpha Changelog

For 3.0, we've got a bunch of new features and bug fixes.

There is still one really big issue that we're working hard on: OSX and the latest Intel GPU drivers break Krita's OpenGL support badly. On OSX, you will still **NOT** see the brush outline, symmetry axis, assistants and so on. On Windows, if you have an Intel GPU, the Krita window might turn totally black. There's no need to report those issues.

- Shift+R+click onto canvas can now select multiple layers! Use this in combination with the multiple properties editor to rename a bunch of layers quickly, or use ctrl+g to group them! [![krita_shiftr_layerselect](/images/posts/2016/krita_shiftr_layerselect.gif)](https://krita.org/wp-content/uploads/2016/02/krita_shiftr_layerselect.gif)
- Improved pop-up palette, now preset-icons are more readable (size depends on maximum amount of presets set in the general settings): [![krita-new-popuppalette](/images/posts/2016/krita-new-popuppalette.png)](https://krita.org/wp-content/uploads/2016/02/krita-new-popuppalette.png)
- Tons of improvements to the color space browser: the Tone curve is now visible, making it easier to find linear spaces, there's feedback for color look-up table profiles like CMYK, there's copyright in the info box, as well as possible conversion intents, and overall just more extra info moved into the tooltips for a cleaner look. The PNG 16bit import is also alphabetised. [![krita-new-gamuts](/images/posts/2016/krita-new-gamuts.png)](https://krita.org/wp-content/uploads/2016/02/krita-new-gamuts.png) 
- Hotkeys for Hue, Saturate/Desaturate, making a color redder, yellower, bluer or greener, as well as making lighter/darker use luminance where possible. The new hotkeys have no default key and need to be set in the shortcuts editor.: [![LK_hotkey](/images/posts/2016/LK_hotkey.gif)](https://krita.org/wp-content/uploads/2016/02/LK_hotkey.gif)[![hue_hotkeys](/images/posts/2016/hue_hotkeys.gif)](https://krita.org/wp-content/uploads/2016/02/hue_hotkeys.gif)[![sat_hotkeys](/images/posts/2016/sat_hotkeys.gif)](https://krita.org/wp-content/uploads/2016/02/sat_hotkeys.gif)[![rygb_hotkeys](/images/posts/2016/rygb_hotkeys.gif)](https://krita.org/wp-content/uploads/2016/02/rygb_hotkeys.gif)
- HSI, HSY and YCrCb for the HSV/HSL adjustment filter. HSY and YCrCb can use the correct coefficients for most rgb spaces, but it isn't linearisable yet, so not true luminance yet. Regardless, below a comparison: [![krita-hsvhslhsihsyycrcb](/images/posts/2016/krita-hsvhslhsihsyycrcb.png)](https://krita.org/wp-content/uploads/2016/02/krita-hsvhslhsihsyycrcb.png)
- The color smudge brush can now do subpixel precision in dulling mode: [![krita-smudge-brush-pixel-precision](/images/posts/2016/krita-smudge-brush-pixel-precision.png)](https://krita.org/wp-content/uploads/2016/02/krita-smudge-brush-pixel-precision.png)
- Add progress reporting when Krita saves a .KRA file
- Fix wheel events in Krita 3.0
- Sanitize the order of resource and tag loading. This makes startup a bit slower, so ideally we'd like to replace the whole system with something more sophisticated but that won't happen for 3.0
- Show more digits in the Memory Reporting popup in the status bar
- Add a workaround for an assert while loading some weird PSD files
- BUG: 346430: Make sure the crop tool always uses the current image size.
- BUG:357173 Fix copy constructor of KisSelectionMask
- BUG:357987 Don't crash on loading the given file
- Fix starting Krita without XDG\_DATA\_PATH set

**Source**

We recommend building Krita from [git](https://phabricator.kde.org/diffusion/KRITA/), not from the source zip file. Krita for OSX is build from a separate branch.

- [krita3prealpha-3c69a59.zip](http://files.kde.org/krita/3/source/krita3prealpha-3c69a59.zip)

**Windows**

- [krita3prealpha-fa2b0d7.zip](http://files.kde.org/krita/3/windows/krita3-prealpha2-fa2b0d7.zip)

Download the zip file. [Unzip the zip file where you want to put Krita.](http://windows.microsoft.com/en-us/windows-10/zip-and-unzip-files#v1h=tab02).

Run the vcredist\_x64.exe installer to install Microsoft’s Visual Studio runtime.

Then double-click the krita link.

Known issues on Windows:

- If the entire window goes black, disable OpenGL for now. We’ve figured out the reason, now we only need to write a fix. It’s a bug in the Intel driver, but we know how to work around it now.

**OSX**

- [krita3-prealpha2-ac4e441.dmg](http://files.kde.org/krita/3/osx/krita3-prealpha2-ac4e441.dmg)

Download the DMG file and open it. Then drag the krita app bundle to the Applications folder, or any other location you might prefer. Double-click to start Krita.

Known issues on OSX:

- We built Krita on El Capitan. The bundle is tested to work on a mid 2011 Mac Mini running Mavericks. It looks like you will need hardware that is capable of running El Capitan to run this build, but you _do not have to have_ El Capitan, you can try running on an earlier version of OSX.
- You will _not_ see a brush outline cursor or any other tool that draws on the canvas, for instance the gradient tool. This is known, we’re working on it, it needs the same fix as the black screen you can get with some Intel drivers.

**Linux**

- [kkrita3-prealpha2-3c69a59-x86\_64.appimage](http://files.kde.org/krita/3/linux/krita3-prealpha2-3c69a59-x86_64.appimage)

For the Linux builds we now have AppImages! These are completely distribution-independent. To use the AppImage, download it, and make it an executable in your terminal or using the file properties dialog of your file manager. Another change is that configuration and custom resources are now stored in the .config/krita.org/kritarc and .local/share/krita.org/ folders of the user home folder, instead of .kde or .kde4.

Known issues on Linux:

- Your distribution needs to have Fuse enabled
- On some distributions or installations, you can only run an AppImage as root because the Fuse system is locked down. Since an AppImage is a simple iso, you can still mount it as a loopback device and execute Krita directly using the AppRun executable in the top folder.

---
title: "Krita 2.9.4 released!"
date: "2015-05-06"
---

We're not just keeping an eye on the [kickstarter campaign](https://www.kickstarter.com/projects/krita/krita-free-paint-app-lets-make-it-faster-than-phot) (three days and almost at 50%! but go ahead and support us by all means, we're not there yet!), we're also working hard on Krita itself. Dmitry is busy with improving the performance of clone layers, adding PSD file support to the Layer Styles feature and fixing loading and saving masks to PSD files (we implemented that in October, but broke it subsequently...), and we've got a brand new release for you today.

Well, I made packages for Windows available already on Sunday, but here's scoop -- what's in, what not! Layer styles, startup speed improvements, memory consumption improvements, bug fixes!

**Big New Things**

And we mean _big_. This is the first release with the layer styles feature sponsored by [last year's kickstarter](https://www.kickstarter.com/projects/krita/krita-open-source-digital-painting-accelerate-deve)!

{{< youtube BHP7HklGUuo >}}

- Implement Photoshop layer styles. Note: this is the first version. Some features are not implemented and we load and save only to Krita's native file format and ASL style library files (not PSD files yet). There is also still a bug with masks and layer styles
- make start up faster by not waiting for the presets to be loaded (startup times are now 30-50% faster )
- Big speed improvement when using transform masks and filters. The move tool is about 20% faster.
- Reduced the  download size of Krita for Windows by 33% (145MB to 97MB). This is the result of cleaning up unused files and fixing translations

**And then there are the bug fixes...**

- Fix the patch count of the color history
- Lots of fixes to the layout of docker panels, dialogs and other parts of Krita
- Lots of fixes for special widgets when using the Plastique style
- Fix issues with resizing the icon size in resource selectors
- Fix usability issues in the crop tool (reset size settings after doing cropping)
- Add a function to hide docker titlebars
- Fix issues with the default settings button
- Save memory by not loading or saving texture information for brush presets that don't use textures
- Automatically add a tag based on the filename for all brush tips from Adobe ABR brush collections
- Make Export and Save as default to the folder the original file came from
- Make it possible to switch off compression for layers in kra files (bigger files, but faster saving)
- Disable opening 32 bit float grayscale TIFF files: we don't support that yet
- Fix memory leak when using gradients
- Fix color serialization from user interface to GMIC (bug 345639)
- Fix crash when toggling GMIC preview checkbox (bug 344058)
- Make it possible to re-enable the splash screen
- Show the label for the sliders inside the slide, to save space.
- Fix HSV options for the grid and spray brush
- Don't show the zoom on-canvas notification while loading an image
- Fix many memory leaks
- Fix the specific color selector docker so it doesn't grow too big
- Allow the breeze theme to be used on platforms other than KDE
- Don't crash when creating a pattern-filled shape if no pattern is selected (bug 346990)
- Fix loading floating point TIFF files (bug 344334)
- Fix loading tags for resources from installed bundles
- Make it possible to ship default tags for our default resources (bug 338134 -- needs more work to create a good default definition)
- Remember the last chosen tag in the resource selectors (bug 346703)
- Fix bug 346355: don't say "All presets" in the brush tip selector's filter

**Downloads**

- Linux:
    - Distributions are expected to create packages for their bleeding edge repositories.
    - Ubuntu and derivatives can use Krita Lime, as usual: [https://launchpad.net/~dimula73/+archive/ubuntu/krita](https://launchpad.net/%7Edimula73/+archive/ubuntu/krita). Currently rebuilding: builds will be ready later today!
    - OpenSUSE users can the KDE:Extra repo: [http://download.opensuse.org/repositories/KDE:/Extra/](http://download.opensuse.org/repositories/KDE:/Extra/) or Leinir's OBS repositories which have Krita built with support for Vc (which makes painting faster):
        - [http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_13.1/](http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_13.1/)
        - [http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_13.2/](http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_13.2/)
        - [http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_Factory/](http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_Factory/)
- Windows. From Vista and up, Windows 7 and up is recommended. There is **no** Windows XP build. If you have a 64 bits version of Windows, don’t use the 32 bits build! The zip files do not need installing, just unpacking, but do not come with the Visual Studio C runtime that is included in the msi installer.
    - 32 bits Windows: [http://files.kde.org/krita/windows/krita_x86_2.9.4.1.msi](http://files.kde.org/krita/windows/krita_x86_2.9.4.1.msi) or [http://files.kde.org/krita/windows/krita_x86_2.9.4.1.zip](http://files.kde.org/krita/windows/krita_x86_2.9.4.1.zip) (This version does not include a working G’Mic.)
    - 64 bits Windows: [http://files.kde.org/krita/windows/krita_x64_2.9.4.1.msi](http://files.kde.org/krita/windows/krita_x64_2.9.4.1.msi) or [http://files.kde.org/krita/windows/krita_x64_2.9.4.1.zip](http://files.kde.org/krita/windows/krita_x64_2.9.4.1.zip) (Not all G'Mic filters work on Windows, some may even crash Krita.)

OSX:

(Please keep in mind that these builds are unstable and experimental. Stuff is expected not to work. We make them so we know we're not introducting build problems and to invite hackers to help us with Krita on OSX.)

- [http://files.kde.org/krita/osx/krita-2.9.4.0.dmg](http://files.kde.org/krita/osx/krita-2.9.4.0.dmg)

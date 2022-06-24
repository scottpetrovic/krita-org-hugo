---
title: "First Krita 3.0 pre-alpha!"
date: "2016-01-17"
categories: 
  - "development-builds"
---

More than a year in the making... We proudly present the first pre-alpha version of Krita 3.0 you can actually try to run! So what is Krita 3.0 pre-alpha? It's the Qt5 port, with animation, instant preview, a handful of new features and portable packages for everyone! When we feel everything is nice and stable we'll release Krita 3.1, and we'll keep on releasing new versions as and when we finish [Kickstarter stretch goals](https://www.kickstarter.com/projects/krita/krita-free-paint-app-lets-make-it-faster-than-phot). So keep in mind: Krita 3.0 is _experimental_.

This "release" includes the latest version of the animation and the instant-preview performance work, plus there are a number of stretch goals from the Kickstarter already available, too. And it is a major upgrade of the core technology that Krita runs on: from Qt4 to Qt5. The latter wasn't something that was a lot of fun, but it's needed to keep Krita code healthy for the future! Whatever may come, we're ready for it!

[![Kiki_Krita_86](/images/posts/2016/Kiki_Krita_86.gif)](/images/posts/2016/Kiki_Krita_86.gif)

The port to Qt5 meant a complete rewrite of our tablet and display code, which, combined with animation and the instant preview means that Krita is really unstable right now! And that means that we need _you_ to help us test!

Another little project was updating our build-systems for Windows, OSX, and Linux. We fully intend to make Krita 3.0 as supported on OSX as on Windows and Linux, and to that end, we got [ourselves a faster Mac](http://www.valdyas.org/fading/index.cgi/hardware/macbookpro.html).

One of the cool things coming from this system is that for Krita 3.0 we can have portable packages for all three systems! We have [AppImages](http://appimage.org/) for Linux, DMG's for OSX and a portable zip file for 64 bits Windows. Sorry, no 32 bits Windows builds yet...

[![krita3-prealpha](/images/posts/2016/krita3-prealpha-1024x621.png)](/images/posts/2016/krita3-prealpha.png)

### Download Instructions

**Windows**

- [krita3-prealpha-b4bac8d.zip](http://files.kde.org/krita/3/windows/krita3-prealpha-b4bac8d.zip)

Download the zip file. [Unzip the zip file where you want to put Krita.](http://windows.microsoft.com/en-us/windows-10/zip-and-unzip-files#v1h=tab02).

Run the vcredist\_x64.exe installer to install Microsoft's Visual Studio runtime.

Then double-click the krita link.

Known issues on Windows:

- The location of the configuration files has changed: configuration data and custom resources, and the new location isn't correct yet. The settings are in %APPDATA%\\Local\\kritarc and the resources in %APPDATA%\\Roaming\\Krita\\krita\\krita
- If the entire window goes black, disable OpenGL for now. We've figured out the reason, now we only need to write a fix. It's a bug in the Intel driver, but we know how to work around it now.

**OSX**

- [krita3-prealpha-ee7b252.dmg](http://files.kde.org/krita/3/osx/krita3-prealpha-ee7b252.dmg)

Download the DMG file and open it. Then drag the krita app bundle to the Applications folder, or any other location you might prefer. Double-click to start Krita.

Known issues on OSX:

- We built Krita on El Capitan. The bundle is tested to work on a mid 2011 Mac Mini running Mavericks. It looks like you will need hardware that is capable of running El Captitan to run this build, but you _do not have to have_ El Capitan, you can try running on an earlier version of OSX.
- You will _not_ see a brush outline cursor or any other tool that draws on the canvas, for instance the gradient tool. This is known, we're working on it, it needs the same fix as the black screen you can get with some Intel drivers.

**Linux**

- [krita3-prealpha-f7f43f2-x86\_64.appimage](http://files.kde.org/krita/3/linux/krita3-prealpha-f7f43f2-x86_64.appimage)

For the Linux builds we now have Appimages! These are completely distribution-independent. To use the AppImage, download it, and make it an executable in your terminal or using the file properties dialog of your file manager,Another change is that configuration and custom resources are now stored in the .config/krita.org/kritarc and .local/share/krita.org/ folders of the user home folder, instead of .kde or .kde4.

Known issues on Linux:

- Your distribution needs to have Fuse enabled
- On some distributions or installations, you can only run an AppImage as root because the Fuse system is locked down. Since an AppImage is a simple iso, you can still mount it as a loopback device and execute Krita directly using the AppRun executable in the top folder.

### What's Next?

More alpha builds! We'll keep fixing bugs and implementing features, and keep making releases! Right now, we're aiming for an update every week. Remember that Krita 3.0 will not include all of the features from the last Kickstarter. We still have a ways to go with adding the rest of the stretch goals, but with this release you'll get...

### Change Log

**All the animation features from the Animation Beta**

And more animation goodness:

**Animation Drop Frame Support**

We implemented a "Drop Frames" mode for Krita and made it default option. Now you can switch on the "Drop Frames" mode in the Animation Docker to ensure your animation is playing with the requested frame rate, even when the GPU cannot handle this amount of data to be shown.

Show the current frames per second (fps) and whether the frames are dropped in the tooltip of the drop frames button.

The animation playback buttons become red if the frames are dropped. The tool tip shows the following values:

-   Effective FPS - the visible speed of the clip
-   Real FPS - how many real frames per second is shown (always smaller)
-   Frames dropped - percentage of the frames dropped

**Other Animation Features**

- Allow switching frames using arrow keys (canvas input setting)
- Add "Show in Timeline" action to the Layers Docker
- Fix Duplicate Layer feature for animated layers
- Let the current frame spin box have a higher limit as well/ Let the user choose the start frame higher than 99
- Fix crashes with cropped animations, the move tool and changed backgrounds.
- Fix loading of the animation playback properties
- Fix initialization of the offset of the frame when it is duplicated
- Fix crash when loading a file with Onion Skins activated
- Frames import: Under file->import animation. This requires that you have removed the krita.rc in the resource folder(settings->manage resources->open resource folder) if you had a previous version of Krita installed. Only has a filebrowser that'll allow you to select multiple files for now, but we'll enhance the UI in the future.

**Tablet handling**

- We rewrote our tablet handling. If tablets didn't work for you with 2.9 or even crashed, check out the 3.0 branch.
- On Windows, we should better support display scaling
- On Windows, support tablet screen rotation

**Tool Improvements**

- Move increment keys for the move tool! This is still under development, but we are sure it's basic form is appreciated.

**Layer Improvements**

- We removed the 'move in/out of group layer' buttons. Moving a layer up and down will also pass it into the group.
- Duplication of multiple layers
- Shift+Delete shortcut to the Remove Layer action
- Move Up/Down actions for multiple layer selections
- Make Merge Down for multiple layers and selecting the right merged layer afterwards
- Ctrl+G when having multiple layers selected now groups them
- Ctrl+Shift+G will now have the currently selected layer put into a group with a alpha inherited layer above it, not unlike Photoshop clipping masks.
- Copy-paste layer actions. This is a little different from regular copy-paste, as the latter copies pixels onto the clipboard, while copy-paste layers copies full layers onto the clipboard
- Implemented Select All/Visible/Locked layers actions. By default they have no shortcuts, but you can assign any to them
- Mass editing of layers. Select multiple layers and press the layer properties to mass-edit or rename them
- properties and renaming layers now have hotkeys: F2 and F3

**Shortcuts**

- Our shortcut system is now ordered into groups.
- You can now save and share custom versions of your shortcuts.
- Krita now has Photoshop and Painttool Sai compatible shortcuts included by default.
- You can now switch the selection modifiers to use ctrl instead of alt. Useful if you are on Linux, or prefer ctrl to alt.
- Reset Canvas Rotation had gotten lost in 2.9, it's now back and visible under view->canvas

**Other features**

- Add import/export of GBR and GIH brush files, generating from animated .kra files is still coming.
- Show editing time of a document in the document information dialog, useful for proffesional illustrators, speedpainters and other commision-takers. It detects when you haven't performed actions for a while, and has a precision of +- 60 seconds. You can empty it in the document info dialog and of course by unzipping you .kra file and editing the meta-data there.

**Minor changes**

- The popup palette now has anti-aliased edges (but it's square on OSX...)
- simple color selector now has white on top and black on the bottom.
- updated ICC profiles.
- Added a Smudge\_water preset to make smudging easier.
- Added printing of the current FPS on canvas when the debugging is activated

Because our release is so fresh and fragile, we are, for once not going to ask you to report bugs. Instead, we have a

# **[Survey](https://www.surveymonkey.com/r/W87RX6X)**

With that in mind, it shouldn't be surprising that we don't recommend using this version for production work! Right now, Krita is in the "may eat your cat"-stage... But it is sure fun to play with!

[![DanceGirl_SEQ_small](/images/posts/2016/DanceGirl_SEQ_small.gif)](/images/posts/2016/DanceGirl_SEQ_small.gif)

(Animations created by [Achille](http://akill-blazard.blogspot.fr/), thanks!)

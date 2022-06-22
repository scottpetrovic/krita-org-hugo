---
title: "FAQ"
date: "2018-05-12"
---

Is your question not answered here? Try our [manual](https://userbase.kde.org/Krita/Manual) or [get in touch](https://krita.org/about/contact/ "Contact").

General

[What is Krita?](#whatiskrita) [Why is Krita Free?](#whyiskritafree) [What are Krita’s Development Goals?](#developmentgoals) [Why is Krita part of the Calligra Suite?](#calligrasuite) [Who translates Krita and are there translations available?](#translations) [Who and what is Kiki?](#whatiskiki) [Who owns Krita?](#legalinformation)

Support

[Is there professional support available for Krita?](#professionalsupport) [How can I learn to use Krita?](#learntousekrita) [Can I use Krita commercially?](#commercial)

Technical Questions - compatibility

[Is there a package for OSX?](#OSXpackage) [Where are the configuration files stored?](#configurationstored) [What Graphics Cards does Krita support?](#graphiccards) [Can I use Krita with sandboxie on Windows?](#sandboxie) [Krita 2.9 shows a black screen on my Windows system with an Intel GPU](#blackscreen) [What tablets does Krita support?](#tabletsupport) [How to make my Huion tablet work with Krita on Linux?](#huiontablet)

Technical Questions - inside Krita

[Can Krita load Photoshop Brushes?](#photoshopbrushes) [Why do I get a checkerboard pattern when I use the eraser?](#checkerboard) [How much memory does my image take?](#memoryconsumption) [Can krita work with 8 bit (indexed) images?](#eightbit)

How can you help us

[Would you like bug reports?](#bugreports) [Can I join the fun?](#joining)

### What is Krita?

This is our vision for the development of Krita:

_Krita is a KDE program for sketching and painting, offering an end–to–end solution for creating digital painting files from scratch by masters. Fields of painting that Krita explicitly supports are concept art, creation of comics and textures for rendering. Modeled on existing real-world painting materials and workflows, Krita supports creative working by getting out of the way and with a snappy response._

Note that when we say "Krita is a KDE program", that doesn't mean you need to run the Plasma Desktop to run Krita. It means that Krita as a project is proud to be part of the wonderful KDE community and uses the great framework technology that the KDE community develops.. You can run Krita on Windows, Gnome, XFCE, and if you spend some effort even on OSX.

There are _three_ versions of Krita: Krita Sketch, for touch devices, Krita Desktop for desktop systems and finally Krita Gemini, available through [Steam](http://steamcommunity.com/app/280680/).

### Is there professional support available for Krita?

Yes, the Krita Foundation offers support for Krita through the [development fund,](https://krita.org/support-us/donations/) sponsoring opportunities, [consultancy and dedicated development contracts](https://krita.org/support-us/commercial/).

### How can I learn to use Krita?

The most awesome way of getting started with Krita is to get the [Muses training DVD](/posts/muses/) by Ramon Miranda! Nearly five hours of instruction by a professional artist, all for just € 32,50. Get your copy today and support the Krita Foundation:

   ![](/images/pages/pixel.gif)If you come from Photoshop, check out our [Krita for Photoshop Users guide](http://files.kde.org/krita/marketing/IntroductiontoKritaforusercomingfromPs.pdf)!

### Who and what is Kiki?

Kiki is a squirrel. She's our mascot and has been designed by Tyson Tan. We choose a squirrel when we discovered that 'krita' is the Albanian word for Squirrel.

### Why is Krita part of the Calligra Suite?

Krita started out as KImageShop inside KOffice because the KOffice libraries gave us things for free we would have to code ourselves otherwise, like filter handling, a really cool rich text tool and so on. The current stable version of Krita, 2.9, is still developed in the calligra git repository. Starting with the Krita 3.0, Krita is developed in its own [repository](https://projects.kde.org/krita).

### Is there a package for OSX?

We have acquired a Mac Mini and are looking into [packages for OSX](https://www.kickstarter.com/projects/krita/krita-open-source-digital-painting-accelerate-deve/posts/902964). Be warned - opengl doesn't work properly, tablet support is broken and there are more bugs.

### Can Krita load Photoshop Brushes?

Yes, but there are limitations.  You can load ABR files by using the Add Brush button in the predefined brush tab in the brush editor. Since Adobe hasn't disclosed the file format specification, we depend on reverse-engineering to figure out what to load, and currently that's limited to basic features.

### Who translates Krita and are there translations available?

Krita is a [KDE application](http://www.kde.org/) -- and proud of it! That means that Krita's translations are done by [KDE localization teams](http://i18n.kde.org/). If you want to help out, join the team for your language! There is another way you can help out making Krita look good in any language, and that is join the development team and fix issues within the code that make Krita harder to translate.

The translations are easy to install on any linux distribution. On Windows, we are working to make it possible to install language packs, but there are a few bugs preventing the translations work correctly at the time of writing.

### What tablets does Krita support?

Krita isn't much fun without a pressure sensitive tablet. If the tablet has been properly configured, Krita works with Wacom, Huion and other uc-logic based tablets, on Windows and Linux (look below for more infos on Huion Linux support). Genius tablets are know to have problems.

### What Graphics Cards does Krita support?

Krita can use OpenGL to accelerate painting and canvas zooming, rotation and panning. Nvidia and recent Intel GPUs give the best results. Make sure your OpenGL drivers support OpenGL 3.2 as the minimum. AMD/ATI GPU's are known to be troublesome, especially on Linux with the proprietary drivers.

### What are Krita's Development Goals?

Krita is primarily a painting program, although it has image processing capabilities. This means that Krita is intended for creative people who desire to paint and draw with computer software as they do with real-world tools in an art studio.

If you are looking for a tool primarily to apply effects to existing images or photos, to catalog images, or to view images other software (such as Digikam) may be more suitable.If you want to work on collage, photo editing or print production work, Gimp might be more suitable. Ease of use and power as a painting application will always have a higher priority in Krita's ongoing development.

### Would you like bug reports?

Definitely. Please take care to include backtraces if you've got a crash, and if there's an image that breaks Krita for you, try to attach the image to the report. If it's too big, contact me (that's 'boud') on irc: #krita, or directly [via email](mailto:boud@valdyas.org). Adding new wishes to bugzilla isn't terribly useful, I'm afraid. We have a lot on our TODO already, and to create a new feature, we need to engage in some deep interaction with you, so drop by on the forum, mailing or irc instead. You can report bugs at the [KDE bug tracker](https://bugs.kde.org/). We try to reply to bug reports within a week.

If you find signing up to KDE's bugzilla too much of a bother, or aren't sure you found a real bug, don't hesitate, and drop by on the forum or on [IRC](https://krita.org/irc/).

### Can I join the fun?

Yes.The best thing you can do is use and enjoy Krita! Learn to use Krita and teach others. Create tutorials and sample files, create artwork to show off what Krita can do and spread the good word. And if you want to be more directly involved, well, I didn't know any C++ when I started hacking on Krita and I managed. You can do it, too! Check the [Join Krita page](/get-involved/overview/ "Get Involved") for more information.

And if you don't feel like hacking C++ -- well, there's the manual that needs someone attending to it, a set of tutorials would be nice, we are everlastingly needing more artwork for interface elements, and finally, we really appreciate reports from people using it, telling me about their work flow and what hampers or helps them.

### Why is Krita Free?

Krita is developed as [free software](http://www.gnu.org/) within the KDE community. We believe that good tools should be available for all artists. Krita Gemini will be available on Valve's Steam platform and will cost money, but will still be open source.

### Can I use Krita commercially?

Yes. What you create with Krita is your sole property. You own your work and can license your art however you want. Krita's GPL license applies to Krita's source code. Krita can be used commercially by artists for any purpose, by studios to make concept art, textures, or vfx, by game artists to work on commercial games, by scientists for research, and by students in educational institutions.

If you modify Krita itself, and distribute the result, you have to share your modifications with us. Krita’s GNU GPL license guarantees you this freedom. Nobody is ever permitted to take it away.

### Where are the configuration files stored?

On Windows, this is %APPDATA%\\krita or %LOCALAPPDATA%\\krita.

On Linux, .kde/share/config/krita or .kde4/share/config/krita

### Who owns Krita?

The Stichting Krita Foundation owns the Krita trademark.

### Can I use Krita with sandboxie on Windows?

No, this is not recommended. Sandboxie causes stuttering and freezes due to the way it intercepts calls for resources on disk.

### Why do I get a checkerboard pattern when I use the eraser?

You're probably used to Gimp or Photoshop. The background, that is default or first layer in these applications doesn't have an alpha channel by default. so, on their background layer, the eraser paints in the background color.

In Krita, all layers have an alpha channel, so if you want to paint in the background color, you should do that, instead of erasing. You get the same effect in, say, gimp, if you create  new image, add an alpha channel and then use the eraser tool. Most Krita users actually on starting a sketch in Krita add a new blank  layer first thing they do (the INSert key is a useful shortcut here.) That doesn't use extra memory, since a blank layer or a layer with a default color just takes one pixel worth of memory.

### How much memory does my image take?

For simple images, that's pretty simple: you mulitply width \* height \* channels \* size of the channels (so, for a 1000x1000 16 bit integer rgba image: 1000 x 1000 x 4 x 2). You multiply this by the number of layers plus two (one for the image, one for the display). If you add masks, filter layers or clone layers, it gets more complicated.

### Can krita work with 8 bit (indexed) images?

No. Krita has been designed from the ground up to use real colors, not indexed palettes. There are no plans to support indexed color images, though Krita can export to some indexed color image formats, such as GIF. However, Krita does not offer detailed control over pixel values.

### Krita 2.9 shows a black screen on my Windows system with an Intel GPU

This is a bug in the Intel OpenGL driver. Update to 10.18.14 or later. On Windows 8.0 and 8.1, you might need to manually install the driver. Follow the instructions from the [Intel Website](http://www.intel.com/support/graphics/sb/cs-022355.htm). No, we don't know either why they made installing an updated driver so hard :-(.

### How to make my Huion tablet work with Krita on Linux?

This applies to Huion models: H610 (maybe others too? report your model here..)

First, if you use a linux kernel version 3.13 or above, remove the buggy huion driver with this command line:

rmmod hid-huion

or, depending on your distribution:

modprobe -r hid-huion

Then build and [install the good kernel driver](https://github.com/DIGImend/huion-driver).

(note that you'll have to redo those steps after each kernel update, until this driver is included in mainline kernel.)

Now you should have a working tablet in Krita and Gimp (sadly, it doesn't work with current mypaint version, probably because of GTK3..) But as by default the whole tablet area is mapped to the whole screen, depending on your screen ratio you may want to adapt the active area of the tablet to have the same proportions.

For this, first you need to install xinput-calibrator (check in your package manager it may be named a bit differently, with - or \_ in the middle...)

Now, you'll need the name or ID of your device, so list devices with this command line:

xinput\_calibrator --list | grep H610

Then I noticed the huion report two different devices with the same name,  just different ID. So to find out which is the one corresponding to the actual stylus tablet area, get devices values with this command line:

xinput\_calibrator --device 10

(adapt id number the the values you found on previous step...)

It will open a sort of calibration window, don't click the crosses, just press any key to abort. Then you can see the default values of the device appeared in the console. One devices has much bigger max values (0 40000 0 25000), this is the one you should get the ID number. (in my case here was ID 10 )

Then calculate the values to set the active area to the same ratio as screen.. For example, for a 1920x1080 screen, I did this operation: 40000\*1080/1920=22500

And finally set the calibration values (TopX BottomX TopY BottomY) like this: xinput set-prop 10 "Evdev Axis Calibration" 0 40000 0 22500

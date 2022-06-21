---
title: "Frequently Asked Questions"
date: "2009-10-03"
---

### WHAT IS KRITA?

Krita is a KDE program for sketching and painting, offering an end–to–end solution for creating digital painting files from scratch by masters. Fields of painting that Krita explicitly supports are concept art, creation of comics and textures for rendering. Modelled on existing real-world painting materials and workflows, Krita supports creative working by getting out of the way and with snappy response.

### WHAT AN UGLY NAME! IT DOESN'T MEAN ANYTHING EITHER, DOES IT?

Krita is Swedish for chalk or crayon. That 'rita' is also Swedish for to draw and that the name Krita could be read as k-rita was unintentional. It is also possible that the then-maintainer of Krita choose 'krita' in the Sanskrit meaning of the word, namely perfect, as in 'krita yuga' -- perfect age. Anyway, since John Califf has disappeared we can never be sure. However, preceding maintainers were fairly sure that we wouldn't get hit by lawyers again by using this name. Me, I would have preferred Kandinsky, but there's already an art app (for the Atari ST) with that name. We won't do another renaming: three names is enough for any application, and Krita is getting quite a bit of name recognition these days.

### Can I sell artwork I created with Krita?

Yes! Krita is free software, licensed under the [GNU Public License](http://www.gnu.org/licenses/gpl.html), but that applies only to the code the application is written in. Anything you make with Krita is completely yours (unless you use somebody else's images!). We appreciate it if you show us what you do on our [gallery forum](http://forum.kde.org/viewforum.php?f=138&sid=bf905b7363f2eb4cc667c995c812285a),  of course, and we love to know that Krita helps you earn your living. Others manage as well -- check out these [cool pillows](http://ico-dy.deviantart.com/art/THROW-PILLOWS-339192508), for instance, or these [awesome bookmarks](http://forum.kde.org/viewtopic.php?f=138&t=107844)! And if you're using Krita and need something extra from it, don't hesitate to [contact us](http://krita.org/chat) and tell us about your needs.

### Why is Krita part of KOffice or Calligra?

It isn't anymore! The Krita team, together with nearly everyone from the KOffice community left KOffice and founded the [Calligra](http://calligra.org) project. Krita started out as KImageShop inside KOffice because the KOffice libraries gave us things for free we would have to code ourselves otherwise, like filter handling, a really cool rich text tool and so on. And that's still true! But these days, most Linux distributions will let you install Krita on its own or together with Karbon. We have separate mailinglist, a separate irc channel on freenode (#krita) and separate forums on [forums.kde.org](http://forum.kde.org/viewforum.php?f=136 "Krita forums at forums.kde.org"). These days we just say that "Krita is based on the Calligra platform".

 

### But it's such a burden! I have to install not just all of KDE, but also all of Calligra. Just to get Krita!

Well, first of all: strictly speaking you need just the kde and Calligra  libraries, but that's not the point. Would you rather have all that functionality duplicated in Krita (and every other application on your system?) Code reuse is good, library sharing is better. Not having to code yet another plugin management library or things like that saves us time we can spend on the cool features you want. On Linux, asking your distribution to install Krita will install just the dependencies, not the other Calligra applications. On Windows, we haven't got a separate Krita installer yet.

 

### I'M USING FEDORA/SUSE/MANDRIVA/KUBUNTU AND KRITA IS BROKEN! WHAT NOW?

There are some known issues with these distributions that the Krita development team cannot do much about right now. Please consult the [wiki](http://community.kde.org/Krita/Known_problem_with_packages "Krita Wiki - Broken Krita Packages") for fixes.

 

### Why does Krita tell me my image has the sRGB (LCMS internal) profile? I didn't know it had a profile!

Krita cannot work without color profiles, so on loading an RGB image without a profile, Krita assign it a default profile. sRGB is what most monitors and printers assume when confronted with an image without a profile. This internal profile will not be saved together with the image.

 

### I want pure red -- 255,0,0 but Krita's color selector keeps giving me something else

Krita's color selectors will not give you colours outside the gamut that's allowed by the icc profile associated with your image and your screen. If you want the widest possible gamut, use sRGB (lcms internal) both for your image and your display. That is the Krita equivalent of 'do not use color correction'.

### I've got an image with an embedded profile, but Krita says it's plain sRGB

Krita has converted your image from the the embedded profile to sRGB because the embedded profile does not provide two-way transformation. That means that it can be used to convert from the profile to the display profile, but not from the display profile to the embedded profile. Since Krita needs to go both ways -- when you paint, the colors you paint with are converted to the image profile, Krita needed to convert your image.

 

### Yet another Paint Program?

In the free graphics application space, Krita is unique: MyPaint is a pure sketching application, Gimp is for image manipulation. Krita is an end-to-end application for creating digital art.

 

### What are Krita's Development Goals ?

Krita is primarily a painting program, although it has image processing capabilities. This means that Krita is intended for creative people who desire to paint and draw with computer software as they do with real-world tools in an art studio. If you are looking for a tool primarily to apply effects to existing images or photos, to catalog images, or to view images other software (such as Digikam) may be more suitable. If you want to work on collage, photo editing or print production work, Gimp might be more suitable. Ease of use and power as a painting application will always have a higher priority in Krita's ongoing development.

 

### This is the Kimp, right?

If I had a penny for every time the Kimp was mentioned, I'd be able to do full-time development on Krita. No, this is not the Kimp. The Kimp was a hack, a clever hack, a KDE developer created using Perl to give the Gimp a KDE interface. This is a completely new application that doesn't share the same design goals as the Gimp does. So, why not? Why reinvent the wheel?

Because we don't want to do the same thing as Gimp. Gimp is outstanding at what it does, and there's indeed no reason to reinvent the wheel.

 

### Can I get it, already?

The first official, public release of Krita - part of KOffice 1.4, was released June 20, 2005. 1.5, 1.6 and 2.0 have followed. We're currently close to releasing version 2.2, which will be the first 2.x release we recommend to users. Version 2.3 should be the no-excuses, you-can-just-use-it release!

 

### Would you like bug reports?

Definitely. Please take care to include backtraces if you've got a crash, and if there's an image that breaks Krita for you, try to attach the image to the report. If it's too big, contact me (that's 'boud') on irc: #krita at irc.freenode.org, or directly on [email](mailto:boud@valdyas.org "email Boud"). Adding new wishes to bugzilla isn't terribly useful, I'm afraid. We have a lot on our TODO already, and to create a new feature, we need to engage in some deep interaction with you, so drop by on the forum, mailing or irc instead.

 

### Can I get in on this thing?

Indubitably. The best thing you can do is use and enjoy Krita! Learn to use Krita and teach others. Create [tutorials](http://userbase.kde.org/Krita "Krita Tutorials") and sample files, create [artwork](http://forum.kde.org/viewforum.php?f=138 "Krita Gallery forum at forums.kde.org") to show off what Krita can do and spread the good word. And if you want to be more directly involved, well, I didn't know any C++ when I started hacking on Krita and I managed. You can do it, too!

And if you don't feel like hacking C++ -- well, there's the manual that needs someone attending to it, a set of [tutorials](http://userbase.kde.org/Krita "Krita Tutorials") would be nice, we are everlastingly needing more artwork for interface elements, and finally, we really appreciate [reports from people using it,](http://forum.kde.org/viewtopic.php?f=137&t=82526 "How does Krita work for you - Forum post") telling me about their workflow and what hampers or helps them.

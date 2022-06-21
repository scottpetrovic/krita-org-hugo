---
title: "Krita April Update"
date: "2011-04-30"
---

I've been wanting to sit down and write a little update on Krita all week -- but was too busy. And that while so much has been happening. The most exciting news are the four Google Summer of Code projects -- well, maybe more properly three, with one being shared with Calligra.

**Dmitry Kazakov**, who last year made Krita's projection update stack -- the bit that computes the final images from your layers -- multithreaded and determinitistic will work this year on making all the tools multithreaded and queued. This will make Krita even more responsive and even more importantly, much more stable.

**Srikanth Tiyyagura** will improve the resource handling in Calligra beyond all recognitions. Right now, handling resources is mostly a manual thing -- you can copy your patterns, gradients, brushes and presets to the right place in your .kde/share/apps/krita directory, and remove them manually. He will make adding new resources, deleting existing resources (or rather, hiding them), getting resources from a Get Hot New Stuff server. And then he will implement tagging (to be compatible with [Gimp's resource tagging](http://sites.google.com/site/gimpwiki/development/gsoc#TOC-Projects-finished-in-GSoC-2008), and finally tagging of images to create a sketchbook interface for Krita. This will integrate with Nepomuk.

**Bruno Morais Ferreira** wants to add a new selection tool to Krita, using the SIOX algorithm. If time permits, he might also spend some time improving the existing selection tools. This neatly ties in with the work Dmitry is doing as a sponsored Krita developer together with Sven Langkamp on improving the actual selection data structures.

**Siddharth Sharma** has already started working on the PSD import/export filter work for his summer of code proposal. Since Adobe has opened up the specs for the CS version of photoshop, writing a psd filter no longer involves a lot of reverse engineering -- merely a little, since experience tells us that the spec seldom is very accurate or up to date. [Okteta](http://utils.kde.org/projects/okteta/) might yet see a great deal of use! The plan is to do both import _and_ export!

Of course, this is not all: in a week, the [Libre Graphics Meeting](http://www.libregraphicsmeeting.org) will be held in Montreal. Lukas Tvrdy will present the latest developments in Krita, Timothy Giet will give a workshop on drawing comics with Krita and Boudewijn will be around to give a personal introduction to Krita to any artist willing to listen and play -- and he will be giving a presentation on Krita to graphics professionals at the Saturday event. 

[![](https://krita.org/wp-content/uploads/2011/04/160x600.jpg)](http://libregraphicsmeeting.org)  

And one week after the Libre Graphics Meeting, Krita developers and users from all over the world will get together in Amsterdam, where the [Blender Institute](http://www.blender.org/blender-institute/) has graciously made available a room for us to gather and discuss the next stage in Krita's development. We already have had some preliminary discussions with artists David Revoy and Timothy Giet which pointed us in one very clear direction: polish, _polish_, **_polish_**!

### Code

**Lukas Tvrdy** pushed his improvements to the sketch brush to master. The sketch brush is very popular with artists, and these changes allow artists to associated sensors with properties like offset scale, density or line width. These sensors can be input from your tablet like pressure, but also randomness, speed, distance... The sketch brush already made for very lively lines, but it's even better now!

**Srikanth Tiyyagura** started working on fixing up the Krita dialog boxes. We were still using the old QGridLayout class to layout dialogs everywhere, but the newer QFormLayout is preferred because it adapts the layout of labers and input widgets to platform standards. It's not done yet, but when done, it will make Krita blend in much better with a Gnome desktop environment, for instance.

**Geoffrey Song** made it possible to compile Krita with an alternative compiler, Clang -- but more importantly, did some hefty optimization work in the ruler assistant and the circle mask generator. The latter is used every dab of every stroke with the circular autobrush to calculate the mask. Any performance improvement there translates directly to a better painting experience!

**Cyrille Berger** fixed a bug in our superslider's look and feel when using the Qt Curve style: this was done at the KDE UX Sprint. He also made it possible to save jpg and png files in directories with non-ascii names.

**Silvio Heinrich** spent a lot of effort on fixing Krita and pigment's composite operations and added a channel alpha lock option. Here we hit a conceptual difficulty. As Silvio explained:

> _Right now we are trying to maintain compatibility with Gimp and Photoshop but this two applications really behave different when it comes down to compositing. For compositing Photoshop uses some kind of weighted average (or whatever) to mix the source color into the resulting color and recalculates the alpha value accordingly when the destination color is semi transparent but Photoshop does this only for compositing while painting.  
>   
> And you can disable this by locking the alpha channel in Photoshop. Gimp doesn't use this at all (besides the "Normal" blending mode"). Gimp behaves for all blending modes expect "Normal" like if the alpha channel is locked.  
>   
> And now we are here with Krita.  
>   
> Krita doesn't distinguish internally between compositing the brush strokes and layer composition (it uses the same code). To make it compatible to Photoshop I implemented the blending mode computations after the specs of Adobe. And since Krita doesn't distinguish between the two compositing types I only could bring this all together by adding the "disable alpha" button so that the user can choose what he/she prefers._

So now we have a new button in the layerbox that allow you to chose the blending behaviour you prefer. It took a bit of effort to get compatibility with old Krita files back. And then Silvio and Cyrille investigated a bug in using selections with 16 bit integer/channel colorspaces. Some good detectve work by Cyrille resulted in a fix by Silvio -- much needed, since more and more artists are discovering that working in 16 bit/integer rgba gives much nicer results!

**Pierre Stirnweiss>** fixed compilation of Krita with Microsoft Visual C++ -- one day we will get Krita packages on windows!

**Dmitry Kazakov** finally fixed a bunch of memory leaks before having to go into hiding because of a gruelling university assignment!

### Envoi

See you soon! Give Krita a try and join the growing band of master users of Krita master! Let's end with a nice bit of art by André Vaz:

![](https://krita.org/wp-content/uploads/2011/04/agent-adam_p16_hr_inks.jpg)

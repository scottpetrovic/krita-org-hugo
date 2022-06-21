---
title: "Krita Sketch on Windows -- Go, go, go!"
date: "2012-07-31"
---

The contract signed, Arjen Hiemstra and I have started good and well on Krita Sketch, the touch-enabled version of Krita. We're developing mostly on Windows, for Windows. All our code is in the krita-sketch-rempt branch in the [projects.kde.org/calligra git repository](https://projects.kde.org/projects/calligra/repository). Arjen created a mockup for the touch gui, and this week the real work begins: coding on the QML gui, the new canvas, the multi-touch interaction system, the psd import/export. The works!

There is one skill badly missing in our team, though, and that is graphics design. We, that is [KO GmbH](http://www.kogmbh.com), is looking for a graphics designer to work with us to create the look of Krita Sketch. That's icons, welcome page, buttons, everything that's needed to make Krita Sketch look right. This is QML, so we're hardly bound to any platform standards. This is the goal:

Krita Sketch is going to be _the_ touch paint application for people who want to really create, not a gimmick like Microsoft's FreshPaint. It has to have a cool, inviting, understated, professional, productive, smooth look and feel. There will be lots of stuff happening, since we will allow people to work with layers, filters, selections, transform tool and so on.

If you want to work with us on this, please mail an application with your ideas, some examples of previous work, your rate and so on to [boudewijn.rempt@kogmbh.com](mailto:boudewijn.rempt@kogmbh.com). Experience with QML would be a good thing, but is not an absolute necessity. It's a freelance job. Working remotely is no problem at all, though a modicum of timezone compatibility with CEST would be nice.

(In other news, Sven Langkamp is an absolute big fixing hero, while I've found time to fix some rather bad bugs in our color management, thanks to the work of Elle Stone, who figured out some discrepancies in the results of Krita and other applications. That work will soon be merged to master, in time for the Krita 2.6 release, as well as work done on the OpenColorIO integration.)

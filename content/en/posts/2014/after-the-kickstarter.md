---
title: "After the Kickstarter..."
date: "2014-07-18"
---

Running a kickstarter is very much like, well, running! Running for thirty solid days. So the weekend after the Kickstarter ended, all of us slacked off a bit, and instead of coding we did some coding! Within a week or so, the Kickstarter should be finalized, the money in our bank account and we can start opening up the surveys for the backers! We didn't reach the stretch goal that would let Sven work full-time on Krita, so the feature survey will be "Choose and Rank 12 out of 24". Dmitry is already looking into 3D transformation stuff, so let's hope that feature won't get voted out! You could also still donate to Krita, [either directly](https://krita.org/support-krita), or through the rewards-enabled paypal button:

 Reward Selection Donate €5,00 EUR Postcard €15,00 EUR Postcard and stickers €25,00 EUR Digital Download of the Muses DVD €50,00 EUR USB Stick with Krita €100,00 EUR Comics with Krita DVD plus signed comic €150,00 EUR Dedicated Tutorial by Wolthera €250,00 EUR Pick your own priority €750,00 EUR A month of dedicated development €2.500,00 EUR 

 ![](/images/posts/2014/pixel.gif)

[Yiynova Europe](http://www.yiynova.eu/) noticed the kickstarter and contacted us -- they loaned us two Yiynova tablet monitors, the [19" MSP19u](http://www.yiynova.eu/msp19u.php) and the the [21,5" MVP22u](http://www.yiynova.eu/mvp22u.php) to test Krita with. We already had a [bug report about multi-monitor setup](https://bugs.kde.org/show_bug.cgi?id=337101) with other tablets than a Cintiq, so this was very welcome! And today there's a new experimental build that works just fine!

- [http://heap.kogmbh.net/downloads/krita\_x64\_2.8.79.13.msi](http://heap.kogmbh.net/downloads/krita_x64_2.8.79.13.msi)

This build also contains Dmitry's new memory pool code. Krita should now be a bit faster and use less memory while painting, and especially, be better behaved with longer painting sessions. Please do test! As developers, long painting sessions isn't something we can regularly indulge in!

As for OSX, I cleaned up a lot of warnings and (probably...) fixed the available memory detection, so Krita can use more than 1GB before it starts to swap. Also, all brush engines are now available! I'm still in two minds about the OSX port, though. I will need at least a month to make a nice beta, at least two months more to get it ready for end-users... This is all coding, and maybe build two, three more dependencies.

- [http://www.valdyas.org/~boud/krita-2.8.79.13.dmg](http://www.valdyas.org/%7Eboud/krita-2.8.79.13.dmg)

In other news, Scott Petrovic has been really busy working on a new look for krita.org. This week, together with KDE's wonderful sysadmin team, a development version of the site went life. Read all about it on [the Krita forum](https://forum.kde.org/viewtopic.php?f=139&t=121313&start=30#p315077)! There's even a link there to the development version of the new website!

---
title: "The Year in Review"
date: "2013-12-31"
---

The year 2013 was pretty hectic for the Krita project. It was the first year that we had the Krita Foundation to support development. The Krita Foundation through the [Development Fund](http://krita.org/support-krita#general) has been supporting Dmitry Kazakov to work full-time on Krita since September, and part-time before that. Lukas Tvrdy's work on G'Mic integration was supported directly by a sponsor. The Krita Foundation has also supported Ramon Miranda to create the Muses training DVD. The DVD is very nearly finished (we need just the subtitles to go to press!).

If you didn't pre-order, get your copy now! The regular price is € 32,50 including shipping.

<table><tbody><tr><td>Muses by Ramon Miranda</td></tr></tbody></table>

 ![](/images/posts/2013/pixel.gif)

Releases

We had two releases this year, 2.6 at February 5th and 2.7 at August 1st. During this year, we have been working on making Krita on Windows steadily better, a process that will (hopefully) lead to a really awesome 2.8 release next month.

### Krita Studio and Krita Gemini

During 2013, KO GmbH has been working on the commercially supported version of Krita, [Krita Studio](http://www.kritastudio.com). All the work done by KO on Krita for Krita studio, for instance Windows packaging and testing, as well as feature development has materially helped improve Krita all round. Commercial uptake of Krita Studio is still low, but interest is growing.

Krita Gemini, developed by Ko GmbH through sponsorship from Intel has been a high-profile demo for Intel and Microsoft, and which is a really cool application in itself: thanks to Krita Gemini, all versions of Krita now have touch support. Krita Gemini and Krita Sketch will be part of the regular Krita 2.8 release, too!

### Commit statistics

We've had a pretty active year, with nearly 3000 commits by 69 contributors, but on the whole, that activity was down a bit. Or so it seems -- we did a lot of development in branches, and those aren't counted by [Ohloh](http://www.ohloh.net/p/krita). Some of our long-standing contributors had to scale down their hacking activity a bit because of family reasons or study, but in this year, we had several people who worked on Krita for the first time: among others Salil Kapur, Christer Stenbrenden, Salil Nagpal, Sascha Suelzer, Juan Palacios and Somsubhra Bairi. Krita development is pretty healthy!

### Bugs and Wishes

We ended 2013 with 116 open bugs -- well, there are a few more hours left as of writing this, so we might close a few more! The Krita user community reported 640 bugs -- and the Krita development team closed 675, which means we have less open bugs now than a year ago! There are 192 open wishes, of which 126 were added in this year, and we implemented 68 wishes. Apart from all the features we implemented that weren't registered as a wish in bugzilla, of course!

### Features

The Krita team added among others the following major features to Krita during 2013:

- Completely rewritten transform tool
- New line smoothing algorithms
- Grayscale masks and selections
- Much faster gradient algorithms
- Improved textured painting options
- Added HSL and colorize options to the HSV filter
- Support for CMYK in the PSD filter
- Image Offset tool for texturing
- Rewritten OpenGL canvas with a high-quality zoom algorithm
- New compsition docker
- File-backed layers
- Replaced the tablet support with custom code that makes non-Wacom tablets work on Windows and Linux
- Implemented support for the G'Mic image processing algorithms library
- Clones array and Wraparound drawing mode for games and texturing
- Touch support (pinch zoom and pan)
- Configurable settings for all canvas interaction operations (zoom, pan, rotate etc.)

And a host of improvements to pretty nearly all aspects of the code, of course!

### Financial stuff

During 2013, the Krita Foundation received 1446,50 euro from pre-orders for the Muses DVD, 969,30 euro recurring donations for the Krita Development Fund and 12000,26 euro in one-time donations.

We spent 155,15 euro on stamps and envelopes, 83,00 euro on bank fees, 88,10 euro on dinner for the Krita team at the LGM in Madrid, 5 euros on taxes, 2000 euros sponsorship for the Muses DVD, 4579,00 euros sponsorship for development (including travel to the Netherlands) and finally 116,00 euro on an NVidia graphics card (for which the community did a special fund raiser.)

At the end of 2013, the Krita Foundation has a positive balance of 10466,74 euros, most of it earmarked for sponsoring development and for postage for the Muses DVD.

We were joined by two OPW interns, Maria Far and Chinkal Nagpal, who helped setup the Krita Shop as well as helped with the website. (There's plenty of [cool art in the shop -- check it out](http://www.zazzle.com/kritashop)!)

In 2013, I want to work much harder on making the Development Fund better known, so we can arrive at a sustainable situation with one or two dedicated developers working on Krita the year round. The incidental donations have given us a kick-start, now we need make the Foundation an ongoing concern! Even a small monthly donation helps to ensure continuity of development.

<table cellspacing="10"><tbody><tr><td valign="top"><p><strong>Monthly Donation through Paypal</strong></p><form action="https://www.paypal.com/cgi-bin/webscr" method="post"><table><tbody><tr><td>Krita Development Funding</td></tr><tr><td><select name="os0"><option value="Bronze">Bronze : €5,00 EUR - monthly</option> <option value="Sliver">Sliver : €10,00 EUR - monthly</option> <option value="Gold">Gold : €25,00 EUR - monthly</option> <option value="Platinum">Platinum : €100,00 EUR - monthly</option> <option value="Diamond">Diamond : €250,00 EUR - monthly</option></select></td></tr></tbody></table><input type="image" name="submit" src="https://www.paypalobjects.com/en_US/i/btn/btn_subscribeCC_LG.gif" alt="PayPal - The safer, easier way to pay online!"> <img src="images/pixel.gif" border="0" alt="" width="1" height="1"></form></td></tr></tbody></table>

<table cellspacing="10"><tbody><tr><td valign="top"><br><p><strong>One-time donation through Paypal</strong></p><form action="https://www.paypal.com/cgi-bin/webscr" method="post"><input type="image" name="submit" src="https://www.paypalobjects.com/en_US/GB/i/btn/btn_donateCC_LG.gif" alt="PayPal — The safer, easier way to pay online."> <img src="images/pixel.gif" border="0" alt="" width="1" height="1"></form></td><td valign="top"><p>&nbsp;</p><p>&nbsp;</p></td></tr></tbody></table>

### Looking Forward

Is always dangerous. But there are plenty of very interesting things going on. Animation is a hot topic, and with Somsubhra's Summer of Code Project we have a good base to work on. In 2014, we'll likely make a start on the port to Qt5, which opens up Android and iOS. Yue Liu has been working on building Krita on OSX and fixing platform-specific issues. We'll definitely be spending a lot of time on optimizing Krita even further. And who know what else? Consider this an invitation to [join the fun](http://krita.org/join-krita)!

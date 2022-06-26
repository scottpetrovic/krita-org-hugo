---
title: "Not just Krita at the 2018 Krita Sprint"
date: "2018-06-02"
categories: 
  - "news"
---

At the 2018 Krita Sprint we had a special guest: Valeriy Malov, the maintainer of the Plasma Wacom tablet settings module. We've asked him to write about his experience at the sprint, so over to him!

Hello,

This is my Krita 2018 sprint report and general report / pre-release announcement for new version of [wacomtablet](https://userbase.kde.org/Wacomtablet).

### Krita 2018 sprint

A couple of weeks ago I've attended the Krita sprint, it was a both fun and productive event. Boudewijn, Timothee and Raghukamath have tested the git version of wacomtablet on their computers. I've also tested a handful of wacom devices with the KCM, got some user input, and made a few fixes:

- Calibration of Cintiq devices should be severely improved. Previously the KCM didn't account for Cintiq's unusual sensor coordinate system, which doesn't start at 0x0, because device sensors are larger than the built-in screen.
- Support for devices that report separate USB ID for touch sensor has been added. It's not great (yet), because it still might require user intervention. If you have a device that is listed twice in the KCM, please run Wacom Tablet Finder utility and mark pen/touch parts of the device accordingly.
- Few other mapping calibration improvements: lock proportions button, calibration screen should now open on the screen the tablet is mapped to, and there's now an option to manually fine tune calibration values without getting into configuration files (this one was requested on the sprint, but has been added only post-sprint).
- A couple of minor bugs fixed: touch should now follow overall tablet rotation, hotkeys should not repeat themselves anymore.
- General consensus was that KCM's UI has some usability issues. I'm going to ask Krita team for some help with that, but this is postponed until 3.1.0 release. There's also an open question about having good default settings.
- I've tested rudimentary LED support. It works granted that system has been configured to allow normal users access to Wacom LED API (probably through udev rules). No OLED support yet, but it uses same API. Basically, this is something to work on, should be easy to fix, but unfortunately not a priority because not many devices have LEDs/OLEDs.

I want to thank Boudewijn and Irina for hosting the sprint, and Krita Foundation and KDE e.V. for sponsoring the event. Without them those issues probably wouldn't get fixed anytime soon.

### On new release and testing

There's also been a major change since 3.0.0: libwacom support. This should increase the number of devices we support out of the box. However, it's only partial for now (no LED support yet, no multiple USB ID devices yet, libwacom-supplied button schemes don't fit very well in current UI). It also requires libwacom 0.29 for devices with quirky buttons (you can still build with older libwacom, but it will be much less useful). So don't throw away "Wacom Tablet Finder" yet.

Another small change is that logging have been ported to QLoggingCategory, which means that for enabling debug logs you need to run **kdebugsettings** and look for "wacom".

With all these changes I'm going to make a 3.1.0 branch soon, which means that a release should happen this month. Most important bug fixes since 3.0.0 are hard to backport, so most likely there will be no 3.0.1, sorry. There will be no beta release either (Neon Dev Unstable, Arch and Gentoo already provide git builds for testing).

Known issues:

- No Wayland support. Like, at all, no ETA. I'm ready to cooperate with someone who wants to implement tablet support in KWin wayland, but I can't work on it myself anytime soon.
- Automated rotation tracking most likely won't work on multi-screen setup. This is a Qt bug.
- Calibration window can enter "drag" mode when touched/dragged by pen. This is quite annoying but it shouldn't affect calibration results. This is a KDE feature (you can disable it in widget style settings) which I don't know how to circumvent yet.

There's also a handful of issues that are kept open for now, but after release of 3.1.0 I'll eventually close some of them as I consider them fixed, unless anyone confirms otherwise:

- [**Bug 334520**](https://bugs.kde.org/show_bug.cgi?id=334520) - Calibration fails on Tablet PC if external screen is connected and tablet mapped to internal screen (should be fixed in git/3.1.0)
- [**Bug 336748**](https://bugs.kde.org/show_bug.cgi?id=336748) - Calibrate doesn't work very good on cintiq13 (should be fixed in git/3.1.0)
- [**Bug 322918**](https://bugs.kde.org/show_bug.cgi?id=322918) - Problem with calibrating wacom cintiq 13HD (should be fixed in git/3.1.0)
- [**Bug 327952**](https://bugs.kde.org/show_bug.cgi?id=327952) - wacom module is not working for calibrating a Cintiq 21ux (should be fixed in git/3.1.0)
- [**Bug 364043**](https://bugs.kde.org/show_bug.cgi?id=364043) - Intuos Pro cannot generate settings profiles, cannot configure buttons.
- [**Bug 343666**](https://bugs.kde.org/show_bug.cgi?id=343666) - Device 'Wacom Bamboo One M Pen' is not in wacom_devicelist, not able to configure using tablet configuration (should be fixed in git/3.1.0)
- [**Bug 339138**](https://bugs.kde.org/show_bug.cgi?id=339138) - Tablet screen mapping resets after KDE restart
- [**Bug 325520**](https://bugs.kde.org/show_bug.cgi?id=325520) - Dell latitude xt2: touchscreen inverted when rotate to portrait (should be fixed in git/3.1.0)

Full list of open bugs/wishes [here](https://bugs.kde.org/buglist.cgi?component=general&list_id=1520931&product=wacomtablet&resolution=---).

Do not hesitate opening a bug if you encounter an issue. If no new issues will surface after the 3.1.0 release, usability improvements is probably the next priority for the project.

### On packaging

This is a sort of very important topic which I can't do much about directly. Currently, wacom support in KDE is an optional component, so if **Tablet** section is missing from **Input Devices** settings, you need to install it. Package usually goes by name **wacomtablet** or **kcm-wacomtablet**. You can check if your distribution packages it [here](https://repology.org/metapackage/kcm-wacomtablet/versions) and [here](https://repology.org/metapackage/wacomtablet/versions). As far as I know, only KDE Neon, Arch (+derivatives) and Gentoo provide up-to-date package for wacomtablet right now. Kubuntu has it too, but it's hidden in [experimental PPA](https://launchpad.net/~kubuntu-ppa/+archive/ubuntu/experimental/+packages). If you're using something else, your options are:

- Building from source and installing as README.md instructs, which I really don't want people doing for a bunch of reasons.
- Asking someone else (preferably your distribution's KDE team) to package it. This is usually done via distribution's bugtracker or support forums.

Unfortunately due to how the project is structured (it's just a bunch of plugins), I don't think I can build an AppImage for everyone to use. So the best way to get it in your distribution is letting distribution maintainers know that it exists and you need it to be packaged.

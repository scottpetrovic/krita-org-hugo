---
title: "Second Beta for Krita 5.0"
date: "2021-10-11"
categories: 
  - "development-builds"
---

A bit later than planned -- after a year and a half of isolation meeting people spreads really bad colds -- we're releasing the second beta of Krita 5.0.0! [**The same warnings we gave with beta 1 still hold**](/item/first-beta-for-krita-5-0-released/)! There are still some [showstoppers](https://bugs.kde.org/buglist.cgi?bug_severity=critical&bug_severity=grave&bug_severity=major&bug_severity=crash&bug_severity=normal&bug_severity=minor&bug_status=UNCONFIRMED&bug_status=CONFIRMED&bug_status=ASSIGNED&bug_status=REOPENED&keywords=regression%2C%20release_blocker%2C%20&keywords_type=anywords&list_id=1918546&product=krita&query_format=advanced), but there we're also over 700 fixes closer to the final release.

This release also includes a reworked GPU accelerated canvas: especially on HiDPI screens and on macOS Krita should perform much better.

![](/images/posts/2021/electrichearts_20201224A_kiki_c1_1080P-1024x512.png) The new splash screen, by Tyson Tan

These are the most important fixes since Beta 1:

- Dmitry Kazakov and Ivan Yossi implemented a new way of uploading image textures to the GPU, improving performance when painting especially on macOS.
- Michał Chojnowski fixed a crash in the gamut mask toolbar ([BUG:441122](https://bugs.kde.org/show_bug.cgi?id=441122))
- Alvin Wong improved the translatability of Krita a lot, and worked really hard on the traditional Chinese translation.
- Tyson Tan also improved the translatability of Krita a lot, and worked really hard on the simplified Chinese translation.
- Amyspark fixed a problem with Krita resetting its settings after using the G'Mic-Qt plugin. G'Mic has also been updated to the latest version.
- Deif Lou fixed several issues in the filter brush engine
- Amyspark reworked the layer metadata framework ([BUG:410341](https://bugs.kde.org/show_bug.cgi?id=410341))
- Agata Cacko fixed the color history button layout ([BUG:434915](https://bugs.kde.org/show_bug.cgi?id=434915))
- Alan North fixed working with shared curves in the brush editor
- Agata Cacko made it possible to load Adobe Style Library files that have styles with conflicting unique id's
- Alvin Wong fixed the zoom level in the floating canvas message ([BUG:429569](https://bugs.kde.org/show_bug.cgi?id=429569))
- Tom Tom Tom fixed a bug in the calligraphy tool
- Eoin O'Neill fixed a crash in the storyboard docker ([BUG:441592](https://bugs.kde.org/show_bug.cgi?id=441592))
- Emmet O'Neill improved the usability of the storyboard docker ([BUG:441593](https://bugs.kde.org/show_bug.cgi?id=441593))
- Sharaf Zaman fixed the welcome page on Android/ChromeOS
- Matthias Wein fixed several issues with the docker titlebars
- Alvin Wong fixed issues with placing popup windows ([BUG:441935](https://bugs.kde.org/show_bug.cgi?id=441935))
- Alvin Wong fixed the touch pan gesture breaking when moving too quickly ([BUG:441706](https://bugs.kde.org/show_bug.cgi?id=441706))
- Wolthera van Hövell tot Westerflier fixed loading KPL palettes defined using the Lab colorspace ([BUG:441139](https://bugs.kde.org/show_bug.cgi?id=441139))
- Alvin Wong fixed a performance issue in the overview docker ([BUG:442075](https://bugs.kde.org/show_bug.cgi?id=442075))
- Wolthera van Hövell tot Westerflier fixed a crash in the channels docker ([BUG:442117](https://bugs.kde.org/show_bug.cgi?id=442117))
- Matthias Wein fixed a performance issue in the channels docker
- Alvin Wong improved the usability of Krita in MDI mode ([BUG:441644](https://bugs.kde.org/show_bug.cgi?id=441644))
- Halla Rempt fixed a crash in the task set docker if disabled actions were executed ([BUG:441638](https://bugs.kde.org/show_bug.cgi?id=441638))
- Halla Rempt fixed a bug in Qt's font database where having a space between angular brackets in a font name would break the parser ([BUG:430220](https://bugs.kde.org/show_bug.cgi?id=430220))
- Agata Cacko fixed the previews of several assistant shapes ([BUG:441212](https://bugs.kde.org/show_bug.cgi?id=441212))
- Alvin Wong fixed an issue using Windows Ink or Wintab, where double tablet events might be sent by broken drivers, and where the second event then would activate a mouse event ([BUG:441687](https://bugs.kde.org/show_bug.cgi?id=441687))
- Matthias Wein fixed an issue where the dimensions for a new image were calculated wrongly ([BUG:442124](https://bugs.kde.org/show_bug.cgi?id=442124))
- Sharaf Zaman fixed incremental backup saving on Android ([BUG:427042](https://bugs.kde.org/show_bug.cgi?id=427042))
- Halla Rempt fixed rotating the system log
- Halla Rempt changed the default setting for undo steps from 30 to 200
- Agata Cacko fixed updating the preview for a gradient after editing
- Amyspark fixed 32 bit floating point RGB in LittleCMS ([BUG:442004](https://bugs.kde.org/show_bug.cgi?id=442004), [BUG:439947](https://bugs.kde.org/show_bug.cgi?id=439947), [BUG:437429](https://bugs.kde.org/show_bug.cgi?id=437429))
- Wolthera van Hövell tot Westerflier fixed creating separations from the alpha channel ([BUG:434288](https://bugs.kde.org/show_bug.cgi?id=434288))
- Halla Rempt added a default shortcut for creating a vector layer: Shift-Insert ([BUG:442585](https://bugs.kde.org/show_bug.cgi?id=442585))
- Wolthera van Hövell tot Westerflier implemented loading a gimp brush or gimp imagehose brush as a color image when editing the brush as a Krita image and fixed saving these brushes  ([BUG:442316](https://bugs.kde.org/show_bug.cgi?id=442316))
- Wolthera van Hövell tot Westerflier added a reset option to the autobrush widget ([BUG:437006](https://bugs.kde.org/show_bug.cgi?id=437006))
- Halla Rempt fixed an issue where when a shortcuts definition file was missing, menu entries would turn out blank ([BUG:428453](https://bugs.kde.org/show_bug.cgi?id=428453))
- Eoin O'Neill implemented a new export user interface for the storyboard docker
- Eoin O'Neill fixed using the move tool on animated masks ([BUG:441974](https://bugs.kde.org/show_bug.cgi?id=441974))
- Eoin O'Neill fixed the crop tool not working properly on cloned animation frames. ([BUG:441369](https://bugs.kde.org/show_bug.cgi?id=441369))
- Wolthera van Hövell tot Westerflier made it possible to add color labels and pin to the timeline for masks ([BUG:438124](https://bugs.kde.org/show_bug.cgi?id=438124))
- Wolthera van Hövell tot Westerflier fixed the task set docker's appearance ([BUG:442185](https://bugs.kde.org/show_bug.cgi?id=442185))
- Alvin Wong fixed issues when using fractional display scaling
- Sharaf Zaman fixed issues with changing the cursor icon on Android ([BUG:431859](https://bugs.kde.org/show_bug.cgi?id=431859))
- Reinold Rojas enabled color sample preview for the color sampler tool ([BUG:396490](https://bugs.kde.org/show_bug.cgi?id=396490))
- Reinold Rojas fixed a problem with Krita's fullscreen mode in canvas-only mode ([BUG:437932](https://bugs.kde.org/show_bug.cgi?id=437932))
- Halla Rempt added a tool preview option combobox to the transform tool so users can switch between fast and in-stack preview
- Black Cat fixed applying font styles in the text tool ([BUG:392343](https://bugs.kde.org/show_bug.cgi?id=392343))
- Agata Cacko fixed the preview of local assistants ([BUG:442619](https://bugs.kde.org/show_bug.cgi?id=442619))
- Wolthera van Hövell tot Westerflier fixed several issues in the crop tool ([BUG:442827](https://bugs.kde.org/show_bug.cgi?id=442827), [BUG:442959](https://bugs.kde.org/show_bug.cgi?id=442959))
- Wolthera van Hövell tot Westerflier fixed flattening a clones array: the flattened layer now is in the correct position ([BUG:437431](https://bugs.kde.org/show_bug.cgi?id=437431))
- Wolthera van Hövell tot Westerflier fixed a possible crash with color adjustment filter masks ([BUG:428349](https://bugs.kde.org/show_bug.cgi?id=428349))
- Agata Cacko fixed thumbnails for gradients when creating a resource bundle
- Agata Cacko fixed several issues with resource tagging
- Dmitry Kazakov improved the performance of masking brushes
- Halla Rempt implemented saving user-defined tags
- Dmitry Kazakov improved the performance of starting a new stroke when the current brush tip is very big ([BUG:436731](https://bugs.kde.org/show_bug.cgi?id=436731))
- Sharaf Zaman improved the usability of the text tool when using Android or ChromeOS
- Dmitry Kazakov fixed updating shapes that belong to a transformed group ([BUG:443161](https://bugs.kde.org/show_bug.cgi?id=443161))
- Dmitry Kazakov fixed canvas updates in wraparound mode ([BUG:442796](https://bugs.kde.org/show_bug.cgi?id=442796))
- Dmitry Kazakov fixed artifacts in the hue sensor of the color smudge brush engine ([BUG:441755](https://bugs.kde.org/show_bug.cgi?id=441755))
- Matthias Wein fixed a memory leak in the create new image dialog
- Halla Rempt fixed an initialization issue in the Notifier scripting class
- Agata Cacko improved the performance of the perspective assistant

We will continue fixing issues that come in from testing the beta and the nightly builds so we can release a solid Krita 5. Please consider supporting Krita's development through the [development fund](https://fund.krita.org/):

[![](/images/posts/2021/devfund-1024x346.png)](https://fund.krita.org)

## Download

### Windows

If you're using the portable zip files, just open the zip file in Explorer and drag the folder somewhere convenient, then double-click on the krita icon in the folder. This will not impact an installed version of Krita, though it will share your settings and custom resources with your regular installed version of Krita. For reporting crashes, also get the debug symbols folder.

Note that we are not making 32 bits Windows builds anymore.

- 64 bits Windows Installer: [krita-x64-5.0.0-beta2-setup.exe](https://download.kde.org/unstable/krita/5.0.0-beta2/krita-x64-5.0.0-beta2-setup.exe)
- Portable 64 bits Windows: [krita-x64-5.0.0-beta2.zip](https://download.kde.org/unstable/krita/5.0.0-beta2/krita-x64-5.0.0-beta2.zip)
- [Debug symbols. (Unpack in the Krita installation folder)](https://download.kde.org/unstable/krita/5.0.0-beta2/krita-x64-5.0.0-beta2-dbg.zip)

### Linux

- 64 bits Linux: [krita-5.0.0-beta2-x86\_64.appimage](https://download.kde.org/unstable/krita/5.0.0-beta2/krita-5.0.0-beta2-x86_64.appimage)

The separate gmic-qt appimage is no longer needed.

(If, for some reason, Firefox thinks it needs to load this as text: to download, right-click on the link.)

### macOS

Note: if you use macOS Sierra or High Sierra, please [check this video](https://www.youtube.com/watch?v=3py0kgq95Hk) to learn how to enable starting developer-signed binaries, instead of just Apple Store binaries.

- macOS disk image: [krita-5.0.0-beta2.dmg](https://download.kde.org/unstable/krita/5.0.0-beta2/krita-5.0.0-beta2.dmg)

### Android

The Android releases are made from the release tarball, so there are translations. We consider Krita on ChromeOS and Android still **_beta_**. There are many things that don't work and other things that are impossible without a real keyboard.

- [64 bits Intel CPU APK](https://download.kde.org/unstable/krita/5.0.0-beta2/krita-x86_64-5.0.0-beta2-release-signed.apk)
- [32 bits Intel CPU APK](https://download.kde.org/unstable/krita/5.0.0-beta2/krita-x86-5.0.0-beta2-release-signed.apk)
- [64 bits Arm CPU APK](https://download.kde.org/unstable/krita/5.0.0-beta2/krita-arm64-v8a-5.0.0-beta2-release-signed.apk)
- [32 bits Arm CPU APK](https://download.kde.org/unstable/krita/5.0.0-beta2/krita-armeabi-v7a-5.0.0-beta2-release-signed.apk)

### Source code

- [krita-5.0.0-beta2.tar.gz](https://download.kde.org/unstable/krita/5.0.0-beta2/krita-5.0.0-beta2.tar.gz)
- [krita-5.0.0-beta2.tar.xz](https://download.kde.org/unstable/krita/5.0.0-beta2/krita-5.0.0-beta2.tar.xz)

### md5sum

For all downloads:

- [md5sum.txt](https://download.kde.org/unstable/krita/5.0.0-beta2/md5sum.txt)

### Key

The Linux appimage and the source .tar.gz and .tar.xz tarballs are signed. You can retrieve the public key [here](https://files.kde.org/krita/4DA79EDA231C852B). The signatures are [here](https://download.kde.org/unstable/krita/5.0.0-beta2/) (filenames ending in .sig).

## Support Krita

Krita is a free and open source project. Please consider supporting the project with [donations](https://fund.krita.org) or by [buying training videos!](/shop/) With your support, we can keep the core team working on Krita full-time.

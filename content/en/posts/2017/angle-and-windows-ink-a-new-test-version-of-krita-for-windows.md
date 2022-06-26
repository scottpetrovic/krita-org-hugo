---
title: "Angle and Windows Ink - a new test version of Krita for Windows"
date: "2017-08-26"
---

We've created a special version of Krita 4.0 pre-alpha for Windows users to test. This version contains two big new features that should solve the biggest problems Krita has on the Windows platform:

- Support for ANGLE. This is really technical, but basically, ANGLE is a technology that presents an OpenGL API but lets Direct3D do the work. On Windows, many OpenGL drivers are very buggy, and that could lead to crashes, black or blank screens. It's the most-hated [issue](https://bugs.kde.org/show_bug.cgi?id=360601) we have, and it is not even a bug in Krita! If you're a Windows user and had to disable OpenGL in the Configure Krita dialog, then you should test this build!
- Support for Windows Ink/Windows 8 Pointer Events. That's to say, native support for the n-trig pen technology in Microsoft's Surface line of products -- also used by Asus, Dell and HP in their convertibles that can use a pen.

**Note:** that this is a build from our development branch. It has got all kinds of nifty, but **highly unstable** features, like scripting, saving in the background, svg graphics... If you load a Krita 3.x file with vector layers and save it with this version of Krita, you will **NOT** be able to open it in your regular, stable Krita. This build is purely experimental! **Do NOT use it for real work. DO help us with testing!**

### Test Instructions for Angle

- Open the survey in your browser: [https://goo.gl/forms/vYxPMbqGyVhPCc2q2](https://goo.gl/forms/vYxPMbqGyVhPCc2q2)
- Download the test build and debug symbols
    - [https://files.kde.org/krita/4/windows/krita_4.0-prealpha_angle_ink-1-x64.zip](https://files.kde.org/krita/4/windows/krita_4.0-prealpha_angle_ink-1-x64.zip)
    - [https://files.kde.org/krita/4/windows/krita_4.0-prealpha_angle_ink-1-x64-dbg.zip](https://files.kde.org/krita/4/windows/krita_4.0-prealpha_angle_ink-1-x64-dbg.zip)
- Open the first zipfile in Windows Explorer, and drag the krita_4.0-prealpha_angle_ink-1-x64 folder to your desktop
- Open the second zipfile in Windows Explorer and drag the bin, lib and share folders into the krita_4.0-prealpha_angle_ink-1-x64 folder on your desktop.
- With Windows Explorer, navigate into the krita_4.0-prealpha_angle_ink-1-x64 folder on your desktop
- Start Krita by double-clicking on the krita link or on the bin\\krita.exe file
- You will now be given a choice:[![](/images/posts/2017/angle_question.png)](/images/posts/2017/angle_question.png)
- Please first choose Test Desktop OpenGL. Create a new image and try to draw for a bit. Fill in the results in the survey: whether you experienced a crash or not.
- Next, restart Krita and choose Test ANGLE. Create a new image and draw for a bit. Fill in the results in the survey.

**NOTE: You won't be able to enable/disable OpenGL/Angle in Krita's Settings/Configure Krita/Display settings dialog; it will be forced enabled for this test.**

### Test Instructions for Windows Ink/Windows Pointer API

This is only relevant for Windows 8 and 10: Windows 7 does not support this API (and Krita does not support Windows 95, 98, XP or Vista). You should be using a Surface Pro with a pen or another convertible that uses Microsoft's n-trig pen technology. It does not matter whether you have the wintab driver installed.

- Open the survey in your browser: [https://goo.gl/forms/N5Exyx8aKSOeAUmu2](https://goo.gl/forms/5TSCWNZvvjN5SVoq1)
- If you haven't performed the previous test for Angle, download the test build and debug symbols
    - [https://files.kde.org/krita/4/windows/krita_4.0-prealpha_angle_ink-1-x64.zip](https://files.kde.org/krita/4/windows/krita_4.0-prealpha_angle_ink-1-x64.zip)
    - [https://files.kde.org/krita/4/windows/krita_4.0-prealpha_angle_ink-1-x64-dbg.zip](https://files.kde.org/krita/4/windows/krita_4.0-prealpha_angle_ink-1-x64-dbg.zip)
- Open the first zipfile in Windows Explorer, and drag the krita_4.0-prealpha_angle_ink-1-x64 folder to your desktop
- Open the second zipfile in Windows Explorer and drag the bin, lib and share folders into the krita_4.0-prealpha_angle_ink-1-x64 folder on your desktop.
- With Windows Explorer, navigate into the krita_4.0-prealpha_angle_ink-1-x64 folder on your desktop
- Start Krita by double-clicking on the krita link or on the bin\\krita.exe file
- Press either Test Desktop OpenGL or Test ANGLE when you see the dialog discussed above: this does not matter
- Go to Settings/Configure Krita/Tablet and check the experimental pointer api/windows ink support checkbox:[![](/images/posts/2017/tablet_support.png)](/images/posts/2017/tablet_support.png)
- Close Krita and start Krita again
- Create a new document and draw with the default brush. Check whether pressure gives a variation in size and opacity. Note your findings in the survey: [https://goo.gl/forms/5TSCWNZvvjN5SVoq1](https://goo.gl/forms/5TSCWNZvvjN5SVoq1)

### Thanks!

Thanks for helping to test this important new features.

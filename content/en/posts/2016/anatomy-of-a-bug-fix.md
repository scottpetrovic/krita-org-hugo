---
title: "Anatomy of a bug fix"
date: "2016-06-03"
---

**Updated builds with the fix are here: [https://www.kickstarter.com/projects/krita/krita-2016-lets-make-text-and-vector-art-awesome/posts/1594853](https://www.kickstarter.com/projects/krita/krita-2016-lets-make-text-and-vector-art-awesome/posts/1594853)**!

People sometimes assume that free software developers are only interested in adding cool new features, getting their few pixels of screenspace fame, and don't care about fixing bugs. That's not true - otherwise we wouldn't have fixed about a thousand bugs in the past year (though it would be better if we hadn't created the bugs in the first place). But sometimes bug fixing is just fun: sherlocking through the code, trying to come up with a mental model of what might be going wrong, hacking the code, discovering that you were right. Heady stuff, everyone should try it some time! Just head over to bugzilla and pick yourself a [crash](https://bugs.kde.org/buglist.cgi?bug_severity=crash&bug_status=UNCONFIRMED&bug_status=CONFIRMED&bug_status=ASSIGNED&bug_status=REOPENED&list_id=1361297&product=krita&query_format=advanced) (crash bugs are among the easiest to fix).

But let's take a look at a particularly nasty bug, one that we couldn't fix for ages. Ever since Krita 2.9.6, we have received crash reports about Krita crashing when people were using drawing tablets. Not just any drawing tablets, but obscure tablets with names like Trust, Peritab, Adesso, Waltop, Aiptek, Genius -- and others. Not the tablets that we do support because the companies have donated test hardware to Krita, like Wacom, Yiynova and Huion.

Also, not tablets that are readily available: most of these brands only produce hardware for a short time, flog it to unsuspecting punters and disappear. I.e., we couldn't just go to the local computer shop and get one, or find one online and have it delivered. And since all these tablets have one thing in common, namely their _cheapness_, the users who bought them in all likelihood not all that flush, otherwise they would have bought a better tablet. So they couldn't afford to donate their tablet to the project.

A hardware related bug without hardware to test with, that's nearly impossible to fix. We had four "facts" to start with:

- The bug started appearing after Krita 2.9.6 -- unfortunately, that was when we rewrote a lot of the tablet support to allow Krita to work with tablets like the Surface Pro, and it was impossible to pinpoint which change was responsible for the crash.
- All these tablets show the same suspicious values when we were querying them for dimensions
- All these crashes happened after that query for the tablet dimensions
- All crashes happen on Windows only

Now, on Windows, you talk to tablets through something called the "[Wintab](http://www.wacomeng.com/windows/docs/Wintab_v140.htm)" API. The tablet manufacturer, or more likely, the manufacturer of the chip that that the tablet manufacturer uses, writes an implementation of this API in the form of a Wintab driver.

Wintab is ancient: it started out in the 16 bits Windows 3.0 times. It's gnarly, it's illogical, it's hoary. You can only have one wintab driver dll on your system, which means that you cannot, like on Linux plug in a Huion, test, plug in a Wacom test, plug in a Yiynova and test -- you need to install and uninstall the driver every time.

Anyway, last week we found a second-hand Trust tablet for sale. Since we've had at least six reports of crashes with just that particular brand, we got it. We installed a fresh Windows 10, installed the driver Trust fortunately still provides despite having discontinued its tablets, installed Krita, started Krita, brought pen to tablet and... Nothing happened. No crash, and Krita painted a shoddy, shakey, pressure sensitive line.

Dash it, 30 euros down the drain.

Next, we got an old Genius tablet and installed Windows 7. And bingo! A crash, and the same suspicious values in the tablet log. Now we're talking! Unfortunately, the crash happened right inside the "Genius" wintab driver. Either we're using the Wintab API wrong, or Genius implemented it wrong, but we cannot see the code. This is what Dmitry was looking at now:

[![Gibberish...](/images/posts/2016/disassembly-1024x576.png)](https://krita.org/wp-content/uploads/2016/06/disassembly.png) Gibberish...

But it gave the hint we needed. It _is_ a bug in the Wintab driver, and we are guessing that since all these drivers give us the same weird context information, they all share the same codebase, come from the same manufacturer in fact, and have the same bug.

It turned out that when we added support for the Surface Pro 3, which has an N-Trig pen, we needed a couple of workarounds for its weirder features. We wrote code that would query the wintab dll for the _name_ of the tablet, and if that was an N-Trig, we set the workaround flag:

UINT nameLength = m\_winTab32DLL.wTInfo(WTI\_DEVICES, DVC\_NAME, 0);
TCHAR\* dvcName = new TCHAR\[nameLength + 1\];
UINT returnLength = m\_winTab32DLL.wTInfo(WTI\_DEVICES, DVC\_NAME, dvcName);
Q\_ASSERT(nameLength == returnLength);
QString qDvcName = QString::fromWCharArray((const wchar\_t\*)dvcName);
// Name changed between older and newer Surface Pro 3 drivers
if (qDvcName == QString::fromLatin1("N-trig DuoSense device") ||
            qDvcName == QString::fromLatin1("Microsoft device")) {
    isSurfacePro3 = true;
}
delete\[\] dvcName;

Now follow me closely: the first line gets some info (wTInfo) from the wintab driver. It's a call and has three parameters: the first says we want info about devices, the second says we want a name, and third one is **0**. That is, zero. Null.  The second call is exactly the same, but passes something called dvcName, that is a pointer to a bit or memory where the wintab driver will write the name of the device. It's a number, significantly bigger than 0.  The Wintab API says that if you pass 0 (null) as the third parameter, the driver should return the length of what it will return if you would pass it the length. Follow me? If you ask for  the name with 0 for length, it tells you the length; if you ask for the name with the right length, it gives you the name.

See for yourself: [http://www.wacomeng.com/windows/docs/Wintab\_v140.htm#\_Toc275759816](http://www.wacomeng.com/windows/docs/Wintab_v140.htm#_Toc275759816)

You have to go through this hoop to set apart a chunk of memory big enough for Wintab to copy the tablet name in. Too short, and you get a crash: that's what happens when you write out of bounds. Too long, and you waste space, and besides, how can you know how long a tablet name could be?

Okay, there's one other way to crash, other than writing too much stuff in too small a chunk of memory. And that's trying to write to Very Special Memory Adress 0. That's zero, the first location in the memory of your computer. In fact, writing to location 0 (zero) is so extremely forbidden that programmers use it to flag, meaning "don't write here". A competent programmer will always check for 0 (zero) before writing to memory.

If you're still here, I'm sure you're getting _suspicious_ now.

Yes, you're right. The people who wrote the driver for the tablets that Trust, Genius, Adesso, Peritab, Aiptek and all their ilk repackaged, rebranded and resold were not competent. They did not check for zero; they blithely started writing the name of the tablet into the address provided.

And poof! Krita crashes, we get the bug reports -- because after all, it must be Krita's fault? The tablet works with Photoshop! Whereas it's entirely likely that the people who cobbled together the driver didn't even read the Wintab spec, but just fiddled with their driver until Photoshop more or less worked, before they called it a day and went to drown their sorrows in baijiu.

Enfin, we have now "fixed" the bug -- we provide 1024 characters of space for the driver to write the name of the tablet in, and hope for the best...

Note that this doesn't mean that your Trust, Genius or whatever tablet will work well and give satisfaction: these are still seriously badly put together products. After fixing the bug, we tried drawing with the Genius tablet and got weird, shaky lines. Then we tested with Photoshop, and after a while, saw the same weird shaky lines there. It almost looks as if the tablet driver developers didn't really care about their product and just returned some randomly rounded numbers for the pen position.

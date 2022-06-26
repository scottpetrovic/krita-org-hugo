---
title: "Krita 2.9.5.1 and Bug Week!"
date: "2015-06-19"
---

It's been a while since we made a new build of Krita... So, here's Krita 2.9.5.1! In all the hectics surrounding the Kickstarter campaign, we worked our tails off to add new features, improvements and fixes, and that caused considerable churn in the code. And that, in turn, meant that the 2.9.5.0 was a bit, well, dot zero! So here's a 2.9.5.1 with the following improvements:

## Features

- Implemented a composite RGB curve for Curves filter
- Adding a Fish Eye Vanishing Point assistant.
- Added concentric ellipse assistant.
- Have the Settings dialog's default button only set the defaults for the  currently selected settings page.
- Added memory configuration options, including the location of the temporary scratch files
- Add a profiler option: [https://userbase.kde.org/Krita/Manual/Preferences/Performance](https://userbase.kde.org/Krita/Manual/Preferences/Performance)
- Create a copy of a currently open image (wish 348256)
- Add a one way pressure sensor(in the sensors) (wish 344753 )
- Show memory consumption in the statusbar

## Fixed Bugs

- Only set the resolution using tiff tags if they exist, this caused issues with Krita saving JPEG files to .kra.
- BUG:349078 Fix trimming an image under Filter Layers
- BUG:324505,294122 Fix Adjustment layers composition
- Bug 349185 Fix explicitly showing the cursor when the Stabilizer is active
- Fix showing a floating message when switching MDI subwindows
- BUG:348533 Fixed a bug when the tools became disabled after new document creation
- BUG:331708,349108 Fix a crash when redoing actions
- BUG:348737 Fix copy/pasto: fade isn't speed
- BUG:345762 Mirror View now correctly remembers which subwindow is mirrored.
- BUG:349058 Fixed bug where rulers were only visible on the canvas that was active when the option was first toggled. Fixed similar bugs with Mirror View and Wrap Around Mode.
- BUG:331708 Fix a crash when trying to redo after canceling a stroke
- Fixes an issue where some config files may not be picked up by the config system.
- BUG:299555 Change cursor to "forbidden" when active layer is locked or can't be edited with the active tool.
- BUG:345564 Don't warn about image file being invalid after user cancels "Background Image (overrides color)" dialog while configuring Krita
- BUG: 348886:Don't scroll up the list while adding or removing resources to the bundle
- fix default presets for bristle engine, restoring scale value to 1
- fixed a small bug in wdglayerproperties.ui that made the color profile not show up properly in the layer properties dialog. Patch by Amadiro, thanks!
- BUG: 348507 Fix issue with import PDF dialog resolution
- BUG:347004 Filter preview button difficult to see state
- BUG:345754 Fixes perspective assistant lockup
- Remember current meta-data author.
- BUG:348726 Be more careful when 'smart' merging metadata
- BUG:348652 Correctly initialize the temporary swap file
- Fix loading PSD files saved in OpenCanvas

**Downloads**

- Linux:
    - Distributions are expected to create packages for their bleeding edge repositories.
    - Ubuntu and derivatives can use Krita Lime, as usual: [https://launchpad.net/~dimula73/+archive/ubuntu/krita](https://launchpad.net/%7Edimula73/+archive/ubuntu/krita).
    - OpenSUSE users can the KDE:Extra repo: [http://download.opensuse.org/repositories/KDE:/Extra/](http://download.opensuse.org/repositories/KDE:/Extra/) or Leinir’s OBS repositories which have Krita built with support for Vc (which makes painting faster):
        - [http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_13.1/](http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_13.1/)
        - [http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_13.2/](http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_13.2/)
        - [http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_Factory/](http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_Factory/)
- Windows and OSX
    - The [download page](https://krita.org/download/krita-desktop/ "Krita Desktop") has been updated, so check out the new builds.

**Bugs...**

Now, that's not to say that 2.9.5.1 is _perfect_... And the increased interest in Krita has also led to an increase in reported bugs! We've got about 315 open bugs now, which is a record!

In fact, we need help. We need help with what's called bug triage: checking which bugs are actually duplicates of each other and which bugs are actually reproducible and which bugs are more like wishes than bugs.

And then we need to do something about the bugs that are proper, valid and reproducible! So, we propose to have our first 2015 bug weekend. We'd like to invite everyone to install Krita 2.9.5.1 and go through some bugs in  the bug list and help us triage!

Here's the list of bugs that need urgent triaging:

[**Unconfirmed, reopened, need-info Krita Bugs**](https://bugs.kde.org/buglist.cgi?bug_severity=critical&bug_severity=grave&bug_severity=major&bug_severity=crash&bug_severity=normal&bug_severity=minor&query_format=advanced&product=krita&bug_status=UNCONFIRMED&bug_status=REOPENED&bug_status=NEEDSINFO)

Let's get this list to zero!

And of course, there are also bugs that are already confirmed, but might have duplicated in the list above:

[**Confirmed Krita Bugs**](https://bugs.kde.org/buglist.cgi?bug_status=CONFIRMED&bug_status=ASSIGNED&bug_severity=critical&bug_severity=grave&bug_severity=major&bug_severity=crash&bug_severity=normal&bug_severity=minor&query_format=advanced&product=krita)

We're not looking for new bugs -- but if you find one, take a moment to read Dmitry's guide on [bug reporting](https://community.kde.org/Krita/docs/Bug_Writing_Guidelines).

Here's the [Bug Hunter Howto](https://community.kde.org/Krita/Docs/Bug_Hunting_Day#Developers), too. Join us this weekend and help us get the bug count down and the bug list manageable! In the coming two weeks, the developers will be busy fixing bugs so we can have a really stable base for all the kickstarter work!

[![Mosquitoes-hunter by David Revoy](/images/posts/2015/Mosquitoes-hunter_by_David-Revoy-238x300.jpg)](/images/posts/2015/Mosquitoes-hunter_by_David-Revoy.jpg) Bug hunter by David Revoy

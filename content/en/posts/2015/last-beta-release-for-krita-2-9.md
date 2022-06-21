---
title: "Last Beta release for Krita 2.9"
date: "2015-02-13"
---

We're getting so close to the release now! (Check the count-down counter on krita.org!) Sure, there are still a bunch of bugs to fix, but we're down to very nearly no release blockers now. And we fixed an awful lot of bugs since the last beta release, too!

The 2.9.0 release is scheduled for February 26th, with monthly bug fix releases planned until we release Krita 3.1.

Here's the fixes:

- New splash screen by Tyson Tan!
- Fix noisy complaints from libpng about nothing
- Hide the next/previous blending mode, snap-to-grid and reload-file actions because they don't work
- Fix the shortcuts for setting brush opacity
- Fix inverted softness (bug [342747](https://bugs.kde.org/show_bug.cgi?id=342747))
- Fix ghost pixels on group layers with no children (bug [331554](https://bugs.kde.org/show_bug.cgi?id=331554))
- Fix opacity setting for pattern fill layers
- G'Mic: Add progress reporting for small previews
- G'Mic: Cancel now stops execution of slow filters
- G'Mic: Don't crash when closing the G'Mic dialog after doing nothing
- G'Mic; fix url for updates
- Fix issues with Genius Tablets (bug [342641](https://bugs.kde.org/show_bug.cgi?id=342641))
- Fix painting on selection masks
- Make the palettes docker follow the general background color setting
- Add a temporary dialog to fix issues when the desktop resolution and the wintab resolution don't match up
- Fix crash when using the color transfer filter (bug [342287](https://bugs.kde.org/show_bug.cgi?id=342287))
- Fix KToolLine to handle end and cancel requests (bug [336959](https://bugs.kde.org/show_bug.cgi?id=336959))
- Fix a bunch of menu options to only be active at the right moment
- Add unit of measurement to offset image dialog
- Fix initialization of the crop tool (bug [342842](https://bugs.kde.org/show_bug.cgi?id=342842))
- Improve default values for the crop tool (bug [242844](https://bugs.kde.org/show_bug.cgi?id=242844))
- Fix crash in shaped gradient with shaped smaller than 3px wide (bug [342942](https://bugs.kde.org/show_bug.cgi?id=342942))
- Show open/save buttons in the ruler assistant tool on Windows (bug [342348](https://bugs.kde.org/show_bug.cgi?id=342348))
- Add auto-leveling to the adjust/levels filter (Aleksander Demko's first patch!)
- Don't push the Copy action on the undo stack (bug [343328](https://bugs.kde.org/show_bug.cgi?id=343328))
- Remember the constrain proportions settings in the canvas size dialog (bug [343282](https://bugs.kde.org/show_bug.cgi?id=343282))
- Fix spacing of rotating brushes (bug [329026](https://bugs.kde.org/show_bug.cgi?id=329026))
- Fix crash when selecting the texture option for the pixel brush engine (bug [342749](https://bugs.kde.org/show_bug.cgi?id=342749))
- Make the "on hover" layer thumbnail configurable (bug [342168](https://bugs.kde.org/show_bug.cgi?id=342168))
- Fix an issue where you'd have to press cancel multiple times to close Krita (bug [343070](https://bugs.kde.org/show_bug.cgi?id=343070))
- Notify the user when copying an empty selection (bug [343092](https://bugs.kde.org/show_bug.cgi?id=343092))
- Expand the color picker tool to be able to use a radius up to 900 pixels (bug [337406](https://bugs.kde.org/show_bug.cgi?id=337406))
- Don't crash if Krita's settings has an active preset that no longer exists (bug [340229](https://bugs.kde.org/show_bug.cgi?id=340229))
- Don't crash when closing Krita while the reference image docker is still loading thumbnails (bug [342896](https://bugs.kde.org/show_bug.cgi?id=342896))
- Switch to an appropriate tool when switching between pixel and vector layers (bug [335092](https://bugs.kde.org/show_bug.cgi?id=335092))
- Support indirect painting mode for masks (bug [318882](https://bugs.kde.org/show_bug.cgi?id=318882))
- Don't crash when merging selected layers (bug [343540](https://bugs.kde.org/show_bug.cgi?id=343540))
- Bring back the undo docker's preview thumbnails (bug [277884](https://bugs.kde.org/show_bug.cgi?id=277884))
- Don't crash when undoing points in polyline stroke or selection (bug [342921](https://bugs.kde.org/show_bug.cgi?id=342921))
- Make shift-z undo points in all poly tools (bug [342921](https://bugs.kde.org/show_bug.cgi?id=342921))
- Make the shortcut for undoing poly tool points configurable (bug [342919](https://bugs.kde.org/show_bug.cgi?id=342919))
- Disable the arrow keys for panning the canvas by default (bug [342023](https://bugs.kde.org/show_bug.cgi?id=342023))
- Update the minimum zoom level after scaling the image (bug [342709](https://bugs.kde.org/show_bug.cgi?id=342709))
- Rearrange the settings menu to be more logical (bug [342068](https://bugs.kde.org/show_bug.cgi?id=342068))
- Only lock the tools if the layer is invisible, but allow moving and deleting of invisible layers (bug [337912](https://bugs.kde.org/show_bug.cgi?id=337912))
- Fix issues when working with the color selectors in HDR mode (bug [343531](https://bugs.kde.org/show_bug.cgi?id=343531))
- Don't save the crop tool's force ratio setting (bug [343287](https://bugs.kde.org/show_bug.cgi?id=343287))
- Fix cyclic updates of the currently selected color (bug [343531](https://bugs.kde.org/show_bug.cgi?id=343531))
- G'Mic: Don't crash when enabling the small preview in interactive colorize (bug [343616](https://bugs.kde.org/show_bug.cgi?id=343616))
- Fix a crash on loading an image (bug [340752](https://bugs.kde.org/show_bug.cgi?id=340752))
- G'Mic: increase the stack size to ridiculous proportions on Windows so the parser doesn't crash
- G'Mic: start supporting interactive colorize on Windows (still not done, needs adding support for pthreads)
- Follow the settings for visibillity of the scrollbars (bug [342217](https://bugs.kde.org/show_bug.cgi?id=342217))
- Fix shaped gradients for selections with holes (bug [343187](https://bugs.kde.org/show_bug.cgi?id=343187))
- Fix floodfill for 16 bits integer/channel RGB images (bug [343365](https://bugs.kde.org/show_bug.cgi?id=343365))
- Fix the zoom level of the scratchpad
- Fix a big slowdown in the layer properties dialog with big layers and big images (bug [343685](https://bugs.kde.org/show_bug.cgi?id=343685))
- Fix file layer position resetting
- Add the recent documents to the list in the new images dialog (bug [340949](https://bugs.kde.org/show_bug.cgi?id=340949))
- Fix support for Wacom Airbrush devices. Patch by Arturg. (bug [343545](https://bugs.kde.org/show_bug.cgi?id=343545))
- Make the text brush load and display values from the current brush
- Fix the text brush when rotation is set to drawing angle (bug [330185](https://bugs.kde.org/show_bug.cgi?id=330185))
- Fix recognizing the bamboo stylus (bug [343545](https://bugs.kde.org/show_bug.cgi?id=343545))
- Don't deadlock when loading a fill layer (bug [343734](https://bugs.kde.org/show_bug.cgi?id=343734))
- Don't assert when checking the texture option (bug [343837](https://bugs.kde.org/show_bug.cgi?id=343837))
- Make it possible again to select an image in the color transfer filter on Windows (bug [343706](https://bugs.kde.org/show_bug.cgi?id=343706))
- G'Mic: fix a crash when browsing through the filters
- Update the layer thumbnails in the layerbox after every stroke, instead of when hovering over the layerbox (bug [343699](https://bugs.kde.org/show_bug.cgi?id=343699))
- Fix a crash when applying changes with the style manager.
- Fix crash when using drop caps in the multiline text object (bug [342185](https://bugs.kde.org/show_bug.cgi?id=342185))
- Remove inline objects from manager when Delete command is executed. (bug [303492](https://bugs.kde.org/show_bug.cgi?id=303492))
- Make text flowing around shapes with shadow. (bug [335784](https://bugs.kde.org/show_bug.cgi?id=335784))
- SVG file was wrongly placed. (bug [322377](https://bugs.kde.org/show_bug.cgi?id=322377))
- File dialogs: Fix all-supported formats on Gnome and Windows.
- File dialogs: Restore the All Formats option on Gnome and Windows.

**Downloads**

There are still [157 bugs](https://bugs.kde.org/buglist.cgi?bug_severity=critical&bug_severity=grave&bug_severity=major&bug_severity=crash&bug_severity=normal&bug_severity=minor&bug_status=UNCONFIRMED&bug_status=CONFIRMED&bug_status=ASSIGNED&bug_status=REOPENED&list_id=1167792&product=krita&query_format=advanced) at the moment, but quite a lot are rather minor. We fixed nearly 200 bugs. Lots and lots and lots of thanks to all the beta testers who have been sending in report after report: we got over 100 new reports, too!

For Linux users, [Krita Lime](https://launchpad.net/%7Edimula73/+archive/ubuntu/krita) has been updated. Remember that launchpad is very strict about the versions of Ubuntu it supports. So the update is only available for 14.04 and up.

OpenSUSE users can use the new OBS repositories created by Leinir:

- [http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE\_13.1/](http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_13.1/)
- [http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE\_13.2/](http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_13.2/)
- [http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE\_Factory/](http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_Factory/)

Windows users can choose between an installer and the zip file. You can unzip the zip file anywhere and start Krita by executing bin/krita.exe. The Surface Pro 3 tablet offset issue has been fixed! We only have 64 bits Windows builds at the moment, we’re working on fixing a problem with the 32 bits build.

- [http://files.kde.org/krita/windows/krita\_x64\_2.8.93.0.zip](http://files.kde.org/krita/windows/krita_x64_2.8.93.0.zip)
- [http://files.kde.org/krita/windows/krita\_x64\_2.8.93.0.msi](http://files.kde.org/krita/windows/krita_x64_2.8.93.0.msi)

Right now, we're trying to fix a bug in the OSX builds were icons aren't loaded, so we don't have OSX builds for Beta 3 yet.

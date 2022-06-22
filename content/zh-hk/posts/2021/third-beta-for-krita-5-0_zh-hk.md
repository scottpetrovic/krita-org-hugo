---
title: "發佈 Krita 5.0 嘅第三個測試版本 (Beta 3)"
date: "2021-12-01"
categories: 
  - "development-builds_zh-hk"
---

今日，我哋推出咗 Krita 5 嘅第三個 Beta 測試版本。比起 Beta 2 今次又有更多嘅修正事項。我哋們希望喺聖誕節之前可以正式推出 Krita 5，而我哋抱有信心可以達成依個目標。

（順帶一提，就喺啱啱推出 Beta 3 冇耐之後，「Krita Plus」測試版本已經多咗幾項修正……）

[![](/images/posts/2021/electrichearts_20201224A_kiki_c1_1080P-1024x512.png)](https://krita.org/wp-content/uploads/2021/08/electrichearts_20201224A_kiki_c1_1080P.png) 由 Tyson Tan 繪畫創作嘅新版啟動畫面圖片

![](/images/posts/2021/2021-11-16_kiki-piggy-bank_krita5.png) Krita 係自由、免費同開源嘅專案。請考慮[向 Krita 發展基金捐款](https://fund.krita.org)或者[購買教學影片](https://krita.org/en/shop/)支持我哋啦！有你哋嘅支持，我哋先可以俾核心開發者全職為 Krita 工作。

以下係推出咗 Beta 2 之後最值得留意嘅新修正事項： （譯者按：由於內容太多而人力資源有限，因此依段唔做完整嘅翻譯，保留返英文原文。）

- Resources can no longer be assigned the speciall All and All Untagged tags. [BUG:446148](https://bugs.kde.org/show_bug.cgi?id=446148)
- Alpha-mask PNG brush tips work correctly again. [BUG:445691](https://bugs.kde.org/show_bug.cgi?id=445691)
- Android: creating a 16 bits integer image no longer crashes. [BUG:445179](https://bugs.kde.org/show_bug.cgi?id=445179)
- Thumbnail for MYB mypaint brushes in a bundle now are loaded.
- Fix a performance issue in the magnetic selection tool.
- The recorder no longer goes in an infinite loop if the selected colorspace is not supported by the recorder.
- Drag and drop of remote images and copy/paste of images from Chrome is fixed. [BUG:446029](https://bugs.kde.org/show_bug.cgi?id=446029)
- Cancelling pasting is fixed. [BUG:438426](https://bugs.kde.org/show_bug.cgi?id=438426)
- Tyson Tan provided many disambiguations for user-visible text, which helps improve translations.
- A crash that happened when opening the popup palette, closing the image then creating a new image was fixed. [BUG:443402](https://bugs.kde.org/show_bug.cgi?id=443402)
- Paste at Cursor now positions the clip correctly. [BUG:446120](https://bugs.kde.org/show_bug.cgi?id=446120)
- The outline of brushes with a non-standard number of spikes is now correct. [BUG:445927](https://bugs.kde.org/show_bug.cgi?id=445927)
- Disable subpixel translation in the transform tool. [BUG:445714](https://bugs.kde.org/show_bug.cgi?id=445714)
- Fix saving palette on quitting Krita. [BUG:444309](https://bugs.kde.org/show_bug.cgi?id=444309)
- Fix deduplication of resources on import. [BUG:445367](https://bugs.kde.org/show_bug.cgi?id=445367)
- A crash when using the text brush was fixed. [BUG:443308](https://bugs.kde.org/show_bug.cgi?id=443308)
- The handling of pattern files of types other than gimp patterns was fixed. [BUG:443151](https://bugs.kde.org/show_bug.cgi?id=443151)
- Resource libraries are now sorted in alphabetical order in the bundle manager. Patch by Reinold Rojas.
- Handling of really broken .kra files was improved. [BUG:443559](https://bugs.kde.org/show_bug.cgi?id=443559)
- Performance of textured brushes was improved.
- Renaming brush presets and SeExpr presets was fixed. [BUG:445048](https://bugs.kde.org/show_bug.cgi?id=445048)
- Fix saving MyPaint brush presets after modification. [BUG:445281](https://bugs.kde.org/show_bug.cgi?id=445281), [BUG:445282](https://bugs.kde.org/show_bug.cgi?id=445282)
- Improve the stylinmg of the tagging widget. [BUG:445625](https://bugs.kde.org/show_bug.cgi?id=445625)
- Fix a crash when trying to add or move layers too quickly. [BUG:445831](https://bugs.kde.org/show_bug.cgi?id=445831), [BUG:444516](https://bugs.kde.org/show_bug.cgi?id=444516)
- Fix a crash in the transform tool. [BUG:441826](https://bugs.kde.org/show_bug.cgi?id=441826)
- Fix the text tool not updating the font size correctly.
- Fix the initialization of the random generator for non-brush tools. [BUG:445775](https://bugs.kde.org/show_bug.cgi?id=445775)
- Fix tilt rotation when the canvas is rotated and the stabilizer is active. [BUG:436618](https://bugs.kde.org/show_bug.cgi?id=436618)
- Make the mesh gradient respond to the first invocation. [BUG:445617](https://bugs.kde.org/show_bug.cgi?id=445617)
- Make mesh gradient handles consistent with the mesh transform tool handles. [BUG:442201](https://bugs.kde.org/show_bug.cgi?id=442201)
- Fix canceling saving an edited gradient.
- Fix loading palettes of types other than GPL and KPL.
- Fix an assert when opening an SVG document.
- Make it possible to actually change between different resource folder locations.
- Make it possible to overwrite existing workspace definitions. [BUG:444975](https://bugs.kde.org/show_bug.cgi?id=444975)
- Fix a crash when warning the user when there is a problem saving a resource. [BUG:445581](https://bugs.kde.org/show_bug.cgi?id=445581)
- Update the Intel GPU driver version detection.
- Fix artefacts in the freehand selection tool in polygonal mode. [BUG:441569](https://bugs.kde.org/show_bug.cgi?id=441565)
- Fix issues with layer styles not be able to retrieve resources such as patterns or gradients. [BUG:443621](https://bugs.kde.org/show_bug.cgi?id=443621)
- Blacklist line tool to make it work while recorder is active.
- Make the line tool's preview faster. [BUG:411768](https://bugs.kde.org/show_bug.cgi?id=411768)
- Fix the flickering in the line tool's preview.
- Make it possible to save mypaint brush presets to resource bundles.
- Fix issues creating a new image from the clipboard. [BUG:443111](https://bugs.kde.org/show_bug.cgi?id=443111)
- Do not select control handles when using the Edit Shapes Tool rectangular selection option. [BUG:434535](https://bugs.kde.org/show_bug.cgi?id=434535)
- Fix updates when undoing pasting multiple layers.
- Fix adding a new file layer.
- Fix issues with testing the speed sensor in the scratch pad. [BUG:425124](https://bugs.kde.org/show_bug.cgi?id=425124)
- Fix issues with retrieving the pattern in the pattern fill layer generator.
- Fix artefacts in the color smudge lightness mode.
- Improve font style selection, enabling the proper styles to be selected. [BUG:425312](https://bugs.kde.org/show_bug.cgi?id=425312)
- Report to the user when a bundle fails to save. [BUG:439110](https://bugs.kde.org/show_bug.cgi?id=439110)
- Improve importing bundles. [BUG:445336](https://bugs.kde.org/show_bug.cgi?id=445336)
- Improve handling layer styles.
- Remove the vertical shift-drag to resize the current brush feature. [BUG:442544](https://bugs.kde.org/show_bug.cgi?id=442544)
- Improve handling and editing palettes.
- Fix a crash in the freehand selection tool.
- Fix issues with embedding palettes and other resources in a .KRA document.
- Fix a crash when working with gamut masks.
- Animation: fix caching bug when scrubbing from cached to uncached frame. [BUG:445265](https://bugs.kde.org/show_bug.cgi?id=445265)
- Fix some crashes when Krita is built with optional dependencies missing. [BUG:445276](https://bugs.kde.org/show_bug.cgi?id=445276)
- On database creation, add tags only after all storages have been added, so all resources that can be tagged by default are tagged.
- In the scale and resize image dialogs, set the focus on the first field instead of the OK button. [BUG:445250](https://bugs.kde.org/show_bug.cgi?id=445250), [BUG:444806](https://bugs.kde.org/show_bug.cgi?id=444806)
- Android: write document state info in mdiArea title.
- Fix issues creating, saving and updating SeExpr scripts.
- Fix issues creating, saving and updating workspaces. [BUG:444980](https://bugs.kde.org/show_bug.cgi?id=444980)
- Android: Fix crash in file handling on Android 11.
- Fix a crash when exporting an image with EXIV data. [BUG:444256](https://bugs.kde.org/show_bug.cgi?id=444256)
- Android: fix problems with the Android Back Button.
- Fix a crash when selecting a new color after a document has been closed. [BUG:444308](https://bugs.kde.org/show_bug.cgi?id=444308)
- Android: Fix closing the popup palette with a keyboard shortcut. [BUG:443631](https://bugs.kde.org/show_bug.cgi?id=443631)
- Improve color drag & drop on the canvas
- Fix update issues in KoDualColorButton. [BUG:442861](https://bugs.kde.org/show_bug.cgi?id=442861)
- Fix a possible crash on closing a document. [BUG:444613](https://bugs.kde.org/show_bug.cgi?id=444613)
- Improve the welcome page.
- Improve the preset history docker so the correct row is selected. Patch by Mike Will.
- Fix exporting a recorder session.
- Improve discrete canvas rotation. Patch by Reinold Rojas. [BUG:429637](https://bugs.kde.org/show_bug.cgi?id=429637)
- Animation: Improve the usability of navigating keyframes. [BUG:444310](https://bugs.kde.org/show_bug.cgi?id=444310)
- Animation: Fix a Windows-specific issue with the autokey blank causing artefacts. [BUG:441588](https://bugs.kde.org/show_bug.cgi?id=441588)
- Refine tablet right click popup palette behavior. [BUG:441899](https://bugs.kde.org/show_bug.cgi?id=441899)
- Fix saving the current session to the right location. [BUG:443652](https://bugs.kde.org/show_bug.cgi?id=443652)
- Fix the translation context of the layer group menu. [BUG:444238](https://bugs.kde.org/show_bug.cgi?id=444238)
- Make it possible to select and deselect ABR files in the brush tip tab of the preset editor.
- Fix handling jpeg2000 images.
- Fix a problem where editing text makes the color selector select the wrong color. [BUG:443793](https://bugs.kde.org/show_bug.cgi?id=443793)
- Android: fix hiding the popup palette when using Samsung Air Actions. [BUG:443600](https://bugs.kde.org/show_bug.cgi?id=443600)
- Make Krita 5 and Krita 4 session files compatible.
- Android: fix a memory leak in the Android Window Manager.
- Do not make the toolbars immovable after configuring a toolbar. [BUG:441808](https://bugs.kde.org/show_bug.cgi?id=441808)
- Change Lod in Move Tool to 'true' by default.
- Set Crop Tool to have Grow checked by default.
- Change autosave to be every 7 minutes.
- Change the default DPI when importing a PDF to 300.
- Make the layer docker narrower.
- Update SeExpr with upstream patches.
- OpenGL: support LoD on OpenGL ES 2.
- ANGLE: support 10 and 12-bit HDR.
- OpenGL ES: support float and half textures.
- OpenColorIO: use Natron's workaround for parsing LUTs on localized systems. [BUG:407921](https://bugs.kde.org/show_bug.cgi?id=407921)
- OpenColorIO: support VFX Platform CY2021 and newer. [BUG:435474](https://bugs.kde.org/show_bug.cgi?id=435474)
- Improve the SeExpr user interface and parser.
- Halve the minimum width of recorder's status bar item.
- Fixed default scrollwheel behavior on timeline to be consistent. [BUG:443852](https://bugs.kde.org/show_bug.cgi?id=443852)
- StoryboardDocker: Added more protection from duplicate names in storyboard docker.
- The storyboard export functionality has been improved.
- Fix crash during animation export. [BUG:442578](https://bugs.kde.org/show_bug.cgi?id=442578)
- Fix updates of the brush editor when the preset is chagned externally. [BUG:443579](https://bugs.kde.org/show_bug.cgi?id=443579)
- Fix the textured smudge brush causing square artifacts when drawing on a transparency mask. [BUG:](https://bugs.kde.org/show_bug.cgi?id=443422)443422
- Fix performance issues with textured brushes.

我哋會繼續修正大家喺試用 Beta 同埋 Nightly 測試版本時發現嘅各種問題，以盡力令 Krita 5 正式版發佈嘅時候可以穩定及暢順咁運作。請考慮向 [Krita 發展基金](https://fund.krita.org/)捐款以支持 Krita 嘅開發工作：

[![](/images/posts/2021/devfund-1024x346.png)](https://fund.krita.org)

## 下載

### Windows

如果你使用免安裝版：請注意，免安裝版仍然會同安裝版本共用設定檔同埋資源。如果想用免安裝版測試並回報 crash 嘅問題，請同時下載 debug symbols。

注意：我哋依家唔再提供為 32 位元 Windows 建置嘅版本。

- 64 位元安裝程式：[krita-x64-5.0.0-beta3-setup.exe](https://download.kde.org/unstable/krita/5.0.0-beta3/krita-x64-5.0.0-beta3-setup.exe)
- 64 位元免安裝版：[krita-x64-5.0.0-beta3.zip](https://download.kde.org/unstable/krita/5.0.0-beta3/krita-x64-5.0.0-beta3.zip)
- [Debug symbols（請解壓到 Krita 程式資料夾入面）](https://download.kde.org/unstable/krita/5.0.0-beta3/krita-x64-5.0.0-beta3-dbg.zip)

### Linux

- 64 位元 Linux AppImage：[krita-5.0.0-beta3-x86\_64.appimage](https://download.kde.org/unstable/krita/5.0.0-beta3/krita-5.0.0-beta3-x86_64.appimage)

Linux 版本唔使再另外下載 G'Mic-Qt 外掛程式 AppImage。

### macOS

遺憾地，依個版本嘅 macOS 套件出現咗問題，因此唔可以提供下載。我哋現正處理緊相關嘅問題。

### Android

我哋提供嘅 ChomeOS 同 Android 版本仲係**測試版本**。依個版本或可能含有大量嘅 bug，而且仲有部份功能未能正常運作。由於使用者介面仲未改進好，軟件或者須要配合實體鍵盤先可以用到全部功能。

- [64 位元 Intel CPU APK](https://download.kde.org/unstable/krita/5.0.0-beta3/krita-x86_64-5.0.0-beta3-release-signed.apk)
- [32 位元 Intel CPU APK](https://download.kde.org/unstable/krita/5.0.0-beta3/krita-x86-5.0.0-beta3-release-signed.apk)
- [64 位元 Arm CPU APK](https://download.kde.org/unstable/krita/5.0.0-beta3/krita-arm64-v8a-5.0.0-beta3-release-signed.apk)
- [32 位元 Arm CPU APK](https://download.kde.org/unstable/krita/5.0.0-beta3/krita-armeabi-v7a-5.0.0-beta3-release-signed.apk)

### 原始碼

- [krita-5.0.0-beta3.tar.gz](https://download.kde.org/unstable/krita/5.0.0-beta3/krita-5.0.0-beta3.tar.gz)
- [krita-5.0.0-beta3.tar.xz](https://download.kde.org/unstable/krita/5.0.0-beta3/krita-5.0.0-beta3.tar.xz)

### md5sum

下載檔案嘅 MD5 校對碼可以喺依個檔案入面搵到：

- [md5sum.txt](https://download.kde.org/unstable/krita/5.0.0-beta3/md5sum.txt)

### 數碼簽署

Linux AppImage 以及原始碼嘅 .tar.gz 同 .tar.xz 壓縮檔已使用數碼簽署簽名。你可以由[依度](https://files.kde.org/krita/4DA79EDA231C852B)取得 public key。簽名檔可以喺[依度](https://download.kde.org/unstable/krita/5.0.0-beta3/)搵到（副檔名為 .sig）。

## 支持 Krita

Krita 係自由、免費同開源嘅專案。請考慮[向 Krita 發展基金捐款](https://fund.krita.org)或者[購買教學影片](https://krita.org/en/shop/)支持我哋啦！有你哋嘅支持，我哋先可以俾核心開發者全職為 Krita 工作。

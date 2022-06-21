---
title: "正式發佈 Krita 4.4.5 新版本"
date: "2021-06-09"
categories: 
  - "news_zh-tw"
  - "officialrelease_zh-tw"
---

是次將會是 Krita 5.0 發佈前的最後一個 4.4 修正版本。我們修正了一個在 macOS 運行下的重大問題，而我們希望 macOS 使用者也能獲得最新的修正，因此決定多發佈一個更新。

這次更新也為大家帶來了一些正體中文介面本地化的改進。

## 更新修正

（譯者按：由於內容眾多而人力資源有限，故此段落不作完整翻譯，保留英文原文。）

- Set ElideRight for the tabs in the mdiarea. ([Bug 433640](https://bugs.kde.org/show_bug.cgi?id=433640))
- If loading the image fails too often, stop retrying ([Bug 433652](https://bugs.kde.org/show_bug.cgi?id=433652))
- Use QVersionNumber to compare versions
- Fix oilpaint filter's tiling artifacts [commit](https://invent.kde.org/graphics/krita/-/commit/d08414a8e9017d98e969c5b6e9c4b68b2f973d65)
- Only open the bug dialog when Krita is in alpha or beta
- Fix crash on popup palette on 125% scale ([Bug 431944](https://bugs.kde.org/show_bug.cgi?id=431944))
- Fix compilation for GCC11. Thanks Jonathan Wakely for the suggested fix! ([Bug 434150](https://bugs.kde.org/show_bug.cgi?id=434150))
- Use opengl ES on Arm Linux ([Bug 421136](https://bugs.kde.org/show_bug.cgi?id=421136))
- Fix crash on importing a broken icc profile ([Bug 434273](https://bugs.kde.org/show_bug.cgi?id=434273))
- Remove the hello world demo plugin ([Bug 422380](https://bugs.kde.org/show_bug.cgi?id=422380))
- Bugfix: Crash with crop tool ([Bug 433770](https://bugs.kde.org/show_bug.cgi?id=433770))
- Bugfix: Transform (Shear) tool doesn't use pivot ([Bug 427462](https://bugs.kde.org/show_bug.cgi?id=427462))
- Fix angle range in the angle selector in status bar and overview docker ([Bug 434993](https://bugs.kde.org/show_bug.cgi?id=434993))
- Implement "Scale handles proportionally" feature for the mesh transform
- Bugfix: Crop tool doesn't respond to some events ([Bug 435201](https://bugs.kde.org/show_bug.cgi?id=435201))
- Remove JPG from the list of supported clipboard image formats ([Bug 431310](https://bugs.kde.org/show_bug.cgi?id=431310))
- Don't set the menu text on the action if it's empty ([Bug 437036](https://bugs.kde.org/show_bug.cgi?id=437036))
- Expose the node's unique id to libkis [commit](https://invent.kde.org/graphics/krita/-/commit/57f0af27d358e21ffdaf8af5a38a196df1565dcf)
- Fix quicklook generator ([Bug 436224](https://bugs.kde.org/show_bug.cgi?id=436224))
- Fix random crashes on macOS and fix cursor getting stuck after switching to other apps using cmd+tab and returning to krita using mouse click. ([Bug 434646](https://bugs.kde.org/show_bug.cgi?id=434646))
- Fix data corruption on pressing Ctrl+Z while crop action is active (CC[Bug 433770](https://bugs.kde.org/show_bug.cgi?id=433770))
- Fix zooming of the palette in Lazy Fill Tool ([Bug 410997](https://bugs.kde.org/show_bug.cgi?id=410997))
- Fix outline-selection precision when shift-modifier is pressed ([Bug 437048](https://bugs.kde.org/show_bug.cgi?id=437048))
- Fix crash when closing Krita too quickly while some stroke is still rendering ([Bug 419021](https://bugs.kde.org/show_bug.cgi?id=419021))
- Fix incorrect memory access in KisCanvas2::setProofingOptions()
- Fix a race condition when starting spontaneous jobs ([Bug 434648](https://bugs.kde.org/show_bug.cgi?id=434648))
- Fix display color management in Overview docker ([Bug 428605](https://bugs.kde.org/show_bug.cgi?id=428605))
- Fix Nearest Neighbour filter of the perspective transform mode ([Bug 420811](https://bugs.kde.org/show_bug.cgi?id=420811))
- Fix drift of the transformed image when moving mouse too quickly ([Bug 416899](https://bugs.kde.org/show_bug.cgi?id=416899))
- Fix smoothness of Free Transform mode ([Bug 416899](https://bugs.kde.org/show_bug.cgi?id=416899))
- Fix input method not working on popup widgets ([Bug 395598](https://bugs.kde.org/show_bug.cgi?id=395598))
- Fix export in Krita using CLI [commit](https://invent.kde.org/graphics/krita/-/commit/38b9dfa668494c03a9d11b16e3f619ff3c4f27a8)
- Fix OpenColorIO include dir detection [commit](https://invent.kde.org/graphics/krita/-/commit/1c55fefecb85366feee7d101a343f31d3cfb8e5d)
- Fix order of arguments in OverviewThumbnailStrokeStrategy (CID 310957)
- Do not rely on endianness in psd\_image\_data (CID 35080)
- Widen variables before making calculations (CID 248925)
- 0verride patchWidth and patchHeight being 0 with defaults (CID 248441, CID 248622)
- Check value after dynamic cast in ConvertColorSpacePr.Vis. (CID 304985)
- Properly bound values on conversions (CID 248629, CID 248458)
- Initialize propertyType in KisMetaData::TypeInfo::Private (CID 35498)
- Initialize variables in KoRuler and KisFullRefreshWalker (CID 35523, CID 35612)
- Initialize members of KisImagePyramid (CID 36041)
- Initialize members of DlgOffsetImage and DeformBrush (CID 36144, CID 36265)
- Initialize members in KCanvasPreview (CID 36395)
- Initialize members in DlgClonesArray (CID 248509)
- Initialize members in KisShadeSelectorLine (CID 36338)
- Initialize members of assistant classes (CID 248502, CID 248916)
- Initialize members in spin box related classes (CID 248555, CID 248871)
- Fix xyYtoXYZ color conversion formula
- Make the code in the triangle color selector cleaner [commit](https://invent.kde.org/graphics/krita/-/commit/789edc1cf4fe7c2c885368337788c9db7e22d1c6)
- Fix updates in Channels docker [commit](https://invent.kde.org/graphics/krita/-/commit/cb81820599f35ffae4c4e41ce8039829ffec37d7)
- Fix updates in Histogram docker [commit](https://invent.kde.org/graphics/krita/-/commit/6ddf4a12db10510715b177e71768ea176b6327a2)
- Fix multithreading in Histogram widget [commit](https://invent.kde.org/graphics/krita/-/commit/04d8cf6c586877e76c174aff445fb726962a4984)
- Change typedef to using in HistogramDockerWidget [commit](https://invent.kde.org/graphics/krita/-/commit/4cfcf5e967a195af07c4f4c238183a147d513899)
- Fix referencing of null value in SvgStyleWriter(CID 329512)
- Fix uninitialized values in HistogramDockerWidget (CID 329509)
- Fix High DPI for canvas previews in Undo History docker [commit](https://invent.kde.org/graphics/krita/-/commit/7bfca14742ba2b99c42c33ef3978be1fb7fb868f)
- Fix crash on saving a huge image to .kra ([Bug 432182](https://bugs.kde.org/show_bug.cgi?id=432182))
- Ensure that transform worker won't try to scale to 0 ([Bug 432182](https://bugs.kde.org/show_bug.cgi?id=432182))
- Fix KoQuaZipStore error checking [commit](https://invent.kde.org/graphics/krita/-/commit/80f43d1ce4bb1305731cffc192c4e9907a88b986)
- Show country in language list for disambiguation ([Bug 437994](https://bugs.kde.org/show_bug.cgi?id=437994))
- Fix failing update when transforming a shape layer with a Transform Tool ([Bug 437886](https://bugs.kde.org/show_bug.cgi?id=437886))
- Do not append country name to zh\_CN and zh\_TW ([Bug 437994](https://bugs.kde.org/show_bug.cgi?id=437994))
- Revert "Fix OpenColorIO include dir detection"
- Add more checks on saving to kra [commit](https://invent.kde.org/graphics/krita/-/commit/d47163e4f7e99d790be7905b79b2ca94ef8ef675)
- Fix non-float results in expressions for float values (CID 329390, CID 329448, CID 329482)
- Fix uninitialized values in various classes (CID 329508, CID 329504, CID 329503, CID 329502, CID 329501)
- Don't assert on invalid 0-bytes palettes [commit](https://invent.kde.org/graphics/krita/-/commit/876d61fc8d2b0a3f76277a814ccc9f595f063c7d)
- Initialize members of SVG Symbols classes (CID 304987)
- Initialize members of KisColorSelector classes (CID 36349, CID 248848, CID 248452, CID 248707)
- Android: Make saving operation on exit more robust [commit](https://invent.kde.org/graphics/krita/-/commit/f248c032199be64e9ac4e172155434d793fdd212)
- Bugfix: Artifact with more than one active assitant ([Bug 401940](https://bugs.kde.org/show_bug.cgi?id=401940))
- Android: SAFE\_ASSERT on TouchCancel event [commit](https://invent.kde.org/graphics/krita/-/commit/adebed6735b94bbcd7945aeace304975f43e5667)
- Android: Layer Properties' text field not responding to keyboard events
- Android: Fix Window Manager position when rotating
- Bugfix: Inconsistent stroke fill and shape fill ([Bug 399127](https://bugs.kde.org/show_bug.cgi?id=399127), [Bug 422204](https://bugs.kde.org/show_bug.cgi?id=422204), [Bug 434828](https://bugs.kde.org/show_bug.cgi?id=434828))

## 下載

正式發佈版本跳過了版本編號 4.4.4，因為 Krita 4.4.4 是為 Epic Store 臨時發佈所準備的版本。

### Windows

如果你使用免安裝版：請注意，免安裝版仍然會與安裝版本共用設定檔及資源。如希望以免安裝版測試並回報程式強制終止的問題，請同時下載偵錯符號 (debug symbols)。

注意：由這個版本起，我們不再提供為 32 位元 Windows 建置的版本。

- 64 位元安裝程式：[krita-x64-4.4.5-setup.exe](https://download.kde.org/stable/krita/4.4.5/krita-x64-4.4.5-setup.exe)
- 64 位元免安裝版：[krita-x64-4.4.5.zip](https://download.kde.org/stable/krita/4.4.5/krita-x64-4.4.5.zip)
- [偵錯符號（請解壓到 Krita 程式資料夾之中）](https://download.kde.org/stable/krita/4.4.5/krita-x64-4.4.5-dbg.zip)

### Linux

- 64 位元 Linux AppImage：[krita-4.4.5-x86\_64.appimage](https://download.kde.org/stable/krita/4.4.5/krita-4.4.5-x86_64.appimage)
- 64 位元 Linux [G'Mic-Qt 外掛程式 AppImage](https://download.kde.org/stable/krita/4.4.5/gmic_krita_qt-x86_64.appimage)

### macOS

- macOS 套件：[krita-4.4.5.dmg](https://download.kde.org/stable/krita/4.4.5/krita-4.4.5.dmg)

備註：gmic-qt 未支援 macOS。

### Android

我們仍視 ChomeOS 及 Android 的版本為**測試版本**。此版本或可能含有大量程式錯誤，而且仍有部份功能未能正常運作。由於使用者介面並未完善，軟體或須配合實體鍵盤才能使用全部功能。

除了由以下連結下載 APK 安裝檔，你亦可以經由 [Google Play](https://play.google.com/store/apps/details?id=org.krita) 安裝 Krita 4.4.5。

- [64 位元 Intel CPU APK](https://download.kde.org/stable/krita/4.4.5/krita-x86_64-4.4.5-release.apk)
- [32 位元 Intel CPU APK](https://download.kde.org/stable/krita/4.4.5/krita-x86-4.4.5-release.apk)
- [64 位元 Arm CPU APK](https://download.kde.org/stable/krita/4.4.5/krita-arm64-v8a-4.4.5-release.apk)
- [32 位元 Arm CPU APK](https://download.kde.org/stable/krita/4.4.5/krita-armeabi-v7a-4.4.5-release.apk)

### 原始碼

- [krita-4.4.5.tar.gz](https://download.kde.org/stable/krita/4.4.5/krita-4.4.5.tar.gz)
- [krita-4.4.5.tar.xz](https://download.kde.org/stable/krita/4.4.5/krita-4.4.5.tar.xz)

### md5sum

下載檔案的 MD5 校對碼已於以下檔案中列出：

- [md5sum.txt](https://download.kde.org/stable/krita/4.4.5/md5sum.txt)

### 數位簽章

Linux AppImage 以及原始碼的 .tar.gz 和 .tar.xz 壓縮檔已使用數位簽章簽名。你可以運行 "gpg --recv-key 7468332F" 以取得 GPG 公鑰。簽名檔可於[此處](https://download.kde.org/stable/krita/4.4.5/)找到（副檔名為 .sig）。

## 支持 Krita

Krita 是免費及開放原始碼的項目。請考慮[捐款](https://krita.org/en/support-us/donations/)或[購買教學影片](https://krita.org/en/shop/)支持我們吧！有你的支持我們才能聘請開發人員全職進行 Krita 的開發工作。

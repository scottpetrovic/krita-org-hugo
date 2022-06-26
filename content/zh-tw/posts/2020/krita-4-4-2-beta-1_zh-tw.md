---
title: "Krita 4.4.2 測試版本 (beta 1) 已推出"
date: "2020-12-09"
categories: 
  - "news_zh-tw"
  - "development-builds_zh-tw"
---

Krita 開發團隊現推出 Krita 4.4.2 的首個測試版本。此版本包含超過 300 項程式碼改動，主要為修正程式錯誤，不過同時也加入了一些重大的新功能！

請注意：此版本嘗試修正了[某些情況下組合快捷鍵失效的問題 (Modifier shortcut keys stop working)](https://bugs.kde.org/show_bug.cgi?id=424319)，不過這項修正並未被問題的回報者確定能達到預期效果。我們在此希望各位使用者可以協助我們細心測試一下。

## 新功能

### 網狀漸變

這項由 Sharaf Zaman 於 Google Summer of Code 展開的專案現已於此發佈版本正式成為 Krita 的新功能！這是繼 Inkscape 之後另一個獨立的 SVG 網狀漸變 (Mesh Gradient) 實作，並與 Inkscape 兼容。網狀漸變乃用於向量圖形。它可以產生出非常自然的效果：

[![網狀漸變](/images/posts/2020/Handles-meshgradient-1024x554.png "網狀漸變")](/images/posts/2020/Handles-meshgradient.png) 網狀漸變

### 網狀變形

[![網狀變形的用法](/images/posts/2020/krita_4_4_2_mesh_gradients.png "網狀變形的用法")](/images/posts/2020/krita_4_4_2_mesh_gradients.png) 網狀變形容許作出複雜的曲線變形效果，例如是圖中半圓凸出的窗框。此功能可以大幅提升製作概念藝術的效率。

網狀變形是在此版本加入的另一項新功能。與網狀漸變相似，這項功能同樣是使用貝茲曲線形成的網格，這些網格可以分別控制以產生準確的變形效果，尤其是對繪畫曲面物件非常有幫助。你還可以選擇顯示貝茲曲線的控制點，助你作出更精密的變形控制！

現時提供的快捷鍵如下，不過我們仍在調整中：

1. 網格節點： - 按下並拖曳 --- 移動節點
2. 邊緣節點： - 按下並拖曳 --- 移動節點 - Shift + 按下並拖曳 --- 移動整行或列 - Ctrl + Alt + 按下並拖曳 --- 分割或滑動行或列 - Ctrl + Alt + 按下並向外拖曳 --- 移除分割
3. 控制點： - 按下並拖曳 --- 對稱地修改兩邊控制點 - Shift + 按下並拖曳 --- 修改單邊控制點 此操作會使圖像出現明顯的角度變化，尤如摺痕一樣。
4. 節點或控制點： - Ctrl + 按一下 --- 選取多點
5. 網格內部範圍： - 按下並拖曳 --- 網格自由扭曲 - Shift + 按下並拖曳 --- 移動整個網格
6. 網格外部空白位置： - 按下並拖曳 --- 旋轉網格或已選取項目 - Ctrl + 按下並拖曳 --- 縮放網格或已選取項目 - Shift + 按下並拖曳 --- 平移網格或已選取項目

### 漸變填充圖層及新版漸變編輯工具

[![漸變填充圖層及新版漸變編輯工具](/images/posts/2020/krita_4_4_2_new_gradient_editor_and_fill_layer.png "漸變填充圖層及新版漸變編輯工具")](/images/posts/2020/krita_4_4_2_new_gradient_editor_and_fill_layer.png) 正在使用漸變填充圖層及新版漸變編輯工具。

這項由 Deif Lou 加入的漸變填充圖層讓你可以非常簡便地以非破壞性方式建立各種漸變效果。這項新功能同時亦帶來了一項易用性改進：Krita 中的漸變分為「停駐點漸變」和「分段漸變」兩種，過往各自有不同功能和編輯介面，現在兩者均可在同一個介面中編輯，而且兩者可以互相轉換。

### 改進半調濾鏡

Deif Lou 亦重寫了半調濾鏡。舊版的半調濾鏡運算速度緩慢，又不能作濾鏡遮罩使用，還只提供圓點狀網點。

[![經半調濾鏡處理的 Krita 啟動畫面](/images/posts/2020/krita_4_4_2_halftone_filter.png "經半調濾鏡處理的 Krita 啟動畫面")](/images/posts/2020/krita_4_4_2_halftone_filter.png) 新的半調濾鏡可以分別處理獨立色彩通道，可以用作產生懷舊效果，甚至用於印刷。

新的半調濾鏡可以用作濾鏡遮罩圖層，支援獨立色彩通道，而半調網點圖案亦可經由填充圖層產生，為創作帶來了無限可能。

### 更新 macOS 整合外掛程式

Amyspark 為 Krita 的 QuickLook 外掛程式加入了預覽縮圖功能（需要 macOS 10.15 或更新版本）以及支援在 Spotlight 顯示檔案屬性資訊。

### 新增「貼上圖形樣式」操作

這項功能讓你可以將在剪貼簿中的向量圖形的樣式套用到其他選取中的向量圖形。此操作可在「編輯」功能表中找到，或在「鍵盤快捷鍵」設定中指定快捷鍵。

### 新增「環繞模式」功具列圖示按鈕

Krita 曾經設定了鍵盤快捷鍵「W」用作切換「環繞模式」──今年 Adobe Photoshop 亦曾宣佈於下個版本加入了相類似的功能。

[![](/images/posts/2020/wrap-around-mode.jpg)](/images/posts/2014/wrap-around-mode.jpg)

不過，由於很多使用者因不小心誤按這個快捷鍵而被混淆了，誤以為 Krita 發生錯誤，因此我們從預設快捷鍵中移除了這個快捷鍵。可是這樣卻使環繞模式變得隱蔽起來。有見及此，我們於此版本中加入了一個功具列圖示按鈕以切換「環繞模式」：

[![](/images/posts/2020/wraparound_button.png)](/images/posts/2020/wraparound_button.png) 別再誤按了，好嗎？

### 改進高解像度縮放 (HiDPI) 的支援

![在 4K 顯示器 200% 介面縮放上，舊版和新版中浮動畫具板的分別。此圖亦展示了一個新按鈕和自訂介面字型。左：舊版 / 右：新版](/images/posts/2020/popup_palette_comparison.png "在 4K 顯示器 200% 介面縮放上，舊版和新版中浮動畫具板的分別。此圖亦展示了一個新按鈕和自訂介面字型。左：舊版 / 右：新版") Agata Cacko 改進了下列顯示的 HiDPI 繪製效果 ([BUG:411118](https://bugs.kde.org/show_bug.cgi?id=411118))：

- 像素畫預覽圖
- 參考圖顯示
- 漫畫管理器頁面
- 最近檔案工具面板中的檔案縮圖
- 最近檔案縮圖
- 浮動畫具板
- 建立檔案視窗中的剪貼簿內容縮圖
- 拾色器
- 色域遮罩
- 筆刷預設編輯工具中的筆刷預設圖示
- 圖層縮圖及圖示
- 資源清單
- 資源包圖示

## 程式錯誤修正

（譯者按：由於內容眾多而人力資源有限，故此段落不作完整翻譯，保留英文原文。）

### 檔案處理

- Files with names starting with a number are now autosaved correctly
- Make it possible to load EXR files with non-ascii characters（非 ASCII 字元，例如中日韓字元）in the path
- Disable making the background black for a semi-transparent EXR file ([BUG:427720](https://bugs.kde.org/show_bug.cgi?id=427720))

### 繪畫工具

- The PressureIn（「壓力 (最大值)」）sensor now works correctly in combination with the Hue color expression ([BUG:426234](https://bugs.kde.org/show_bug.cgi?id=426234))
- The speed smoothing algorithm no longer creates blobby lines ([BUG:363364](https://bugs.kde.org/show_bug.cgi?id=363364), [375360](https://bugs.kde.org/show_bug.cgi?id=375360))
- The colorsmudge brush now blends when there is a selection active ([BUG:423851](https://bugs.kde.org/show_bug.cgi?id=423851))
- The brush outline no longer snaps when switching between two images with a different zoom level ([BUG:427094](https://bugs.kde.org/show_bug.cgi?id=427094))

### 動畫製作

除下列的變更外，大多數與動畫製作相關的改進將會在 Krita 5.0 實現。

- Onion skins are hidden when playing an animation ([BUG:426246](https://bugs.kde.org/show_bug.cgi?id=426246))
- Warn the user when they are trying to run the ffmpeg download archive, instead of unpacking it
- Fix converting an animated transparency mask to a paint layer ([BUG:419223](https://bugs.kde.org/show_bug.cgi?id=419223))

### 易用性改進

- The default shortcuts for changing the mode in the selection tools have been removed: they are replaced by ctrl/shift/alt modifiers. The actions still exist, so you can configure single-key shortcuts in Krita's shorcut settings dialog.
- The magnetic selection tool now has buttons to confirm or discard a selection
- An issue where moving a selection would jump was fixed ([BUG:426949](https://bugs.kde.org/show_bug.cgi?id=426949))
- A Fit to Height zoom shortcut was added, patch by Jonathan Colman ([BUG:410929](https://bugs.kde.org/show_bug.cgi?id=410929))
- The screentone generator's defaults were improved
- File layers that are dragged and dropped now have a proper name (patch by Jonathan Colman) ([BUG:427235](https://bugs.kde.org/show_bug.cgi?id=427235))
- The popup palette now has a clear color history button (patch by Emilio Del Castillo)
- The report bug dialog now provides the system information and usage logs in an easy to copy/paste manner
- Blacklisted resources that contain a \\ in the filename were ignored ([BUG:421575](https://bugs.kde.org/show_bug.cgi?id=421575))
- Displays are shown by name in the color management settings page ([BUG:412943](https://bugs.kde.org/show_bug.cgi?id=412943))
- Fix showing custom icons for user-defined templates (patch by Evan Thompson) ([BUG:395894](https://bugs.kde.org/show_bug.cgi?id=395894))
- The fill layer dialog and seexpr widgets were polished
- The x/y position spin boxes in the move tool options were fixed ([BUG:420329](https://bugs.kde.org/show_bug.cgi?id=420329), [423452](https://bugs.kde.org/show_bug.cgi?id=423452))
- Add default letter spacing for the text shape (patch by Lucid Sunlight)
- Add support for user-installed color schemes (patch by Daniel)
- All dialogs and message boxes are now correctly parented to the main window (patch by Daniel)
- Make it possible to export groups as merged layers (patch by Dmitrij Antsevich)
- Fix kerning handling in the text editor (patch by Lucid Sunlight)
- Add support for color opacity in the text editor (patch by Lucid Sunlight) ([BUG:342303](https://bugs.kde.org/show_bug.cgi?id=342303))
- Fix cropping the transform mask when moving the masked layer
- Improve switching between SVG source and rich text editor (patch by Lucid Sunlight) ([BUG:424213](https://bugs.kde.org/show_bug.cgi?id=424213))
- Fix issues with the brush outline getting stuck when the brush size is smaller than 0 ([BUG:427751](https://bugs.kde.org/show_bug.cgi?id=427751))
- Improve the Python plugin importer so action files get imported correctly. (Patch by Rebecca Breu) ([BUG:429262](https://bugs.kde.org/show_bug.cgi?id=429262))
- Fix tearing of patterns when scrolling in the resource chooser.
- The rectangle and ellipse tool now have default shortcuts: Shift+R and Shift+J, respectively
- Allow the Select Similar Color selection tool to pick from a set of layers, make work correctly with image bounds and handle transparent layers correctly. ([BUG:428441](https://bugs.kde.org/show_bug.cgi?id=428441))
- Fix the isometric grid so it is drawn correctly
- The outline selection tool was renamed to freehand selection tool ([BUG:425894](https://bugs.kde.org/show_bug.cgi?id=425894))

### 濾鏡功能

- The bundled g'mic plugin is updated to 2.9.2 which contains a correct Boost-Fade filter (BUG:412617)
- The gradient map filter was improved and made faster (patch by Deif Lou)

### 穩定性及效能改進

- Fix a lot of memory leaks
- Improve performance by removing a bottleneck when transforming internal colors to and from QColor
- Fix a race condition in the Comics Manager plugin ([BUG:426701](https://bugs.kde.org/show_bug.cgi?id=426701))
- Fix the fill layers updating too many times
- Fix random crashes when changing screentone fill layer parameters ([BUG:428014](https://bugs.kde.org/show_bug.cgi?id=428014))
- Fix a crash in the Square Gradient strategy (patch by Deif Lou)
- Fix a crash when converting SVG source to rich text or back (patch by Lucid Sunlight)
- Fix an assert when trying to liquify transform an empty layer ([BUG:428685](https://bugs.kde.org/show_bug.cgi?id=428685))
- Fix an assert when creating a new layer from the visible layers while the active layer is hidden ([BUG:428683](https://bugs.kde.org/show_bug.cgi?id=428683))
- Make the Select Similar selection tool multithreaded.

### macOS

- On macOS, the Delete key (which is actually backspace) now deletes a selection. ([BUG:425370](https://bugs.kde.org/show_bug.cgi?id=425370))

### Android

- It's now possible to open files from external sources, like a file manager, google drive or a download manager on Android
- Add mimetype and pathpatter for .kra files
- Make Krita a SingleTask application: this means that opening a file of a type supported by Krita will work properly even if Krita is already running.
- Fix possible corruption when saving .kra or .ora files
- Fix a crash on closing Krita ([BUG:426092](https://bugs.kde.org/show_bug.cgi?id=426092))
- Fix "also save as KRA" ([BUG:424612](https://bugs.kde.org/show_bug.cgi?id=424612))
- Handle mouse buttons state and touch events properly
- Make resaving with different mime type work on Android ([BUG:429056](https://bugs.kde.org/show_bug.cgi?id=429056))
- Make the theme background black for chromeos: this used to be pink, which looked ugly when resizing a window.
- Fix flickering tiles when OpenGL is enabled ([BUG:424347](https://bugs.kde.org/show_bug.cgi?id=424347))

## 下載

### Windows

如果你使用免安裝版：請注意，免安裝版仍然會與安裝版本共用設定檔及資源。如希望以免安裝版測試並回報程式強制終止的問題，請同時下載偵錯符號 (debug symbols)。

- 64 位元安裝程式：[krita-x64-4.4.2-beta1-setup.exe](https://download.kde.org/unstable/krita/4.4.2-beta1/krita-x64-4.4.2-beta1-setup.exe)
- 64 位元免安裝版：[krita-x64-4.4.2-beta1.zip](https://download.kde.org/unstable/krita/4.4.2-beta1/krita-x64-4.4.2-beta1.zip)
- [偵錯符號（請解壓到 Krita 程式資料夾之中）](https://download.kde.org/unstable/krita/4.4.2-beta1/krita-x64-4.4.2-beta1-dbg.zip)

- 32 位元安裝程式：[krita-x86-4.4.2-beta1-setup.exe](https://download.kde.org/unstable/krita/4.4.2-beta1/krita-x86-4.4.2-beta1-setup.exe)
- 32 位元免安裝版：[krita-x86-4.4.2-beta1.zip](https://download.kde.org/unstable/krita/4.4.2-beta1/krita-x86-4.4.2-beta1.zip)
- [偵錯符號（請解壓到 Krita 程式資料夾之中）](https://download.kde.org/unstable/krita/4.4.2-beta1/krita-x86-4.4.2-beta1-dbg.zip)

### Linux

- 64 位元 Linux AppImage：[krita-4.4.2-beta1-x86_64.appimage](https://download.kde.org/unstable/krita/4.4.2-beta1/krita-4.4.2-beta1-x86_64.appimage)
- 64 位元 Linux [G'Mic-Qt 外掛程式 AppImage](https://download.kde.org/unstable/krita/4.4.2-beta1/gmic_krita_qt-x86_64.appimage)

### macOS

- macOS 套件：[krita-4.4.2-beta1.dmg](https://download.kde.org/unstable/krita/4.4.2-beta1/krita-4.4.2-beta1.dmg)

備註：gmic-qt 未支援 macOS。

### Android

我們仍視 ChomeOS 及 Android 的版本為**測試版本**。此版本或可能含有大量程式錯誤，而且仍有部份功能未能正常運作。由於使用者介面並未完善，軟體或須配合實體鍵盤才能使用全部功能。

- [64 位元 Intel CPU APK](https://download.kde.org/unstable/krita/4.4.2-beta1/krita-x86_64-4.4.2-beta1.apk)
- [32 位元 Intel CPU APK](https://download.kde.org/unstable/krita/4.4.2-beta1/krita-x86-4.4.2-beta1.apk)
- [64 位元 Arm CPU APK](https://download.kde.org/unstable/krita/4.4.2-beta1/krita-arm64-4.4.2-beta1.apk)
- [32 位元 Arm CPU APK](https://download.kde.org/unstable/krita/4.4.2-beta1/krita-arm32-4.4.2-beta1.apk)

### 原始碼

- [krita-4.4.2-beta1.tar.gz](https://download.kde.org/unstable/krita/4.4.2-beta1/krita-4.4.2-beta1.tar.gz)
- [krita-4.4.2-beta1.tar.xz](https://download.kde.org/unstable/krita/4.4.2-beta1/krita-4.4.2-beta1.tar.xz)

### md5sum

下載檔案的 MD5 校對碼已於以下檔案中列出：

- [md5sum.txt](https://download.kde.org/unstable/krita/4.4.2-beta1/md5sum.txt)

### 數位簽章

Linux AppImage 以及原始碼的 .tar.gz 和 .tar.xz 壓縮檔已使用數位簽章簽名。你可以運行 "gpg --recv-key 7468332F" 以取得公鑰。簽名檔可於[此處](https://download.kde.org/unstable/krita/4.4.2-beta1/)找到（副檔名為 .sig）。

## 支持 Krita

Krita 是免費及開放原始碼的項目。請考慮[捐款](https://krita.org/en/support-us/donations/)或[購買教學影片](https://krita.org/en/shop/)支持我們吧！有你的支持我們才能聘請開發人員全職進行 Krita 的開發工作。

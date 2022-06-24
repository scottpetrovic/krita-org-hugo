---
title: "Krita 4.4.2 測試版本 (beta 1) 已推出"
date: "2020-12-09"
categories: 
  - "news_zh-hk"
  - "development-builds_zh-hk"
---

Krita 開發團隊推出咗 Krita 4.4.2 嘅首個測試版本。依個版本包含超過 300 項程式碼改動，主要係修正程式錯誤，不過同時都加入咗一啲重大嘅新功能！

請注意：依個版本嘗試修正咗[某些情況下組合快捷鍵失效嘅問題 (Modifier shortcut keys stop working)](https://bugs.kde.org/show_bug.cgi?id=424319)，不過依項修正並未被問題嘅回報者確定可以達到預期效果。我哋喺依度希望各位使用者可以協助我哋細心測試一下。

## 新功能

### 網狀漸變

依項由 Sharaf Zaman 喺 Google Summer of Code 展開嘅計畫喺依個發佈版本正式成為 Krita 嘅新功能！依個係繼 Inkscape 之後另一個獨立嘅 SVG 網狀漸變 (Mesh Gradient) 實作，並且同 Inkscape 兼容。網狀漸變係用喺向量圖形。佢可以產生出非常自然嘅效果：

[![網狀漸變](/images/posts/2020/Handles-meshgradient-1024x554.png "網狀漸變")](/images/posts/2020/Handles-meshgradient.png) 網狀漸變

### 網狀變形

[![網狀變形嘅用法](/images/posts/2020/krita_4_4_2_mesh_gradients.png "網狀變形嘅用法")](/images/posts/2020/krita_4_4_2_mesh_gradients.png) 網狀變形容許作出複雜嘅曲線變形效果，例如係圖中半圓凸出嚟嘅窗框。依項功能可以大幅提升製作概念藝術嘅效率。

網狀變形係依個版本加入嘅另一項新功能。同網狀漸變相似，依項功能同樣係使用貝茲曲線形成嘅網格。依啲網格可以分別控制以產生準確嘅變形效果，尤其係對繪畫曲面物件非常有幫助。你仲可以選擇顯示貝茲曲線嘅控制點，俾你做出更加精密嘅變形控制！

現時提供嘅快捷鍵如下，不過我們仍然調整緊：

1. 網格節點： - 按下並拖曳 --- 移動節點
2. 邊緣節點： - 按下並拖曳 --- 移動節點 - Shift + 按下並拖曳 --- 移動整行或列 - Ctrl + Alt + 按下並拖曳 --- 分割或滑動行或列 - Ctrl + Alt + 按下並向外拖曳 --- 移除分割
3. 控制點： - 按下並拖曳 --- 對稱修改兩邊控制點 - Shift + 按下並拖曳 --- 修改單邊控制點 依項操作會令圖像出現明顯嘅角度變化，好似摺痕咁，亦可以話係令圖像起角。
4. 節點或控制點： - Ctrl + 按一下 --- 選取多點
5. 網格內部範圍： - 按下並拖曳 --- 網格自由扭曲 - Shift + 按下並拖曳 --- 移動整個網格
6. 網格外部空白位置： - 按下並拖曳 --- 旋轉網格或已選取項目 - Ctrl + 按下並拖曳 --- 縮放網格或已選取項目 - Shift + 按下並拖曳 --- 平移網格或已選取項目

### 漸變填充圖層同新版漸變編輯工具

[![漸變填充圖層同新版漸變編輯工具](/images/posts/2020/krita_4_4_2_new_gradient_editor_and_fill_layer.png "漸變填充圖層同新版漸變編輯工具")](/images/posts/2020/krita_4_4_2_new_gradient_editor_and_fill_layer.png) 正在使用漸變填充圖層同新版漸變編輯工具。

依項由 Deif Lou 加入嘅漸變填充圖層俾你可以非常簡單方便咁以非破壞性方式建立各種漸變效果。依項新功能同時亦帶嚟咗一項易用性改進：Krita 入面嘅漸變分為「停駐點漸變」同埋「分段漸變」兩種，過往各自有唔同功能同編輯介面，依家兩者都可以喺同一個介面入面編輯，而且兩者可以互相轉換。

### 改進半調濾鏡

Deif Lou 亦重寫咗半調濾鏡。舊版嘅半調濾鏡運算速度緩慢，又唔可以用嚟做濾鏡遮罩，仲只係提供圓點狀網點。

[![經半調濾鏡處理嘅 Krita 啟動畫面](/images/posts/2020/krita_4_4_2_halftone_filter.png "經半調濾鏡處理嘅 Krita 啟動畫面")](/images/posts/2020/krita_4_4_2_halftone_filter.png) 新的半調濾鏡可以分別處理獨立色彩通道，可以用嚟產生懷舊效果，甚至係用於印刷。

新嘅半調濾鏡可以用喺濾鏡遮罩圖層，支援獨立色彩通道，而半調網點圖案亦可以經由填充圖層產生，為創作帶嚟咗無限可能。

### 更新 macOS 整合外掛程式

Amyspark 為 Krita 嘅 QuickLook 外掛程式加入咗預覽縮圖功能（需要 macOS 10.15 或更新版本）以及支援喺 Spotlight 顯示檔案屬性資訊。

### 新增「貼上圖形樣式」操作

依項功能俾你可以將喺剪貼簿入面嘅向量圖形嘅樣式套用喺其他選取中嘅向量圖形。依個操作可以喺「編輯」功能表入面搵到，或者喺「鍵盤快捷鍵」設定入面指定快捷鍵。

### 新增「環繞模式」功具列圖示按鈕

Krita 曾經設定咗一個鍵盤快捷鍵「W」嚟用作切換「環繞模式」──今年 Adobe Photoshop 亦曾經宣佈喺下個版本加入咗相類似嘅功能。

[![](/images/posts/2020/wrap-around-mode.jpg)](/images/posts/2014/wrap-around-mode.jpg)

不過，由於好多使用者因為唔小心㩒咗依個快捷鍵而被混淆咗，誤以為 Krita 出現咗 bug，因此我哋喺預設快捷鍵入面移除咗依個快捷鍵。但係這樣反而令環繞模式變得隱蔽起嚟。有見及此，我哋喺依個版本入面加入咗一個功具列圖示按鈕用嚟切換「環繞模式」：

[![](/images/posts/2020/wraparound_button.png)](/images/posts/2020/wraparound_button.png) 唔好再㩒錯喇，好唔好？

### 改進高解像度縮放 (HiDPI) 嘅支援

![喺 4K 顯示器 200% 介面縮放上，舊版同新版入面浮動畫具板嘅分別。依幅圖亦展示咗一個新按鈕同自訂介面字型。左：舊版 / 右：新版](/images/posts/2020/popup_palette_comparison.png "喺 4K 顯示器 200% 介面縮放上，舊版同新版入面浮動畫具板嘅分別。依幅圖亦展示咗一個新按鈕同自訂介面字型。左：舊版 / 右：新版") Agata Cacko 改進咗以下顯示嘅 HiDPI 畫面效果 ([BUG:411118](https://bugs.kde.org/show_bug.cgi?id=411118))：

- 像素畫預覽圖
- 參考圖顯示
- 漫畫管理器頁面
- 最近檔案工具面板入面嘅檔案縮圖
- 最近檔案縮圖
- 浮動畫具板
- 建立檔案視窗入面嘅剪貼簿內容縮圖
- 色彩選擇器
- 色域遮罩
- 筆刷預設編輯工具入面嘅筆刷預設圖示
- 圖層縮圖及圖示
- 資源清單
- 資源包圖示

## 程式 bug 修正

（譯者按：由於內容太多而人力資源有限，因此依段唔做完整嘅翻譯，保留返英文原文。）

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

除咗以下嘅改變之外，大多數同動畫製作有關嘅改進將會擺喺 Krita 5.0 版本入面。

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

### 穩定性同效能改進

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

如果你使用免安裝版：請注意，免安裝版仍然會同安裝版本共用設定檔同埋資源。如果想用免安裝版測試並回報 crash 嘅問題，請同時下載 debug symbols。

- 64 位元安裝程式：[krita-x64-4.4.2-beta1-setup.exe](https://download.kde.org/unstable/krita/4.4.2-beta1/krita-x64-4.4.2-beta1-setup.exe)
- 64 位元免安裝版：[krita-x64-4.4.2-beta1.zip](https://download.kde.org/unstable/krita/4.4.2-beta1/krita-x64-4.4.2-beta1.zip)
- [Debug symbols（請解壓到 Krita 程式資料夾入面）](https://download.kde.org/unstable/krita/4.4.2-beta1/krita-x64-4.4.2-beta1-dbg.zip)

- 32 位元安裝程式：[krita-x86-4.4.2-beta1-setup.exe](https://download.kde.org/unstable/krita/4.4.2-beta1/krita-x86-4.4.2-beta1-setup.exe)
- 32 位元免安裝版：[krita-x86-4.4.2-beta1.zip](https://download.kde.org/unstable/krita/4.4.2-beta1/krita-x86-4.4.2-beta1.zip)
- [Debug symbols（請解壓到 Krita 程式資料夾入面）](https://download.kde.org/unstable/krita/4.4.2-beta1/krita-x86-4.4.2-beta1-dbg.zip)

### Linux

- 64 位元 Linux AppImage：[krita-4.4.2-beta1-x86\_64.appimage](https://download.kde.org/unstable/krita/4.4.2-beta1/krita-4.4.2-beta1-x86_64.appimage)
- 64 位元 Linux [G'Mic-Qt 外掛程式 AppImage](https://download.kde.org/unstable/krita/4.4.2-beta1/gmic_krita_qt-x86_64.appimage)

### macOS

- macOS 套件：[krita-4.4.2-beta1.dmg](https://download.kde.org/unstable/krita/4.4.2-beta1/krita-4.4.2-beta1.dmg)

備註：gmic-qt 未支援 macOS。

### Android

我哋提供嘅 ChomeOS 同 Android 版本仲係**測試版本**。依個版本或可能含有大量嘅 bug，而且仲有部份功能未能正常運作。由於使用者介面仲未改進好，軟件或者須要配合實體鍵盤先可以用到全部功能。

- [64 位元 Intel CPU APK](https://download.kde.org/unstable/krita/4.4.2-beta1/krita-x86_64-4.4.2-beta1.apk)
- [32 位元 Intel CPU APK](https://download.kde.org/unstable/krita/4.4.2-beta1/krita-x86-4.4.2-beta1.apk)
- [64 位元 Arm CPU APK](https://download.kde.org/unstable/krita/4.4.2-beta1/krita-arm64-4.4.2-beta1.apk)
- [32 位元 Arm CPU APK](https://download.kde.org/unstable/krita/4.4.2-beta1/krita-arm32-4.4.2-beta1.apk)

### 原始碼

- [krita-4.4.2-beta1.tar.gz](https://download.kde.org/unstable/krita/4.4.2-beta1/krita-4.4.2-beta1.tar.gz)
- [krita-4.4.2-beta1.tar.xz](https://download.kde.org/unstable/krita/4.4.2-beta1/krita-4.4.2-beta1.tar.xz)

### md5sum

下載檔案嘅 MD5 校對碼可以喺依個檔案入面搵到：

- [md5sum.txt](https://download.kde.org/unstable/krita/4.4.2-beta1/md5sum.txt)

### 數碼簽署

Linux AppImage 以及原始碼嘅 .tar.gz 同 .tar.xz 壓縮檔已使用數碼簽署簽名。你可以運行 "gpg --recv-key 7468332F" 以取得 public key。簽名檔可以喺[依度](https://download.kde.org/unstable/krita/4.4.2-beta1/)搵到（副檔名為 .sig）。

## 支持 Krita

Krita 係免費及開放原始碼嘅項目。請考慮[捐款](https://krita.org/en/support-us/donations/)或者[購買教學影片](https://krita.org/en/shop/)支持我哋啦！有你嘅支持我哋先可以聘請開發人員全職進行 Krita 嘅開發工作。

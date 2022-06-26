---
title: "Krita 4.4.3 測試版本 (beta 1) 已推出"
date: "2021-02-25"
categories: 
  - "news_zh-tw"
  - "development-builds_zh-tw"
---

Krita 開發團隊現推出 Krita 4.4.3 的首個測試版本。此版本純粹為修正程式錯誤。

## 錯誤修正

### Android 修正

- Crash when back button was pressed on splash screen
- Crash when loading files while app is still booting
- Use lastUpdateTime for copying assets
- Provide host so pathPattern could be effective
- Fix color selector covering entire screen ([BUG:432459](https://bugs.kde.org/show_bug.cgi?id=432459))
- Saved configs aren't loaded after restart ([BUG:432433](https://bugs.kde.org/show_bug.cgi?id=432433))
- Add key functions to psd_layer_effects_shadow_base ([BUG:432904](https://bugs.kde.org/show_bug.cgi?id=432904))
- Fix reloading presets from user-imported bundles ([BUG:432488](https://bugs.kde.org/show_bug.cgi?id=432488))

### 程式強制終止修正

- Fix crash in halftone filter due to an access to an invalid pointer
- Fix crash when reapplying a filter with reprompting
- Fix crash when painting on a filter mask created from a vector selection ([BUG:432329](http://432329))

### nacOS 修正

- MacOS: fix the finder plugins for showing a thumbnail or a quick look preview ([BUG:432328](https://bugs.kde.org/show_bug.cgi?id=432328))

### 程式指令集修正

- Fix handling the channel flags. Patch by Chris Venter, thanks! ([BUG:432226](https://bugs.kde.org/show_bug.cgi?id=432226))

### 穩定性及效能改進

- Fix synchronization of zoom level between canvas and the scratchpad
- Fix normalization in Smart Patch Tool ([BUG:430953](https://bugs.kde.org/show_bug.cgi?id=430953))
- Fix performance issues in the foreground/background color button ([BUG:432936](https://bugs.kde.org/show_bug.cgi?id=432936))
- Fix saving incremental backups ([BUG:432701](https://bugs.kde.org/show_bug.cgi?id=432701))
- Fix a problem where the scratchpad could be unresponsive ([BUG:431708](https://bugs.kde.org/show_bug.cgi?id=431708))
- Fix Color as Alpha and Preserve Alpha in Custom and Clipboard brushes ([BUG:432274](https://bugs.kde.org/show_bug.cgi?id=432274))
- Fix the RGBA_brushes bundle so Krita doesn't try to recreate it on startup [(BUG:431832](https://bugs.kde.org/show_bug.cgi?id=431832))
- Fix handling of style in KisAngleSelector when the spin box must be shown flat and use the new angle selector everywhere

## 下載

### Windows

如果你使用免安裝版：請注意，免安裝版仍然會與安裝版本共用設定檔及資源。如希望以免安裝版測試並回報程式強制終止的問題，請同時下載偵錯符號 (debug symbols)。

- 64 位元安裝程式：[krita-x64-4.4.3-beta1-setup.exe](https://download.kde.org/unstable/krita/4.4.3-beta1/krita-x64-4.4.3-beta1-setup.exe)
- 64 位元免安裝版：[krita-x64-4.4.3-beta1.zip](https://download.kde.org/unstable/krita/4.4.3-beta1/krita-x64-4.4.3-beta1.zip)
- [偵錯符號（請解壓到 Krita 程式資料夾之中）](https://download.kde.org/unstable/krita/4.4.3-beta1/krita-x64-4.4.3-beta1-dbg.zip)

- 32 位元安裝程式：[krita-x86-4.4.3-beta1-setup.exe](https://download.kde.org/unstable/krita/4.4.3-beta1/krita-x86-4.4.3-beta1-setup.exe)
- 32 位元免安裝版：[krita-x86-4.4.3-beta1.zip](https://download.kde.org/unstable/krita/4.4.3-beta1/krita-x86-4.4.3-beta1.zip)
- [偵錯符號（請解壓到 Krita 程式資料夾之中）](https://download.kde.org/unstable/krita/4.4.3-beta1/krita-x86-4.4.3-beta1-dbg.zip)

### Linux

- 64 位元 Linux AppImage：[krita-4.4.3-beta1-x86_64.appimage](https://download.kde.org/unstable/krita/4.4.3-beta1/krita-4.4.3-beta1-x86_64.appimage)
- 64 位元 Linux [G'Mic-Qt 外掛程式 AppImage](https://download.kde.org/unstable/krita/4.4.3-beta1/gmic_krita_qt-x86_64.appimage)

### macOS

- macOS 套件：[krita-4.4.3-beta1.dmg](https://download.kde.org/unstable/krita/4.4.3-beta1/krita-4.4.3-beta1.dmg)

備註：gmic-qt 未支援 macOS。

### Android

我們仍視 ChomeOS 及 Android 的版本為**測試版本**。此版本或可能含有大量程式錯誤，而且仍有部份功能未能正常運作。由於使用者介面並未完善，軟體或須配合實體鍵盤才能使用全部功能。

- [64 位元 Intel CPU APK](https://download.kde.org/unstable/krita/4.4.3-beta1/krita_build_apk-release-x86_64-unsigned.apk)
- [32 位元 Intel CPU APK](https://download.kde.org/unstable/krita/4.4.3-beta1/krita_build_apk-release-x86_unsigned.apk)
- [64 位元 Arm CPU APK](https://download.kde.org/unstable/krita/4.4.3-beta1/krita_build_apk-release-arm64-v8a-unsigned.apk)
- [32 位元 Arm CPU APK](https://download.kde.org/unstable/krita/4.4.3-beta1/krita_build_apk-release-armeabi-v7a-unsigned.apk)

### 原始碼

- [krita-4.4.3-beta1.tar.gz](https://download.kde.org/unstable/krita/4.4.3-beta1/krita-4.4.3-beta1.tar.gz)
- [krita-4.4.3-beta1.tar.xz](https://download.kde.org/unstable/krita/4.4.3-beta1/krita-4.4.3-beta1.tar.xz)

### md5sum

下載檔案的 MD5 校對碼已於以下檔案中列出：

- [md5sum.txt](https://download.kde.org/unstable/krita/4.4.3-beta1/md5sum.txt)

### 數位簽章

Linux AppImage 以及原始碼的 .tar.gz 和 .tar.xz 壓縮檔已使用數位簽章簽名。你可以運行 "gpg --recv-key 7468332F" 以取得 GPG 公鑰。簽名檔可於[此處](https://download.kde.org/unstable/krita/4.4.3-beta1/)找到（副檔名為 .sig）。

## 支持 Krita

Krita 是免費及開放原始碼的項目。請考慮[捐款](https://krita.org/en/support-us/donations/)或[購買教學影片](https://krita.org/en/shop/)支持我們吧！有你的支持我們才能聘請開發人員全職進行 Krita 的開發工作。

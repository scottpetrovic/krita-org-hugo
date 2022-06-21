---
title: "正式發佈 Krita 4.4.3 新版本"
date: "2021-03-28"
categories: 
  - "news_zh-hk"
  - "officialrelease_zh-hk"
---

Krita 開發團隊正式推出咗 Krita 4.4.3 更新版本。依個版本純粹係修正程式 bug。喺之前我哋推出咗兩個測試版本，希望確保依個版本可以運作得非常穩定。而嚟緊嘅時間我哋將會專注喺 Krita 5 嘅開發工作。

依個亦會係最後一個支援 32 位元 Windows 嘅 Krita 版本。將來推出嘅 Windows Krita 版本只會支援 64 位元 Windows。

依個係 Krita 首次為 macOS 以 Universal Binary 方式組建嘅版本。依個版本提供嘅 DMG 套件入面同時包含 ARM 以及 X64 架構嘅執行檔。請注意，喺 macOS 上 OpenGL 畫布顯示會降低畫筆輸入效能嘅問題依然存在，無論系統架構係 X64 定係 ARM 都一樣。

## Bug 修正

（譯者按：由於內容太多而人力資源有限，因此依段唔做完整嘅翻譯，保留返英文原文。）

### Android 修正

- Crash when back button was pressed on splash screen
- Crash when loading files while app is still booting
- Use lastUpdateTime for copying assets
- Provide host so pathPattern could be effective
- Fix color selector covering entire screen ([BUG:432459](https://bugs.kde.org/show_bug.cgi?id=432459))
- Saved configs aren't loaded after restart ([BUG:432433](https://bugs.kde.org/show_bug.cgi?id=432433))
- Add key functions to psd\_layer\_effects\_shadow\_base ([BUG:432904](https://bugs.kde.org/show_bug.cgi?id=432904))
- Fix reloading presets from user-imported bundles ([BUG:432488](https://bugs.kde.org/show_bug.cgi?id=432488))

### 程式強制終止修正

- Fix crash in halftone filter due to an access to an invalid pointer
- Fix crash when reapplying a filter with reprompting
- Fix crash when painting on a filter mask created from a vector selection ([BUG:432329](https://bugs.kde.org/show_bug.cgi?id=432329))

### macOS 修正

- MacOS: fix the finder plugins for showing a thumbnail or a quick look preview ([BUG:432328](https://bugs.kde.org/show_bug.cgi?id=432328))

### 程式指令集修正

- Fix handling the channel flags. Patch by Chris Venter, thanks! ([BUG:432226](https://bugs.kde.org/show_bug.cgi?id=432226))

### 穩定性同效能改進

- Fix synchronization of zoom level between canvas and the scratchpad
- Fix normalization in Smart Patch Tool ([BUG:430953](https://bugs.kde.org/show_bug.cgi?id=430953))
- Fix performance issues in the foreground/background color button ([BUG:432936](https://bugs.kde.org/show_bug.cgi?id=432936))
- Fix saving incremental backups ([BUG:432701](https://bugs.kde.org/show_bug.cgi?id=432701))
- Fix a problem where the scratchpad could be unresponsive ([BUG:431708](https://bugs.kde.org/show_bug.cgi?id=431708))
- Fix Color as Alpha and Preserve Alpha in Custom and Clipboard brushes ([BUG:432274](https://bugs.kde.org/show_bug.cgi?id=432274))
- Fix the RGBA\_brushes bundle so Krita doesn't try to recreate it on startup [(BUG:431832](https://bugs.kde.org/show_bug.cgi?id=431832))
- Fix handling of style in KisAngleSelector when the spin box must be shown flat and use the new angle selector everywhere

## 下載

### Windows

如果你使用免安裝版：請注意，免安裝版仍然會同安裝版本共用設定檔同埋資源。如果想用免安裝版測試並回報 crash 嘅問題，請同時下載 debug symbols。

- 64 位元安裝程式：[krita-x64-4.4.3-setup.exe](https://download.kde.org/stable/krita/4.4.3/krita-x64-4.4.3-setup.exe)
- 64 位元免安裝版：[krita-x64-4.4.3.zip](https://download.kde.org/stable/krita/4.4.3/krita-x64-4.4.3.zip)
- [Debug symbols（請解壓到 Krita 程式資料夾入面）](https://download.kde.org/stable/krita/4.4.3/krita-x64-4.4.3-dbg.zip)

- 32 位元安裝程式：[krita-x86-4.4.3-setup.exe](https://download.kde.org/stable/krita/4.4.3/krita-x86-4.4.3-setup.exe)
- 32 位元免安裝版：[krita-x86-4.4.3.zip](https://download.kde.org/stable/krita/4.4.3/krita-x86-4.4.3.zip)
- [Debug symbols（請解壓到 Krita 程式資料夾入面）](https://download.kde.org/stable/krita/4.4.3/krita-x86-4.4.3-dbg.zip)

### Linux

- 64 位元 Linux AppImage：[krita-4.4.3-x86\_64.appimage](https://download.kde.org/stable/krita/4.4.3/krita-4.4.3-x86_64.appimage)
- 64 位元 Linux [G'Mic-Qt 外掛程式 AppImage](https://download.kde.org/stable/krita/4.4.3/gmic_krita_qt-x86_64.appimage)

### macOS

- macOS 套件：[krita-4.4.3.dmg](https://download.kde.org/stable/krita/4.4.3/krita-4.4.3.dmg)

備註：gmic-qt 未支援 macOS。

### Android

我哋提供嘅 ChomeOS 同 Android 版本仲係**測試版本**。依個版本或可能含有大量嘅 bug，而且仲有部份功能未能正常運作。由於使用者介面仲未改進好，軟件或者須要配合實體鍵盤先可以用到全部功能。

除咗用以下連結下載 APK 安裝檔，你亦可以經由 [Google Play](https://play.google.com/store/apps/details?id=org.krita) 安裝 Krita 4.4.3。

- [64 位元 Intel CPU APK](https://download.kde.org/stable/krita/4.4.3/krita_x86_64_apk-release.apk)
- [32 位元 Intel CPU APK](https://download.kde.org/stable/krita/4.4.3/krita_x86_apk-release.apk)
- [64 位元 Arm CPU APK](https://download.kde.org/stable/krita/4.4.3/krita_arm64-v8a_apk-release.apk)
- [32 位元 Arm CPU APK](https://download.kde.org/stable/krita/4.4.3/krita_armeabi-v7a_apk-release.apk)

### 原始碼

- [krita-4.4.3.tar.gz](https://download.kde.org/stable/krita/4.4.3/krita-4.4.3.tar.gz)
- [krita-4.4.3.tar.xz](https://download.kde.org/stable/krita/4.4.3/krita-4.4.3.tar.xz)

### md5sum

下載檔案嘅 MD5 校對碼可以喺依個檔案入面搵到：

- [md5sum.txt](https://download.kde.org/stable/krita/4.4.3/md5sum.txt)

### 數碼簽署

Linux AppImage 以及原始碼嘅 .tar.gz 同 .tar.xz 壓縮檔已使用數碼簽署簽名。你可以運行 "gpg --recv-key 7468332F" 以取得 public key。簽名檔可以喺[依度](https://download.kde.org/stable/krita/4.4.3/)搵到（副檔名為 .sig）。

## 支持 Krita

Krita 係免費及開放原始碼嘅項目。請考慮[捐款](https://krita.org/en/support-us/donations/)或者[購買教學影片](https://krita.org/en/shop/)支持我哋啦！有你嘅支持我哋先可以聘請開發人員全職進行 Krita 嘅開發工作。

---
title: "發佈 Krita 4.4.1 修正版本"
date: "2020-10-29"
categories: 
  - "officialrelease_zh-hk"
---

由於 Krita 4.4.0 出現咗一啲 4.3.0 冇嘅 bug，我哋依家發佈咗 Krita 4.4.1 修正版本。依個版本包含以下修正：

- Android 及 ChromeOS：
    - 使用 SDK version 29，咁即係表示 Krita 唔使要求額外嘅權限，並且可以更容易存取外部檔案；Krita 亦已更新至使用 NDK 20 或更高版本
    - 修正顏色選擇器嘅 bug（[BUG:423254](https://bugs.kde.org/show_bug.cgi?id=423254)）
    - 修正使用浮動畫具板時輸入事件會傳送到畫布嘅 bug
    - 跟部機的語言設定，令使用者介面可以顯示本地化咗嘅文字（[BUG:427692](https://bugs.kde.org/show_bug.cgi?id=427692)）
    - 修正 Android 複製貼上嘅 bug（[BUG:423199](https://bugs.kde.org/show_bug.cgi?id=423199)）
- 修正喺載入包含圖案填充圖層嘅檔案時嘅 crash（[BUG:427866](https://bugs.kde.org/show_bug.cgi?id=427866))
- 修正唔可以正常載入包含向量選取區域嘅遮罩嘅 bug（[BUG:428332](https://bugs.kde.org/show_bug.cgi?id=428332)）
- 修正 double-click 文字物件時嘅 crash（[BUG:427858](https://bugs.kde.org/show_bug.cgi?id=427858)）
- 修正喺柵格選取區域使用移動工具時嘅 crash（[BUG:428260](https://bugs.kde.org/show_bug.cgi?id=428260)）

## 下載

### Windows

如果你使用免安裝版：請注意，免安裝版仍然會同安裝版本共用設定檔同埋資源。如果想用免安裝版測試並回報 crash 嘅問題，請同時下載 debug symbols。

- 64 位元安裝程式：[krita-x64-4.4.1-setup.exe](https://download.kde.org/stable/krita/4.4.1/krita-x64-4.4.1-setup.exe)
- 64 位元免安裝版：[krita-x64-4.4.1.zip](https://download.kde.org/stable/krita/4.4.1/krita-x64-4.4.1.zip)
- [Debug symbols（請解壓到 Krita 程式資料夾入面）](https://download.kde.org/stable/krita/4.4.1/krita-x64-4.4.1-dbg.zip)

- 32 位元安裝程式：[krita-x86-4.4.1-setup.exe](https://download.kde.org/stable/krita/4.4.1/krita-x86-4.4.1-setup.exe)
- 32 位元免安裝版：[krita-x86-4.4.1.zip](https://download.kde.org/stable/krita/4.4.1/krita-x86-4.4.1.zip)
- [Debug symbols（請解壓到 Krita 程式資料夾入面）](https://download.kde.org/stable/krita/4.4.1/krita-x86-4.4.1-dbg.zip)

### Linux

- 64 位元 Linux AppImage：[krita-4.4.1-x86_64.appimage](https://download.kde.org/stable/krita/4.4.1/krita-4.4.1-x86_64.appimage)
- 64 位元 Linux [G'Mic-Qt 外掛程式 AppImage](https://download.kde.org/stable/krita/4.4.1/gmic_krita_qt-x86_64.appimage)

### macOS

- macOS 套件：[krita-4.4.1.dmg](https://download.kde.org/stable/krita/4.4.1/krita-4.4.1.dmg)

備註：gmic-qt 未支援 macOS。

### ChromeOS 同 Android Beta 測試版本

我哋提供嘅 ChomeOS 同 Android 版本仲係**測試版本**。依個版本或可能含有大量嘅 bug，而且仲有部份功能未能正常運作。由於使用者介面仲未改進好，軟件或者須要配合實體鍵盤先可以用到全部功能。

- [64 位元 Intel CPU APK](https://download.kde.org/stable/krita/4.4.1/krita-x86_64-4.4.1-release.apk)
- [32 位元 Intel CPU APK](https://download.kde.org/stable/krita/4.4.1/krita-x86-4.4.1-release.apk)
- [64 位元 Arm CPU APK](https://download.kde.org/stable/krita/4.4.1/krita-arm64-4.4.1-release.apk)
- [32 位元 Arm CPU APK](https://download.kde.org/stable/krita/4.4.1/krita-arm32-4.4.1-release.apk)

### 原始碼

- [krita-4.4.1.tar.gz](https://download.kde.org/stable/krita/4.4.1/krita-4.4.1.tar.gz)
- [krita-4.4.1.tar.xz](https://download.kde.org/stable/krita/4.4.1/krita-4.4.1.tar.xz)

### md5sum

下載檔案嘅 MD5 校對碼可以喺依個檔案入面搵到：

- [md5sum.txt](https://download.kde.org/stable/krita/4.4.1/md5sum.txt)

## 支持 Krita

Krita 係免費及開放原始碼嘅項目。請考慮[捐款](https://krita.org/en/support-us/donations/)或者[購買教學影片](https://krita.org/en/shop/)支持我哋啦！有你嘅支持我哋先可以聘請開發人員全職進行 Krita 嘅開發工作。

---
title: "發佈 Krita 5.0 嘅第五個測試版本 (Beta 5)"
date: "2021-12-03"
categories: 
  - "news_zh-hk"
  - "development-builds_zh-hk"
---

因為先前 Beta 3 嘅 macOS 版本建置出現咗問題，所以依家我哋推出咗第五個 Beta 測試版本。本來我哋打算推出 Beta 4，只不過當我們正喺度準備建置依個版本嘅時候，Dmitry Kazakov 又再修正咗一個我哋非常希望修正嘅問題，因為咁我哋跳過咗依個版本。

![](images/2021-11-16_kiki-piggy-bank_krita5.png) Krita 係自由、免費同開源嘅專案。請考慮[向 Krita 發展基金捐款](https://fund.krita.org)或者[購買教學影片](https://krita.org/en/shop/)支持我哋啦！有你哋嘅支持，我哋先可以俾核心開發者全職為 Krita 工作。

以下係 Beta 3 之後再修正咗嘅問題：

- 修正咗 macOS 建置嘅問題……
- Fix an issue with the resource selector where the wrong resource would be selected
- Only save color palettes if they are modified
- Fix the line height of text shapes being too large
- Fix the size of text in text shapes compared to Krita 4
- Remove the obsolete shortcut for the brightness/contrast filter
- Create MSIX packages of Krita on the binary builder
- Fix wrong animation for preset save dialog
- Fix loading resources from bundles if newer versions of the resource are deleted from the resource folder
- Fix the color model of group layers
- Fix issues with soft proofing
- Fix brush presets that use the gradient map mode

## 下載

### Windows

如果你使用免安裝版：請注意，免安裝版仍然會同安裝版本共用設定檔同埋資源。如果想用免安裝版測試並回報 crash 嘅問題，請同時下載 debug symbols。

注意：我哋依家唔再提供為 32 位元 Windows 建置嘅版本。

- 64 位元安裝程式：[krita-x64-5.0.0-beta5-setup.exe](https://download.kde.org/unstable/krita/5.0.0-beta5/krita-x64-5.0.0-beta5-setup.exe)
- 64 位元免安裝版：[krita-x64-5.0.0-beta5.zip](https://download.kde.org/unstable/krita/5.0.0-beta5/krita-x64-5.0.0-beta5.zip)
- [Debug symbols（請解壓到 Krita 程式資料夾入面）](https://download.kde.org/unstable/krita/5.0.0-beta5/krita-x64-5.0.0-beta5-dbg.zip)

### Linux

- 64 位元 Linux AppImage：[krita-5.0.0-beta5-x86\_64.appimage](https://download.kde.org/unstable/krita/5.0.0-beta5/krita-5.0.0-beta5-x86_64.appimage)

Linux 版本唔使再另外下載 G'Mic-Qt 外掛程式 AppImage。

### macOS

注意：如果你用緊 macOS Sierra 或者 High Sierra，請睇下[依段影片](https://www.youtube.com/watch?v=3py0kgq95Hk)了解點樣執行開發者簽署嘅程式。

- macOS 套件：[krita-5.0.0-beta5.dmg](https://download.kde.org/unstable/krita/5.0.0-beta5/krita-5.0.0-beta5.dmg)

### Android

我哋提供嘅 ChomeOS 同 Android 版本仲係**測試版本**。依個版本或可能含有大量嘅 bug，而且仲有部份功能未能正常運作。由於使用者介面仲未改進好，軟件或者須要配合實體鍵盤先可以用到全部功能。

- [64 位元 Intel CPU APK](https://download.kde.org/unstable/krita/5.0.0-beta5/krita-x86_64-5.0.0-beta5-release-signed.apk)
- [32 位元 Intel CPU APK](https://download.kde.org/unstable/krita/5.0.0-beta5/krita-x86-5.0.0-beta5-release-signed.apk)
- [64 位元 Arm CPU APK](https://download.kde.org/unstable/krita/5.0.0-beta5/krita-arm64-v8a-5.0.0-beta5-release-signed.apk)
- [32 位元 Arm CPU APK](https://download.kde.org/unstable/krita/5.0.0-beta5/krita-armeabi-v7a-5.0.0-beta5-release-signed.apk)

### 原始碼

- [krita-5.0.0-beta5.tar.gz](https://download.kde.org/unstable/krita/5.0.0-beta5/krita-5.0.0-beta5.tar.gz)
- [krita-5.0.0-beta5.tar.xz](https://download.kde.org/unstable/krita/5.0.0-beta5/krita-5.0.0-beta5.tar.xz)

### md5sum

下載檔案嘅 MD5 校對碼可以喺依個檔案入面搵到：

- [md5sum.txt](https://download.kde.org/unstable/krita/5.0.0-beta5/md5sum.txt)

### 數碼簽署

Linux AppImage 以及原始碼嘅 .tar.gz 同 .tar.xz 壓縮檔已使用數碼簽署簽名。你可以由[依度](https://files.kde.org/krita/4DA79EDA231C852B)取得 public key。簽名檔可以喺[依度](https://download.kde.org/unstable/krita/5.0.0-beta5/)搵到（副檔名為 .sig）。

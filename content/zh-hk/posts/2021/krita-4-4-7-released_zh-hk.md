---
title: "正式發佈 Krita 4.4.7 新版本"
date: "2021-08-07"
categories: 
  - "news_zh-hk"
  - "officialrelease_zh-hk"
---

今次**真係** Krita 5.0 發佈前嘅最後一個 4.4 修正版本。我哋修正咗一個喺 Krita 4.4.5 出現嘅效能問題。此外其他的修正有：

- Fix a crash on exit with certain versions of Qt and PyQt
- Fix moving selection with the magnetic selection tool ([BUG:433633](https://bugs.kde.org/show_bug.cgi?id=433633))
- Fix crashes in the magnetic selection tool when deleting nodes ([BUG:439896](https://bugs.kde.org/show_bug.cgi?id=439896))
- Fix an assert when converting the image color space from Python ([BUG:437980](https://bugs.kde.org/show_bug.cgi?id=437980))
- Fix a crash when closing a gamut mask document ([BUG:438914](https://bugs.kde.org/show_bug.cgi?id=438914))
- Fix drag and drop of clone layers between images ([BUG:414699](https://bugs.kde.org/show_bug.cgi?id=414699))
- Fix crash when saving the image with trimming enabled ([BUG:437626](https://bugs.kde.org/show_bug.cgi?id=437626))

## 下載

正式發佈版本跳過咗版本編號 4.4.6，因為 Krita 4.4.6 係為 Epic Store 臨時發佈所準備嘅版本。

### Windows

如果你使用免安裝版：請注意，免安裝版仍然會同安裝版本共用設定檔同埋資源。如果想用免安裝版測試並回報 crash 嘅問題，請同時下載 debug symbols。

注意：我哋依家唔再提供為 32 位元 Windows 建置嘅版本。

- 64 位元安裝程式：[krita-x64-4.4.7-setup.exe](https://download.kde.org/stable/krita/4.4.7/krita-x64-4.4.7-setup.exe)
- 64 位元免安裝版：[krita-x64-4.4.7.zip](https://download.kde.org/stable/krita/4.4.7/krita-x64-4.4.7.zip)
- [Debug symbols（請解壓到 Krita 程式資料夾入面）](https://download.kde.org/stable/krita/4.4.7/krita-x64-4.4.7-dbg.zip)

### Linux

- 64 位元 Linux AppImage：[krita-4.4.7-x86_64.appimage](https://download.kde.org/stable/krita/4.4.7/krita-4.4.7-x86_64.appimage)
- 64 位元 Linux [G'Mic-Qt 外掛程式 AppImage](https://download.kde.org/stable/krita/4.4.7/gmic_krita_qt-x86_64.appimage)

### macOS

注意：如果你用緊 macOS Sierra 或者 High Sierra，請睇下[依段影片](https://www.youtube.com/watch?v=3py0kgq95Hk)了解點樣執行開發者簽署嘅程式。

- macOS 套件：[krita-4.4.7.dmg](https://download.kde.org/stable/krita/4.4.7/krita-4.4.7.dmg)

備註：gmic-qt 未支援 macOS。

### Android

我哋提供嘅 ChomeOS 同 Android 版本仲係**測試版本**。依個版本或可能含有大量嘅 bug，而且仲有部份功能未能正常運作。由於使用者介面仲未改進好，軟件或者須要配合實體鍵盤先可以用到全部功能。

除咗用以下連結下載 APK 安裝檔，你亦可以經由 [Google Play](https://play.google.com/store/apps/details?id=org.krita) 安裝 Krita 4.4.7。

- [64 位元 Intel CPU APK](https://download.kde.org/stable/krita/4.4.7/krita-x86_64-4.4.7-release.apk)
- [32 位元 Intel CPU APK](https://download.kde.org/stable/krita/4.4.7/krita-x86-4.4.7-release.apk)
- [64 位元 Arm CPU APK](https://download.kde.org/stable/krita/4.4.7/krita-arm64-v8a-4.4.7-release.apk)
- [32 位元 Arm CPU APK](https://download.kde.org/stable/krita/4.4.7/krita-armeabi-v7a-4.4.7-release.apk)

### 原始碼

- [krita-4.4.7.tar.gz](https://download.kde.org/stable/krita/4.4.7/krita-4.4.7.tar.gz)
- [krita-4.4.7.tar.xz](https://download.kde.org/stable/krita/4.4.7/krita-4.4.7.tar.xz)

### md5sum

下載檔案嘅 MD5 校對碼可以喺依個檔案入面搵到：

- [md5sum.txt](https://download.kde.org/stable/krita/4.4.7/md5sum.txt)

### 數碼簽署

Linux AppImage 以及原始碼嘅 .tar.gz 同 .tar.xz 壓縮檔已使用數碼簽署簽名。你可以運行 "gpg --recv-key 7468332F" 以取得 public key。簽名檔可以喺[依度](https://download.kde.org/stable/krita/4.4.7/)搵到（副檔名為 .sig）。

## 支持 Krita

Krita 係免費及開放原始碼嘅項目。請考慮[捐款](https://krita.org/en/support-us/donations/)或者[購買教學影片](https://krita.org/en/shop/)支持我哋啦！有你嘅支持我哋先可以聘請開發人員全職進行 Krita 嘅開發工作。

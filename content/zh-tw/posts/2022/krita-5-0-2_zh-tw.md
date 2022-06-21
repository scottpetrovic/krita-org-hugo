---
title: "發佈 Krita 5.0.2 修正版本"
date: "2022-01-07"
categories: 
  - "news_zh-tw"
  - "officialrelease_zh-tw"
---

在正式發佈 Krita 5.0 之後，我們並沒有停步，而現在我們要發佈首個修正版本了喔！（這次版本編號是 5.0.2，因為我們在 Microsoft Store 進行測試時佔用了 5.0.0 這個版本編號，導致在正式發佈 5.0 時需要改用 5.0.1……因此別擔心，你並沒有錯過 5.0.1 版本喔！）

這次更新包含了以下修正： （譯者按：由於內容眾多而人力資源有限，故此段落不作完整翻譯，保留英文原文。）

- Fix a crash when changing the Instant Preview setting of a brush preset.
- Fix a crash when there are ABR brush libraries present with an uppercase ABR extension. [BUG:447454](https://bugs.kde.org/show_bug.cgi?id=447454)
- Fix a similar issue with Krita resource bundles with an upper case .BUNDLE extension
- Fix the macOS entitlements to allow uploading Krita to the Steam Store
- Fix the macOS entitlements so Krita can be accepted by the MacOS App Store
- Make Krita use the native macOS file dialog by default
- Remove the tkInter module from the embedded Python libraries on macOS.
- Fix rendering 16 bit integer images on macOS on the M1 architecture
- Fix a crash when undoing multiple layer operations too quickly. [BUG:447462](https://bugs.kde.org/show_bug.cgi?id=447462)
- Workaround a crash when a transform mask is applied to a passthrough group. [BUG:447506](https://bugs.kde.org/show_bug.cgi?id=447506)
- Filter out two new Epic Store single-dash-multi-character commandline options. Really, Epic, it's bad for to pass commandline parameters in this format!
- Fix toolbox arrow buttons not visible on starting Krita
- Fix the photoshop compatibilty shortcut profile. [BUG:447771](https://bugs.kde.org/show_bug.cgi?id=447771)
- Fix bundling AppimageUpdate into appimages.
- Restore the QImageIO fallback for loading WebP images
- Make the dock widget titlebars so they can be smaller
- Disable all accelerator keys for dockers
- Fix a race condition in the image metadata system
- Fix the tool option widget's layout sporadically going wrong. [BUG:447522](https://bugs.kde.org/show_bug.cgi?id=447522)
- Update fill layers correctly when changing the options from a Python script. [BUG:447807](https://bugs.kde.org/show_bug.cgi?id=447807)
- Fix the built-in file dialog's image preview. [BUG:447806](https://bugs.kde.org/show_bug.cgi?id=447806)
- Fix the slowness opening and closing documents if there are many resource bundles present. [BUG:447298](https://bugs.kde.org/show_bug.cgi?id=447298)
- Fix clicking external urls on Android
- Work around a possible crash on Android due to bugs in Qt's Accessibilty framework.
- Fix importing bundles on Android
- Work around issues with file permissions not being set correctly by ChromeOS

![](images/2021-11-16_kiki-piggy-bank_krita5.png) Krita 是自由、免費及開源的專案。請考慮[加入 Krita 發展基金](https://fund.krita.org/)、[損款](https://krita.org/en/support-us/donations/)，或[購買教學影片](https://krita.org/en/shop/)支持我們吧！得到您們的熱心支持，我們才能夠讓核心開發者全職為 Krita 工作。

## 下載

### Windows

如果你使用免安裝版：請注意，免安裝版仍然會與安裝版本共用設定檔及資源。如希望以免安裝版測試並回報程式強制終止的問題，請同時下載偵錯符號 (debug symbols)。

注意：我們已不再提供為 32 位元 Windows 建置的版本。

- 64 位元安裝程式：[krita-x64-5.0.2-setup.exe](https://download.kde.org/stable/krita/5.0.2/krita-x64-5.0.2-setup.exe)
- 64 位元免安裝版：[krita-x64-5.0.2.zip](https://download.kde.org/stable/krita/5.0.2/krita-x64-5.0.2.zip)
- [偵錯符號（請解壓到 Krita 程式資料夾之中）](https://download.kde.org/stable/krita/5.0.2/krita-x64-5.0.2-dbg.zip)

### Linux

- 64 位元 Linux AppImage：[krita-5.0.2-x86\_64.appimage](https://download.kde.org/stable/krita/5.0.2/krita-5.0.2-x86_64.appimage)

Linux 版本現不再需要另行下載 G'Mic-Qt 外掛程式 AppImage。

### macOS

注意：如果你正在使用 macOS Sierra 或 High Sierra，請參見[這部影片](https://www.youtube.com/watch?v=3py0kgq95Hk)了解如何執行由開發者簽署的程式。

- macOS 套件：[krita-5.0.2.dmg](https://download.kde.org/stable/krita/5.0.2/krita-5.0.2.dmg)

### Android

我們仍視 ChomeOS 及 Android 的版本為**測試版本**。此版本或可能含有大量程式錯誤，而且仍有部份功能未能正常運作。由於使用者介面並未完善，軟體或須配合實體鍵盤才能使用全部功能。

- [64 位元 Intel CPU APK](https://download.kde.org/stable/krita/5.0.2/krita-x86_64-5.0.2-release-signed.apk)
- [32 位元 Intel CPU APK](https://download.kde.org/stable/krita/5.0.2/krita-x86-5.0.2-release-signed.apk)
- [64 位元 Arm CPU APK](https://download.kde.org/stable/krita/5.0.2/krita-arm64-v8a-5.0.2-release-signed.apk)
- [32 位元 Arm CPU APK](https://download.kde.org/stable/krita/5.0.2/krita-armeabi-v7a-5.0.2-release-signed.apk)

### 原始碼

- [krita-5.0.2.tar.gz](https://download.kde.org/stable/krita/5.0.2/krita-5.0.2.tar.gz)
- [krita-5.0.2.tar.xz](https://download.kde.org/stable/krita/5.0.2/krita-5.0.2.tar.xz)

### md5sum

下載檔案的 MD5 校對碼已於以下檔案中列出：

- [md5sum.txt](https://download.kde.org/stable/krita/5.0.2/md5sum.txt)

### 數位簽章

Linux AppImage 以及原始碼的 .tar.gz 和 .tar.xz 壓縮檔已使用數位簽章簽名。你可以從[這裡](https://files.kde.org/krita/4DA79EDA231C852B)取得 GPG 公鑰。簽名檔可於[此處](https://download.kde.org/stable/krita/5.0.2/)找到（副檔名為 .sig）。

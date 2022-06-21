---
title: "發佈 Krita 5.0.2 修正版本"
date: "2022-01-07"
categories: 
  - "news_zh-hk"
  - "officialrelease_zh-hk"
---

喺正式發佈咗 Krita 5.0 之後，我哋並冇停低，而依家我哋就要發佈第一個修正版本喇！（今次嘅版本編號係 5.0.2，咁係因為我哋喺 Microsoft Store 做測試嗰陣用咗 5.0.0 依個版本編號，導致喺正式發佈 5.0 嘅時候需要改用 5.0.1……咁所以唔使擔心，你並冇錯過 5.0.1 版本呀！）

今次更新包含咗以下修正： （譯者按：由於內容太多而人力資源有限，所以依段唔做完整嘅翻譯，保留返英文原文。）

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

![](images/2021-11-16_kiki-piggy-bank_krita5.png) Krita 係自由、免費同開源嘅專案。請考慮[加入 Krita 發展基金](https://fund.krita.org/)、[損款](https://krita.org/en/support-us/donations/)，或者[購買教學影片](https://krita.org/en/shop/)支持我哋啦！有你哋嘅熱心支持，我哋先可以俾核心開發者全職為 Krita 工作。

## 下載

### Windows

如果你使用免安裝版：請注意，免安裝版仍然會同安裝版本共用設定檔同埋資源。如果想用免安裝版測試並回報 crash 嘅問題，請同時下載偵錯符號 (debug symbols)。

注意：我哋依家唔再提供為 32 位元 Windows 建置嘅版本。

- 64 位元安裝程式：[krita-x64-5.0.2-setup.exe](https://download.kde.org/stable/krita/5.0.2/krita-x64-5.0.2-setup.exe)
- 64 位元免安裝版：[krita-x64-5.0.2.zip](https://download.kde.org/stable/krita/5.0.2/krita-x64-5.0.2.zip)
- [偵錯符號 Debug symbols（請解壓到 Krita 程式資料夾入面）](https://download.kde.org/stable/krita/5.0.2/krita-x64-5.0.2-dbg.zip)

### Linux

- 64 位元 Linux AppImage：[krita-5.0.2-x86\_64.appimage](https://download.kde.org/stable/krita/5.0.2/krita-5.0.2-x86_64.appimage)

Linux 版本依家唔使再另外下載 G'Mic-Qt 外掛程式 AppImage。

### macOS

注意：如果你用緊 macOS Sierra 或者 High Sierra，請睇下[依段影片](https://www.youtube.com/watch?v=3py0kgq95Hk)了解點樣執行開發者簽署嘅程式。

- macOS 套件：[krita-5.0.2.dmg](https://download.kde.org/stable/krita/5.0.2/krita-5.0.2.dmg)

### Android

我哋提供嘅 ChomeOS 同 Android 版本仲係**測試版本**。依個版本或可能含有大量嘅 bug，而且仲有部份功能未能正常運作。由於使用者介面仲未改進好，軟件或者須要配合實體鍵盤先可以用到全部功能。

- [64 位元 Intel CPU APK](https://download.kde.org/stable/krita/5.0.2/krita-x86_64-5.0.2-release-signed.apk)
- [32 位元 Intel CPU APK](https://download.kde.org/stable/krita/5.0.2/krita-x86-5.0.2-release-signed.apk)
- [64 位元 Arm CPU APK](https://download.kde.org/stable/krita/5.0.2/krita-arm64-v8a-5.0.2-release-signed.apk)
- [32 位元 Arm CPU APK](https://download.kde.org/stable/krita/5.0.2/krita-armeabi-v7a-5.0.2-release-signed.apk)

### 原始碼

- [krita-5.0.2.tar.gz](https://download.kde.org/stable/krita/5.0.2/krita-5.0.2.tar.gz)
- [krita-5.0.2.tar.xz](https://download.kde.org/stable/krita/5.0.2/krita-5.0.2.tar.xz)

### md5sum

下載檔案嘅 MD5 校對碼可以喺依個檔案入面揾到：

- [md5sum.txt](https://download.kde.org/stable/krita/5.0.2/md5sum.txt)

### 數碼簽署

Linux AppImage 以及原始碼嘅 .tar.gz 同 .tar.xz 壓縮檔已使用數碼簽署簽名。你可以由[依度](https://files.kde.org/krita/4DA79EDA231C852B)取得 public key。簽名檔可以喺[依度](https://download.kde.org/stable/krita/5.0.2/)揾到（副檔名為 .sig）。

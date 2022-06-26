---
title: "Krita 4.4.3 第二測試版本 (beta 2) 已推出"
date: "2021-03-12"
categories: 
  - "news_zh-tw"
  - "development-builds_zh-tw"
---

Krita 開發團隊現推出 Krita 4.4.3 的第二個測試版本。此版本修正了某些於上一個測試版本發現的程式錯誤。我們仍需要大家幫忙測試一下。

- Thanks to Jonathan Wakely, Krita 4.4.3 beta 2 now can be compiled with GCC 11.
- Fixed: a crash when showing the popup palette on Linux if the display was set to 125% ([BUG:431944](https://bugs.kde.org/show_bug.cgi?id=431944))
- Fixed: tiling artefacts in the oilpaint filter
- Fixed an issue showing that there are updates available in the welcome screen when the latest version was already running
- If the image name no longer fits the tab, the right-hand side is elided, instead of the middle
- Fixed: using shortcuts with special keys on non-US layouts ([BUG:430479](https://bugs.kde.org/show_bug.cgi?id=430479))

## 下載

### Windows

如果你使用免安裝版：請注意，免安裝版仍然會與安裝版本共用設定檔及資源。如希望以免安裝版測試並回報程式強制終止的問題，請同時下載偵錯符號 (debug symbols)。

- 64 位元安裝程式：[krita-x64-4.4.3-beta2-setup.exe](https://download.kde.org/unstable/krita/4.4.3-beta2/krita-x64-4.4.3-beta2-setup.exe)
- 64 位元免安裝版：[krita-x64-4.4.3-beta2.zip](https://download.kde.org/unstable/krita/4.4.3-beta2/krita-x64-4.4.3-beta2.zip)
- [偵錯符號（請解壓到 Krita 程式資料夾之中）](https://download.kde.org/unstable/krita/4.4.3-beta2/krita-x64-4.4.3-beta2-dbg.zip)

- 32 位元安裝程式：[krita-x86-4.4.3-beta2-setup.exe](https://download.kde.org/unstable/krita/4.4.3-beta2/krita-x86-4.4.3-beta2-setup.exe)
- 32 位元免安裝版：[krita-x86-4.4.3-beta2.zip](https://download.kde.org/unstable/krita/4.4.3-beta2/krita-x86-4.4.3-beta2.zip)
- [偵錯符號（請解壓到 Krita 程式資料夾之中）](https://download.kde.org/unstable/krita/4.4.3-beta2/krita-x86-4.4.3-beta2-dbg.zip)

### Linux

- 64 位元 Linux AppImage：[krita-4.4.3-beta2-x86_64.appimage](https://download.kde.org/unstable/krita/4.4.3-beta2/krita-4.4.3-beta2-x86_64.appimage)
- 64 位元 Linux [G'Mic-Qt 外掛程式 AppImage](https://download.kde.org/unstable/krita/4.4.3-beta2/gmic_krita_qt-x86_64.appimage)

### macOS

- macOS 套件：[krita-4.4.3-beta2.dmg](https://download.kde.org/unstable/krita/4.4.3-beta2/krita-4.4.3-beta2.dmg)

備註：gmic-qt 未支援 macOS。

### Android

我們仍視 ChomeOS 及 Android 的版本為**測試版本**。此版本或可能含有大量程式錯誤，而且仍有部份功能未能正常運作。由於使用者介面並未完善，軟體或須配合實體鍵盤才能使用全部功能。

- [64 位元 Intel CPU APK](https://download.kde.org/unstable/krita/4.4.3-beta2/krita_x86_64_apk-4.4.3-beta2.apk)
- [32 位元 Intel CPU APK](https://download.kde.org/unstable/krita/4.4.3-beta2/krita_x86_apk-4.4.3-beta2.apk)
- [64 位元 Arm CPU APK](https://download.kde.org/unstable/krita/4.4.3-beta2/krita_arm64-v8a_apk-4.4.3-beta2.apk)
- [32 位元 Arm CPU APK](https://download.kde.org/unstable/krita/4.4.3-beta2/krita_armeabi-v7a_apk-4.4.3-beta2.apk)

### 原始碼

- [krita-4.4.3-beta2.tar.gz](https://download.kde.org/unstable/krita/4.4.3-beta2/krita-4.4.3-beta2.tar.gz)
- [krita-4.4.3-beta2.tar.xz](https://download.kde.org/unstable/krita/4.4.3-beta2/krita-4.4.3-beta2.tar.xz)

### md5sum

下載檔案的 MD5 校對碼已於以下檔案中列出：

- [md5sum.txt](https://download.kde.org/unstable/krita/4.4.3-beta2/md5sum.txt)

### 數位簽章

Linux AppImage 以及原始碼的 .tar.gz 和 .tar.xz 壓縮檔已使用數位簽章簽名。你可以運行 "gpg --recv-key 7468332F" 以取得 GPG 公鑰。簽名檔可於[此處](https://download.kde.org/unstable/krita/4.4.3-beta2/)找到（副檔名為 .sig）。

## 支持 Krita

Krita 是免費及開放原始碼的項目。請考慮[捐款](https://krita.org/en/support-us/donations/)或[購買教學影片](https://krita.org/en/shop/)支持我們吧！有你的支持我們才能聘請開發人員全職進行 Krita 的開發工作。

---
title: "發佈 Krita 4.4.1 修正版本"
date: "2020-10-29"
categories: 
  - "officialrelease_zh-tw"
---

由於 Krita 4.4.0 出現了數項 4.3.0 中不存在的程式錯誤，因此我們現在發佈 Krita 4.4.1 修正版本。此版本含以下修正：

- Android 及 ChromeOS：
    - 使用 SDK version 29，這表示 Krita 不用要求額外權限，並能更容易存取外部檔案；Krita 亦已更新至使用 NDK 20 或更高版本
    - 修正拾色器問題（[BUG:423254](https://bugs.kde.org/show_bug.cgi?id=423254)）
    - 修正使用浮動畫具板時輸入事件會傳送到畫布的問題
    - 使用裝置的語言設定，令使用者介面可以顯示已本地化的文字（[BUG:427692](https://bugs.kde.org/show_bug.cgi?id=427692)）
    - 修正 Android 複製貼上的問題（[BUG:423199](https://bugs.kde.org/show_bug.cgi?id=423199)）
- 修正於載入含圖案填充圖層的檔案時程式強制終止的問題（[BUG:427866](https://bugs.kde.org/show_bug.cgi?id=427866))
- 修正不能正常載入含向量選取區域的遮罩的問題（[BUG:428332](https://bugs.kde.org/show_bug.cgi?id=428332)）
- 修正連按兩下文字物件時程式強制終止的問題（[BUG:427858](https://bugs.kde.org/show_bug.cgi?id=427858)）
- 修正在柵格選取區域使用移動工具時程式強制終止的問題（[BUG:428260](https://bugs.kde.org/show_bug.cgi?id=428260)）

## 下載

### Windows

如果你使用免安裝版：請注意，免安裝版仍然會與安裝版本共用設定檔及資源。如希望以免安裝版測試並回報程式強制終止的問題，請同時下載偵錯符號（debug symbols）。

- 64 位元安裝程式：[krita-x64-4.4.1-setup.exe](https://download.kde.org/stable/krita/4.4.1/krita-x64-4.4.1-setup.exe)
- 64 位元免安裝版：[krita-x64-4.4.1.zip](https://download.kde.org/stable/krita/4.4.1/krita-x64-4.4.1.zip)
- [偵錯符號（請解壓到 Krita 程式資料夾之中）](https://download.kde.org/stable/krita/4.4.1/krita-x64-4.4.1-dbg.zip)

- 32 位元安裝程式：[krita-x86-4.4.1-setup.exe](https://download.kde.org/stable/krita/4.4.1/krita-x86-4.4.1-setup.exe)
- 32 位元免安裝版：[krita-x86-4.4.1.zip](https://download.kde.org/stable/krita/4.4.1/krita-x86-4.4.1.zip)
- [偵錯符號（請解壓到 Krita 程式資料夾之中）](https://download.kde.org/stable/krita/4.4.1/krita-x86-4.4.1-dbg.zip)

### Linux

- 64 位元 Linux AppImage：[krita-4.4.1-x86\_64.appimage](https://download.kde.org/stable/krita/4.4.1/krita-4.4.1-x86_64.appimage)
- 64 位元 Linux [G'Mic-Qt 外掛程式 AppImage](https://download.kde.org/stable/krita/4.4.1/gmic_krita_qt-x86_64.appimage)

### macOS

- macOS 套件：[krita-4.4.1.dmg](https://download.kde.org/stable/krita/4.4.1/krita-4.4.1.dmg)

備註：gmic-qt 未支援 macOS。

### ChromeOS 及 Android Beta 測試版本

我們仍視 ChomeOS 及 Android 的版本為**測試版本**。此版本或可能含有大量程式錯誤，而且仍有部份功能未能正常運作。由於使用者介面並未完善，軟體或須配合實體鍵盤才能使用全部功能。

- [64 位元 Intel CPU APK](https://download.kde.org/stable/krita/4.4.1/krita-x86_64-4.4.1-release.apk)
- [32 位元 Intel CPU APK](https://download.kde.org/stable/krita/4.4.1/krita-x86-4.4.1-release.apk)
- [64 位元 Arm CPU APK](https://download.kde.org/stable/krita/4.4.1/krita-arm64-4.4.1-release.apk)
- [32 位元 Arm CPU APK](https://download.kde.org/stable/krita/4.4.1/krita-arm32-4.4.1-release.apk)

### 原始碼

- [krita-4.4.1.tar.gz](https://download.kde.org/stable/krita/4.4.1/krita-4.4.1.tar.gz)
- [krita-4.4.1.tar.xz](https://download.kde.org/stable/krita/4.4.1/krita-4.4.1.tar.xz)

### md5sum

下載檔案的 MD5 校對碼已於以下檔案中列出：

- [md5sum.txt](https://download.kde.org/stable/krita/4.4.1/md5sum.txt)

## 支持 Krita

Krita 是免費及開放原始碼的項目。請考慮[捐款](https://krita.org/en/support-us/donations/)或[購買教學影片](https://krita.org/en/shop/)支持我們吧！有你的支持我們才能聘請開發人員全職進行 Krita 的開發工作。

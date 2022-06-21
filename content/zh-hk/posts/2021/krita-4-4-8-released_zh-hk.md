---
title: "發佈 Krita 4.4.8 修正版本"
date: "2021-08-25"
categories: 
  - "news_zh-hk"
  - "officialrelease_zh-hk"
---

今次認真真係 Krita 5.0 發佈前嘅最後一個 4.4 修正版本。我們修正咗一個關於嵌入調色板資料流失嘅問題，而且改咗預設會停用喺 Windows 上嘅非整數 Hi-DPI（高解像度）縮放支援。

## 下載

### Windows

如果你使用免安裝版：請注意，免安裝版仍然會同安裝版本共用設定檔同埋資源。如果想用免安裝版測試並回報 crash 嘅問題，請同時下載 debug symbols。

注意：我哋依家唔再提供為 32 位元 Windows 建置嘅版本。

- 64 位元安裝程式：[krita-x64-4.4.8-setup.exe](https://download.kde.org/stable/krita/4.4.8/krita-x64-4.4.8-setup.exe)
- 64 位元免安裝版：[krita-x64-4.4.8.zip](https://download.kde.org/stable/krita/4.4.8/krita-x64-4.4.8.zip)
- [Debug symbols（請解壓到 Krita 程式資料夾入面）](https://download.kde.org/stable/krita/4.4.8/krita-x64-4.4.8-dbg.zip)

### Linux

- 64 位元 Linux AppImage：[krita-4.4.8-x86\_64.appimage](https://download.kde.org/stable/krita/4.4.8/krita-4.4.8-x86_64.appimage)
- 64 位元 Linux [G'Mic-Qt 外掛程式 AppImage](https://download.kde.org/stable/krita/4.4.8/gmic_krita_qt-x86_64.appimage)

### macOS

注意：如果你用緊 macOS Sierra 或者 High Sierra，請睇下[依段影片](https://www.youtube.com/watch?v=3py0kgq95Hk)了解點樣執行開發者簽署嘅程式。

- macOS 套件：[krita-4.4.8.dmg](https://download.kde.org/stable/krita/4.4.8/krita-4.4.8.dmg)

備註：gmic-qt 未支援 macOS。

### Android

由於我哋嘅建置環境為咗 Krita 5.0 Beta 1 做咗啲改動，依家我們唔能夠提供俾 Android 用嘅 4.4.8 更新版本。

### 原始碼

- [krita-4.4.8.tar.gz](https://download.kde.org/stable/krita/4.4.8/krita-4.4.8.tar.gz)
- [krita-4.4.8.tar.xz](https://download.kde.org/stable/krita/4.4.8/krita-4.4.8.tar.xz)

### md5sum

下載檔案嘅 MD5 校對碼可以喺依個檔案入面搵到：

- [md5sum.txt](https://download.kde.org/stable/krita/4.4.8/md5sum.txt)

### 數碼簽署

Linux AppImage 以及原始碼嘅 .tar.gz 同 .tar.xz 壓縮檔已使用數碼簽署簽名。你可以由[依度](https://files.kde.org/krita/4DA79EDA231C852B)取得 public key。簽名檔可以喺[依度](https://download.kde.org/stable/krita/4.4.8/)搵到（副檔名為 .sig）。

## 支持 Krita

Krita 係免費及開放原始碼嘅項目。請考慮[捐款](https://fund.krita.org)或者[購買教學影片](https://krita.org/en/shop/)支持我哋啦！有你嘅支持我哋先可以聘請開發人員全職進行 Krita 嘅開發工作。

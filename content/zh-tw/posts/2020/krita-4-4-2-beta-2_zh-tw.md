---
title: "Krita 4.4.2 第二測試版本 (beta 2) 已推出"
date: "2020-12-24"
categories: 
  - "development-builds_zh-tw"
---

Krita 開發團隊現推出 Krita 4.4.2 的第二個測試版本。Ramon Miranda 亦發佈了一段介紹此版本的新功能⸺網狀變形⸺的影片（只提供英文）：

https://www.youtube.com/watch?v=DLXWynZT\_8s&feature=youtu.be

與[第一個測試版本](https://krita.org/zh-tw/item/krita-4-4-2-beta-1_zh-tw/)相比，這個版本修正了以下的問題：

- 修正在套用網狀變形時向量圖層顯示出錯的問題
- 修正等角網格顯示更新及繪製出錯的問題 ([BUG:427833](https://bugs.kde.org/show_bug.cgi?id=427833))
- 修正三角形拾色器在高解像度縮放顯示之下滑鼠輸入失效的問題
- 改善 MyPaint 光影拾色器的效能和外觀
- 修正在動畫影格中分組圖層的變形預覽 ([BUG:413968](https://bugs.kde.org/show_bug.cgi?id=413968))
- 加入支援連續變形⸺在完成一次變形之後，按住 Shift 並按一下圖層即可進行下一次變形
- 加入切換網格控制柄對稱模式的選項
- 當 Krita 以 Wayland 平台執行時，Krita 會顯示一項警告訊息，指出 Krita 現時不支援 Wayland 平台 ([BUG:430426](https://bugs.kde.org/show_bug.cgi?id=430426), [BUG:429079](https://bugs.kde.org/show_bug.cgi?id=429079))
- 修正在使用選取區域工具時輔助尺的顯示問題 ([BUG:427658](https://bugs.kde.org/show_bug.cgi?id=427658))
- 修正在修改向量圖形貝茲曲線線段時的問題 ([BUG:430377](https://bugs.kde.org/show_bug.cgi?id=430377))
- 修正載入產生器圖層的問題 ([BUG:430246](https://bugs.kde.org/show_bug.cgi?id=430246), [BUG:430244](https://bugs.kde.org/show_bug.cgi?id=430244))
- 修正在拖放空白圖層時程式強制終止的問題 ([BUG:429049](https://bugs.kde.org/show_bug.cgi?id=429049))
- 停用 macOS 的 QuickLook 整合外掛程式（縮圖產生外掛），因其可能會導致 Finder 當機 ([BUG:430553](https://bugs.kde.org/show_bug.cgi?id=430553))
- 修正歡迎畫面上檔案縮圖的尺寸 ([BUG:430359](https://bugs.kde.org/show_bug.cgi?id=430359))

此版本亦加入了六個由 Ramon Miranda 新設計的筆刷預設：

[![](images/rgba_brushes.png)](https://krita.org/wp-content/uploads/2020/12/rgba_brushes.png)

## 下載

### Windows

如果你使用免安裝版：請注意，免安裝版仍然會與安裝版本共用設定檔及資源。如希望以免安裝版測試並回報程式強制終止的問題，請同時下載偵錯符號 (debug symbols)。

- 64 位元安裝程式：[krita-x64-4.4.2-beta2-setup.exe](https://download.kde.org/unstable/krita/4.4.2-beta2/krita-x64-4.4.2-beta2-setup.exe)
- 64 位元免安裝版：[krita-x64-4.4.2-beta2.zip](https://download.kde.org/unstable/krita/4.4.2-beta2/krita-x64-4.4.2-beta2.zip)
- [偵錯符號（請解壓到 Krita 程式資料夾之中）](https://download.kde.org/unstable/krita/4.4.2-beta2/krita-x64-4.4.2-beta2-dbg.zip)

- 32 位元安裝程式：[krita-x86-4.4.2-beta2-setup.exe](https://download.kde.org/unstable/krita/4.4.2-beta2/krita-x86-4.4.2-beta2-setup.exe)
- 32 位元免安裝版：[krita-x86-4.4.2-beta2.zip](https://download.kde.org/unstable/krita/4.4.2-beta2/krita-x86-4.4.2-beta2.zip)
- [偵錯符號（請解壓到 Krita 程式資料夾之中）](https://download.kde.org/unstable/krita/4.4.2-beta2/krita-x86-4.4.2-beta2-dbg.zip)

### Linux

- 64 位元 Linux AppImage：[krita-4.4.2-beta2-x86\_64.appimage](https://download.kde.org/unstable/krita/4.4.2-beta2/krita-4.4.2-beta2-x86_64.appimage)
- 64 位元 Linux [G'Mic-Qt 外掛程式 AppImage](https://download.kde.org/unstable/krita/4.4.2-beta2/gmic_krita_qt-x86_64.appimage)

### macOS

- macOS 套件：[krita-4.4.2-beta2.dmg](https://download.kde.org/unstable/krita/4.4.2-beta2/krita-4.4.2-beta2.dmg)

備註：gmic-qt 未支援 macOS。

### Android

我們仍視 ChomeOS 及 Android 的版本為**測試版本**。此版本或可能含有大量程式錯誤，而且仍有部份功能未能正常運作。由於使用者介面並未完善，軟體或須配合實體鍵盤才能使用全部功能。

- [64 位元 Intel CPU APK](https://download.kde.org/unstable/krita/4.4.2-beta2/krita-x86_64-4.4.2-beta2.apk)
- [32 位元 Intel CPU APK](https://download.kde.org/unstable/krita/4.4.2-beta2/krita-x86-4.4.2-beta2.apk)
- [64 位元 Arm CPU APK](https://download.kde.org/unstable/krita/4.4.2-beta2/krita-arm64-4.4.2-beta2.apk)
- [32 位元 Arm CPU APK](https://download.kde.org/unstable/krita/4.4.2-beta2/krita-arm32-4.4.2-beta2.apk)

### 原始碼

- [krita-4.4.2-beta2.tar.gz](https://download.kde.org/unstable/krita/4.4.2-beta2/krita-4.4.2-beta2.tar.gz)
- [krita-4.4.2-beta2.tar.xz](https://download.kde.org/unstable/krita/4.4.2-beta2/krita-4.4.2-beta2.tar.xz)

### md5sum

下載檔案的 MD5 校對碼已於以下檔案中列出：

- [md5sum.txt](https://download.kde.org/unstable/krita/4.4.2-beta2/md5sum.txt)

## 支持 Krita

Krita 是免費及開放原始碼的項目。請考慮[捐款](https://krita.org/en/support-us/donations/)或[購買教學影片](https://krita.org/en/shop/)支持我們吧！有你的支持我們才能聘請開發人員全職進行 Krita 的開發工作。

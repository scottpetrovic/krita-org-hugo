---
title: "現已發佈 Krita 5.0 嘅首個測試版本 (Beta 1)"
date: "2021-08-18"
categories: 
  - "news_zh-hk"
  - "development-builds_zh-hk"
---

今日，Krita 開發團隊推出咗 Krita 5.0 嘅首個 beta 測試版本。Krita 5.0 係一個重大更新，包含咗大量嘅新功能同埋改動。

[![](/images/posts/2021/electrichearts_20201224A_kiki_c1_1080P-1024x512.png)](https://krita.org/wp-content/uploads/2021/08/electrichearts_20201224A_kiki_c1_1080P.png) 由 Tyson Tan 繪畫創作嘅新版啟動畫面圖片

首先係一啲**注意事項**：

- Krita 5 帶有一個全新嘅資源管理系統。Krita 唔再喺啟動時重新載入全部嘅筆刷預設、圖案、漸變等等嘅資源，取而代之係喺首次啟動時載入並建立一個快取資料庫。Krita 5 喺首次啟動時會用多啲時間，但之後嘅每次啟動會比以前快。
- Krita 5 用一個不兼容 Krita 4 嘅方式嚟儲存用家修改資源嘅歷史。當你使用過 Krita 5 之後，降返去 Krita 4 嘅話有可能會喺 Krita 4 入面見到重複嘅資源。
- Krita 5 唔再支援載入由 Krita 3 或更舊版本整嘅向量圖層。
- 用 Krita 5.0 整嘅 Krita 文件 (.kra) 同 Krita 筆刷預設檔案 (.kpp) 並**唔保證**能夠兼容 Krita 4！
- Krita 5.0 修正咗一個[同文件入面文字大細相關嘅 bug](https://krita.org/en/krita-5-0-release-notes/#text_size_dpi_issue_fix)。遺憾嘅係，依項修正導致喺開啟由較舊版本整嘅文件時或者須要[修改一項設定](https://docs.krita.org/en/reference_manual/preferences/general_settings.html#miscellaneous)先可以令文件入面嘅文字顯示為預期正確嘅大細。
- Beta 1 已知問題：喺使用 G'Mic 濾鏡之後，Krita 嘅設定值將暫時被重設到預設值。重新開啟 Krita 後，本身嘅自訂設定將會被還原。

咁依個版本入面有啲咩新嘢呢？答案喺：[好多呀！](https://krita.org/en/krita-5-0-release-notes/)完整嘅[發佈通告](https://krita.org/en/krita-5-0-release-notes/)入面有更詳細嘅說明，而依度列出咗部份較重大嘅事項：

- 開發歷時五年嘅新資源系統
- 漸變抖色同埋寛色域漸變
- 由 LittleCMS fastfloat 外掛帶嚟效能改進
- 全新嘅 MyPaint 筆刷引擎
- 經重新編寫嘅色彩塗抹筆刷引擎
- 重新設計後嘅動畫時間軸工具面板
- 動畫用嘅再製影格
- 更新嘅動畫曲線工具面板
- 變形遮罩動畫支援
- 全新嘅分鏡圖功能
- 重新設計咗圖示同埋潤飾介面
- 加入 HEIF、AVIF、WebP 影像格式嘅支援
- 改善對 TIFF 影像格式嘅支援
- 全新嘅繪畫過程錄影工具
- 全新嘅兩點透視輔助尺，以及一個限制輔助尺運作區域嘅功能
- 變形工具依家可以顯示圖層堆疊中嘅預覽，即係變形嘅時候可以同時預覽圖層嘅混色模式、不透明度、濾鏡、遮罩等效果
- 新增貼上到使用中圖層而唔係貼上為新圖層嘅功能
- G'Mic 外掛程式濾鏡依家支援 macOS

此外仲有大量嘅小改進、小功能同埋效能改進！

**正體中文改動：**喺 Krita 5.0，翻譯者為正體中文翻譯做咗唔少改動，當中修正咗一些唔符合一般正體中文慣例嘅語句或者用詞，並為一部份功能重新改名。詳情請參見[正體中文版本嘅發佈通告](https://krita.org/zh-hk/krita-5-0-release-notes_zh-hk/#trad-chinese-changes)。

[![Krita，在使用舊嘅 Oxygen 樣式](/images/posts/2021/krita-style-change-1024x533.png)](https://krita.org/wp-content/uploads/2021/08/krita-style-change.png)

我們希望可以喺九月發佈正式版，不過唔一定保證會做到㗎！喺之前，我哋會繼續修正大家喺試用 Beta 同埋 Nightly 測試版本時所發現嘅 bug，目標喺正式發佈 Krita 5 嘅時候能夠推出一個運作穩定及暢順嘅繪畫程式。請考慮向 [Krita 發展基金](https://fund.krita.org/)捐款以支持 Krita 嘅開發工作：

[![](/images/posts/2021/devfund-1024x346.png)](https://fund.krita.org)

## 下載

### Windows

如果你使用免安裝版：請注意，免安裝版仍然會同安裝版本共用設定檔同埋資源。如果想用免安裝版測試並回報 crash 嘅問題，請同時下載 debug symbols。

注意：我哋依家唔再提供為 32 位元 Windows 建置嘅版本。

- 64 位元安裝程式：[krita-x64-5.0.0-beta1-setup.exe](https://download.kde.org/unstable/krita/5.0.0-beta1/krita-x64-5.0.0-beta1-setup.exe)
- 64 位元免安裝版：[krita-x64-5.0.0-beta1.zip](https://download.kde.org/unstable/krita/5.0.0-beta1/krita-x64-5.0.0-beta1.zip)
- [Debug symbols（請解壓到 Krita 程式資料夾入面）](https://download.kde.org/unstable/krita/5.0.0-beta1/krita-x64-5.0.0-beta1-dbg.zip)

### Linux

- 64 位元 Linux AppImage：[krita-5.0.0-beta1-x86\_64.appimage](https://download.kde.org/unstable/krita/5.0.0-beta1/krita-5.0.0-beta1-x86_64.appimage)

Linux 版本唔使再另外下載 G'Mic-Qt 外掛程式 AppImage。

### macOS

注意：如果你用緊 macOS Sierra 或者 High Sierra，請睇下[依段影片](https://www.youtube.com/watch?v=3py0kgq95Hk)了解點樣執行開發者簽署嘅程式。

- macOS 套件：[krita-5.0.0-beta1.dmg](https://download.kde.org/unstable/krita/5.0.0-beta1/krita-5.0.0-beta1.dmg)

### Android

我哋提供嘅 ChomeOS 同 Android 版本仲係**測試版本**。依個版本或可能含有大量嘅 bug，而且仲有部份功能未能正常運作。由於使用者介面仲未改進好，軟件或者須要配合實體鍵盤先可以用到全部功能。

- [64 位元 Intel CPU APK](https://download.kde.org/unstable/krita/5.0.0-beta1/krita-x86_64-5.0.0-beta1-release-signed.apk)
- [32 位元 Intel CPU APK](https://download.kde.org/unstable/krita/5.0.0-beta1/krita-x86-5.0.0-beta1-release-signed.apk)
- [64 位元 Arm CPU APK](https://download.kde.org/unstable/krita/5.0.0-beta1/krita-arm64-v8a-5.0.0-beta1-release-signed.apk)
- [32 位元 Arm CPU APK](https://download.kde.org/unstable/krita/5.0.0-beta1/krita-armeabi-v7a-5.0.0-beta1-release-signed.apk)

### 原始碼

- [krita-5.0.0-beta1.tar.gz](https://download.kde.org/unstable/krita/5.0.0-beta1/krita-5.0.0-beta1.tar.gz)
- [krita-5.0.0-beta1.tar.xz](https://download.kde.org/unstable/krita/5.0.0-beta1/krita-5.0.0-beta1.tar.xz)

### md5sum

下載檔案嘅 MD5 校對碼可以喺依個檔案入面搵到：

- [md5sum.txt](https://download.kde.org/unstable/krita/5.0.0-beta1/md5sum.txt)

### 數碼簽署

Linux AppImage 以及原始碼嘅 .tar.gz 同 .tar.xz 壓縮檔已使用數碼簽署簽名。你可以由[依度](https://files.kde.org/krita/4DA79EDA231C852B)取得 public key。簽名檔可以喺[依度](https://download.kde.org/unstable/krita/5.0.0-beta1/)搵到（副檔名為 .sig）。

## 支持 Krita

Krita 係免費及開放原始碼嘅項目。請考慮[捐款](https://fund.krita.org)或者[購買教學影片](https://krita.org/en/shop/)支持我哋啦！有你嘅支持我哋先可以聘請開發人員全職進行 Krita 嘅開發工作。

---
title: "現已發佈 Krita 5.0 的首個測試版本 (Beta 1)"
date: "2021-08-18"
categories: 
  - "news_zh-tw"
  - "development-builds_zh-tw"
---

今天，Krita 開發團隊推出了 Krita 5.0 的首個 beta 測試版本。Krita 5.0 是一個重大更新，包含了大量的新功能及更動。

[![](/images/posts/2021/electrichearts_20201224A_kiki_c1_1080P-1024x512.png)](/images/posts/2021/electrichearts_20201224A_kiki_c1_1080P.png) 由 Tyson Tan 繪畫創作的新版啟動畫面影像

首先是一些**注意事項**：

- Krita 5 帶有一個全新的資源管理系統。Krita 不再於啟動時重新載入全部的筆刷預設、圖案、漸變等等的資源，取而代之是在首次啟動時載入並建立一個快取資料庫。Krita 5 在首次啟動時會耗用較多時間，但之後的每次啟動會較以往快。
- Krita 5 以一個不兼容 Krita 4 的方式來儲存使用者修改資源的歷程記錄。當你使用過 Krita 5 以後，降回 Krita 4 的話有可能會在 Krita 4 出現重複的資源。
- Krita 5 不再支援載入在 Krita 3 或更舊版本中建立的向量圖層。
- 在 Krita 5.0 中建立的 Krita 文件 (.kra) 和 Krita 筆刷預設檔案 (.kpp) 並**不保證**能夠與 Krita 4 兼容！
- Krita 5.0 修正了一個[與文件中文字大小相關的程式錯誤](https://krita.org/en/krita-5-0-release-notes/#text_size_dpi_issue_fix)。遺憾的是，這項修正導致在開啟由較舊版本建立的文件時或須[修改一項設定](https://docs.krita.org/en/reference_manual/preferences/general_settings.html#miscellaneous)才能使文件內的文字顯示為預期正確的大小。
- Beta 1 已知問題：在使用 G'Mic 濾鏡之後，Krita 的設定值將暫時被重設到預設值。重新開啟 Krita 後，先前的自訂設定將會被還原。

那麼，這個版本裡面有甚麼新鮮事呢？答案是：[好多啊！](https://krita.org/en/krita-5-0-release-notes/)完整的[發佈通告](https://krita.org/en/krita-5-0-release-notes/)內有更詳盡的解說，而這裡列出了部份較重大的事項：

- 開發歷時五年的新資源系統
- 漸變抖色及寛色域漸變
- 由 LittleCMS fastfloat 外掛帶來效能改進
- 全新的 MyPaint 筆刷引擎
- 經重新編寫的色彩塗抹筆刷引擎
- 重新設計後的動畫時間軸工具面板
- 動畫用的再製影格
- 更新的動畫曲線工具面板
- 變形遮罩動畫支援
- 全新的分鏡圖功能
- 重新設計了圖示和潤飾介面
- 加入 HEIF、AVIF、WebP 影像格式的支援
- 改善對 TIFF 影像格式的支援
- 全新的繪畫過程錄影工具
- 全新的兩點透視輔助尺，以及一個限制輔助尺運作區域的功能
- 變形工具現可顯示圖層堆疊中的預覽，即變形時可同時預覽圖層的混色模式、不透明度、濾鏡、遮罩等效果
- 新增貼上到使用中圖層而非貼上為新圖層的功能
- G'Mic 外掛程式濾鏡現支援 macOS

此外還有大量的小改進、小功能和效能改進！

**正體中文更動：**在 Krita 5.0，翻譯者為正體中文翻譯作出了不少更動，當中修正了一些不符合一般正體中文慣例的語句或用詞，並為一部份功能重新命名。詳情請參見[正體中文版本的發佈通告](https://krita.org/zh-tw/krita-5-0-release-notes_zh-tw/#trad-chinese-changes)。

[![Krita，在使用舊的 Oxygen 樣式](/images/posts/2021/krita-style-change-1024x533.png)](/images/posts/2021/krita-style-change.png)

我們希望可以在九月發佈正式版，不過這不一定保證會發生的啊！在此之前，我們會繼續修正大家在試用 Beta 及 Nightly 測試版本時所發現的問題，目標在正式發佈 Krita 5 的時候能夠推出一個運作穩定及順暢的繪畫程式。請考慮向 [Krita 發展基金](https://fund.krita.org/)捐款以支持 Krita 的開發工作：

[![](/images/posts/2021/devfund-1024x346.png)](https://fund.krita.org)

## 下載

### Windows

如果你使用免安裝版：請注意，免安裝版仍然會與安裝版本共用設定檔及資源。如希望以免安裝版測試並回報程式強制終止的問題，請同時下載偵錯符號 (debug symbols)。

注意：我們已不再提供為 32 位元 Windows 建置的版本。

- 64 位元安裝程式：[krita-x64-5.0.0-beta1-setup.exe](https://download.kde.org/unstable/krita/5.0.0-beta1/krita-x64-5.0.0-beta1-setup.exe)
- 64 位元免安裝版：[krita-x64-5.0.0-beta1.zip](https://download.kde.org/unstable/krita/5.0.0-beta1/krita-x64-5.0.0-beta1.zip)
- [偵錯符號（請解壓到 Krita 程式資料夾之中）](https://download.kde.org/unstable/krita/5.0.0-beta1/krita-x64-5.0.0-beta1-dbg.zip)

### Linux

- 64 位元 Linux AppImage：[krita-5.0.0-beta1-x86\_64.appimage](https://download.kde.org/unstable/krita/5.0.0-beta1/krita-5.0.0-beta1-x86_64.appimage)

Linux 版本現不再需要另行下載 G'Mic-Qt 外掛程式 AppImage。

### macOS

注意：如果你正在使用 macOS Sierra 或 High Sierra，請參見[這部影片](https://www.youtube.com/watch?v=3py0kgq95Hk)了解如何執行由開發者簽署的程式。

- macOS 套件：[krita-5.0.0-beta1.dmg](https://download.kde.org/unstable/krita/5.0.0-beta1/krita-5.0.0-beta1.dmg)

### Android

我們仍視 ChomeOS 及 Android 的版本為**測試版本**。此版本或可能含有大量程式錯誤，而且仍有部份功能未能正常運作。由於使用者介面並未完善，軟體或須配合實體鍵盤才能使用全部功能。

- [64 位元 Intel CPU APK](https://download.kde.org/unstable/krita/5.0.0-beta1/krita-x86_64-5.0.0-beta1-release-signed.apk)
- [32 位元 Intel CPU APK](https://download.kde.org/unstable/krita/5.0.0-beta1/krita-x86-5.0.0-beta1-release-signed.apk)
- [64 位元 Arm CPU APK](https://download.kde.org/unstable/krita/5.0.0-beta1/krita-arm64-v8a-5.0.0-beta1-release-signed.apk)
- [32 位元 Arm CPU APK](https://download.kde.org/unstable/krita/5.0.0-beta1/krita-armeabi-v7a-5.0.0-beta1-release-signed.apk)

### 原始碼

- [krita-5.0.0-beta1.tar.gz](https://download.kde.org/unstable/krita/5.0.0-beta1/krita-5.0.0-beta1.tar.gz)
- [krita-5.0.0-beta1.tar.xz](https://download.kde.org/unstable/krita/5.0.0-beta1/krita-5.0.0-beta1.tar.xz)

### md5sum

下載檔案的 MD5 校對碼已於以下檔案中列出：

- [md5sum.txt](https://download.kde.org/unstable/krita/5.0.0-beta1/md5sum.txt)

### 數位簽章

Linux AppImage 以及原始碼的 .tar.gz 和 .tar.xz 壓縮檔已使用數位簽章簽名。你可以從[這裡](https://files.kde.org/krita/4DA79EDA231C852B)取得 GPG 公鑰。簽名檔可於[此處](https://download.kde.org/unstable/krita/5.0.0-beta1/)找到（副檔名為 .sig）。

## 支持 Krita

Krita 是免費及開放原始碼的項目。請考慮[捐款](https://fund.krita.org)或[購買教學影片](https://krita.org/en/shop/)支持我們吧！有你的支持我們才能聘請開發人員全職進行 Krita 的開發工作。

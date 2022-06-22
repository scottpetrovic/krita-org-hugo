---
title: "Krita 4.1.3 がリリースされました"
date: "2018-09-29"
categories: 
  - "news-jp"
  - "officialrelease-jp"
---

Kritaの最新バージョンをリリースしました！[2018年の開発資金募集キャンペーン](https://www.krita.org)が進行中ですが、Krita 4.1.3のリリース準備を行う時間を確保することができました。大体100個の修正があるので、重要なリリースです。皆さんにアップデートを推奨します！バグ修正を続けていけるように、是非、2018年の開発資金募集キャンペーンにも参加してください！

[![](/images/posts/2018/2018-fundraiser-hero2.png)](https://krita.org)

Krita 4.1.2はどこに行ってしまったのか気になる人もいるかもしれません…実のところ、4.1.2を準備していたのですが、ビルドインフラの変更によってWindowsのビルドが壊れていました。その修正の間に、Dmitryがいくつか今すぐリリースに含みたいような修正を行いました。例えば、中央揃えの複数行テキストがテキスト編集後に一行になってしまう、といった問題への修正です。 そこで、新しいバージョン、4.1.3を作ることにしました！

[![](/images/posts/2018/text_tool-1024x577.jpg)](https://krita.org/wp-content/uploads/2018/09/text_tool.jpg)

Krita 4.1.3はバグ修正リリースなのでバグ修正がメインですが、新機能もいくつか含まれています。まず最初は、Scott Petrovicによる新しいウェルカムスクリーンです。便利なリンク、最近使ったファイルのリスト、新規ファイル作成やファイルオープンの機能に、空のウィンドウに画像をドラッグアンドドロップして開けるというTipがあります。

[![](/images/posts/2018/welcome_page-1024x781.png)](https://krita.org/wp-content/uploads/2018/09/welcome_page.png)

ここ数週間Dmitry Kazakovは猛烈な勢いでバグを修正しKritaを改善しています。その中の一つは高速プレビューモードの改善です。元々は2015年のKickstarterで資金を集めて開発した高速プレビューモードは、画像の縮小版を計算してそれを表示することで高速化を行います。ただ、ブラシの一部で、ストローク後に遅延が起きたり、キャンバスのちらつきが起きていました。[BUG:361448](https://bugs.kde.org/show_bug.cgi?id=361448). これは修正されました。ブラシでのペイントもよりスムーズに感じるようになりました！スムーズさに関しては[Ivan YossiのGoogle Summer of Codeでの開発](https://colorathis.wordpress.com/tag/kde/)もこのリリースに含まれています。

選択の改善も行いました。Kritaでは、ベクター選択とピクセルマスクの選択があります。ベクター選択を使っている時は、図形ツール（四角や楕円）で選択にベクターを追加することが可能になりました。これまではベクター選択がラスタライズされてしまっていました。

移動ツールも改善されて、移動ツール内の操作もアンドゥできるようになりました。これまではもともとのレイヤー位置に戻ってしまっていました詳細はこちらです。[BUG:392014](https://bugs.kde.org/show_bug.cgi?id=392014)

ベジェ曲線ツールも改善されました。オートスムーズオプションが追加されました。オートスムーズを選択すると、作成される曲線は直線多角形ではなく、すべてのポイントが「スムーズ」に設定されたスムーズなカーブになります。[BUG:351787](https://bugs.kde.org/show_bug.cgi?id=351787)

[![](/images/posts/2018/bezier_smoothing-1024x726.png)](https://krita.org/wp-content/uploads/2018/09/bezier_smoothing.png)

新機能の最後は矩形ツールです。ピクセルレイヤーでもベクターレイヤーでも角を丸めることができるようになりました。[BUG:335568](https://bugs.kde.org/show_bug.cgi?id=335568). もちろん後から編集して角を丸めることはこれまでも可能でしたが、今の方が簡単です。

[![](/images/posts/2018/rounded_rectangles-1024x726.png)](https://krita.org/wp-content/uploads/2018/09/rounded_rectangles.png)

Wolthera van Hövell tot Westerflierが作成したPythonプラグインのコミックプロジェクトマネージャーも大幅に改善されました。特に標準準拠のepubとacbfファイルの生成が改善されています。関連情報になりますが、[KDEのコミックブックリーダーソフトのPeruse](https://peruse.kde.org/)もチェックしてみてください。改善点の長いリストはこちらです:

- 生成されたepubのナビゲーションの改善追加内容…
    - epubの仕様に従った、パネルと吹き出しの範囲ナビゲーション
    - acbf\_titleキーワードで生成したnav.xhtmlとncxのTOCを使用するナビゲーション
    - nav.xhtmlとncxのページリスト
- 生成したEPUBがバリデーションを通ることの確認zipに最初にmimetypeが追加されることの確認、および著者メタデータとNCXページリストへの修正が含まれます
- 言語まわりのおかしい部分を修正
- EPUB メタデータ出力の問題を改善
    - refinesを使用するMARC-relatorsの追加
    - acbfとepubのUUID共有を追加
    - 変更日と正しい日付関連のデータを追加
- epub\_spreadの実装、主要色ahlメタなど。さらに…
    - 吹き出しローカライゼーションの柔軟性を強化
    - すべての吹き出しをより正確にtext-areaとして命名
    - 著者にシーケンスを設定
    - 随所にドキュメントを追加
- 生成したEPUB 3ファイルをpre-paginatedに設定これでコミックがスプレッドの一部としてレンダリングされるようになり結果が改善するはずです
- Epub生成でQDomDocumentを使用、ncx/opfを分割これはよりよい見た目のxmlファイルを得るためにも必要ですそして正しいepub 2/3/3+の生成の余裕を持つためにも必要です
- ComicBookInfoとComicRackジェネレータの更新

[![](/images/posts/2018/Screenshot_20180828_155852-1024x797.png)](https://krita.org/wp-content/uploads/2018/09/Screenshot_20180828_155852.png)

以下がバグ修正の一覧です:

**アニメーション**

- Add a workaround for loading broken files with negative frame ids. [BUG:395378](https://bugs.kde.org/show_bug.cgi?id=395378)
- Delete existing frame files only within exported range [BUG:377354](https://bugs.kde.org/show_bug.cgi?id=377354)
- Fix a problem of Insert Hold Frames action. We should also "offset" empty cell to make sure the expanding works correctly. [BUG:396848](https://bugs.kde.org/show_bug.cgi?id=396848)
- Fix an assert when trying to export a PNG image sequence [BUG:398608](https://bugs.kde.org/show_bug.cgi?id=398608)
- Fix updates when switching frame on a layer with scalar channel
- Use user-selected color label for the auto-created animation frames [BUG:394072](https://bugs.kde.org/show_bug.cgi?id=394072)
- saving of the multiple frames insertion/removal options to the config

**様々なファイル形式のサポートでの改善**

- Fix an assert if an imported SVG file links to non-existent color profile [BUG:398576](https://bugs.kde.org/show_bug.cgi?id=398576)
- Fix backward compatibility of adjustment curves. Older versions supported fewer adjustable channels, so we can no longer assume the count in configuration data to matches exactly. [BUG:396625](https://bugs.kde.org/show_bug.cgi?id=396635)
- Fix saving layers with layer styles [BUG:396224](https://bugs.kde.org/show_bug.cgi?id=396224)
- Let Krita save all the kinds of layers into PSD (in rasterized way) [BUG:399002](https://bugs.kde.org/show_bug.cgi?id=399002)
- PNG Export: convert to rgb, if the image isn't rgb or gray [BUG:398241](https://bugs.kde.org/show_bug.cgi?id=398241)
- Remove fax-related tiff options. In fax mode tiff can store only 1 bit per channel images, which Krita doesn't support. So just remove these options from the GUI [BUG:398548](https://bugs.kde.org/show_bug.cgi?id=398548)

**フィルタ**

- Add a shortcut for the threshold filter [BUG:383818](https://bugs.kde.org/show_bug.cgi?id=383818)
- Fix Burn filter to work in 16-bit color space [BUG:387102](https://bugs.kde.org/show_bug.cgi?id=387102)
- Make color difference threshold for color labels higher
- Restore the shortcut for the invert filters.

**ペイント**

- Remove hardcoded brush size limit for the Quick Brush [BUG:376085](https://bugs.kde.org/show_bug.cgi?id=376085)
- Fix rotation direction when the transformed piece is mirrored. [BUG:398928](https://bugs.kde.org/show_bug.cgi?id=398928)
- Make Stamp brush preview be scaled correctly [CCBUG:399065](https://bugs.kde.org/show_bug.cgi?id=399065)

**タブレット**

- Add a workaround for tablets not reporting tablet events in hover mode [BUG:363284](https://bugs.kde.org/show_bug.cgi?id=363284)

**テキスト**

- Do not reset text style when selecting something in text editor
- Fix saving line breaks when the text is not left aligned [BUG:395769](https://bugs.kde.org/show_bug.cgi?id=395769)

**参照画像ツール**

- Fix reference image cache update conditions [BUG:397208](https://bugs.kde.org/show_bug.cgi?id=397208)

**ビルドシステム**

- Fix build with dcraw 0.19

**キャンバス**

- Disable pixel grid action if opengl is disabled [BUG:388903](https://bugs.kde.org/show_bug.cgi?id=388903) Patch by Shingo Ohtsuka, thanks!
- Fix painting of selection decoration over grids [BUG:362662](https://bugs.kde.org/show_bug.cgi?id=362662)

**コア部分の修正**

- Fix saving to a dropbox or google driver folder on Windows temporary workaround until [QTBUG-57299](https://bugreports.qt.io/browse/QTBUG-57299): QSaveFile should be disabled on Windows.
- Fix to/fromLab16/Rgb16 methods of the Alpha color space
- Fix undo in the cloned KisDocument [BUG:398730](https://bugs.kde.org/show_bug.cgi?id=398730)

**レイヤー**

- Automatically avoid conflicts between color labels and system colors
- Fix cursor jumps in the Layer Properties dialog [BUG:398958](https://bugs.kde.org/show_bug.cgi?id=398958)
- Fix resetting active tool when moving layers above vector layers [BUG:398095](https://bugs.kde.org/show_bug.cgi?id=398095)
- Fix selecting of the layer after undoing Flatten Image [BUG:398814](https://bugs.kde.org/show_bug.cgi?id=398814)
- Fix showing two nodes when converting to a Filter Mask 1) When a filter mask we should first remove the source layer, and only after that show the filter selection dialog 2) Also make sure that the operation is rolled back when the user presses Cancel button
- Fix updates of Clone Layers when the nodes are updated with subtree walker
- a spurious assert in layer cloning [BUG:398788](https://bugs.kde.org/show_bug.cgi?id=398788)

**メタデータ処理**

- Fix a memory access problem in KisExifIO
- Fix memory access problems in KisExifIo
- Show metadata in the dublin core page of the metadata editor. The editor plugin is still broken, with dates not working, bools not working, but now at least a string one has entered is shown again. [CCBUG:396672](https://bugs.kde.org/show_bug.cgi?id=396672)

**Pythonスクリプト機能**

- SegFault in LibKis Node mergeDown [BUG:397043](https://bugs.kde.org/show_bug.cgi?id=397043)
- apidox for Node.position() [BUG:393035](https://bugs.kde.org/show_bug.cgi?id=393035)
- Add modified() getter to the Document class [BUG:397320](https://bugs.kde.org/show_bug.cgi?id=397320)
- Add resetCache() Python API to FileLayer [BUG:398740](https://bugs.kde.org/show_bug.cgi?id=398740)
- Fix memory management of the Filter's InfoObject [BUG:392183](https://bugs.kde.org/show_bug.cgi?id=392183)
- Fix setting file path of the file layer through python API [BUG:398740](https://bugs.kde.org/show_bug.cgi?id=398740)
- Make sure we wait for the filter to be done

**リソース処理**

- Fix saving a fixed bundle under the original name

**選択**

- Fix "stroke selection" to work with local selections [BUG:398007](https://bugs.kde.org/show_bug.cgi?id=398007)
- Fix a crash when moving a vector shape selection when it is an overlay
- Fix crash when converting a shape selection shape into a shape selection
- Fix crash when undoing removing of a selection mask
- Fix rounded rectangular selection to actually work [BUG:397806](https://bugs.kde.org/show_bug.cgi?id=397806)
- Fix selection default bounds when loading old type of adjustment layers
- Stroke Selection: don't try to add a shape just because a layer doesn't have a paint device [BUG:398015](https://bugs.kde.org/show_bug.cgi?id=398015)

**その他のツール**

- Fix color picking from reference images. Desaturation now affects the picked color, and reference images are ignored for picking if hidden.
- Fix connection points on cage transform [BUG:396788](https://bugs.kde.org/show_bug.cgi?id=396788)
- Fix minor UIX issues in the move tool: 1) adds an explicit frame when the move stroke is in progress; 2) Ctrl+Z now cancels the stroke if there is nothing to undo [BUG:392014](https://bugs.kde.org/show_bug.cgi?id=392014)
- Fix offset in Move Tool in the end of the drag
- Fix shift modifier in Curve Selection Tool. The modifier of the point clicked the last should define the selection mode. For selection tools we just disable shift+click "path-close" shortcut of the base path tool. [BUG:397932](https://bugs.kde.org/show_bug.cgi?id=397932)
- Move tool crops the bounding area by exact bounds
- Reduce aliasing in reference images [BUG:396257](https://bugs.kde.org/show_bug.cgi?id=396257)

**雑多な問題とUIの問題**

- Add the default shortcut for the close action: when opening Krita with an image, the close document shortcut was not available.
- FEATURE: Add a hidden config option to lock all dockers in place
- Fix KMainWindow saving incorrect widget settings
- Fix broken buddy: Scale to New Size's Alt-F points to Alt-T [BUG:396948](https://bugs.kde.org/show_bug.cgi?id=396948)
- Fix http link color in KritaBlender.colors: The link are now visible on the startup page of Krita and were dark blue, exact same value as the background making the frame hard to read. Switching them to bright cyan improves the situation.
- Fix loading the template icons
- Fix the offset dialog giving inaccurate offsets. [BUG:397218](https://bugs.kde.org/show_bug.cgi?id=397218)
- Make color label selector handle mouse release events [CCBUG:394072](https://bugs.kde.org/show_bug.cgi?id=394072)
- Remember the last opened settings page in the preferences dialog
- Remember the last used filter bookmark
- Remove the shortcut for wraparound mode: It's still available from the menu and could be put on the toolbar, or people could assign a shortcut, but having it on by default makes life too hard for people who are trying to support our users.
- Remove the shortcuts from the mdi window's system menu's actions. The Close Window action can now have a custom shortcut, and there are no conflicts with hidden actions any more. [BUG:398729](https://bugs.kde.org/show_bug.cgi?id=398729) [BUG:375524](https://bugs.kde.org/show_bug.cgi?id=375524) [BUG:352205](https://bugs.kde.org/show_bug.cgi?id=352205)
- Set color scheme hint for compositor. This is picked up by KWin and sets the palette on the decoration and window frame, ensuring a unified look.
- Show a canvas message when entering wraparound mode
- Show the zoom widget when switching documents [BUG:398099](https://bugs.kde.org/show_bug.cgi?id=398099)
- Use KSqueezedTextLabel for the pattern name in the pattern docker and brush editor [BUG:398958](https://bugs.kde.org/show_bug.cgi?id=398958)
- sort the colorspace depth combobox

## ダウンロード

### Windows

Windowsユーザーの皆さんへ：もしクラッシュする事案に遭遇した場合は、[この案内（英語）](https://docs.krita.org/en/reference_manual/dr_minw_debugger.html#dr-minw) に従いデバッグシンボルをKritaに追加してください。これによってKritaがクラッシュした原因をログから解析できるようになります。

- 64 bits Windows: [krita-x64-4.1.3-setup.exe](https://download.kde.org/stable/krita/4.1.3/krita-x64-4.1.3-setup.exe)
- Portable 64 bits Windows: [krita-x64-4.1.3.zip](https://download.kde.org/stable/krita/4.1.3/krita-x64-4.1.3.zip)
- [デバッグシンボル(Kritaをインストールしたフォルダに展開して使用)](https://download.kde.org/stable/krita/4.1.3/krita-x64-4.1.3-dbg.zip)

- 32 bits Windows: [krita-x86-4.1.3-setup.exe](https://download.kde.org/stable/krita/4.1.3/krita-x86-4.1.3-setup.exe)
- Portable 32 bits Windows: [krita-x86-4.1.3.zip](https://download.kde.org/stable/krita/4.1.3/krita-x86-4.1.3.zip)
- [デバッグシンボル(Kritaをインストールしたフォルダに展開して使用)](https://download.kde.org/stable/krita/4.1.3/krita-x86-4.1.3-dbg.zip)

### Linux

- 64 bits Linux: [krita-4.1.3-x86\_64.appimage](https://download.kde.org/stable/krita/4.1.3/krita-4.1.3-x86_64.appimage)
- 64 bits Linux [G'Mic-Qt plugin appimage](https://download.kde.org/stable/krita/4.1.3/gmic_krita_qt-x86_64.appimage)

(なぜかFirefoxはテキストとして読み込もうとするようです。ダウンロードするにはリンクの右クリックから保存してください) 更新がされると、Ubuntuと派生ディストリビューションでは[Krita Lime PPA](https://launchpad.net/%7Ekritalime/+archive/ubuntu/ppa)からもKrita 4.1.3をインストールできるようになります。snapの更新については作業中です。

### OSX

- OSX disk image: [krita-4.1.3.dmg](https://download.kde.org/stable/krita/4.1.3/krita-4.1.3.dmg)

注意: タッチドッキングパネル、gmic-qtとPythonプラグインはmacOSで利用できません。

### ソースコード

- Source code: [krita-4.1.3.tar.gz](https://download.kde.org/stable/krita/4.1.3/krita-4.1.3.tar.gz)

### md5sum

すべてのダウンロード向け:

- [md5sum.txt](https://download.kde.org/stable/krita/4.1.3/md5sum.txt)

### キー

Linux appimageとソースのtarボールは署名されています。パブリックキーをhttps経由で取得できます: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8) 署名は [こちら](http://download.kde.org/stable/krita/4.1.3/)です (.sigのファイルです)

## Kritaを支援してください

Kritaは自由なオープンソースのプロジェクトです。[寄付](https://krita.org/jp/support-us-jp/donations-jp/)や[トレーニングビデオやアートブックの購入](https://krita.org/jp/support-us-jp/shop-jp/)で、プロジェクトを支援することを検討してみてください！皆様の支援によって、コアチームがフルタイムでKritaの開発作業を続けることが可能になります。

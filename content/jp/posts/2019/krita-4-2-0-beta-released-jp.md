---
title: "Krita 4.2.0 Beta Released"
date: "2019-05-18"
categories: 
  - "uncategorized-jp"
---

Krita 4.2.0の今月リリースに向けて引き続き予定通り進行しています！ [アルファ](https://krita.org/jp/item/krita-4-2-0-alpha-released-jp/)から30以上の問題を修正しました。またTyson Tanによる新しいスプラッシュスクリーンが追加され、Linux AppImageでのPythonサポートが修復されました。Linux AppImageにはサウンドサポートがなく、macOSビルドはG'Micをサポートしません。

[![](images/electrichearts_20190316_kiki_a_sm-1.png)](https://krita.org/wp-content/uploads/2019/05/electrichearts_20190316_kiki_a_sm-1.png)

**注意**: Linuxユーザーはディストリビューションパッケージに気を付けてください。私たちは [Qt向けのパッチをまとめています](https://phabricator.kde.org/T10838)パッチが新しいバージョンのQtにマージされるまで、これらをディストリビューションがホストすることが重要です。

## ダウンロード

### Windows

Windowsユーザーの皆さんへ：もしクラッシュする事案に遭遇した場合は、[この案内（英語）](https://docs.krita.org/en/reference_manual/dr_minw_debugger.html#dr-minw) に従いデバッグシンボルをKritaに追加してください。これによってKritaがクラッシュした原因をログから解析できるようになります。

- 64ビットWindows版: [krita-x64-4.2.0-beta2-setup.exe](https://download.kde.org/unstable/krita/4.2.0-beta2/krita-x64-4.2.0-beta2-setup.exe)
- 64ビットWindowsポータブル版: [krita-x64-4.2.0-beta2.zip](https://download.kde.org/unstable/krita/4.2.0-beta2/krita-x64-4.2.0-beta2.zip)
- [デバッグシンボル(Kritaをインストールしたフォルダに展開して使用)](https://download.kde.org/unstable/krita/4.2.0-beta2/krita-x64-4.2.0-beta2-dbg.zip)

- 32ビットWindows版: [krita-x86-4.2.0-beta2-setup.exe](https://download.kde.org/unstable/krita/4.2.0-beta2/krita-x86-4.2.0-beta2-setup.exe)
- 32ビットWindowsポータブル版: [krita-x86-4.2.0-beta2.zip](https://download.kde.org/unstable/krita/4.2.0-beta2/krita-x86-4.2.0-beta2.zip)
- [デバッグシンボル(Kritaをインストールしたフォルダに展開して使用)](https://download.kde.org/unstable/krita/4.2.0-beta2/krita-x86-4.2.0-beta2-dbg.zip)

### Linux

- 64ビットLinux用AppImage版: [krita-4.2.0-beta-x86\_64.appimage](https://download.kde.org/unstable/krita/4.2.0-beta2/krita-4.2.0-beta-x86_64.appimage)
- 64ビットLinux [G'Mic-Qt plugin appimage](https://download.kde.org/unstable/krita/4.2.0-beta2/gmic_krita_qt-x86_64.appimage)

(なぜかFirefoxはテキストとして読み込もうとするようです。ダウンロードするにはリンクの右クリックから保存してください)

### OSX

- OSXディスクイメージ版: [krita-4.2.0-beta2.dmg](https://download.kde.org/unstable/krita/4.2.0-beta2/krita-4.2.0-beta2.dmg)

注意: タッチドッキングパネル、gmic-qtとPythonプラグインはmacOSで利用できません。

### ソースコード

- [krita-4.2.0-beta2.tar.gz](https://download.kde.org/unstable/krita/4.2.0-beta2/krita-4.2.0-beta2.tar.gz)
- [krita-4.2.0-beta2.tar.xz](https://download.kde.org/unstable/krita/4.2.0-beta2/krita-4.2.0-beta2.tar.xz)

### md5sum

すべてのダウンロード向け:

- [md5sum.txt](https://download.kde.org/unstable/krita/4.2.0-beta2/md5sum.txt)

### キー

Linux appimageとソースのtarボールは署名されています。パブリックキーをhttps経由で取得できます: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8) 署名は [こちら](http://download.kde.org/unstable/krita/4.2.0-beta2/)です (.sigのファイルです)

## Kritaを支援してください

Kritaは自由なオープンソースのプロジェクトです。[寄付](https://krita.org/jp/support-us-jp/donations-jp/)や[トレーニングビデオやアートブックの購入](https://krita.org/jp/support-us-jp/shop-jp/)で、プロジェクトを支援することを検討してみてください！皆様の支援によって、コアチームがフルタイムでKritaの開発作業を続けることが可能になります。

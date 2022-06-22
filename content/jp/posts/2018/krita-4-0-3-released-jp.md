---
title: "Krita 4.0.3リリース！"
date: "2018-05-13"
categories: 
  - "news-jp"
  - "officialrelease-jp"
---

KritaチームはKrita4.0.0のバグ修正リリースであるKrita 4.0.3をリリースしました。Krita 4.0.2のクリティカルなリグレッションバグを修正するものです: Kritaで開かれた画像間のコピーペーストがクラッシュを起こすことがある ([BUG:394068](https://bugs.kde.org/show_bug.cgi?id=394068)).

[![](/images/posts/2018/kiki_4.0_sm-1-1024x463.png)](https://krita.org/wp-content/uploads/2018/03/kiki_4.0_sm-1.png)

## その他の改善点

- Windowsでシステムカラープロファイルを読み込もうとするようになりました
- Kritaが.rw2 RAWファイルを開けるようになりました
- HiDPIとRetinaディスプレイ向けにスプラッシュスクリーンが更新されました ([BUG:392282](https://bugs.kde.org/show_bug.cgi?id=392282))
- OpenEXR出力フィルタはエラーを出す代わりに整数チャンネルデプスを変換するようになりました
- OpenEXR出力フィルタはTIFFフィルタと名乗ってエラーメッセージを出すことがなくなりました
- いくつかの出力フィルタが誤って表示していた空のエラーメッセージダイアログが表示されないようになりました ([BUG:393850](https://bugs.kde.org/show_bug.cgi?id=393850)).
- Python APIのsetBackGroundColorメソッドは一貫性を保つためにsetBackgroundColorに名前が変更されました
- KisColorizeMaskのクラッシュを修正 ([BUG:393753](https://bugs.kde.org/show_bug.cgi?id=393753))

## ダウンロード

### Windows

Windowsユーザーの皆さんへ：もしクラッシュする事案に遭遇した場合は、[この案内（英語）](https://docs.krita.org/Dr._Mingw_debugger) に従いデバッグシンボルをKritaに追加してください。これによってKritaがクラッシュした原因をログから解析できるようになります。

- 64ビットWindows版: [krita-x64-4.0.3-setup.exe](https://download.kde.org/stable/krita/4.0.3/krita-x64-4.0.3-setup.exe)
- 64ビットWindowsポータブル版: [krita-x64-4.0.3.zip](https://download.kde.org/stable/krita/4.0.3/krita-x64-4.0.3.zip)
- [32ビット版向けデバッグシンボル(Kritaをインストールしたフォルダに展開して使用)](https://download.kde.org/stable/krita/4.0.3/krita-x64-4.0.3-dbg.zip)

- 32ビットWindows版: [krita-4.0.3-x86-setup.exe](https://download.kde.org/stable/krita/4.0.3/krita-x86-4.0.3-setup.exe)
- 32ビットWindowsポータブル版: [krita-x86-4.0.3.zip](https://download.kde.org/stable/krita/4.0.3/krita-x86-4.0.3.zip)
- [32ビット版向けデバッグシンボル(Kritaをインストールしたフォルダに展開して使用)](https://download.kde.org/stable/krita/4.0.3/krita-x86-4.0.3-dbg.zip)

### Linux

- 64ビットLinux用AppImage版: [krita-4.0.3-x86\_64.appimage](https://download.kde.org/stable/krita/4.0.3/krita-4.0.3-x86_64.appimage)

(なぜかFirefoxはテキストとして読み込もうとするようです。ダウンロードするにはリンクの右クリックから保存してください) 更新がされると、Ubuntuと派生ディストリビューションでは[Krita Lime PPA](https://launchpad.net/%7Ekritalime/+archive/ubuntu/ppa)からもKrita 4.0.3をインストールできるようになります。snapの更新については作業中です。

### OSX

- OSXディスクイメージ版: [krita-4.0.3.1.dmg](https://download.kde.org/stable/krita/4.0.3/krita-4.0.3.1.dmg)

注意: gmic-qtとPythonプラグインはOSXで利用できません。

### ソースコード

- ソースコード: [krita-4.0.3.tar.gz](https://download.kde.org/stable/krita/4.0.3/krita-4.0.3.tar.gz)

### md5sum

すべてのダウンロード向け:

- [md5sum.txt](https://download.kde.org/stable/krita/4.0.3/md5sum.txt)

### キー

Linux appimageとソースのtarボールは署名されています。パブリックキーをhttps経由で取得できます: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8) 署名は [こちら](http://download.kde.org/stable/krita/4.0.3/)です (.sigのファイルです)

## Kritaを支援してください

Kritaは自由なオープンソースのプロジェクトです。[寄付](https://krita.org/jp/support-us-jp/donations-jp/)や[トレーニングビデオやアートブックの購入](https://krita.org/jp/support-us-jp/shop-jp/)で、プロジェクトを支援することを検討してみてください！皆様の支援によって、コアチームがフルタイムでKritaの開発作業を続けることが可能になります。

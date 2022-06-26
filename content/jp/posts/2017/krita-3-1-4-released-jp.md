---
title: "Krita 3.1.4リリース"
date: "2017-05-28"
categories: 
  - "uncategorized-jp"
---

Krita 3.1.4をリリースしました。これは純粋にバグ修正リリースですが、すべての人にアップデートを推奨します。

- OpenGLを無効にした場合、アニメーション再生時に起こるクラッシュを修正
- 指定したフォルダが存在しない場合のアニメーションフレームレンダリングを修正
- タブレット/画面解像度の不一致ダイアログを複数回開かないように修正
- 変形ツールで小さすぎる場合はプレビューをスケールダウンしないように修正、変形ツールでの珍しいクラッシュが修正されます
- ドキュメント変更中に最後のドキュメントの最後のビューを閉じようとした場合のクラッシュを修正
- カラータグがあるレイヤー間を早く切り替えた時のクラッシュを修正
- いくつかのGimp 2.9ファイルの読み込みの問題を修正。Gimp2.9ファイル形式は公式にはKritaでサポートされていないことに注意してください
- マクロ記録プラグインを完全に削除。3.1.4ではメニューだけが残っていました。
- 新規画像ダイアログでテンプレート選択部分を非表示にできないように変更しました。テンプレート選択部分を非表示にするとダイアログのキャンセルボタンも非表示になります。

#### ダウンロード

KDEダウンロードサイトはアップデートされてhttpsをサポートするようになりました。

#### Windows

Windowsユーザーの皆さんへ：もしクラッシュする事案に遭遇した場合は、[この案内（英語）](https://docs.krita.org/Dr._Mingw_debugger)に従いデバッグシンボルをKritaに追加してください。これによってKritaがクラッシュした原因をログから解析できるようになります。

- 32ビットWindows版: [krita-3.1.4-x86-setup.exe](https://download.kde.org/stable/krita/3.1.4/krita-3.1.4-x86-setup.exe)
- 32ビットWindows用ポータブル版: [krita-3.1.4-x86.zip](https://download.kde.org/stable/krita/3.1.4/krita-3.1.4-x86.zip)
- [32ビット版向けデバッグシンボル (Kritaをインストールしたフォルダに展開して使用)](https://download.kde.org/stable/krita/3.1.4/krita-3.1.4-x86-dbg.zip)

- 64ビットWindows版: [krita-3.1.4-x64-setup.exe](https://download.kde.org/stable/krita/3.1.4/krita-3.1.4-x64-setup.exe)

- 64ビットWindows用ポータブル版: [krita-3.1.4-x64.zip](https://download.kde.org/stable/krita/3.1.4/krita-3.1.4-x64.zip)
- [64ビット版向けデバッグシンボル (Kritaをインストールしたフォルダに展開して使用)](https://download.kde.org/stable/krita/3.1.4/krita-3.1.4-x64-dbg.zip)

- ファイルエクスプローラシェル拡張: [kritashellex-1.2.3.0-setup.exe](https://download.kde.org/stable/krita/kritashellex-1.2.3.0-setup.exe)

#### Linux

- - 64ビットLinux用AppImage版: [krita-3.1.4-x86_64.appimage](https://download.kde.org/stable/krita/3.1.4/krita-3.1.4-x86_64.appimage)

(なぜかFirefoxはテキストとして読み込もうとするようです。ダウンロードするにはリンクの右クリックから保存してください)

Ubuntu App Store向けのsnapイメージは近日中に利用可能になります。 Ubuntuと派生ディストリビューションでは[Krita Lime PPA](https://launchpad.net/~kritalime/+archive/ubuntu/ppa)を使ってKrita 3.1.4をインストールすることも可能です。

#### OSX

- OSXディスクイメージ版:: [krita-3.1.4.dmg](https://download.kde.org/stable/krita/3.1.4/krita-3.1.4.dmg)

### ソースコード

- ソースコード: [krita-3.1.4.tar.gz](https://download.kde.org/stable/krita/3.1.4/krita-3.1.4.tar.gz)

#### md5sums

すべてのダウンロード向け:

- [md5sums.txt](https://download.kde.org/stable/krita/3.1.4/md5sums.txt)

#### Key

Linux appimageとソースのtarボールは署名されています。パブリックキーをhttps経由で取得できます: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8) 署名は [こちら](http://download.kde.org/stable/krita/3.1.4/)

#### Kritaを支援してください

Kritaは自由なオープンソースのプロジェクトです。[寄付](https://krita.org/jp/support-us-jp/donations-jp/)や[トレーニングビデオやアートブックの購入](https://krita.org/jp/support-us-jp/shop-jp/)で、プロジェクトを支援することを検討してみてください！皆様の支援によって、コアチームがフルタイムでKritaの開発作業を続けることが可能になります。

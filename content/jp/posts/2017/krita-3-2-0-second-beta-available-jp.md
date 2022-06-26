---
title: "Krita 3.2.0: ベータ第2版公開"
date: "2017-07-25"
categories: 
  - "uncategorized-jp"
---

Krita 3.2.0のベータ第2版をリリースしました! [3.2.0ベータ第1版](https://krita.org/jp/item/krita-3-2-beta-1-released-jp/)とくらべて以下の修正が含まれています。これはベータ版ということを忘れないでください。テストして問題を[bugs.kde.org](https://bugs.kde.org)に報告して開発チームを助けてください。

- Windowsでのgmic-qtプラグインのインテグレーションにはまだ問題がありますが、いくつかのフリーズを修正しました
- スマートパッチツールのマージが失敗していました。今回修正されています。
- マウスでベクターオブジェクトが動かせなくなっていました(指とタブレットは問題ありません)。今回修正されています。
- サイズと流量スライダーを修正しました
- 透明チャンネルのないjpg、png画像の保存問題を修正

#### ダウンロード

KDEダウンロードサイトはアップデートされてhttpsをサポートするようになりました。

#### Windows

Windowsユーザーの皆さんへ：もしクラッシュする事案に遭遇した場合は、[この案内（英語）](https://docs.krita.org/Dr._Mingw_debugger)に従いデバッグシンボルをKritaに追加してください。これによってKritaがクラッシュした原因をログから解析できるようになります。

- 32ビットWindows版: [krita-3.2.0-beta.2-x86-setup.exe](https://download.kde.org/unstable/krita/3.2.0-beta.2/krita-3.2.0-beta.2-x86-setup.exe)
- 32ビットWindows用ポータブル版: [krita-3.2.0-beta.2-x86.zip](https://download.kde.org/unstable/krita/3.2.0-beta.2/krita-3.2.0-beta.2-x86.zip)
- [32ビット版向けデバッグシンボル (Kritaをインストールしたフォルダに展開して使用)](https://download.kde.org/unstable/krita/3.2.0-beta.2/krita-3.2.0-beta.2-x86-dbg.zip)

- 64ビットWindows版: [krita-3.2.0-beta.2-x64-setup.exe](https://download.kde.org/unstable/krita/3.2.0-beta.2/krita-3.2.0-beta.2-x64-setup.exe)
- 64ビットWindows用ポータブル版: [krita-3.2.0-beta.2-x64.zip](https://download.kde.org/unstable/krita/3.2.0-beta.2/krita-3.2.0-beta.2-x64.zip)
- [64ビット版向けデバッグシンボル (Kritaをインストールしたフォルダに展開して使用)](https://download.kde.org/unstable/krita/3.2.0-beta.2/krita-3.2.0-beta.2-x64-dbg.zip)

- ファイルエクスプローラシェル拡張: [kritashellex-1.2.3.0-setup.exe](https://download.kde.org/stable/krita/kritashellex-1.2.3.0-setup.exe)

#### Linux

- - 64ビットLinux用AppImage版: [krita-3.2.0-beta.2-x86_64.appimage](https://download.kde.org/unstable/krita/3.2.0-beta.2/krita-3.2.0-beta.2-x86_64.appimage)

(なぜかFirefoxはテキストとして読み込もうとするようです。ダウンロードするにはリンクの右クリックから保存してください)

Ubuntu App Store向けのsnapイメージは近日中に利用可能になります。 Ubuntuと派生ディストリビューションでは[Krita Lime PPA](https://launchpad.net/~kritalime/+archive/ubuntu/ppa)を使ってKrita 3.2.0-beta.2をインストールすることも可能になります。

#### OSX

- OSXディスクイメージ版: [krita-3.2.0-beta.2.dmg](https://download.kde.org/unstable/krita/3.2.0-beta.2/krita-3.2.0-beta.2.dmg)

### ソースコード

- ソースコード: [krita-3.2.0-beta.2.tar.gz](https://download.kde.org/unstable/krita/3.2.0-beta.2/krita-3.2.0-beta.2.tar.gz)

#### md5sums

すべてのダウンロード向け:

- [md5sums.txt](https://download.kde.org/unstable/krita/3.2.0-beta.2/md5sums.txt)

#### Key

Linux appimageとソースのtarボールは署名されています。パブリックキーをhttps経由で取得できます: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8). 署名は[こちら](http://download.kde.org/unstable/krita/3.2.0-beta.2/)。

#### Kritaを支援してください

Kritaは自由なオープンソースのプロジェクトです。[寄付](https://krita.org/jp/support-us-jp/donations-jp/)や[トレーニングビデオやアートブックの購入](https://krita.org/jp/support-us-jp/shop-jp/)で、プロジェクトを支援することを検討してみてください！皆様の支援によって、コアチームがフルタイムでKritaの開発作業を続けることが可能になります。

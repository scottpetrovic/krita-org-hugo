---
title: "Krita 3.2.1 リリース！"
date: "2017-08-26"
categories: 
  - "uncategorized-jp"
---

Krita 3.2.1はバグ修正リリースです。以下の問題が修正されました:

- OpenGL2.1しか見つからない場合の起動時のクラッシュ: もし3.2.0でOpenGLを無効にする必要があった人は、有効に戻してみてください
- gmic-qtプラグインでレイヤー種類を変更した時のクラッシュ
- 画像サイズによってはgmic-qtがクラッシュすることがあったバグ
- テキストツールを使うとブラシツールが壊れるリグレッションバグ
- ファイルダイアログにプラットホームネイティブのものを使うオプションが復元されました
- 直線ツールを選ぶと流量スライダーが無効になるバグ
- LUTドッキングパネルのいくつかの問題

### ダウンロード

#### Windows

Windowsユーザーの皆さんへ：もしクラッシュする事案に遭遇した場合は、[この案内（英語）](https://docs.krita.org/Dr._Mingw_debugger)に従いデバッグシンボルをKritaに追加してください。これによってKritaがクラッシュした原因をログから解析できるようになります。

- 32ビットWindows版: [krita-3.2.1-x86-setup.exe](https://download.kde.org/stable/krita/3.2.1/krita-3.2.1-x86-setup.exe)
- 32ビットWindows用ポータブル版: [krita-3.2.1-x86.zip](https://download.kde.org/stable/krita/3.2.1/krita-3.2.1-x86.zip)
- [32ビット版向けデバッグシンボル (Kritaをインストールしたフォルダに展開して使用)](https://download.kde.org/stable/krita/3.2.1/krita-3.2.1-x86-dbg.zip)

- 64ビットWindows版: [krita-3.2.1-x64-setup.exe](https://download.kde.org/stable/krita/3.2.1/krita-3.2.1-x64-setup.exe)
- 64ビットWindows用ポータブル版: [krita-3.2.1-x64.zip](https://download.kde.org/stable/krita/3.2.1/krita-3.2.1-x64.zip)
- [64ビット版向けデバッグシンボル (Kritaをインストールしたフォルダに展開して使用)](https://download.kde.org/stable/krita/3.2.1/krita-3.2.1-x64-dbg.zip)

- ファイルエクスプローラシェル拡張: [kritashellex-1.2.4.0-setup.exe](https://download.kde.org/stable/krita/KritaShellExtension-v1.2.4-setup.exe)

#### Linux

- 64ビットLinux用AppImage版: [krita-3.2.1-x86\_64.appimage](https://download.kde.org/stable/krita/3.2.1/krita-3.2.1-x86_64.appimage)

(なぜかFirefoxはテキストとして読み込もうとするようです。ダウンロードするにはリンクの右クリックから保存してください)

Ubuntuと派生ディストリビューションでは[Krita Lime PPA](https://launchpad.net/~kritalime/+archive/ubuntu/ppa)を使ってKrita 3.2.1をインストールすることも可能になります。

#### OSX

- OSXディスクイメージ版: [krita-3.2.1.dmg](https://download.kde.org/stable/krita/3.2.1/krita-3.2.1.dmg)

注意: gmic-qtとpdfプラグインはOSXでは利用できません。

### ソースコード

- ソースコード: [krita-3.2.1.tar.gz](https://download.kde.org/stable/krita/3.2.1/krita-3.2.1.tar.gz)

#### md5sums

すべてのダウンロード向け:

- [md5sums.txt](https://download.kde.org/stable/krita/3.2.1/md5sums.txt)

#### Key

Linux appimageとソースのtarボールは署名されています。パブリックキーをhttps経由で取得できます: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8). 署名は[こちら](http://download.kde.org/stable/krita/3.2.1/).

#### Kritaを支援してください

Kritaは自由なオープンソースのプロジェクトです。[寄付](https://krita.org/jp/support-us-jp/donations-jp/)や[トレーニングビデオやアートブックの購入](https://krita.org/jp/support-us-jp/shop-jp/)で、プロジェクトを支援することを検討してみてください！皆様の支援によって、コアチームがフルタイムでKritaの開発作業を続けることが可能になります。

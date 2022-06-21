---
title: "Krita 3.3.1"
date: "2017-10-14"
categories: 
  - "uncategorized-jp"
---

Krita 3.3.1を本日リリースしました。Krita3.3.0のバグ修正リリースです。2つの重要なリグレッションバグを修正しています:

- リファレンス画像ドッキングパネルをフローティングにした状態でKritaを閉じると、次に起動した時にKritaがクラッシュする問題
- 手動でZip解凍されてから再圧縮された.kraバックアップファイルをKrita 3.3.0が読み込めない問題

追加して以下の修正と機能改善も含まれています:

- OSXでのスワップファイル作成時のクラッシュを修正 (Bernhard Liebl).
- 下のレイヤーへの統合でロックされたレイヤーが削除されないように変更 (Nikita Smirnov)
- 様々なパフォーマンス改善、特にmacOS向け改善 (Bernhard Liebl)
- レイヤーのドラッグ・アンド・ドロップの見た目と振る舞いを改善 (Bernhard Liebl)
- ブラシプリセットセレクタのツールチップを改善 (Bernhard Liebl)
- カラーセレクタのメモリリークを修正(Boudewijn Rempt)
- Windows Ink APIでの回転とティルトを修正 (Alvin Wong)
- グループレイヤーに対して塗りつぶしツールを使用できないように変更 (Boudewijn Rempt)
- テクスチャブラシに明度、コントラストスライダーを追加 (Rad)
- paste-at-cursor(カーソル位置に貼り付け)を追加  (Dmitry Kazakov)
- CPUキャンバスのパフォーマンス向上 (Alvin Wong)
- クリップボードに何かがある状態でKritaを閉じた際のクラッシュを修正 (Dmitry Kazakov)
- Kritaでファイルレイヤーの画像を開くボタンを追加 (Wolthera van Hövell tot Westerflier)

### Download

#### Windows

Windowsユーザーの皆さんへ：もしクラッシュする事案に遭遇した場合は、[この案内（英語）](https://docs.krita.org/Dr._Mingw_debugger)に従いデバッグシンボルをKritaに追加してください。これによってKritaがクラッシュした原因をログから解析できるようになります。

- 64ビットWindows版:  [krita-3.3.1-x64-setup.exe](https://download.kde.org/stable/krita/3.3.1/krita-3.3.1-x64-setup.exe)
- 64ビットWindowsポータブル版: [krita-3.3.1-x64.zip](https://download.kde.org/stable/krita/3.3.1/krita-3.3.1-x64.zip)
- [64ビット版向けデバッグシンボル (Kritaをインストールしたフォルダに展開して使用)](https://download.kde.org/stable/krita/3.3.1/krita-3.3.1-x64-dbg.zip)

- 32ビットWindows版: [krita-3.3.1-x86-setup.exe](https://download.kde.org/stable/krita/3.3.1/krita-3.3.1-x86-setup.exe)
- 32ビットWindowsポータブル版: [krita-3.3.1-x86.zip](https://download.kde.org/stable/krita/3.3.1/krita-3.3.1-x86.zip)
- [32ビット版向けデバッグシンボル (Kritaをインストールしたフォルダに展開して使用)](https://download.kde.org/stable/krita/3.3.1/krita-3.3.1-x86-dbg.zip)

- ファイルエクスプローラシェル拡張: [kritashellex-1.2.4.0-setup.exe](https://download.kde.org/stable/krita/KritaShellExtension-v1.2.4-setup.exe)

#### Linux

- 64ビットLinux用AppImage版: [krita-3.3.1-x86\_64.appimage](https://download.kde.org/stable/krita/3.3.1/krita-3.3.1-x86_64.appimage)

(なぜかFirefoxはテキストとして読み込もうとするようです。ダウンロードするにはリンクの右クリックから保存してください)

Ubuntuと派生ディストリビューションでは更新されれば[Krita Lime PPA](https://launchpad.net/~kritalime/+archive/ubuntu/ppa)を使ってKrita 3.3.1をインストールすることも可能になります。snap版も更新されています。

#### OSX

- OSXディスクイメージ版: [krita-3.3.1.dmg](https://download.kde.org/stable/krita/3.3.1/krita-3.3.1.dmg)

注意: gmic-qtとpdfプラグインはOSXでは利用できません。

### ソースコード

- ソースコード: [krita-3.3.1.tar.gz](https://download.kde.org/stable/krita/3.3.1/krita-3.3.1.tar.gz)

#### md5sums

すべてのダウンロード向け:

- [md5sums.txt](https://download.kde.org/stable/krita/3.3.1/md5sums.txt)

#### Key

Linux appimageとソースのtarボールは署名されています。パブリックキーをhttps経由で取得できます:  [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8). 署名は[こちら](http://download.kde.org/stable/krita/3.3.1/).

#### Kritaを支援してください

Kritaは自由なオープンソースのプロジェクトです。[寄付](https://krita.org/jp/support-us-jp/donations-jp/)や[トレーニングビデオやアートブックの購入](https://krita.org/jp/support-us-jp/shop-jp/)で、プロジェクトを支援することを検討してみてください！皆様の支援によって、コアチームがフルタイムでKritaの開発作業を続けることが可能になります。

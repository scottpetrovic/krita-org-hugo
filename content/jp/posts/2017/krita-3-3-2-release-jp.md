---
title: "Krita 3.3.2リリース"
date: "2017-11-05"
categories: 
  - "uncategorized-jp"
---

Krita 3.3.2を今日リリースしました。Krita3.3.0のバグ修正リリースです。2つの重要なリグレッションバグの修正を行っています:

- Krita 3.3.1はテクスチャ設定のあるブラシプリセットを正しく読み込めていませんでした。この修正が行われました。
- Windows 1709ビルドはwintabとWindows Inkタブレットの処理を壊しました。回避策を見つけてこのバージョンでは再び動くようになっています。

追加して以下の修正と機能追加も行われています:

- アニメーション: アニメーション最後の後の空白フレームを出力することを可能に
- アニメーション: 10000フレームまでレンダリングを可能に
- 新規の空の画像でKritaを起動するコマンドラインオプションを追加: krita --new-image RGBA,8,5000,3000
- パフォーマンス: エフェクトと選択マスクのキャッシュを向上
- パフォーマンス: スマッジブラシのリークを修正
- パフォーマンス: ハードウェアアクレラレーションを使ったキャンバスのパフォーマンスを向上
- パフォーマンス, Windows: アイコンロードのパフォーマンスを向上
- macOS: 1秒のフレーム数のオーバレイウィジェットのレンダリングを修正
- フィルタ: Krita形式ファイルでフィルタを保存をするために仕様しているXMLの直接編集を可能に
- フィルタ: ASC\_CDLカラーバランスフィルタの追加。Slope、Offset、Powerオプション付き
- クラッシュ: 無限キャンバスをアクティブにしている2つ目のドキュメントを閉じた場合のクラッシュを修正
- レイヤー: グループレイヤーのコピーを可能に
- UI: パターンパレットの幅が狭い場合にホイールでスクロールを可能に
- UI: レイヤーパネルでのドラッグアンドドロップフィードバックを改善
- UI: パネルがフローティング中にはタイトルバーのロックと畳むアイコンを隠すように変更
- G'Mic: 同梱のG'Micを最新リリースに更新

### Download

#### Windows

Windowsユーザーの皆さんへ：もしクラッシュする事案に遭遇した場合は、[この案内（英語）](https://docs.krita.org/Dr._Mingw_debugger)に従いデバッグシンボルをKritaに追加してください。これによってKritaがクラッシュした原因をログから解析できるようになります。

- 64ビットWindows版: [krita-3.3.2-x64-setup.exe](https://download.kde.org/stable/krita/3.3.2/krita-3.3.2-x64-setup.exe)
- 64ビットWindowsポータブル版: [krita-3.3.2.1-x64.zip](https://download.kde.org/stable/krita/3.3.2/krita-3.3.2.1-x64.zip)
- [64ビット版向けデバッグシンボル (Kritaをインストールしたフォルダに展開して使用)](https://download.kde.org/stable/krita/3.3.2/krita-3.3.2.1-x64-dbg.zip)

- 32ビットWindows版: [krita-3.3.2-x86-setup.exe](https://download.kde.org/stable/krita/3.3.2/krita-3.3.2-x86-setup.exe)
- 32ビットWindowsポータブル版: [krita-3.3.2.1-x86.zip](https://download.kde.org/stable/krita/3.3.2/krita-3.3.2.1-x86.zip)
- [32ビット版向けデバッグシンボル (Kritaをインストールしたフォルダに展開して使用)](https://download.kde.org/stable/krita/3.3.2/krita-3.3.2.1-x86-dbg.zip)

- ファイルエクスプローラシェル拡張: [kritashellex-1.2.4.0-setup.exe](https://download.kde.org/stable/krita/KritaShellExtension-v1.2.4-setup.exe)

#### Linux

- 64ビットLinux用AppImage版: [krita-3.3.2-x86\_64.appimage](https://download.kde.org/stable/krita/3.3.2/krita-3.3.2-x86_64.appimage)

(なぜかFirefoxはテキストとして読み込もうとするようです。ダウンロードするにはリンクの右クリックから保存してください)

Ubuntuと派生ディストリビューションでは更新されれば[Krita Lime PPA](https://launchpad.net/~kritalime/+archive/ubuntu/ppa)を使ってKrita 3.3.2をインストールすることも可能になります。snap版も更新されています。

#### OSX

- OSXディスクイメージ版: [krita-3.3.2.dmg](https://download.kde.org/stable/krita/3.3.2/krita-3.3.2.dmg)

注意: gmic-qtとpdfプラグインはOSXでは利用できません。

### ソースコード

- ソースコード: [krita-3.3.2.1.tar.xz](https://download.kde.org/stable/krita/3.3.2/krita-3.3.2.1.tar.gz)

#### md5sums

すべてのダウンロード向け:

- [md5sums.txt](https://download.kde.org/stable/krita/3.3.2/md5sums.txt)

#### Key

Linux appimageとソースのtarボールは署名されています。パブリックキーをhttps経由で取得できます: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8). 署名は[こちら](http://download.kde.org/stable/krita/3.3.2/).

#### Kritaを支援してください

Kritaは自由なオープンソースのプロジェクトです。[寄付](https://krita.org/jp/support-us-jp/donations-jp/)や[トレーニングビデオやアートブックの購入](https://krita.org/jp/support-us-jp/shop-jp/)で、プロジェクトを支援することを検討してみてください！皆様の支援によって、コアチームがフルタイムでKritaの開発作業を続けることが可能になります。

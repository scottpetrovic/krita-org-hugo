---
title: "新しい安定版リリース: Krita 3.3.3"
date: "2018-01-13"
categories: 
  - "uncategorized-jp"
---

今日Krita 3.3.3をリリースしました。これはおそらくKrita 3シリーズでの最後の安定版リリースになるでしょう。このリリースには数個のバグ修正とWindowsユーザにとって大事な変更が含まれています:

- Intelユーザ向けにはDirect3d/Angleレンダラが新しいデフォルトになりました。Intelディスプレイドライバの最近のアップデートで以前よりさらに多くのPCでKritaに支障が出たため、この回避策をデフォルトにするほうが望ましいと考えました。パフォーマンスがわるくなったと感じたら、手動でOpenGLを有効にしてみることも可能です。

その他の修正と機能改善:

- RGB画像でグレースケールレイヤーを使用している時に選択できない合成モードがあった問題を修正
- WindowsのKritaからバグを報告する際にOSとプラットホーム情報を自動で設定するようにしました
- 特定色選択ドッキングパネルでパーセント形式での色指定を可能にしました
- IntelのGPUを使用している場合に、OpenGLの警告を行いANGLEをデフォルトにするように変更しました
- レベルフィルタに反転ボタンを追加
- PSDからグループレイヤーのスタイルの読み込みと保存を実装
- ブラシツールに戻った時に、消しゴムモードが正しく表示されないことがある問題を修正
- 個々の補助線の可視状態を.kraファイルに保存するように修正
- 定規メモリを2の乗数で描画するオプションを追加
- 移動、変形ツールの時の自動スクロールを無効に変更
- ペンとWindow Ink API使用時のマウスイベント処理方法を改善
- ズームジェスチャの中心ポイントを修正
- コメント付きnetpbmファイルの読み込みを修正

### ダウンロード

#### Windows

Windowsユーザーの皆さんへ：もしクラッシュする事案に遭遇した場合は、[この案内（英語）](https://docs.krita.org/Dr._Mingw_debugger) に従いデバッグシンボルをKritaに追加してください。これによってKritaがクラッシュした原因をログから解析できるようになります。

- 64ビットWindows版: [krita-3.3.3-x64-setup.exe](https://download.kde.org/stable/krita/3.3.3/krita-3.3.3-x64-setup.exe)
- 64ビットWindowsポータブル版: [krita-3.3.3-x64.zip](https://download.kde.org/stable/krita/3.3.3/krita-3.3.3-x64.zip)
- [64ビット版向けデバッグシンボル(Kritaをインストールしたフォルダに展開して使用)](https://download.kde.org/stable/krita/3.3.3/krita-3.3.3-x64-dbg.zip)

- 32ビットWindows版: [krita-3.3.3-x86-setup.exe](https://download.kde.org/stable/krita/3.3.3/krita-3.3.3-x64-setup.exe)
- 32ビットWindowsポータブル版: [krita-3.3.3-x86.zip](https://download.kde.org/stable/krita/3.3.3/krita-3.3.3-x64.zip)
- [64ビット版向けデバッグシンボル(Kritaをインストールしたフォルダに展開して使用)](https://download.kde.org/stable/krita/3.3.3/krita-3.3.3-x64-dbg.zip)

#### Linux

- 64ビットLinux用AppImage版: [krita-3.3.3-x86_64.appimage](https://download.kde.org/stable/krita/3.3.3/krita-3.3.3-x86_64.appimage)

(なぜかFirefoxはテキストとして読み込もうとするようです。ダウンロードするにはリンクの右クリックから保存してください) 更新がされると、Ubuntuと派生ディストリビューションでは[Krita Lime PPA](https://launchpad.net/%7Ekritalime/+archive/ubuntu/ppa)からもKrita 3.3.3をインストールできるようになります。snapの更新については作業中です。

#### OSX

- OSXディスクイメージ版: [krita-3.3.3.dmg](https://download.kde.org/stable/krita/3.3.3/krita-3.3.3.dmg)

注意: gmic-qtとpdfプラグインはOSXで利用できません。

### ソースコード

- ソースコード: [krita-3.3.3.tar.gz](https://download.kde.org/stable/krita/3.3.3/krita-3.3.3.tar.gz)

#### md5sums

すべてのダウンロード向け:

- [md5sums.txt](https://download.kde.org/stable/krita/3.3.3/md5sums.txt)

#### キー

Linux appimageとソースのtarボールは署名されています。パブリックキーをhttps経由で取得できます: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8) 署名は [こちら](http://download.kde.org/stable/krita/3.3.3/)

#### Kritaを支援してください

Kritaは自由なオープンソースのプロジェクトです。[寄付](https://krita.org/jp/support-us-jp/donations-jp/)や[トレーニングビデオやアートブックの購入](https://krita.org/jp/support-us-jp/shop-jp/)で、プロジェクトを支援することを検討してみてください！皆様の支援によって、コアチームがフルタイムでKritaの開発作業を続けることが可能になります。

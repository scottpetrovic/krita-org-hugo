---
title: "Krita 3.2.0リリース"
date: "2017-08-19"
categories: 
  - "uncategorized-jp"
---

予定より遅れてしまいましたが、Krita 3.2.0のリリースです！新しいG'Mic-qtプラグインを統合し、スマートパッチツール、タッチスクリーンでの指でのペイント機能、新しいブラシプリセットと数多くのバグ修正が含まれています。

[詳細についてはこちらのリリースノートを参照してください!（英語)。](https://krita.org/en/release-notes-for-krita-3-2/)また[GDQuest](http://gdquest.com/)による3.2.0の紹介動画はこちらです:

https://youtu.be/f9K48jXml4s

注意: gmic-qtプラグインはOSXでは使用できません、WindowsとLinuxAppImage版のKritaはビルド済みの[gmic-qtプラグイン](https://github.com/c-koi/gmic-qt)を同梱するようになりました。ベータ版やリリース候補版ビルドをテストしていたユーザは、[設定をリセット](https://docs.krita.org/KritaFAQ#Resetting_Krita_configuration)する必要があるかもしれません。

### リリース候補版ビルドからの変更点:

- Kritaのウィンドウをモニタ間で移動した時にLUTドッキングパネルをリセットしないように変更
- LUTドッキングパネルの露光ディスプレイフィルタの初期化を修正
- パン(表示範囲移動)ツールのアクションを追加
- 「通常」合成モードのパフォーマンスを30%向上(Daria ScherbatyukさんによるKritaのはじめてのパッチです!)
- 画像の2個めのビューを作成する時のクラッシュを修正
- 2個めのウィンドウを作成する時に起こる可能性があるクラッシュを修正
- gmic-qtプラグインの探索方法を改善: Kritaは実行ファイルと同じ場所を最初に探すようになりました
- KritaをQt 5.7.1以降でビルドした時のスクロールホイールの挙動を修正
- RGBA以外の画像にgmic-qtを適用した時のパンニングを修正
- RGBA以外の画像をgmic-qtで使用した時のチャンネル値スケーリングが正しくなるように修正
- 複数のKritaインスタンスを許可するデフォルト設定を修正
    
    ### ダウンロード
    
    #### Windows
    
    Windowsユーザーの皆さんへ：もしクラッシュする事案に遭遇した場合は、[この案内（英語）](https://docs.krita.org/Dr._Mingw_debugger)に従いデバッグシンボルをKritaに追加してください。これによってKritaがクラッシュした原因をログから解析できるようになります。
    
    - 32ビットWindows版: [krita-3.2.0-x86-setup.exe](https://download.kde.org/stable/krita/3.2.0/krita-3.2.0-x86-setup.exe)
    - 32ビットWindows用ポータブル版: [krita-3.2.0-x86.zip](https://download.kde.org/stable/krita/3.2.0/krita-3.2.0-x86.zip)
    - [32ビット版向けデバッグシンボル (Kritaをインストールしたフォルダに展開して使用)](https://download.kde.org/stable/krita/3.2.0/krita-3.2.0-x86-dbg.zip)
    
    - 64ビットWindows版: [krita-3.2.0-x64-setup.exe](https://download.kde.org/stable/krita/3.2.0/krita-3.2.0-x64-setup.exe)
    - 64ビットWindows用ポータブル版: [krita-3.2.0-x64.zip](https://download.kde.org/stable/krita/3.2.0/krita-3.2.0-x64.zip)
    - [64ビット版向けデバッグシンボル (Kritaをインストールしたフォルダに展開して使用)](https://download.kde.org/stable/krita/3.2.0/krita-3.2.0-x64-dbg.zip)
    
    - ファイルエクスプローラシェル拡張: [kritashellex-1.2.4.0-setup.exe](https://download.kde.org/stable/krita/KritaShellExtension-v1.2.4-setup.exe)
    
    #### Linux
    
    - 64ビットLinux用AppImage版: [krita-3.2.0-x86\_64.appimage](https://download.kde.org/stable/krita/3.2.0/krita-3.2.0-x86_64.appimage)
    
    (なぜかFirefoxはテキストとして読み込もうとするようです。ダウンロードするにはリンクの右クリックから保存してください)
    
    Ubuntu App Store向けのsnapイメージは近日中に利用可能になります。 Ubuntuと派生ディストリビューションでは[Krita Lime PPA](https://launchpad.net/~kritalime/+archive/ubuntu/ppa)を使ってKrita 3.2.0をインストールすることも可能になります。
    
    #### OSX
    
    - OSXディスクイメージ版: [krita-3.2.0.dmg](https://download.kde.org/stable/krita/3.2.0/krita-3.2.0.dmg)
    
    注意: gmic-qtとpdfプラグインはOSXでは利用できません。
    
    ### ソースコード
    
    - ソースコード: [krita-3.2.0.tar.gz](https://download.kde.org/stable/krita/3.2.0/krita-3.2.0.tar.gz)
    
    #### md5sums
    
    すべてのダウンロード向け:
    
    - [md5sums.txt](https://download.kde.org/stable/krita/3.2.0/md5sums.txt)
    
    #### Key
    
    Linux appimageとソースのtarボールは署名されています。パブリックキーをhttps経由で取得できます:: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8)。署名は[こちら](http://download.kde.org/stable/krita/3.2.0/)。
    
    #### Kritaを支援してください
    
    Kritaは自由なオープンソースのプロジェクトです。[寄付](https://krita.org/jp/support-us-jp/donations-jp/)や[トレーニングビデオやアートブックの購入](https://krita.org/jp/support-us-jp/shop-jp/)で、プロジェクトを支援することを検討してみてください！皆様の支援によって、コアチームがフルタイムでKritaの開発作業を続けることが可能になります。

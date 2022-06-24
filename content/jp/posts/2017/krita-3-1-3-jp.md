---
title: "Krita 3.1.3"
date: "2017-05-02"
categories: 
  - "uncategorized-jp"
---

本日Krita 3.1.3正式版を皆さんに自信を持ってお届けします！今回のリリースには大量のバグ修正のみならず、いくつかの新機能も含まれています。DmitryとBoudはKrita 3.1.3を可能な限り安定にするため、Kickstarterによる機能の実装を数か月中断しています。アルファ版・ベータ版・リリース候補版をテストして下さったすべての皆さんに感謝申し上げます！翻訳作業を行ってくれた皆さん及びUbuntu Lime PPAのメンテナンスを買って出てくれたAlexey Samoilovにも感謝申し上げます。

[![Transform around Pivot](/images/posts/2017/pivot-1024x527.png)](/images/posts/2017/pivot.png)

ピボット中心の変形（画像は[David Revoy](https://peppercarrot.com)氏より）

また.kraファイル及び.oraファイルのサムネイルを表示できるようにするWindowsファイルエクスプローラ統合プラグインについてもバージョン更新を行いました。いくつかのメモリリークが修正され、Oracle detabaseによって生成された.oraファイルとの競合が解決されました。Alvin Wongに感謝を！

### 新機能

- ピボット中心の拡大縮小を追加
- デフォルトツール（切り取り・コピー・貼り付け及びオブジェクト配列）へのコンテキストメニューアクションを実装
- Kritaが複数のインスタンスを持てるようにするオプションを追加(BUG 377199)

50個以上のバグが修正された今回のリリースでの変更の一覧は[こちら（※日本語翻訳版）](https://krita.org/jp/release-notes-for-3-1-3-jp/)をごらんください

#### ダウンロード

KDEのダウンロードサイトは今回からhttpsに更新されました。

#### Windows

Windowsユーザーの皆さんへ：もしクラッシュする事案に遭遇した場合は、[この案内（英語）](https://docs.krita.org/Dr._Mingw_debugger)に従いデバッグシンボルをKritaに追加してください。これによってKritaがクラッシュした原因をログから解析できるようになります。

- 32ビットWindows版: [krita-3.1.3-x86-setup.exe](https://download.kde.org/stable/krita/3.1.3/krita-3.1.3-x86-setup.exe)
- 32ビットWindows用ポータブル版: [krita-3.1.3-x86.zip](https://download.kde.org/stable/krita/3.1.3/krita-3.1.3-x86.zip)
- [32ビット版向けデバッグシンボル (Kritaをインストールしたフォルダに展開して使用)](https://download.kde.org/stable/krita/3.1.3/krita-3.1.3-x86-dbg.zip)

- 64ビットWindows版: [krita-3.1.3-x64-setup.exe](https://download.kde.org/stable/krita/3.1.3/krita-3.1.3-x64-setup.exe)
- 64ビットWindows用ポータブル版: [krita-3.1.3-x64.zip](https://download.kde.org/stable/krita/3.1.3/krita-3.1.3-x64.zip)
- [64ビット版向けデバッグシンボル (Kritaをインストールしたフォルダに展開して使用)](https://download.kde.org/stable/krita/3.1.3/krita-3.1.3-x64-dbg.zip)

- ファイルエクスプローラシェル拡張: [kritashellex-1.2.3.0-setup.exe](https://download.kde.org/stable/krita/kritashellex-1.2.3.0-setup.exe)

#### Linux

- 64ビットLinux用AppImage版: [krita-3.1.3-x86\_64.appimage](https://download.kde.org/stable/krita/3.1.3/krita-3.1.3-x86_64.appimage)

Ubuntu App Store向けのsnapイメージは近日中に利用可能になります。 Ubuntuと派生ディストリビューションでは[Krita Lime PPA](https://launchpad.net/~kritalime/+archive/ubuntu/ppa)を使ってKrita 3.1.3をインストールすることも可能です。

#### OSX

- OSXディスクイメージ版: [krita-3.1.3.dmg](https://download.kde.org/stable/krita/3.1.3/krita-3.1.3.dmg)

### ソースコード

- ソースコード: [krita-3.1.3.tar.gz](https://download.kde.org/stable/krita/3.1.3/krita-3.1.3.tar.gz)

#### md5sums

すべてのダウンロード向け:

- [md5sums.txt](https://download.kde.org/stable/krita/3.1.3/md5sums.txt)

#### 公開鍵

Linux appimageとソースのtarボールは署名されています。パブリックキーをhttps経由で取得できます:  [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8)。署名は[こちら](http://download.kde.org/stable/krita/3.1.3/)。

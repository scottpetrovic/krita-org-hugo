---
title: "Krita 4.1.1 リリース"
date: "2018-07-21"
categories: 
  - "news-jp"
  - "officialrelease-jp"
---

Krita 4.1.0のバグ修正リリースであるKrita 4.1.1をリリースしました。

- PyQt 5.11を使用した時のPyKritaの読み込みを修正 (Antonio Rojasによるパッチです、ありがとうございます！) ([BUG:396381](https://bugs.kde.org/show_bug.cgi?id=396381))
- ベクターオブジェクトに関するクラッシュを修正 ([BUG:396145](https://bugs.kde.org/show_bug.cgi?id=396145))
- ブラシエディタでのピクセルブラシサイズ変更に関する問題の修正 ([BUG:396136](https://bugs.kde.org/show_bug.cgi?id=396136))
- macOSで複数言語が有効になっている場合のシステム言語の読み込みを修正
- ベクターオブジェクトツールプロパティドッキングパネルで実装されていないカラーピッカーを表示しないように修正 ([BUG:389525](https://bugs.kde.org/show_bug.cgi?id=389525))
- 変更、保存、変更サイクル後の自動保存時間起動を修正 ([BUG:393266](https://bugs.kde.org/show_bug.cgi?id=393266))
- クロスチャンネルカーブフィルタでの範囲外ルックアップを修正 ([BUG:396244](https://bugs.kde.org/show_bug.cgi?id=396244))
- リファレンス画像レイヤーでPageUpを押した場合のassertを修正
- このレイヤーのみ表示モードにしたレイヤーをマージする時のクラッシュを修正([BUG:395981](https://bugs.kde.org/show_bug.cgi?id=395981))
- ボックストランスフォームフィルタを使用したトランスフォームマスクを含むファイル読み込みを修正 ([BUG:395979](https://bugs.kde.org/show_bug.cgi?id=395979))
- ボックストランスフォームフィルタが選択された時のトランスフォームツールの起動を修正 ([BUG:395979](https://bugs.kde.org/show_bug.cgi?id=395979))
- サポートされていないバージョンのWindowsを使用しているユーザ向け警告を追加
- 表示している最後のチャンネルを隠した時のクラッシュを修正 ([BUG:395301](https://bugs.kde.org/show_bug.cgi?id=395301))
- 以下のような標準的ではないGPLパレットの読み込みも可能に修正 https://lospec.com/palette-list/endesga-16
- ワープトランスフォームグリッドの表示を単純化
- メニューに「選択の反転」を復活 ([BUG:395764](https://bugs.kde.org/show_bug.cgi?id=395764))
- 数字のフォーマットにKFormatを使用(Pino Toscanoによるパッチです。ありがとうございます！)
- カラースライダーコンフィグページを非表示にしました
- 完全に透明な参照画像から色はピックしないようになりました ([BUG:396358](https://bugs.kde.org/show_bug.cgi?id=396358))
- 参照画像埋め込み時のクラッシュを修正
- 参照画像の保存読み込みの問題を修正 ([BUG:396143](https://bugs.kde.org/show_bug.cgi?id=396143))
- 参照画像でカラーピッカーツールが正しく機能しない問題を修正 ([BUG:396144](https://bugs.kde.org/show_bug.cgi?id=396144))
- パン範囲を参照画像を含むように拡張

## ダウンロード

### Windows

Windowsユーザーの皆さんへ：もしクラッシュする事案に遭遇した場合は、[この案内（英語）](https://docs.krita.org/en/reference_manual/dr_minw_debugger.html#dr-minw) に従いデバッグシンボルをKritaに追加してください。これによってKritaがクラッシュした原因をログから解析できるようになります。

- 64ビットWindows版: [krita-x64-4.1.1-setup.exe](https://download.kde.org/stable/krita/4.1.1/krita-x64-4.1.1-setup.exe)
- 64ビットWindowsポータブル版: [krita-x64-41.1.zip](https://download.kde.org/stable/krita/4.1.1/krita-x64-4.1.1.zip)
- [デバッグシンボル(Kritaをインストールしたフォルダに展開して使用)](https://download.kde.org/stable/krita/4.1.1/krita-x64-4.1.1-dbg.zip)

- 32ビットWindows版: [krita-x86-4.1.1-setup.exe](https://download.kde.org/stable/krita/4.1.1/krita-x86-4.1.1-setup.exe)
- 32ビットWindowsポータブル版: [krita-x86-4.1.1.zip](https://download.kde.org/stable/krita/4.1.1/krita-x86-4.1.1.zip)
- [デバッグシンボル(Kritaをインストールしたフォルダに展開して使用)](https://download.kde.org/stable/krita/4.1.1/krita-x86-4.1.1-dbg.zip)

### Linux

- 64ビットLinux用AppImage版: [krita-4.1.1-x86\_64.appimage](https://download.kde.org/stable/krita/4.1.1/krita-4.1.1-x86_64.appimage)
- 64ビットLinux [G'Mic-Qt plugin appimage](https://download.kde.org/stable/krita/4.1.1/gmic_krita_qt-x86_64.appimage)

(なぜかFirefoxはテキストとして読み込もうとするようです。ダウンロードするにはリンクの右クリックから保存してください) 更新がされると、Ubuntuと派生ディストリビューションでは[Krita Lime PPA](https://launchpad.net/%7Ekritalime/+archive/ubuntu/ppa)からもKrita 4.1.1をインストールできるようになります。snapの更新については作業中です。

### OSX

- OSXディスクイメージ版: [krita-4.1.1.dmg](https://download.kde.org/stable/krita/4.1.1/krita-4.1.1.dmg)

注意: タッチドッキングパネル、gmic-qtとPythonプラグインはmacOSで利用できません。

### ソースコード

- ソースコード: [krita-4.1.1.tar.gz](https://download.kde.org/stable/krita/4.1.1/krita-4.1.1.tar.gz)

### md5sum

すべてのダウンロード向け:

- [md5sum.txt](https://download.kde.org/stable/krita/4.1.1/md5sum.txt)

### キー

Linux appimageとソースのtarボールは署名されています。パブリックキーをhttps経由で取得できます: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8) 署名は [こちら](http://download.kde.org/stable/krita/4.1.1/)です (.sigのファイルです)

## Kritaを支援してください

Kritaは自由なオープンソースのプロジェクトです。[寄付](https://krita.org/jp/support-us-jp/donations-jp/)や[トレーニングビデオやアートブックの購入](https://krita.org/jp/support-us-jp/shop-jp/)で、プロジェクトを支援することを検討してみてください！皆様の支援によって、コアチームがフルタイムでKritaの開発作業を続けることが可能になります。

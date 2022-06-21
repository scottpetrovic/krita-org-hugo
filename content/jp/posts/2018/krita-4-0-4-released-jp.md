---
title: "Krita 4.0.4 リリース!"
date: "2018-06-18"
categories: 
  - "uncategorized-jp"
---

KritaチームはKrita4.0.0のバグ修正リリースであるKrita 4.0.4をリリースしました。Krita 4.0系列の最後のバグ修正リリースになります。

Krita 4.0.4で修正されたバグのリストはこちらです:

- OpenColorIOがmacOSで機能するようになりました
- 透明度マスクでピクセルブラシでペイントしたときのゴミを修正しました ([BUG:394438](https://bugs.kde.org/show_bug.cgi?id=394438))
- ジェネレータレイヤーを使用したときの競合状態を修正しました
- 変形マスク編集時のクラッシュを修正 ([BUG:395224](https://bugs.kde.org/show_bug.cgi?id=395224))
- Ten Brushスクリプトにプリセットメモリを追加しました。ブラシプリセット間のスイッチ切り替えがよりスムーズになったはずです
- ストロークレイヤースタイルのパフォーマンス改善 ([BUG:361130](https://bugs.kde.org/show_bug.cgi?id=361130), [BUG:390985](https://bugs.kde.org/show_bug.cgi?id=390985))
- .kraファイルの入れ子構造を禁止しました: .kraファイルをファイルレイヤーでの埋め込みに使用するとロード時に壊れてしまいます
- 閾値フィルタを適用する際にアルファチャンネルを保持するようになりました ([BUG:394235](https://bugs.kde.org/show_bug.cgi?id=394235))
- バンドル名をタグ名として自動的に使用することをやめました ([BUG:394345](https://bugs.kde.org/show_bug.cgi?id=394345))
- Pythonパレットドッキングパネルを使用している時の色選択を修正 ([BUG:394705](https://bugs.kde.org/show_bug.cgi?id=394705))
- 新しいビューを開いたタイミングではなく、Krita起動時に前回使用した色を復元するようになりました ([BUG:394816](https://bugs.kde.org/show_bug.cgi?id=394816))
- 現在選択しているのがマスクであってもレイヤーグループの作成を許可するように変更 ([BUG:394832](https://bugs.kde.org/show_bug.cgi?id=394832))
- セグメントグラデーションエディタで正しい不透明度を表示するように修正 ([BUG:394887](https://bugs.kde.org/show_bug.cgi?id=394887))
- 古いテキストツールのショートカットを削除 ([BUG:393508](https://bugs.kde.org/show_bug.cgi?id=393508))
- マルチブラシの角度で小数点以下を許可するように変更
- OpenGLキャンバスのパフォーマンス改善、特にmacOSで改善
- アイソレートモードでのパススルーグループレイヤーのペイントを修正 ([BUG:394437](https://bugs.kde.org/show_bug.cgi?id=394437))
- OpenEXRファイルの読み込みパフォーマンス改善(Jeroen Hoolmansによるパッチ)
- Kritaが非常にビジー状態であっても自動保存を行うように変更
- デフォルト言語の読み込みを改善
- ダブルクリップでの色ピックを修正 ([BUG:394396](https://bugs.kde.org/show_bug.cgi?id=394396))
- FFMpeg読み出し時のフレーム数値の不一致を修正 ([BUG:389045](https://bugs.kde.org/show_bug.cgi?id=389045))
- macOSでのチャンネル入れ替わり問題を修正、16,32 bit浮動小数点数チャンネルの赤と青が入れ替わっていました
- 最近のQtバージョンで起きていたタッチイベントの受け入れ問題を修正
- Breezeテーマのインテグレーション時の問題を修正: Kritaはウィジェットをマルチスレッドで生成しなくなりました ([BUG:392190](https://bugs.kde.org/show_bug.cgi?id=392190))
- Pythonから画像を読み込んだ時のバッチモードフラグを修正
- WindowsとmacOSでのシステムカラープロファイルの読み込み
- macOSでのクラッシュを修正 ([BUG:394068](https://bugs.kde.org/show_bug.cgi?id=394068))

## ダウンロード

### Windows

Windowsユーザーの皆さんへ：もしクラッシュする事案に遭遇した場合は、[この案内（英語）](https://docs.krita.org/en/reference_manual/dr_minw_debugger.html#dr-minw) に従いデバッグシンボルをKritaに追加してください。これによってKritaがクラッシュした原因をログから解析できるようになります。

- 64ビットWindows版: [krita-x64-4.0.4-setup.exe](https://download.kde.org/stable/krita/4.0.4/krita-x64-4.0.4-setup.exe)
- 64ビットWindowsポータブル版: [krita-x64-4.0.4.zip](https://download.kde.org/stable/krita/4.0.4/krita-x64-4.0.4.zip)
- [32ビット版向けデバッグシンボル(Kritaをインストールしたフォルダに展開して使用)](https://download.kde.org/stable/krita/4.0.0/krita-x64-4.0.4-dbg.zip)

- 32ビットWindows版: [krita-4.0.4-x86-setup.exe](https://download.kde.org/stable/krita/4.0.4/krita-x86-4.0.4-setup.exe)
- 32ビットWindowsポータブル版: [krita-x86-4.0.4.zip](https://download.kde.org/stable/krita/4.0.4/krita-x86-4.0.4.zip)
- [32ビット版向けデバッグシンボル(Kritaをインストールしたフォルダに展開して使用)](https://download.kde.org/stable/krita/4.0.4/krita-x86-4.0.4-dbg.zip)

### Linux

- 64ビットLinux用AppImage版: [krita-4.0.4-x86\_64.appimage](https://download.kde.org/stable/krita/4.0.4/krita-4.0.4-x86_64.appimage)

(なぜかFirefoxはテキストとして読み込もうとするようです。ダウンロードするにはリンクの右クリックから保存してください) 更新がされると、Ubuntuと派生ディストリビューションでは[Krita Lime PPA](https://launchpad.net/%7Ekritalime/+archive/ubuntu/ppa)からもKrita 4.0.4をインストールできるようになります。snapの更新については作業中です。

### OSX

- OSXディスクイメージ版: [krita-4.0.4.dmg](https://download.kde.org/stable/krita/4.0.4/krita-4.0.4.dmg)

注意: タッチドッキングパネル、gmic-qtとPythonプラグインはmacOSで利用できません。

### ソースコード

- ソースコード: [krita-4.0.4.tar.gz](https://download.kde.org/stable/krita/4.0.4/krita-4.0.4.tar.gz)

### md5sum

すべてのダウンロード向け:

- [md5sum.txt](https://download.kde.org/stable/krita/4.0.4/md5sum.txt)

### キー

Linux appimageとソースのtarボールは署名されています。パブリックキーをhttps経由で取得できます: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8) 署名は [こちら](http://download.kde.org/stable/krita/4.0.4/)です (.sigのファイルです)

## Kritaを支援してください

Kritaは自由なオープンソースのプロジェクトです。[寄付](https://krita.org/jp/support-us-jp/donations-jp/)や[トレーニングビデオやアートブックの購入](https://krita.org/jp/support-us-jp/shop-jp/)で、プロジェクトを支援することを検討してみてください！皆様の支援によって、コアチームがフルタイムでKritaの開発作業を続けることが可能になります。

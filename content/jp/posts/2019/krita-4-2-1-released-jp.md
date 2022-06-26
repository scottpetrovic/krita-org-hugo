---
title: "Krita 4.2.1 リリース"
date: "2019-06-07"
categories: 
  - "officialrelease-jp"
---

## Krita 4.2.1

4.2.0のすぐ後ですが、Krita 4.2.1をリリースします。最重要事項は、このリリースが長時間ペイントした時にUndoスタックが無限に拡大するためスローダウンするという問題を修正するということです。他の修正もあります。latin 1以外の文字を使った画像名の場合に起こるベクターレイヤーを持つ.kraファイルの保存と読み込みの問題も修正しています。修正の一部は新しい貢献者のCarl OlssonとDmitry Utkinによるものです。ありがとうございます！

修正リストは以下です。

- Fix slowdown after a longer period of use ([BUG:408255](https://bugs.kde.org/show_bug.cgi?id=408255), [BUG:408133](https://bugs.kde.org/show_bug.cgi?id=408133))
- Fix loading vector layers when the image name is not latin1 ([BUG:408280](https://bugs.kde.org/show_bug.cgi?id=408280))
- Fix rectangular grid spacing limits incorrect after resizing canvas ([BUG:408166](https://bugs.kde.org/show_bug.cgi?id=408166))
- Fix layer properties window draws on top of other application windows ([BUG:408170](https://bugs.kde.org/show_bug.cgi?id=408170))
- Fix the posterize filter to use non-linear sRGB for computation
- Allow the animation render to start at frame 0 at all times ([BUG:408198](https://bugs.kde.org/show_bug.cgi?id=408198))
- Enable the Select Opaque actions for group layers ([BUG:408236](https://bugs.kde.org/show_bug.cgi?id=408236))
- Check whether the drive still exists before creating a temporary directory for animation rendering ([BUG:408246](https://bugs.kde.org/show_bug.cgi?id=408246))
- Prevent the user from deleting locked layers when pressing shift-del too quickly
- Fix copying and duplicating vector layers ([BUG:408028](https://bugs.kde.org/show_bug.cgi?id=408028))
- Fix Krita's canvas being transparent on Linux when built against older versions of Qt ([BUG:408225](https://bugs.kde.org/show_bug.cgi?id=408225))
- Fix possible small delays at the beginning of a stroke ([BUG:408133](https://bugs.kde.org/show_bug.cgi?id=408133))
- Fix folding/unfolding when clicking on a layer thumbnail
- Fix undo/redo when working with guides (patches by Summer of Code student Tusooa Zhu)
- Fix reversed Python API guides lock/show states ([BUG:408113](https://bugs.kde.org/show_bug.cgi?id=408113))
- Make the minimum size for brushes consistent through the application
- Make the auto brush spacing precision values consistent ([BUG:359453](https://bugs.kde.org/show_bug.cgi?id=359453))
- Improve selection behaviour on the layer docker ([BUG:408002](https://bugs.kde.org/show_bug.cgi?id=408002))
- Fix macOS zoom and rotate icon getting stuck ([BUG:404321](https://bugs.kde.org/show_bug.cgi?id=404321))
- Fix the vector stroke style propagating to other vector objects [(BUG:407683](https://bugs.kde.org/show_bug.cgi?id=407683))
- Fix the Document Tools plugin ([BUG:408146](https://bugs.kde.org/show_bug.cgi?id=408146))
- Fix the layer name being deselected when opening the layer name editor ([BUG:400357](https://bugs.kde.org/show_bug.cgi?id=400357))

Krita 4.2.1のビルドでQt 5.12.3を使用するようになりました。ドラッグアンドドロップの一部の問題が解決するはずです。Windowsではディスプレイスケールの新しい問題が起きている恐れがあります。というのも4.2.0で使用したQtの実験的パッチがコンフリクトを起こすようになってしまったからです。

## ダウンロード

### Windows

Windowsユーザーの皆さんへ：もしクラッシュする事案に遭遇した場合は、[この案内（英語）](https://docs.krita.org/en/reference_manual/dr_minw_debugger.html#dr-minw) に従いデバッグシンボルをKritaに追加してください。これによってKritaがクラッシュした原因をログから解析できるようになります。

- 64 bits Windows: [krita-x64-4.2.1-setup.exe](https://download.kde.org/stable/krita/4.2.1/krita-x64-4.2.1-setup.exe)
- 64ビットWindowsポータブル版: [krita-x64-4.2.1.zip](https://download.kde.org/stable/krita/4.2.1/krita-x64-4.2.1.zip)
- [デバッグシンボル(Kritaをインストールしたフォルダに展開して使用)](https://download.kde.org/stable/krita/4.2.1/krita-x64-4.2.1-dbg.zip)

- 32ビットWindows版: [krita-x86-4.2.1-setup.exe](https://download.kde.org/stable/krita/4.2.1/krita-x86-4.2.1-setup.exe)
- 32ビットWindowsポータブル版: [krita-x86-4.2.1.zip](https://download.kde.org/stable/krita/4.2.1/krita-x86-4.2.1.zip)
- [デバッグシンボル(Kritaをインストールしたフォルダに展開して使用)](https://download.kde.org/stable/krita/4.2.1/krita-x86-4.2.1-dbg.zip)

### Linux

- 64ビットLinux用AppImage版: [krita-4.2.1-x86_64.appimage](https://download.kde.org/stable/krita/4.2.1/krita-4.2.1-x86_64.appimage)
- 64ビットLinux [G'Mic-Qt plugin appimage](https://download.kde.org/stable/krita/4.2.1/gmic_krita_qt-x86_64.appimage)

(なぜかFirefoxはテキストとして読み込もうとするようです。ダウンロードするにはリンクの右クリックから保存してください)

### OSX

- OSXディスクイメージ版: [krita-4.2.1.dmg](https://download.kde.org/stable/krita/4.2.1/krita-4.2.1.dmg)

注意: gmic-qtはOSXで利用できません。

### ソースコード

- [krita-4.2.1.tar.gz](https://download.kde.org/stable/krita/4.2.1/krita-4.2.1.tar.gz)
- [krita-4.2.1.tar.xz](https://download.kde.org/stable/krita/4.2.1/krita-4.2.1.tar.xz)

### md5sum

すべてのダウンロード向け:

- [md5sum.txt](https://download.kde.org/stable/krita/4.2.1/md5sum.txt)

### キー

Linux appimageとソースのtarボールは署名されています。パブリックキーをhttps経由で取得できます: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8) 署名は [こちら](http://download.kde.org/unstable/krita/4.2.0-beta2/)です (.sigのファイルです)

## Kritaを支援してください

Kritaは自由なオープンソースのプロジェクトです。[寄付](https://krita.org/jp/support-us-jp/donations-jp/)や[トレーニングビデオやアートブックの購入](https://krita.org/jp/support-us-jp/shop-jp/)で、プロジェクトを支援することを検討してみてください！皆様の支援によって、コアチームがフルタイムでKritaの開発作業を続けることが可能になります。

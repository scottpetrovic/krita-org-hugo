---
title: "Krita 3.1第4ベータ版リリース"
date: "2016-11-21"
categories: 
  - "uncategorized-jp"
---

Krita 3.1の第4ベータです! Krita 3.1より、Kritaは正式にOSXに対応します。OSXユーザーの皆さんには以前の「安定版」のOSX版の代わりにぜひこのバージョンを使うことを強くおすすめします。第4ベータをリリースするのは画像の保存に関するコードにさらに変更を加えたからです…より安全になっているはずですが、テストを是非お願いします！

最重要の修正項目は以下になります:

- スタビライザのフレームレート改善
- 以前のベータ(3.0.92)でのアニメーション保存に関するリグレッションバグの修正
- スクラッチパッドに描いた時のクラッシュバグを修正
- 「色をアルファに」フィルタでの色選択が正しく機能するように修正

注意：このベータ版にはまだ自動塗り分けマスク/自動塗り分けブラシプラグインが含まれていますが、現在のアルゴリズムは実用とするには遅すぎるため3.1安定版リリースにはこの機能はおそらく含まれません。現在も開発は新しいアルゴリズムの調査と実験を続けています。今回のベータ版では自動塗り分けマスクのインターフェースを実際に触って確かめることができますが、自動塗り分けマスクの動作が実用には遅すぎること、そして我々もそのことを把握しており、現在修正作業を行っているということは心の片隅に留めておいてください。

第4ベータ版はこれまでのベータより遥かに安定で実用に堪えるものとなっています。そして皆さんに是非このバージョンを制作に使っていただいて、バグや問題の発見に協力してくださるとうれしいです！

Krita 3.1の新機能については[リリースノート](https://krita.org/en/release-notes-for-krita-3-1)でさらに知ることができます。リリースノートはまだ作業中ですが、それでも機能のスニークピークは可能です！

### Windows

Windowsユーザ向けのお知らせ: クラッシュに遭遇した場合は、[こちらの手順](https://docs.krita.org/Dr._Mingw_debugger) に従ってデバッグシンボルを使い、Kritaがどこでクラッシュしているかを突き止められるようにしてください。

- 32ビットWindows版: [krita-3.0.93-x86-setup.exe](http://download.kde.org/unstable/krita/3.0.93/krita-3.0.93-x86-setup.exe) (MD5 Hash: ad8d773b10772616e5d8ed623c648a80)
- 32ビットWindows用ポータブル版: : [krita-3.0.93-x86.zip](http://download.kde.org/unstable/krita/3.0.93/krita-3.0.93-x86.zip) (MD5 Hash: a4632822eeea5ce572544ea9a3b53d41)
- [32ビット向けデバッグ用コンポーネント（Kritaをインストールしたフォルダに解凍してください)](http://download.kde.org/unstable/krita/3.0.93/krita-3.0.93-x86-dbg.zip) (MD5 Hash: dc59208feabb7af99267984a6fe5a5e1)

- 64ビットWindows版: [krita-3.0.93-x64-setup.exe](http://download.kde.org/unstable/krita/3.0.93/krita-3.0.93-x64-setup.exe) (MD5 Hash: 2930af181a810c4974d7f056d751e766)
- 64ビットWindows用ポータブル版: [krita-3.0.93-x64.zip](http://download.kde.org/unstable/krita/3.0.93/krita-3.0.93-x64.zip) (MD5 Hash: 9d895b6727d835e0267e4c20aa3d8934)
- [64ビット向けデバッグ用コンポーネント（Kritaをインストールしたフォルダに解凍してください)](http://download.kde.org/unstable/krita/3.0.93/krita-3.0.93-x64-dbg.zip) (MD5 Hash: 3beca45f6ba2b3c43ce70aee2b27742d)

### Linux

- 64ビットLinux版: [krita-3.0.93-x86\_64.appimage](http://download.kde.org/unstable/krita/3.0.93/krita-3.0.93-x86_64.appimage) (MD5 Hash: ff3e3f49fbd095504b7cdb3af5698c96)

またUbuntu App Storeのベータチャンネルからsnap imageも利用可能です。

### OSX

- OSX ディスクイメージ: [krita-3.0.93.dmg](http://download.kde.org/unstable/krita/3.0.93/krita-3.0.93.dmg) (MD5 Hash: acd4056716f8c272d8975ed9ca8f0a9d)

### ソースコード

- ソースコード: [krita-3.0.93.tar.gz](http://download.kde.org/unstable/krita/3.0.93/krita-3.0.93.tar.gz) (MD5 Hash: 6c26648fe82887ad28a0bf84711292cc)

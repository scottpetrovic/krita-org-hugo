---
title: "Krita 3.1第3ベータ版リリース"
date: "2016-11-09"
categories: 
  - "uncategorized-jp"
tags: 
  - "japanese"
---

Krita 3.1第3ベータ版がリリースされました。Krita 3.1より、Kritaは正式にOSXに対応します。OSXユーザーの皆さんには以前の「安定版」のOSX版の代わりにぜひこのバージョンを使うことを強くおすすめします。

[![krita_animation_3_0_2](/images/posts/2016/krita_animation_3_0_2-1024x826.gif)](/images/posts/2016/krita_animation_3_0_2.gif)

このベータ版での特筆すべき重要な変更点は保存が画像の出力を待たなくなったことです。つまり、Kritaが何かの作業で手一杯の時に保存を行おうとした場合、保存したファイルが壊れているという警告が出る可能性があるということです。現在もこれに関する開発は続行中で、この解決策が保存に関する問題の最終結果になるわけではありません。もしデータを失いたくない場合は、こまめに保存するようにしましょう…

以下が最重要の修正です。

- 幾つかのクラッシュが起きるバグを修正
- 2つのレイヤーを結合した際、前後フレームの表示まで結合しないように修正
- 上下左右対称描画モードが開いた画像それぞれに異なる対称軸を持てるように修正
- 解像度タグが壊れているPNG画像を読み込めるように修正
- 変形ツール使用時の剪断カーソルを復元
- スプラッシュ画面のイラストを更新
- ACOファイルの色名の読み込みを修正
- Photoshopショートカットキーテーマの読み込みの修正（前回のベータ版でメニュー画面に何も表示されなくなっていた場合、ええ、このベータ版でその修正が行われています）

※このベータ版にはまだ自動塗り分けマスク/自動塗り分けブラシプラグインが含まれていますが、現在のアルゴリズムは実用とするには遅すぎるため3.1安定版リリースにはこの機能はおそらく含まれません。現在も開発は新しいアルゴリズムの調査と実験を続けています。今回のベータ版では自動塗り分けマスクのインターフェースを実際に触って確かめることができますが、自動塗り分けマスクの動作が実用には遅すぎること、そして我々もそのことを把握しており、現在修正作業を行っているということは心の片隅に留めておいてください。

第3ベータ版はまた第1、第2ベータ版より遥かに安定で実用に堪えるものとなっています。そして皆さんに是非このバージョンを制作に使っていただいて、バグや問題の発見に協力してくださるとうれしいです！

### Windows

- 32ビットWindows版: [krita-3.0.92-x86-setup.exe](http://download.kde.org/unstable/krita/3.0.92/krita-3.0.92-x86-setup.exe) (MD5 Hash: 092d30cbb158b7ebdc027ddba4ae768d)
- 32ビットWindows用ポータブル版: [krita-3.0.92-x86.zip](http://download.kde.org/unstable/krita/3.0.92/krita-3.0.92-x86.zip) (MD5 Hash: 78de5fb91b81b6b2c2f08711be5b9a57)
- [32ビット向けデバッグ用コンポーネント（Kritaをインストールしたフォルダに解凍してください） (MD5 Hash: 634630de985522f6b9f88b5f07d30c65)](http://download.kde.org/unstable/krita/3.0.92/krita-3.0.92-x86-dbg.zip)

- 64ビットWindows版: [krita-3.0.92-x64-setup.exe](http://download.kde.org/unstable/krita/3.0.92/krita-3.0.92-x64-setup.exe) (MD5 Hash: 37ae1e819948abeefb2b50497bd01993)
- 64ビットWindows用ポータブル版: [krita-3.0.92-x64.zip](http://download.kde.org/unstable/krita/3.0.92/krita-3.0.92-x64.zip) (MD5 Hash: 74f15723011b8429c6431aba65d77e1a)
- [64ビット向けデバッグ用コンポーネント（Kritaをインストールしたフォルダに解凍してください）(MD5 Hash: 7d958532d84e73d1d3eaeb29a7ae17b8)](http://download.kde.org/unstable/krita/3.0.92/krita-3.0.92-x64-dbg.zip)

### Linux

- 64ビットLinux版: [krita-3.0.92-x86_64.appimage](http://download.kde.org/unstable/krita/3.0.92/krita-3.0.92-x86_64.appimage) (MD5 Hash: 2437a99ca375fcf79647147680714076)

またUbuntu App Storeのベータチャンネルからsnap imageも利用可能です。

### OSX

- OSXディスクイメージ: [krita-3.0.92.dmg](http://download.kde.org/unstable/krita/3.0.92/krita-3.0.92.dmg) (MD5 Hash: 4a938af31688f321d75285825a19d902)

### ソースコード

- ソースコード: [krita-3.0.92.tar.gz](http://download.kde.org/unstable/krita/3.0.92/krita-3.0.92.tar.gz) (MD5 Hash: 1a794cd2758e1bf1c63354ae829b0947)

---
title: "Krita 2.9.10リリース"
date: "2015-12-09"
categories: 
  - "uncategorized-jp"
tags: 
  - "japanese"
---

もう2.9台10番目のリリースとなりました！かなりの数のバグ修正が行われましたが、ここ最近はKrita 3.0の最初のアルファ版のリリースのための作業に追われています。AMDプロセッサを使用しているシステムをお使いの皆さんにおきましては、今回のバージョンはベクトル化のサポートを無効にできるオプションが加わったという点で特に注目すべきものとなっています。これでパフォーマンスの向上が望めるでしょうが、AMDシステムを使われている皆さんに限った話です！そして今回のバグ修正には新たなコントリビューター、Nicholas LaPointe氏が加わっています！

順番は整っていないですが、以下が今回のバグ修正の一覧です：

-  芸術的テキストツールの選択で起こるクラッシュを修正（bug 354907）
- タグの保存を修正：タグ保存の際にロケールコーデックの代わりにUTF-8コーデックを使用する（bug 356306：※これでタグを日本語にしても文字化けすることがなくなります）
- 画像を縮小の際、倍率が0に近くなりすぎた時にクラッシュしないように修正（bug 356156）
- 基本的な絵コンテテンプレートを追加
- .kraファイル及び.oraファイルのサムネイル生成を修正（bug 355884）
- Kritaで保存したPSDファイルのPhotoshopでの読み込みを修正（bug 355110）
- ベクトル化による高速化を無効にするオプションを追加。これはAMDプロセッサのバグに対するものです。
- デバッグ用にOpenGLのログをとるオプションを追加
- 色プロファイルがタグ付けされていない16ビット/チャンネルPNG画像をインポートする際に一番最近使用したプロファイルを記憶するように修正
- ユーザーがキャンセルした時に間違ったエラーコードを吐くいくつかのインポート/エクスポートフィルタを修正。これはNicholas LaPointe氏によるパッチです。ありがとうございます！
- 遅い動作の時に稀に起こるクラッシュを修正（bug 352918）
- ある状況下での画像の再計算時にごくまれに発生するクラッシュを修正（bug 353043）
- レイヤーを削除後にサブウィンドウを切り替えた時にクラッシュする問題を修正（bug 355205）
- 画像を保存し、解像度の高い画像を新規作成した後これをサムネイルサイズまで縮小した時のメモリの使い方を向上
- 小型色選択を他の色選択と色レイアウトで矛盾することが無いように修正（bug 353505）
- 複数の画像で作業した際に時々発生するクラッシュを修正（bug 354975）
- 描画補助線を使った際に起こるクラッシュを修正（bug 353152）
- 複雑な演算の際に発生しうる稀な状況を修正（bug 345562）
- キャンバスのみ表示にした時から元に戻した時ウィンドウが正しく復元されるように修正（bug 352018）

Ubuntu Linux、Windows及びOSXのパッケージは[いつものところ](https://krita.org/download/krita-desktop/)にあります！Steam版のユーザーの皆さんはベータチャンネルから新パッケージにアクセスできるようになりました。現在Stuart氏がアニメーションブランチからのパッケージの作業を行っています。そしてアニメーションベータ版についてですが…今週末、おそらくUbuntu LinuxとWindowsへの新たなアニメーションブランチパッケージをリリースすることになるはずです！
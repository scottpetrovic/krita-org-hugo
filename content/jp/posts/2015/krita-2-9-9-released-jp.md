---
title: "Krita 2.9.9リリース"
date: "2015-11-05"
categories: 
  - "uncategorized-jp"
tags: 
  - "japanese"
---

Kritaの毎月のバグ修正リリースの9個目です！アップグレードすると以下の修正と機能が利用できます:

### 新機能

- ベクターレイヤーでフリーハンドブラシを使用しようとした時にメッセージ表示を追加
- カラーカーブフィルタダイアログを呼び出すctrl-mショートカットの追加。Raghavendra Kamathさんによるパッチです。ありがとうございます!
- 空のレイヤーやマスクを追加した時の更新を行わないことでパフォーマンスを向上

### 修正

- 芸術的テキストツールの修正。2.9.8での退行バグでグローバルのショートカットで使用されている文字が入力できなくなっていました。この問題は修正されました
- Inkscapeで作成したODGを読み込んだ時のクラッシュの修正。ただしファイル自体が正しく表示されない問題については原因調査中です
- ガウシアンブラーフィルタの修正。2.9.8の退行バグで、ガウシアンブラーフィルタを適用すると右端と下端が半透明になっていました
- OSXでの使用可能メモリ計算の修正。René J.V. Bertinさんのパッチに感謝します!
- レイヤーの複製時に、チャンネルフラグも複製するように修正。元のレイヤーがアルファをロックしている場合、新しいレイヤーもその状態になります
- Undoシステムとコンポジットドッキングパネルの見つけにくいクラッシュ問題を数個修正
- exiv2関係のjpeg保存の修正
- ダークテーマの新しいパススルーアイコンの追加

最新のKritaの入手は[ダウンロードページ](https://jp.krita.org/download/krita-desktop/)で! ([ScottのKrita本](https://jp.krita.org/item/new-krita-book-release-and-giveaway/) や [Animtimの最新トレーニングDVD](https://jp.krita.org/item/secrets-of-krita-the-third-krita-training-dvd/)のチェックもお忘れなく!)

### 次期バージョンのKrita

次のKritaのメジャーバージョンは3.0で、確実に近づいてきています!ショートカットの問題、OpenGLキャンバスの問題、アイコンの問題といった修正について、そしてパッケージ作成について多くの開発作業が行われています。Ubuntu Linuxユーザは既に[Lime](https://launchpad.net/~dimula73/+archive/ubuntu/krita)リポジトリでKrita 3.0 Unstableパッケージが利用可能です。WindowsとOSXのパッケージについては作業中です。

以下はWoltheraによるデモです:

<iframe src="https://www.youtube.com/embed/kWHK68iCRHk?feature=oembed" width="500" height="281" frameborder="0" allowfullscreen="allowfullscreen"></iframe>

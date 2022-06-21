---
title: "Windows向け新しいKrita 3.0アルファ/開発中ビルド"
date: "2016-04-19"
categories: 
  - "uncategorized-jp"
tags: 
  - "japanese"
---

今まで、KritaのWindowsリリースはマイクロソフトのVisual C++コンパイラで作成してきました。Krita2.9はVisual C++の2012バージョン、3.0は2015バージョンでビルドされていました。どちらのバージョンも[G’Mic library](http://gmic.eu/)のビルド、そして最新の[Vc library](https://github.com/VcDevel/)のビルドにおいて問題があります。G'Micは広範なフィルタを提供し、Vcはピクセルのブレンド、ブラシマスクのコードを最適化するものです。

ライブラリを修正することも、マイクロソフトのコンパイラの修正も我々には不可能で、Kritaが遅くなることも機能を減らすことも望ましくない、ということで残された解決策は1つでした。別のコンパイラを探すことです。開発サイクルの遅くにこうしたことを行うのは恐ろしいことではあります。どのコンパイラにもそれぞれの癖とバグがあるからです。今回の[ビルドは実はLinuxで作成しています](http://www.valdyas.org/fading/index.cgi/hacking/krita/mxe_krita.html)。

テスト用の新しいビルドを用意しました。4つのビルドが存在しています。デバッグ情報の有無、そして32bitと64bit版です。クラッシュした場合、デバッグ版のビルドもダウンロードして、そのビルドでクラッシュの再現テストをお願いします。先日の3.0アルファに比べて、修正されたバグもあります。機能も増えています。カメラRAWインポートプラグインとPDFインポート/エクスポートプラグインが含まれています。32bit版にもG'Micが同梱されています。これはVisual Studioでは不可能でした。Linux版に存在していてWindows版にない唯一の機能は.jp2ファイルの読み書きを行うOpenJPEGサポートです。(通常のjpegファイルはサポートされています。)

ビルドはこの場所にあります: [http://files.kde.org/krita/3/windows/devbuilds](http://files.kde.org/krita/3/windows/devbuilds). sha1チェックサムファイルでダウンロードの検証が可能です。 デバッグではないビルドの直接ダウンロードリンクはこちらです:

- [32 bits](http://files.kde.org/krita/3/windows/devbuilds/krita-master-f38b47e-x86.zip)
- [64 bits](http://files.kde.org/krita/3/windows/devbuilds/krita-master-f38b47e-x64.zip)

実行するには、Zipファイルを展開して、binフォルダに移動し、krita.exeを実行します。Visual Studio Cランタイムのインストールは必要ありません!Krita3.0はKrita2.9とは違う場所から設定とリソースファイルを読み込むので、既にインストールしたには影響を与えません。

[MXE](http://mxe.cc/)プロジェクトのおかげでこのビルド環境の設定は予想よりは簡単だったものの、それでもバグ修正に使う時間がとられてしまいました。そのため、3.0のリリーススケジュールを一か月延長することも検討しています。Windowsを使っているのなら、このビルドを全般的にテストをしてみてください、お願いします!

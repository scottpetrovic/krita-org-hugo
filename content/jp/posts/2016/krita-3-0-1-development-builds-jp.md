---
title: "Krita 3.0.1開発版"
date: "2016-07-23"
categories: 
  - "uncategorized-jp"
tags: 
  - "japanese"
---

予期せぬ事情により、今回はリリースのスケジュールを再調整せざるを得ず、昨週はリリースを行いませんでした。ですが、現在は9月5日に予定されている3.0.1のリリースで実装される予定のもののいくつかをぜひ皆さんにも体験してほしいと思っています。バグ修正（ファイルの名前にピリオドが二つ付いてしまうバグや安価なタブレットでクラッシュが発生する問題が修正され、グラフィックカードでメモリリークが発生する大きな問題も修正されました）から新機能（ソフトプルーフ等）までたくさんあります。もしかしたらバグがあるかもしれませんし、新機能がすべてうまく動くとも限りません。アニメGIF・動画の出力は現在も開発中で、多分開発者のPC以外では上手く動かないようです。

つまりこれは開発版です。ですが試してみて下さい。多くの観点で既に3.0安定版よりもいいものになっているはずです！

OSXでも既にいくつかの進展がありました。この開発版はOSX 10.9以降で動くはずです。全てのライブラリも最新版に合わせてアップデートされました。

#### Windows

WindowsではKritaはWacom、Huion、Yiynovaのタブレット及びSurface Proシリーズのタブレットをサポートしています。ポータブルZIPファイル版は解凍してショートカットkritaをダブルクリックして起動してください。

Windows版KritaはWindows 7、8、10でテストされています。現在は64ビット版のみです。DrMingwデバッガと一緒に使うことでクラッシュの原因を見つけられるデバッグビルドも用意されています。くわしくは[よくある質問の当該項（※英語）](https://docs.krita.org/KritaFAQ#How_can_I_produce_a_backtrace_on_Windows.3F)をご覧ください。このビルドにはベクトル化による最適化が適用されていないため、通常のビルドより低速である恐れがあります。

- [krita-3.0.1-Alpha-ef558bb-x64.zip](http://files.kde.org/krita/3/windows/devbuilds/krita-3.0.1-Alpha-ef558bb-x64.zip) (MD5: b4e4bc6563fdf1fd62f2b90ba66b3b6e)
- [krita3-x64-dbg-latest.zip](http://files.kde.org/krita/3/windows/debugbuilds/krita3-x64-dbg-latest.zip) (MD5: c039820a78272f2502cc3270b1cc7307

 

#### Linux

Linuxについてはあらゆる最近のLinuxディストリビューションで動作するはずの[AppImage](http://appimage.org/)版を提供します。AppImageをダウンロードして、実行可能にして起動してください。インストールは必要ありません。現時点では64ビット版のみです。

- [krita-3.0.1-Alpha-4c91a18-x86\_64.appimage](http://files.kde.org/krita/3/linux/devbuilds/krita-3.0.1-Alpha-4c91a18-x86_64.appimage) (MD5: 772ca9e719cf00d4de49fe68c226c41f)

#### OSXおよびMacOS

OSX版Kritaは3.1でフルサポートが実現される予定です。OSX版Krita 3.0にはまだ高速プレビューと高品質キャンバス表示が実装されていません。また画像のレンダリングの問題もあります―この問題はApple社がOpenGL互換性プロファイルのサポートを自社製品のディスプレイドライバとタッチパッドとタブレットのサポートの配布で打ち切ったことによるものです。現在Krita開発はこれらの機能のOpenGL 3.0コアプロファイルを使用した再実装を行っています。今のところはOSX版Kritaを何らかの生産的作業に使う際はOpenGLを無効にすることを推奨します。OSX版Kritaは10.9、10.10、10.11で動作し、MacOSでも動くことが報告されています。

- [krita-3.0.1-Alpha-4c91a18.dmg](http://files.kde.org/krita/3/osx/devbuilds/krita-3.0.1-Alpha-4c91a18.dmg) (MD5: 1d0faca3c92a36527c6fae048e442ce8)

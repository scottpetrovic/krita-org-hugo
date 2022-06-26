---
title: "Krita 3.0.1アルファビルド"
date: "2016-08-17"
categories: 
  - "uncategorized-jp"
tags: 
  - "japanese"
---

マージ期間が先週で終わり、Kritaは4週間の安定化期間に入りました。とても興味深いブランチがいくつかマージされ、ブラシ設定を手早く変更するための新しいヘッドアップディスプレイや、ウェーブレットフィルタ、閾値(二値化)フィルタ、数値入力欄に簡単な数式を使って入力できるようになったといった機能が入りました！残念ながら、ビデオ出力ブランチはすべて取り込めていないため、Gifアニメとビデオを保存する機能は入っていません。

またハードウェアの故障のため、一週間の間新しいビルドを作成できませんでした。KritaはすべてのOSに対してしっかりとしたビルドを作成する手助けするボランティアをまだ必要としています。今現在は、メンテナが他の仕事もしながら一人でビルド作成作業を行っています。とはいえ、ディスクを交換して、ようやく新しいビルドができました！

既にバグ修正の面では最新ではないのですが、それでも、どうかテストをしてください！バグを見つけたら、重ねてお願いですが、報告する前に、既に同じ報告がないかbugs.kde.orgでチェックしてください!

来週には最初のベータビルドを公開する予定です！正式リリースの予定は9月5日です。

#### Windows

WindowsではKritaはWacom、Huion、Yiynovaのタブレット及びSurface Proシリーズのタブレットをサポートしています。ポータブルZIPファイル版は解凍してショートカットkritaをダブルクリックして起動してください。

Windows版KritaはWindows 7、8、10でテストされています。現在は64ビット版のみです。DrMingwデバッガと一緒に使うことでクラッシュの原因を見つけられるデバッグビルドも用意されています。くわしくは[よくある質問の当該項（※英語）](https://docs.krita.org/KritaFAQ#How_can_I_produce_a_backtrace_on_Windows.3F)をご覧ください。このビルドにはベクトル化による最適化が適用されていないため、通常のビルドより低速である恐れがあります。

- [krita-3.0.1-alpha2-x64.zip](http://files.kde.org/krita/3/windows/devbuilds/krita-3.0.1-alpha2-x64.zip) (a0ee7187035d890445c468a381d3fc2c)
- [krita3-x64-dbg-latest.zip](http://files.kde.org/krita/3/windows/debugbuilds/krita3-x64-dbg-latest.zip) (a0c100335a7d55cfc2710fe1cb2b39a2)

#### Linux

Linuxについてはあらゆる最近のLinuxディストリビューションで動作するはずの[AppImage](http://appimage.org/)版を提供します。AppImageをダウンロードして、実行可能にして起動してください。インストールは必要ありません。現時点では64ビット版のみです。このappimageは実験的なデスクトップ統合を含んでいます。

- [krita-3.0.1-Alpha2-d33dbe0-x86_64.appimage](http://files.kde.org/krita/3/linux/devbuilds/krita-3.0.1-Alpha2-d33dbe0-x86_64.appimage) (f61f8991a517a7835ceebf7159288d8e)

#### OSXおよびMacOS

OSX版Kritaは3.1でフルサポートが実現される予定です。OSX版Krita 3.0にはまだ高速プレビューと高品質キャンバス表示が実装されていません。また画像のレンダリングの問題もあります―この問題はApple社が OpenGL互換性プロファイルのサポートを自社製品のディスプレイドライバとタッチパッドとタブレットのサポートの配布で打ち切ったことによるもので す。現在Krita開発はこれらの機能のOpenGL 3.0コアプロファイルを使用した再実装を行っています。今のところはOSX版Kritaを何らかの製作作業に使う際はOpenGLを無効にすることを 推奨します。OSX版Kritaは10.9、10.10、10.11で動作し、MacOSでも動くことが報告されています。

 

- [krita-3.0.1-Alpha2.dmg](http://files.kde.org/krita/3/osx/devbuilds/krita-3.0.1-Alpha2.dmg) (26a2ee299e63aed6a0a77b6c5a78ab0b)

#### ソース

ソースのtarには翻訳も含まれるようになりました。

- [krita-3.0.99.89.tar.xz](http://files.kde.org/krita/3/source/krita-3.0.99.89.tar.xz) (af9424c06ce6b1504859a5abd703955a)

---
title: "Krita 3.0.1ベータ版開発ビルド"
date: "2016-08-24"
categories: 
  - "uncategorized-jp"
tags: 
  - "japanese"
---

Krita 3.0.1に向け、新しい開発ビルドを作りました。今回修正されたバグの中でも重要なものは以下の通りです。

- 保存及びエクスポートがもっと安定しました（ただしTempフォルダにちゃんと空きがある必要があります）
- 二値化フィルタについて、マスクを使った時と8ビットRGBA以外の色空間でのプレビューの問題が修正されました。
- 3\_textureブラシ形状の問題が修正されました
- テンプレートの保存が再びちゃんと働くようになりました
- レイヤードッキングパネルの色ラベルの見た目が修正されました
- グリッドと基準線ドッキングパネルのレイアウトが修正されました
- マルチスレッド処理が全体的に改良されました。Andrew Savonichevさんのパッチに感謝を
- 倍率変更がブラシの変形の前に行われるようになり、新しい縦横比オプションはより正しく見えるようになりました
- NVidiaのGPUで補助線を使用した際に発生する表示の問題（画面が真っ暗になる等）が修正されました
- ブラシの切り替えがより速やかに行えるようになり、その際にメモリリークも起こらなくなりました

別のニュースとして、Krita開発チームは今週末オランダのデーフェンテルで実際に会っての会合を開きます。バグを修正し、新しい機能と新しいトレーニングビデオの企画等について話し合うことになります！

#### Windows

WindowsではKritaはWacom、Huion、Yiynovaのタブレット及びSurface Proシリーズのタブレットをサポートしています。ポータブルZIPファイル版は解凍してショートカットkritaをダブルクリックして起動してください。

Windows版KritaはWindows 7、8、10でテストされています。現在は64ビット版のみです。DrMingwデバッガと一緒に使うことでクラッシュの原因を見つけられるデバッグビルドも用意されています。くわしくは[よくある質問の当該項（※英語）](https://docs.krita.org/KritaFAQ#How_can_I_produce_a_backtrace_on_Windows.3F)をご覧ください。このビルドにはベクトル化による最適化が適用されていないため、通常のビルドより低速である恐れがあります。

- [krita-3.0.99.90-x64-beta.zip](http://files.kde.org/krita/3/windows/devbuilds/krita-3.0.99.90-x64-beta.zip) (MD5 e98b07a732e05bcb86ba038badcb44a4)
- [krita3-x64-dbg-latest.zip](http://files.kde.org/krita/3/windows/debugbuilds/krita3-x64-dbg-latest.zip) (MD5 65220e9f12ead3bf2752c4db989634f4)

#### Linux

Linuxについてはあらゆる最近のLinuxディストリビューションで動作するはずの[AppImage](http://appimage.org/)版を提供します。AppImageをダウンロードして、実行可能にして起動してください。インストールは必要ありません。現時点では64ビット版のみです。このappimageは実験的なデスクトップ統合を含んでいます。

- [krita-3.0.99.90-x64.appimage](http://files.kde.org/krita/3/linux/devbuilds/krita-3.0.99.90-x64.appimage) (MD5 2a39fddc1dece779ea36c3d03d08bb60)

また [UbuntuのApp Storeからsnap format](https://uappexplorer.com/app/krita.krita)でKritaを手に入れることもできます（※NVidiaのプロプライエタリドライバを使っている場合、Ubuntuの制限によりSnap版Kritaは使えません）このバージョンにはKrita自体への翻訳も含まれています。

#### OSX及びMacOS

OSX版Kritaは3.1でフルサポートが実現される予定です。OSX版Krita 3.0にはまだ高速プレビューと高品質キャンバス表示が実装されていません。また画像のレンダリングの問題もあります―この問題はApple社が OpenGL互換性プロファイルのサポートを自社製品のディスプレイドライバとタッチパッドとタブレットのサポートの配布で打ち切ったことによるもので す。現在Krita開発はこれらの機能のOpenGL 3.0コアプロファイルを使用した再実装を行っています。今のところはOSX版Kritaを何らかの製作作業に使う際はOpenGLを無効にすることを 推奨します。OSX版Kritaは10.9、10.10、10.11で動作し、MacOSでも動くことが報告されています。

- [krita-3.0.99.90.dmg](http://files.kde.org/krita/3/osx/devbuilds/krita-3.0.99.90.dmg) (a4c2dc7c51aa43adee7acceacaf82164)

#### ソースコード

- [krita-3.0.99.90.tar.gz](http://files.kde.org/krita/3/source/krita-3.0.99.90.tar.gz) (MD5 e5b50274b617cb5356030aa22cbcdf1b)

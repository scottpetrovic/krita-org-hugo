---
title: "新テスト用ビルド公開、及びKrita Sprintがもうすぐ終了します"
date: "2016-08-30"
categories: 
  - "uncategorized-jp"
tags: 
  - "japanese"
---

デーフェンテルで行われたKrita Sprintは火曜日に終わる予定で、参加したアーティストや開発者、ウェブサイト管理者たちは次々と帰宅の途についています。何人かはもう少しデーフェンテルにとどまる予定ですが、日曜日には既に帰っていた人もいました。

[![DSCF5848](/images/posts/2016/DSCF5848-1024x768.jpg)](/images/posts/2016/DSCF5848.jpg)

このような実際に会っての会合は疲れますがワクワクするものです！たくさんの議題が議論されました。

- 今年のKickstarterの目標だったベクターと[テキスト機能](https://phabricator.kde.org/T1004#50665)のUI設計について議論を行いました。実のところ、これに関する議論はまだ継続中です。
- OSXの正式サポートに向け、たくさんの作業がなされました―[OpenGLに関するパッチ](https://codereview.qt-project.org/#/c/166202)は遂にQt本体への統合が視野に入ってきました！またペンタブの操作についてもいくつかの修正が加えられました。
- KritaからGoogle Summer of Codeに参加した生徒三人全員が今回のスプリントに参加しました！Woltheraは彼女の担当したプロジェクトの2番目(1番目は3.0.1に実装予定の[ソフトプルーフ](http://wolthera.info/?p=802)です)となるKritaの内部色選択の完全な色管理への移行を完了させました。Jouniは開発中のアニメーション機能をプレゼンし、JulianはQtのOpenGL QPainterエンジンに関する彼の成果をプレゼンしました。

[![index](/images/posts/2016/index-1024x584.png)](/images/posts/2016/index.png)

 

- 我々はKrita財団から[Pepper＆Carrot](http://www.peppercarrot.com/)の本を出版する計画についてその作者であるDavid Revoyと議論を行いました。

[![Pepper loves Kiki!](/images/posts/2016/PepperLovesKiki_001-1024x724.png)](/images/posts/2016/PepperLovesKiki_001.png)

PepperはKikiが大好きです！

- リリース工程及び[ユーザーの機能提案](https://krita.org/jp/item/ways-to-help-krita-work-on-feature-requests-jp/)から実装と機能のリリースまでの過程を洗練させました
- Jouniはこの記事のスケッチを描いた人であり、優秀なアニメーターでもあるSteven氏とKritaのAnimationワークフローについて話し合いました
- リソース管理に対する新しいアーキテクチャとUXの必要性の大きさについて話し合いました
- ウェブサイトとウェブショップを改良すべく計画を立てました
- Dmitryは非常に大きな直径でも問題なく動作する―2500ピクセルも不可能ではありません―新しいブラシエンジン(油性ペン)を披露しました
- バグの修正に次ぐ修正を行いました…

[![Kiki_Angel &Demon](/images/posts/2016/Kiki_Angel-Demon-1-1024x724.png)](/images/posts/2016/Kiki_Angel-Demon-1.png)

- そして最後に、我々は素晴らしい時間を過ごせました。Kritaへの熱心な貢献者の多くは今まで実際に互いの顔を見たことはありませんでした、これからはIRCのニックネームたちやコミットメッセージ、Eメールアドレスにちゃんと顔と声がイメージできるようになるのです！

2016年度のKrita Sprintは[KDE e.V.](https://www.kde.org/community/donations/)(旅費)及び[Krita Foundation](https://krita.org/jp/support-us-jp/donations-jp/)(設備と食事)の提供で行われました。ありがとうございます！また我々は今回のスプリントを熱波がオランダを襲ったまさにその週に設定してしまいました。幸運にも我々は[デーフェンテル聖使徒ペトロ・パヴェル聖堂](http://petrusenpaulus.eu/)の涼しくて快適な地下室を使うことが出来ました。インターネットと電源を繋げば、素晴らしい開発兼ディナールームの出来上がりです！

[![DSCF5836](/images/posts/2016/DSCF5836-1024x768.jpg)](/images/posts/2016/DSCF5836.jpg)

#### テストビルド

そして新ビルドが出来ました！今回のビルドではスプラッシュスクリーンを新しいものにしました！そしてバグ修正も行われています。

[![electrichearts_20160517_20160820_kiki_02](/images/posts/2016/electrichearts_20160517_20160820_kiki_02-1024x594.png)](/images/posts/2016/electrichearts_20160517_20160820_kiki_02.png)

- OSXで線を引き始めた時の不透明度100%BLOBを修正しました
- 自動生成されたグラデーションをユーザーが削除できないようにしました
- リソース選択で削除したリソースを表示しようとしたときに発生するクラッシュを修正しました
- デフォルトのワークスペースを更新しました
- アニメーションのCSVフォーマットへのエクスポートを修正しました
- Windowsでの翻訳を修正しました(※訳注：frameworks-ki18nの何らかのバグにより、翻訳が上手く行われない場合があります。その場合Fallback language(予備言語)をAmerican English及び現在Kritaで選択している言語以外の言語(お勧めはBritish English)に変更して再起動すると選択している言語での翻訳が有効になります)

#### Windows

WindowsではKritaはWacom、Huion、Yiynovaのタブレット及びSurface Proシリーズのタブレットをサポートしています。ポータブルZIPファイル版は解凍してショートカットkritaをダブルクリックして起動してください。

Windows版KritaはWindows 7、8、10でテストされています。現在は64ビット版のみです。DrMingwデバッガと一緒に使うことでクラッシュの原因を見つけられるデバッグビルドも用意されています。くわしくは[よくある質問の当該項（※英語）](https://docs.krita.org/KritaFAQ#How_can_I_produce_a_backtrace_on_Windows.3F)をご覧ください。このビルドにはベクトル化による最適化が適用されていないため、通常のビルドより低速である恐れがあります。

- [krita\_3.0.99.91-x64.zip](http://files.kde.org/krita/3/windows/devbuilds/krita_3.0.99.91-x64.zip)
- [krita3-x64-dbg-latest.zip](http://files.kde.org/krita/3/windows/debugbuilds/krita3-x64-dbg-latest.zip)

#### Linux

Linuxについてはあらゆる最近のLinuxディストリビューションで動作するはずの[AppImage](http://appimage.org/)版を提供します。AppImageをダウンロードして、実行可能にして起動してください。インストールは必要ありません。現時点では64ビット版のみです。このappimageは実験的なデスクトップ統合を含んでいます。

- [krita-3.0.99.91-Beta-x86\_64.appimage](http://files.kde.org/krita/3/linux/devbuilds/krita-3.0.99.91-Beta-x86_64.appimage)

また [UbuntuのApp Storeからsnap format](https://uappexplorer.com/app/krita.krita)でKritaを手に入れることもできます。このバージョンにはKrita自体への翻訳も含まれています。インストールは以下で行ってください

snap install --beta krita

#### OSX及びMacOS

OSX版Kritaは3.1でフルサポートが実現される予定です。OSX版Krita 3.0にはまだ高速プレビューと高品質キャンバス表示が実装されていません。また画像のレンダリングの問題もあります―この問題はApple社が OpenGL互換性プロファイルのサポートを自社製品のディスプレイドライバとタッチパッドとタブレットのサポートの配布で打ち切ったことによるもので す。現在Krita開発はこれらの機能のOpenGL 3.0コアプロファイルを使用した再実装を行っています。今のところはOSX版Kritaを何らかの製作作業に使う際はOpenGLを無効にすることを 推奨します。OSX版Kritaは10.9、10.10、10.11で動作し、MacOSでも動くことが報告されています。

- [krita-3.0.99.91.dmg](http://files.kde.org/krita/3/osx/devbuilds/krita-3.0.99.91.dmg)

#### ソースコード

ソースコードのtarballは翻訳もすべて含んでいます。

- [krita-3.0.99.91.tar.gz](http://files.kde.org/krita/3/source/krita-3.0.99.91.tar.gz)

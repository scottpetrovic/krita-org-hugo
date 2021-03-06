---
title: "Google Summer of CodeでKritaに3つの枠が与えられました"
date: "2016-04-27"
categories: 
  - "uncategorized-jp"
tags: 
  - "japanese"
---

![GSoC2016Logo](/images/posts/2016/GSoC2016Logo.jpg)

毎年GoogleはGoogle Summer of Code (GSoC)というプログラムを行っています。世界中の学生がオープンソースソフトウェアでの開発での給与付きインターンシップに参加します。今年度は嬉しいことにKritaから3人の学生がこのプログラムへの参加を認められました！(誰が参加を認められるかはどれだけのソフトウェアが参加しているか、Googleがいくつ参加枠を用意しているか、そしてその枠がどれだけ[KDE](https://www.kde.org/)に割り当てられるかにかかっています) この3人の生徒は今年の夏はKritaで働き、Kritaの3つの重要な領域での開発を行うことになります。

以下がその3人が夏休みの数か月で挑む課題です。

1. **Jouni Pentikäinen**さん―GSoCプロジェクト概要―「このプロジェクトはKritaのアニメーション機能をさらに多くの種類のレイヤーとマスクにも拡張し、ある種のフレーム補完を行う手段を提供し、これらの機能のためにユーザーインターフェースを拡張することを狙います。」まとめると、Jouniは不透明度とフィルタレイヤー、もしかしたら変形マスクすらもアニメーションできるようにしようとしています。それだけでなく、Jouniはフレーム補完を制御する素晴らしいグラフエディタも実装しようとしています。
2. **Wolthera van Hövell tot Westerflier**さん―GSoCプロジェクト概要―「今のところ、Kritaのアーキテクチャは広色域での編集にはまだ必要なものが足りません。それには大きく二つのものがあげられます。それはソフトプルーフ機能と、sRGB色空間の外側の色を選択するための優れた色選択ダイアログです。」Woltheraさんの開発は、RGB画像を印刷した際にどれだけ元の画像からの変化が最小限にとどめられるかをプレビューで確認できるようにして、イラストレーションの印刷ワークフローをより楽にすることを狙うものです。さらにWoltheraさんはKritaの強力なカラーコアを拡張し、広色域ファイルでもフィルタをより正確に使えるようにすることも狙っています。
3. **Julian Thijsen**さん―GSoCプロジェクト概要―「私はQPainter classを動かすOpenGLエンジンのこれまでの機能に信頼性を取り戻し、その機能をOpenGL 3.2コアプロファイルを使って動かせるように書き換えることを狙っています―今のところQPainter classをOpenGL 3.2を使って動かすには互換性プロファイルが必要です。このプロジェクトはOSXの一部の表示を正常にし、おそらくKritaをMac OS Xコンピュータで動かすことが可能になるでしょう。」これは「OpenGLキャンバスバイパス演算」としか説明しようがありません。Kritaは現在OpenGL 2.1と3.0を使用しています。OSXでKritaを動かすには、全てを少なくともOpenGL 3.0で動かせるようにする必要があります。これは完全なOSXサポートを阻む最大の障害であり、我々はNimmyがこの挑戦を決意してくれたことに非常に興奮しています。

この説明は専門家以外には少し分かりづらく聞こえるかもしれませんが、これらの機能向上は大きな成果を生むことになるはずです。参加が認められた3人はおめでとう、そして今年の夏の幸運を祈ります！

---
title: "Kritaの2018年Google Summer of Code"
date: "2018-09-15"
categories: 
  - "news-jp"
---

今年もKritaは3人の学生とGoogle Summer of Codeに参加しました。今年の参加者は[Ivan](https://colorathis.wordpress.com/)、[Andrey](https://lieroz.github.io/)、 [Michael](https://simeir.github.io/)です。この3人の素晴らしい学生によるコードの一部は既に4.1.1に含まれています。残りのコードも既にマージされているので、[Windows](https://binary-factory.kde.org/job/Krita_Nightly_Windows_Build/)や[Linux](https://binary-factory.kde.org/job/Krita_Nightly_Appimage_Build/)のナイトリービルドでは利用可能です。では今年の成果を見てみましょう！

**Ivan**のプロジェクトはベクトル化によるブラシの高速化でした。技術的な感じがしますね。実際そうです。CPUは別の数字を使う同じ計算の場合、同時に非常に多くの計算を行うことができます。200個の数字をCPUに渡して、全部掛け算するように命令すると、1つの数字の掛け算と同じくらいの速度で完了します。ブラシでの計算も、そうした種類の計算に近いのです。もちろん、実際はもっと複雑です。Ivanはまだ同じロジックを定義済みブラシに適用する方法を探しています。何はともあれIvanの[ブログ](https://colorathis.wordpress.com/)からの素敵な画像です。

[![](/images/posts/2018/avx_cgauss_60.gif)](https://krita.org/wp-content/uploads/2018/09/avx_cgauss_60.gif)

上が以前の、下が今のパフォーマンスです。

Ivanのプロジェクトはパフォーマンスについてでしたが、**Andrey**のプロジェクトもそうです。Andreyも同じくらい技術的で頭が痛くなる問題に取り組んでいます。最近のCPUには多くのコアがあります。4個や8個、10個や20個やそれ以上の場合もあります。そして使用されないシリコンは砂の無駄使いになってしまいます！Kritaは昔からマルチコアを活用してきました。2009年のDmitry Kazakovによる[summer of codeプロジェクト](http://dimula73.blogspot.com/2009/08/gsoc-krita-tile-engine-wrap-up.html)、タイルエンジンについての開発からです。9年が経ち、Dmitryは今回Andreyのタイルエンジンの開発のメンタリングを行いました。タイルエンジンは画像を複数の小さなタイルに分割し、それぞれを独立して処理することを可能にします。

去年、DmitryはKritaがより多くのコアを使用できるようにする開発の中で、Kritaがコアが相互に処理を待ってしまう箇所があることを発見しました。何かをする必要がありました。これはロックと呼ばれるものです。このロックを取り除くことが解決策です。

そしてAndreyのプロジェクトはロックなしのタイル機能を作成することでした。この開発は完了しました。まだいくつかバグはあります。こうしたものは非常に複雑で、真剣にテストする必要があります。成果はKrita 4.2に含まれることになります。今年の終わりまでにリリースされる予定です。作業の一部はKrita 4.1.1にもマージされています。パフォーマンス改善が実現しています。

[![](/images/posts/2018/lockless-1024x506.png)](https://krita.org/wp-content/uploads/2018/09/lockless.png)

**Michael**はまったく違う開発を行いました。Kritaのパレットサポートです。パレット、カラーセットは色の集まりです。これはリソースです。かつてパレット編集はCalligra、KOfficeと共通したものでした。コードは複雑でこんがらがって散らばっていました。Michaelの最初のタスクはこの混沌を整理することで、それは既にKrita 4.1.1にマージされました。

次はパレットドッキングパネルです。詳細は[Phabricator](https://phabricator.kde.org/D14815)を参照してください。まだ開発中のものもありますが、Summer of Codeプロジェクトとして予定されていたものはすべて完了しました！

[![](/images/posts/2018/listanddocker-1024x512.jpg)](https://krita.org/wp-content/uploads/2018/09/listanddocker.jpg)

そしてこれがエディタです:

[![](/images/posts/2018/DlgPaletteEditor-1024x517.png)](https://krita.org/wp-content/uploads/2018/09/DlgPaletteEditor.png)

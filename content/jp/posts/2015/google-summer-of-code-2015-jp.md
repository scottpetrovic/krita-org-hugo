---
title: "2015年度Google’s Summer of code"
date: "2015-05-04"
categories: 
  - "uncategorized-jp"
---

[Google’s Summer of code 2015年度](http://www.google-melange.com/gsoc/projects/list/google/gsoc2015) の選抜学生一覧が発表されました。我々からは2人が選ばれました：JouniとWoltheraです。Woltheraは長年Kritaの開発者として作業を行っており、現在は色選択と遠近法補助線の開発を行っています。一方Jouniは2.9のバクフィックスを行ってきました。

Woltheraは現在新しいブラシエンジン、[接線法線マップブラシエンジン](http://www.google-melange.com/gsoc/project/details/google/gsoc2015/wolthera/5668600916475904) の開発を行っています。表面の法線は光が表面でどのように反射するかを決定するのに用いられるベクトルの一種です。3Dグラフィックで用いられる手法としてこれらを法線マップ(ノーマルマップ)としてエンコードするというものはあります。人間の目にはこのエンコードは虹のように見えます。このブラシエンジンはペンタブペンの傾きセンサを使用し、これを表面の法線の様に扱い、法線マップとして使用できる正しい色として出力します。手書きテクスチャへの関心から、私はこれがKritaにとって時間をかけて取り組むだけの価値あるものと考えています。[彼女の開発](https://projects.kde.org/projects/calligra/repository/show?rev=krita-testing-wolthera) はすでにかなりの進展を見せています。[フォーラムのスレッド](https://forum.kde.org/viewtopic.php?f=288&t=126128&p=333828#p333828) もぜひご確認ください。

[![tangent](/images/posts/2015/tangent-1024x683.png)](https://krita.org/wp-content/uploads/2015/04/tangent.png)

Jouniは昨年のアニメーションプロジェクトから得た教訓に基づき、[アニメーションをKritaコアへと統合](http://www.google-melange.com/gsoc/project/details/google/gsoc2015/joupent/5649050225344512) すべく開発を続けています。過去3つのアニメーションプラグインは全てプラグインであるということにより機能などに避けがたい制限がありました。Kritaのネイティブファイルフォーマット(.kra)はアニメーションのサポートも開始することになるはずです。JouniはGoogle Summer of Codeが発表される前からすでにアニメーション機能の開発を開始しており、そして実は既に概念実証と作動の段階にまで入っています。

[![animation](/images/posts/2015/animation-1024x640.png)](https://krita.org/wp-content/uploads/2015/04/animation.png)

実は2週間前に我々はKrita財団の支援を得て最初のスプリントをDeventerで行っていました。参加したのは開発者として期待されるJouniとWolthera、そして二人の指導者として期待されるDmitryとBoudewijnです。

[![2015-sprint](/images/posts/2015/2015-sprint-1024x768.jpg)](https://krita.org/wp-content/uploads/2015/04/2015-sprint.jpg)

JouniとWoltheraにおめでとうを、そして素晴らしいGoogle Summer of Codeを楽しみにしていてください！

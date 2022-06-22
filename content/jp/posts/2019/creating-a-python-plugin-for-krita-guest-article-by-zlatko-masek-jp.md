---
title: "Krita向けPythonプラグインの作成: Zlatko Mašekによるゲスト記事"
date: "2019-03-17"
categories: 
  - "uncategorized-jp"
---

# 著者について:

私はZlatko Mašekです。クロアチア出身のプログラマで、今はアイルランドに住んでいます。[ブログ](https://www.offsetlab.net/)を見ていただければわかると思いますが、アートと料理と社会変革について順不同ですが興味があります。情報科学の修士号を持っていて、大学では自然言語処理について作業したときにPythonに恋に落ちました。今ではPythonが私の選んだプログラム言語で、キャリアとしては社会に役立つ意義のあるアプリケーションを作ろうとしています。その一方で、Pythonは、いろいろな目的に使える言語で、趣味の小さなプロジェクトでも役立ちます。アートについては、いつも惹かれてきました。描けるようになるには時間がかかりましたが。今は仕事ではなく趣味ですが、アナログでもタブレットを使ってデジタルでも絵を描いています。絵を描くとリラックスして想像が広がります。

# Krita プラグイン:

KritaでPythonスクリプティングが可能になってから、何ができるか調べていました。KritaはQtを使っているのですが、私はそれまでQtの経験がありませんでした。普段の仕事でもPythonを使っているので、少し学んでみたいと思いました。画像処理によって異なるシステムでの利用用途に合わせて画像を変換することは常に面白いチャレンジです。仕事時間と趣味の時間でのコンテキスト切り替えを避けられるように、直接の画像スクリプティングからプラグインワークフローに切り替えたいと思いました。KritaはクロスプラットフォームでPythonが入っていないOSでインストールする必要はありませんでした。私が作ったプラグインは単純なものです。画像をスライスして[Leaflet](https://leafletjs.com/)などのタイリングライブラリで使用できるようにする、というものです。まず画像を統合して_保存_して、出力を最後に行います。またプラグインが自動でクロップしないようにしたい場合は画像が長方形であることを確認してください。プラグインの実行はメニューバーのTools（ツール） -> Scripts -> Krita - Leaflet から行います。

> [![](/images/posts/2019/plugin-selection.png)](https://krita.org/wp-content/uploads/2019/03/plugin-selection.png)![plugin-selection.png](/images/posts/2019/plugin-selection.png)

ファイルを出力するフォルダとズームレベルを選びます。ここでは低いズームレベルにしました。ズームレベルを高くすると処理に時間がかかり、リソース使用の面でも重くなります。"Leafletize"ボタンを押して処理が終わるのを待ちます。

> ![plugin.png](/images/posts/2019/plugin.png)[![](/images/posts/2019/plugin.png)](https://krita.org/wp-content/uploads/2019/03/plugin.png)

出力フォルダをチェックしてから、保存した画像を読み込みなおします。この処理は破壊的だからです。. タイルは256x256ピクセルの大きさで、Leafletが使える形でフォルダに分かれています。この結果を読み込む基本的なJavaScriptコードを書くことは簡単でしょう。テストするにはアウトプットフォルダにindex.htmlを作り、ダウンロードが必要ないようCDNライブラリを使う以下のコードを書き込みます:

<!doctype html>
<html lang="en">
  <head>
    <meta name="viewport" content="width=device-width, minimum-scale=1.0, initial-scale=1.0, user-scalable=yes">
    <title>Krita - Leaflet example</title>
    <link rel="stylesheet" href="https://unpkg.com/leaflet@1.4.0/dist/leaflet.css" integrity="sha512-puBpdR0798OZvTTbP4A8Ix/l+A4dHDD0DGqYW6RQ+9jxkRFclaxxQb/SJAWZfWAkuyeQUytO7+7N4QKrDh+drA==" crossorigin=""/>
    <script src="https://unpkg.com/leaflet@1.4.0/dist/leaflet.js" integrity="sha512-QVftwZFqvtRNi0ZyCtsznlKSWOStnDORoefr1enyq5mVL4tmKB3S/EnC3rRJcxCPavG10IcrVGSmPh6Qw5lwrg==" crossorigin=""></script>
    <style type="text/css">
        body {
            text-align: center;
        }
        #map {
            margin: auto;
            width: 800px;
            height: 600px;
        }
    </style>
  <head>
  body {
      <div id="map"></div>
      <script type="text/javascript">
          var map = L.map('map').setView(\[0.0, -0.0\], 0);
          L.tileLayer('./{z}/{x}/{y}.png', {
              maxZoom: 4,
              noWrap: true
          }).addTo(map);
      </script>
  </body>
</html>

HTMLを読み込むことも簡単です。ここではモジュールとしてPythonサーバーを実行します。同じフォルダにいる必要があります:

python -m SimpleHTTPServer

ブラウザで結果を見てみましょう。[http://localhost:8000/](http://localhost:8000/)を開きます。

> [![](/images/posts/2019/leaflet.png)](https://krita.org/wp-content/uploads/2019/03/leaflet.png)![leaflet.png](/images/posts/2019/leaflet.png)

マップ機能が必要なブラウザベースのゲームのためにカスタムマップをタイルとしてスライスするためにプラグインを作成する必要がありました。キャンバス処理のすごいライブラリを使うつもりはなく、普通のウェブ技術を使いました。そのためにこのプラグインを作りました。このプラグインは[Krita-Leafletレポジトリ](https://bitbucket.org/zmasek/krita-leaflet/)から入手できます。

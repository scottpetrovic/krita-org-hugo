---
title: "アニメーションベータ第2弾リリース"
date: "2015-12-12"
categories: 
  - "uncategorized-jp"
tags: 
  - "japanese"
---

多くのバグ修正を含むアニメーションベータ第2弾です。まだKrita3.0ベースではなく、安定板の2.9バージョンをベースにしたベータになります。ただ、数多くのクラッシュ問題の修正、バグ修正と機能改善を含んでいて、以下の操作がアニメーションでも機能するようになりました。:

- 下のレイヤーの統合
- 複数レイヤーの統合
- レイヤーの統合
- 画像の統合
- 画像/レイヤーのカラースペースを変換
- 画像/レイヤーを切り抜き
- 画像/レイヤーを拡大縮小Scale Image/Layer
- 画像/レイヤーを回転
- 画像/レイヤーを剪断変形

Nathan Lovatoさんが素敵な入門ビデオを製作しています:

<iframe src="https://www.youtube.com/embed/9uvju6sUNJA?feature=oembed" width="500" height="281" frameborder="0" allowfullscreen="allowfullscreen"></iframe>

(Nathanさんの[kickstarter](https://www.kickstarter.com/projects/gdquest/game-art-quest-make-professional-2d-art-with-krita)もお忘れなく! 最初のストレッチゴールまであと少しです)

Ubuntu LinuxではKrita Limeリポジトリからこのベータの入手が可能です。以下のように「krita-animation-testing」パッケージを選択してください:

sudo add-apt-repository ppa:dimula73/krita
sudo apt-get update
sudo apt-get install krita-animation-testing 

#### Windows版パッケージ：

32ビット版、64ビット版の2つのパッケージが使用可能です。

- [64ビットWindows版ZIPファイル](http://files.kde.org/krita/windows/krita_2.9.10.1ae_beta_x64.zip)
- [32ビットWindows版ZIPファイル](http://files.kde.org/krita/windows/krita_2.9.10.1ae_beta_x86.zip)

ZIPファイルをダウンロードして、例えばデスクトップに解凍するだけで動作します。Visual Studio 2012 Runtime DLLが足りないという警告が出る場合は、足りないdllを[ここ](https://www.microsoft.com/en-us/download/details.aspx?id=30679)からダウンロードしてください。このパッケージを試すにあたり、パッケージを入れる前に導入したKritaをアンインストールする必要はありませんよ！

注意：

※UIを日本語にしているとレイヤー及びタイムライン（Timeline） ドッキングパネルでアルファを相続（Inherit Alpha）及びアルファをロック（Alpha Locked）が操作できなくなる現象をベータ第1弾から引き続き確認しています。その場合、アプリケーションの言語を一時的にアメリカ英語に切り替えると操作できるようになります。（再起動の必要はなく、一時的に切り替えるだけで大丈夫です）

#### ユーザーマニュアル及びチュートリアル

- [アニメーション機能ユーザーマニュアル](https://userbase.kde.org/Krita/Manual/Animation)（※英語）暫定日本語版は[こちら](https://jp.krita.org/animation_tmp_jp/)
- [高速表示モードユーザーマニュアル](https://userbase.kde.org/Krita/Manual/BrushEngines/LODstrokes)（※英語）暫定日本語版は[こちら](https://jp.krita.org/instantpreview_tmp_jp/)

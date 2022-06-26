---
title: "新しい3.0開発ビルド！(ちょっとした新機能も含まれています)"
date: "2016-05-13"
categories: 
  - "uncategorized-jp"
tags: 
  - "japanese"
---

[kickstarterキャンペーン](http://www.krita.org/2016kickstarter)も4日目になり、あと2000ユーロで50%を達成できます！もちろん、これはKickstarterなので、100%にならないと成果はゼロです。まだまだ我々は頑張らないといけません！

さて、最近、Dmitryが[Geektimesで記事を公開](https://geektimes.ru/post/275530/#comment_9247098)したのですが、その記事へのコメントにブラシ角度を固定するオプションについての提案があり、ちょうどKritaチャットチャンネルにKritaアーティストのWolthera、 David Revoy、Raghukamathが揃っていて、モックアップを見た全員がその機能が是非欲しいと感嘆しました！

この実装は新しい文字列追加なしに行えるものだったので、Dmitryは半日バグ修正を休んでこの機能実装を行いました。そしてDavid Revoy本人がセザンヌにインスパイアされたデモ動画を撮影しました:

<iframe src="https://www.youtube.com/embed/bbL7qeVAaC8?feature=oembed" width="500" height="281" frameborder="0" allowfullscreen="allowfullscreen"></iframe>

それから、さらに、Windowsでのアプリケーションアイコン、Windowsの翻訳での問題、カラーピッカーの問題を修正して、[Spriter scmlエクスポート](https://brashmonkey.com/)プラグインを完成させ、ポップアップやダイアログが間違ったモニタに表示されるQtのバグを回避する修正を加え、PNG画像に作者とタイトル情報が保存されるように確認し、インスタントプレビューモード使用時の画面表示問題を解決し、フェード、距離、時間ブラシエンジンセンサー入力の方向を修正し、ブラシエンジンでのランダムオフセットパラメータの読み込みを修正し、カスタムショートカットの処理を改善して、クラッシュもいくつか修正しました。また、[Ubuntu 16.04でのKrita Limeリポジトリビルド](https://launchpad.net/~dimula73/+archive/ubuntu/krita)の問題を修正したので、Ubuntuが提供する古い2.9.7を新しい2.9.11に置き換えられるようになりました。

Krita 3.0は日々より安定してきています。新しいベータは来週に公開する予定ですが、 かなり良い感じのビルドになってきたのでこの開発中のビルドのダウンロードリンクを[ダウンロードページ](http://krita.org/download)にも追加しました！(訳注：現時点で英語サイトのダウンロードページのみ開発版のリンクが追加されています。)最新ビルドへの直接リンクもこちらに用意しました:

Alvin WongによるWindowsシェルエクステンションパッケージです。インストールすると、WindowsのエクスプローラでKritaファイルのプレビュー表示とメタ情報の表示が可能になります。(ウイルスチェッカーで警告が出るかもしれませんが無視してください。このパッケージはNSISインストーラメーカーで作成されていて、それをウイルス感染と勘違いするウイルスチェッカーソフトがあります。).

- インストールパッケージ: [kritashellex_1.1.0.1_setup.exe](http://files.kde.org/krita/3/windows/kritashellex_1.1.0.1_setup.exe)

**Windows:** ZIPファイルを解凍してbinフォルダの中にあるkrita.exeを実行してください！

- Zip版: [krita-3.0-Beta-master-d330a4a-x64.zip (64 bits)](http://files.kde.org/krita/3/windows/devbuilds/krita-3.0-Beta-master-d330a4a-x64.zip)
- Zip版: [krita-3.0-Beta-master-d330a4a-x86.zip (32 bits)](http://files.kde.org/krita/3/windows/devbuilds/krita-3.0-Beta-master-d330a4a-x86.zip)

**OSXディスクイメージ版**にはまだOpenGLを有効にするとブラシ輪郭を表示するカーソル、基準線その他が見えなくなる既存の問題が残っています。現在我々はその問題を解決すべく作業中ですが、3.0リリースまでにキャンバスのコードの書き換えは間に合わないと思われます。

- ディスクイメージ版: [http://files.kde.org/krita/3/osx/devbuilds/krita3-beta1-ad04a1c.dmg](http://files.kde.org/krita/3/osx/devbuilds/krita3-beta1-ad04a1c.dmg)

**The Linux appimage****版:**ダウンロードした後、実行可能にして起動してください。インストールは必要ありません。CentOS 6とUbuntu 12.04には、OpenMPなしでビルドされたG’Mic(これにより動作はかなり遅くなります)が入ったAppImage版を別に配布します。

- AppImage版 [krita-3.0-Beta-master-562442e-x86_64.appimage](http://files.kde.org/krita/3/linux/devbuilds/krita-3.0-Beta-master-562442e-x86_64.appimage) (新しいディストリビューション向け)
- AppImage版 [krita-3.0-Beta-master-562442e-no-openmp-x86_64.appimage](http://files.kde.org/krita/3/linux/devbuilds/krita-3.0-Beta-master-562442e-no-openmp-x86_64.appimage) (古いディストリビューション向け)

(2.9インストールに影響せずにこれらのビルドは使用可能です)

最後に、[キュートなKikiです!](https://twitter.com/ramskullsart/status/730023741711777792/photo/1)

[![kiki](/images/posts/2016/kiki-782x1024.jpg)](/images/posts/2016/kiki.jpg)

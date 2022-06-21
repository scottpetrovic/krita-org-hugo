---
title: "Krita 3.0 リリース候補版1の公開"
date: "2016-05-19"
categories: 
  - "uncategorized-jp"
tags: 
  - "japanese"
---

Krita3.0のリリースがさらに近づいています。アニメーションツール、インスタントプレビューを含むQt5ベースの初めてのバージョンになります! 今日のリリース候補版には、これまでのベータに比べて数多くの修正と改善が含まれています。アニメーションとインスタントプレビューは去年の [Kickstarterプロジェクトの成功](https://www.kickstarter.com/projects/krita/krita-free-paint-app-lets-make-it-faster-than-phot)による資金で可能になりました。 そして今、[3度目となるKickstarterキャンペーンを実施しています。今年のメイントピックは素晴らしいテキストツールとベクターツールキットです。](https://www.kickstarter.com/projects/krita/krita-2016-lets-make-text-and-vector-art-awesome) 1週間で、既に半分まで来ています!

[![support-krita-2016-3](images/support-krita-2016-3-1024x132.png)](https://www.kickstarter.com/projects/krita/krita-2016-lets-make-text-and-vector-art-awesome)

一番大きい新機能は、疑う余地もなく、手書きアニメーションのサポートでしょう。この夏にはJouni Pentikäinenがさらにアニメーションツールの改善の作業を続けますが、現状でもしっかりとしたツールセットになっています。下の動画チュートリアルでは、WoltheraがKickstarterストレッチゴールのアニメーションヘッダー(炎テキストアニメーション)を作った手順について説明をしています:

<iframe src="https://www.youtube.com/embed/NnxbhYSLAsE?feature=oembed" width="500" height="281" frameborder="0" allowfullscreen="allowfullscreen"></iframe>

また、次の動画ではWoltheraがインスタントプレビュー機能のデモをしています。大きいキャンバスで大きいブラシを使用することを可能にします。メモリ消費は大きくなりますが、その代わりに速度が大幅に向上します:

<iframe src="https://www.youtube.com/embed/lEXnpwIL45Y?feature=oembed" width="500" height="281" frameborder="0" allowfullscreen="allowfullscreen"></iframe>

インスタントプレビュー、アニメーション、Qt5サポート以外にも、Krita3.0ではKickstarterストレッチゴールから数個の機能を実装しています。レイヤー操作、ショートカットの扱い、接線法線ブラシ、カラースペースセレクタ、ガイド、グリッドとガイドのドッキングパネルやスナップ、ショートカットパレットの改善、グラデーションマップフィルタ、などなど様々です。そして、最終リリース前にさらに修正を行うつもりです。

完全版のリリースアナウンスを準備している状態ですが、[Nathan Lovato](http://gdquest.com/)による新機能まとめをチェックしてみてください:

<iframe src="https://www.youtube.com/embed/k51OK2PlTz4?feature=oembed" width="500" height="281" frameborder="0" allowfullscreen="allowfullscreen"></iframe>

### リリース候補版修正内容

前回のベータから、以下の修正が行われました:

- カーソルがキャンバス上にない場合にもショートカットが正しく機能するように修正
- 翻訳の修正
- PDF出力ダイアログにページプレビュー表示を追加
- 詳細色選択を高速化
- ベクターグラデーションツールの改善
- フィルレイヤーの保存と読み込みの修正
- インスタントプレビューの改善
- テキストツールでフォント設定を行った時のクラッシュの修正
- 対称軸ハンドルの扱いを修正
- WindowsとLinusでG'MicにOpenMPを使用、大部分のフィルタの高速化
- ファイルダイアログの修正
- Spriter出力プラグインのリライト
- 様々なクラッシュの修正
- ツールボックスアイコンのスケーリングの修正
- パンツールとズームツールに新しいアイコンを追加
- 環境変数KRITA\_HIDPIをONに設定することで、高DPIモードをオンにできるように改善
- ブラシエディタのフェード、距離、タイムセンサの修正
- カラーパレットを開く際の問題を修正
- オニオンスキンのオンオフのショートカットを追加
- オニオンスキンボタン状態の読み込みを修正
- ブラシ描画角度のロック機能を追加
- マルチモニタ環境でのポップアップとダイアログの位置処理を修正

その他細かい修正も行われています!

### ダウンロード

Alvin Wongによる**Windowsシェルエクステンションパッケージ**です。インストールすると、WindowsのエクスプローラでKritaファイルのプレビュー表示とメタ情報の表示が可能になります。(ウイルスチェッカーで警告が出るかもしれませんが無視してください。このパッケージはNSISインストーラメーカーで作成されていて、それをウイルス感染と勘違いするウイルスチェッカーソフトがあります。).

- インストールパッケージ: [kritashellex\_1.1.0.1\_setup.exe](http://files.kde.org/krita/3/windows/kritashellex_1.1.0.1_setup.exe)

**Windows:** ZIPファイルを解凍してbinフォルダの中にあるkrita.exeを実行してください！既存のインストールには影響しません。設定ファイルの場所は%APPDATA%\\Local\\kritarc から %APPDATA%\\Local\\krita\\kritarcに変更されました。

- Zip版: [krita-3.0-RC-1-master-6f75b0f-x64.zip (64 bits)](http://files.kde.org/krita/3/windows/krita-3.0-RC-1-master-6f75b0f-x64.zip)
- Zip版: [krita-3.0-RC-1-master-6f75b0f-x86.zip (32 bits)](http://files.kde.org/krita/3/windows/krita-3.0-RC-1-master-6f75b0f-x86.zip)

**OSXディスクイメージ版**にはまだOpenGLを有効にするとブラシ輪郭を表示するカーソル、基準線その他が見えなくなる既存の問題が残っています。現在我々はその問題を解決すべく作業中ですが、3.0リリースまでにキャンバスのコードの書き換えは間に合わないと思われます。設定でOpenGLをオフにすれば、カーソル、グリッド、ガイドなどが表示されます。

- ディスクイメージ版: [krita3-rc1-f345497.dmg](http://files.kde.org/krita/3/osx/krita3-rc1-f345497.dmg)

**Linux appimage****版:**ダウンロードした後、実行可能にして起動してください。インストールは必要ありません。CentOS 6とUbuntu 12.04には、OpenMPなしでビルドされたG’Mic(これにより動作はかなり遅くなります)が入ったAppImage版を別に配布します。

- AppImage版 [krita-3.0-RC-1-master-6f75b0f-x86\_64.appimage](http://files.kde.org/krita/3/linux/krita-3.0-RC-1-master-6f75b0f-x86_64.appimage) (新しいディストリビューション向け)
- AppImage版 [krita-3.0-RC-1-master-6f75b0f-no-openmp-x86\_64.appimage](http://files.kde.org/krita/3/linux/krita-3.0-RC-1-master-6f75b0f-no-openmp-x86_64.appimage) (古いディストリビューション向け)

2.9インストールに影響せずにこれらのビルドは使用可能です。

**ソースコード: ソースコードはこちらから入手可能です**:

- [http://download.kde.org/unstable/krita/2.99.91/](http://download.kde.org/unstable/krita/2.99.91/)

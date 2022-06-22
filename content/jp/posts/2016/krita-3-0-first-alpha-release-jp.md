---
title: "Krita 3.0：最初のアルファ版リリース！"
date: "2016-04-10"
categories: 
  - "uncategorized-jp"
tags: 
  - "japanese"
---

Krita 3.0リリースを目指して、本日我々は最初のアルファ版をリリースします。今回のアルファ版は3.0で実装予定の全機能と、プリアルファ版では除外されていた多言語サポート（※ただし現時点ではリソースファイルがないため実質的には意味がありません）が含まれていますが、なお不安定です。我々はずっとバグを直していますが、直すべきバグはまだまだ多いです！最悪の問題は把握できたと考えており、皆さんにはぜひこのバージョンを試して下さるとうれしいです。最終リリースは5月1日になる予定です。

[![Screenshot_20160409_212626](images/Screenshot_20160409_212626-1024x576.png)](https://krita.org/wp-content/uploads/2016/04/Screenshot_20160409_212626.png)

### 何が新しくなったの？

2.9と比べての新機能の端的な概要です：

- 手描きアニメーションを作るツール
- 大きいブラシと大きいキャンバスで働く高速プレビュー
- 座標目盛と基準線、グリッド、スナップ機能
- レイヤーパネルの刷新
- GIMPブラシの読み込み及び保存
- その他にもたくさん…

またKrita 3.0はQt 5及びKDE Framework 5ライブラリを基盤にしています。

前の[開発版](https://jp.krita.org/item/3-0-pre-alpha-3-is-out/)より我々はバグの修正及びパフォーマンス向上に集中していました。

我々が行った山のような修正の他にいくつかの変更点があります。以下は前のプレアルファ版リリース後に追加された改良点です。

### 新機能

- レイヤーを複数選択して移動させることができるようになりました。
- さらにCtrl＋PgUp/PgDnでマスクを移動させられるようになりました
- G'micを1.7にアップデートしました（[G'micのリリースノート](https://discuss.pixls.us/t/release-of-gmic-1-7-0/835)）
- デザインテンプレートをアップデートしました

また印刷及び印刷プレビューオプションを削除しました。Kritaの印刷機能は今まで上手く動いたためしがなく、Qt5への移植後は全く働かなくなったためです。

インターフェース及び使い勝手の改善

- スプラッシュスクリーンはセットアップ中にどのエリアが読み込み中なのかを表示するようになりました。
- グリッドと基準線ツールオプションのUI要素をアップデート
- 切り取りやジオメトリツールオプションのようないくつかのチェックボックスをロックアイコンに入れ替え
- グローバル入力筆圧カーブにX軸Y軸の説明を追加（Settings > Configure Krita > Tablet Settings）
- ツールボックスの選択中のツールにハイライトカラーを使用するようにしました（見やすくするため）
- リソースマネージャにリソースをインポートするための専用のボタンが追加されました。これはこのエリアの安定性を改善しています。

[![Screenshot_20160409_212649](images/Screenshot_20160409_212649-1024x576.png)](https://krita.org/wp-content/uploads/2016/04/Screenshot_20160409_212649.png)

### 既存の問題

我々はバグを狂ったように修正していますが、まだなおそれなりの数の既知のバグが存在しています。アルファ版をテストしてそれらのバグが本当にもう修正されているかを確認して我々を助けてください！[バグの分類](https://jp.krita.org/item/ways-to-help-krita-bug-triaging/)も我々のコミュニティに参加する素晴らしいやり方の一つです。

### ダウンロード

Windows版は二つあります。すなわちmsiインストーラ版とポータブルZIP版です。MSIインストーラにはファイルエクスプローラでKritaファイルのサムネイルを表示できるようにするシェル拡張が含まれています。このシェル拡張はAlvin Wongさんによって書かれたものです。

- ZIP版：[Windows 64ビットアルファ版（ZIP）](http://files.kde.org/krita/3/windows/krita-2.99.89.zip)
- MSIインストーラ版：[Windows 64ビットアルファ版（msi）](http://files.kde.org/krita/3/windows/krita-2.99.89.zip)**注意**；このインストーラ版は古いバージョンのKritaを置換してしまいます！

**OSXディスクイメージ版**にはまだOpenGLを有効にするとブラシ輪郭を表示するカーソル、基準線その他が見えなくなる既存の問題が残っています。現在我々はその問題を解決すべく作業中ですが、3.0リリースまでにキャンバスのコードの書き換えは間に合わないと思われます。

- ディスクイメージ版：[OSXアルファ1](http://files.kde.org/krita/3/osx/krita3-2.99.89.dmg)

**Linux AppImage版**は2012年以降にリリースされたあらゆるLinuxディストリビューションで動くはずです。ダウンロードした後に、AppImageを実行可能にして動かしてください。インストールの必要はありません。

- AppImage版：[Linux AppImageアルファ1](http://files.kde.org/krita/3/linux/krita-2.99.89.appimage)

これが3.0最初の公式リリースですから、ソースコードもあります！

- [krita\_2.99.89](http://download.kde.org/unstable/krita/2.99.89/)
---
title: "Krita 2.9.5 リリース！"
date: "2015-06-10"
categories: 
  - "uncategorized-jp"
tags: 
  - "japanese"
---

Kickstarterキャンペーンが成功した後も、新しい機能追加とバグ修正は続きます！グループレイヤーへのパススルーモードの追加、すべてのレイヤータイプでのアルファ相続のサポート、PSDサポートの向上、ピックしたカラーのキャンバス上でのプレビューの追加などに進捗がありました。新しく、ブラシプリセット履歴ドッキングパネルも追加しました！リリースノートは以下になります。

**Krita 2.9.5は2.9.4.7に存在したクリティカルなバグの修正も含んでいます。Kritaを再起動した時にクラッシュする現象が起こっている場合は、2.9.5にアップデートをお願いします。**

### 新機能:

- チャンネルごとのフィルタに明度カーブを追加 (bug 324332)
- ブラシプリセット履歴ドッキングパネルを追加 (bug 322425)
- ファイルを開くダイアログに、すべての種類を表示するオプションを追加
- レイヤースタイル機能にグローバルライトを追加 (bug 348178)
- タグ情報のないPNG画像に対するプロファイルをユーザが選択できるように変更 (bug 345913, 348014)
- パフォーマンスロギング機能を追加
- デフォルトブラシプリセットへのタグ付けを追加(デフォルトタグの削除は現時点ではできません！)
- .kraファイルに作者プロフィール機能(デフォルト、匿名、カスタム)を追加
- レイヤードッキングパネルにレイヤースタイルのボタンと操作を追加
- フィルタの再適用をするCtrl-Fショートカットの追加 (bug 348119)
- Intelユーザへのディスプレイドライバを更新する必要について警告を追加
- PSDファイルのレイヤースタイルの読み込み、保存を実装
- レイヤースタイルでのパターンの読み込み、保存のサポートを追加
- すべての種類のレイヤーでアルファ相続をサポート
- グループレイヤーにパススルーモードスイッチを追加 (bug 347746, 185448)
- PSDファイルへのグループレイヤーの保存を実装
- WebP (Linux環境)サポートを追加
- 新しい画像に貼りつけ機能のショートカット (Ctrl-Shift-N)を追加 (bug 344750)
- 色のピック時の、キャンバス上プレビューを追加 (bug 338128)
- mypaintスタイルの円形ブラシアウトラインを追加
- カーソル形状の設定を、アウトライン部分の設定と、カーソル形状の設定に分離
- PSDグループの透明マスクの読み込み、保存を追加

### パフォーマンス向上:

- 翻訳UIを使用している場合のストローク開始遅れの除去

### バグ修正:

- ビュー回転メニューの修正。回転アクションの追加。
- グローバル選択マスクを複製しようとした場合のクラッシュの修正 (bug 348461)
- 詳細色選択ドッキングパネルに設定アイコンを追加(レンチのアイコンです)
- ポップアップのお気に入りプリセット数がリセットされる問題の修正(bug 344610)
- クリアアクションに適切な起動フラグを設定 (bug 34838)
- 複数画像、ビュー、ウィンドウの扱いのバグを数個修正(bug 348341, bug 348162)
- ドキュメント解像度の制限を修正 (bug 348339)
- .kraファイルにレイヤースタイルを持つ複数レイヤーを保存する時の問題を修正 (bug 348178)
- 16 bitチャンネルRGB画像の表示を修正 (bug 343765)
- P_Graphite_Pencil_grain.gihペン先ファイルの修正
- レイヤー削除をUndoした時のプロジェクション更新の問題を修正 (bug 345600)
- コマンドライン引数の扱いを改善
- Windows上でのオートセーブ回復ダイアログを修正
- 現在の画像からのテンプレート作成を修正 (bug 348021)
- レイヤースタイルとアルファ相続を修正 (bug 347120)
- アニメーションをオンにしたときのOxygenウィジェットスタイルのクラッシュの回避策を追加 (bug 347367)
- Photoshopで保存されたJPEG画像を読み込む時に、メタデータの解像度情報を確認するように修正 (bug 347572)
- 変形マスクを独立表示しようとした時にもクラッシュしないように修正 (変形マスクには描きこむことはできません) (bug 347622)
- PSDからの焼き込み、ColorBurn(焼き込みカラー)ブレンドモードを正しく読み込むように修正 (bug 333454)
- グループレイヤーの不透明部分を選択できるように修正(bug 347500)
- アウトライン表示をしない設定の場合も、クローンブラシのアウトラインを表示するように修正 (bug 288194)
- レイヤースタイルのグラデーション保存を修正
- ツールバーのスライダーレイアウトの改善
- 浮動小数点TIFFファイルの読み込みを修正 (bug 344334)

**ダウンロード**

- Linux:
    - 各ディストリビューションは各ディストリビューションでのbleeding edgeレポジトリからパッケージを作成することを期待されています。
    - UbuntuとUbuntu派生ディストリビューションでは通常通りKrita Limeを使用できます: [https://launchpad.net/~dimula73/+archive/ubuntu/krita](https://launchpad.net/~dimula73/+archive/ubuntu/krita).
    - OpenSUSEユーザはKDE:Extraレポジトリ: [http://download.opensuse.org/repositories/KDE:/Extra/](http://download.opensuse.org/repositories/KDE:/Extra/) もしくはVcサポート付でビルドされたKrita(ペイントが高速化)を含むLeinir’s OBS repositoriesを使用できます:
        - [http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_13.1/](http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_13.1/)
        - [http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_13.2/](http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_13.2/)
        - [http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_Factory/](http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_Factory/)
- WindowsとOSX
    - 更新された[ダウンロードページ](https://jp.krita.org/download/krita-desktop/ "Krita Desktop")から新しいビルドがダウンロードできます。

---
title: "Krita 2.9.6リリース！"
date: "2015-07-09"
categories: 
  - "uncategorized-jp"
tags: 
  - "japanese"
coverImage: "2015-06-26_screenshot_002.png"
---

一か月のバグ修正を経て、Krita 2.9.6のリリースです！多くのバグ修正も含まれていますが、それだけではありません。数個の新機能も含まれています！

1番大きな変更は、_選択モディファイア_の追加です！以下のような設定になっています:

- Shift+クリック: 選択への追加
- Alt+クリック: 選択からの除外
- Shift+alt+クリック: 交差選択(現在の選択範囲との共通部分の選択)
- Ctrl+クリック: 選択の置き換え(選択モードを他のものに変えて置き換えたい時)

これらは現時点ではパスツールでは使用できず、ショートカットを変更することもできませんが、開発して対処する予定です。選択ツールの詳細と、四角選択と楕円選択のコンストレインとの関係については[マニュアルページ(英語)](https://userbase.kde.org/Krita/Manual/Tools/RectangleSelect) を参照してください。

さらに新機能があります。変形と切り抜きツールの継続です！

このビルドから、変形や切り抜きツールを適用した直後にキャンバスをクリックすると、Kritaは直前の変形や切り抜き操作を記憶していて、継続して調整を行うことができます！この「継続モード」で「ESC」キーを押すと、継続変形の情報をKritaが忘れて、新しい変形を開始できます。

大きな新機能の最後は、ツールオプションをツールバーに入れるできるようになった、というものです。

[![tool options in the toobar](/images/posts/2015/2015-06-26_screenshot_002.png)](/images/posts/2015/2015-06-26_screenshot_002.png)

デフォルトではツールオプションはドッキングパネルのままですが、設定>Kritaを設定>全般から設定を変更することができます。このメニューを「\\」キーで呼び出すこともできます！

さらにThorsten Zachmannさんがすべての色調整フィルタを高速化しました。4倍かそれ以上になったものもあります。

2.9.6の新機能のリストはこちらです:

- 切り抜きツールアクションを継続して調整できるようにしました
- 色のバランス、脱色、覆い焼き、HSV補正、チャンネルごと色を索引にのせる、ポスタリゼーションフィルタの高速化
- Cut Sharp/Copy Sharpアクションのメニューへの追加
- キャンバスクリックでの継続した変形ツール調整を実装
- 新しいデフォルトワークスペース
- 新しいショートカットの追加 (「\\」はツールオプション、F5はブラシエディタ、F7はプリセット選択を開きます)
- ツールオプションのポップアップ表示(全般設定でオンオフ可能、設定変更後にKrita再起動が必要)
- 新しいデフォルトショートカットの追加(グループレイヤーの作成 = Ctrl+G, 選択したレイヤーの統合 = Ctrl+Alt+E, 画像を新しいサイズにスケール = Alt+Ctrl+I )
- 詳細色選択ドッキングパネルに「マウスクリックのポップアップを隠す」オプションを追加
- ブラシの「速度」センサが正しく機能するようになりました
- 「画像背景色と透明度」ダイアログにプレビュー機能を追加
- 選択モディファイアパッチがようやく入りました！(shift=追加, alt=除外, shift+alt=交差, ctrl=置換 パスツールではまだ正しく機能しません。まだ設定変更もできない状態です)

2.9.6のバグ修正内容はこちらです

- BUG:346932 パターンを\*.kraに保存するときのクラッシュの修正
- グループレイヤーがパススルーモードでも正しい範囲を返すように修正
- パススルーモードの修正
- スライダースピンボックスに最適化を追加
- BUG:348599 間違った画像にノードがアクティブになる問題の修正
- BUG:349792 パレットドッキングパネルでの色削除の修正
- BUG:349823 ファイルレイヤーを追加するときの、画像に合わせて拡大縮小の修正
- レイヤースタイルダイアログのダイヤルウィジェットの問題を修正
- .kraファイルの読み込み時のY解像度計算を修正
- BUG:349598 0除算の予防
- BUG:347800 キャンバス拡張時にカーソルをリセットして、カーソルが「指さし手」のままにならないように変更
- BUG:348730 デフォルトのツールオプションの可視性を修正
- BUG:349446 テーマ変更がユーザ設定を更新しないことがある問題を修正
- BUG:348451 LJFスモークの内部ブラシ名を修正
- BUG:349424 クリップボードから作成されたドキュメントを変更済みとマーク
- BUG:349451 より頑健に。使用する前にポインタをチェック
- kraとoraの保存時に独自コードで統合画像を保存するように変更(速度が上がりました)
- BUG:313296 Soak Inkモードの時に、絵筆(Hairy)ブラシが透明ピクセル上に黒を塗れなかった問題の修正
- 絵筆ブラシのPVS警告の修正
- (gmic) カーソルがビジー状態になる問題への回避策テスト
- BUG:348750 ドッキングエリア制限を解除
- BUG:348795 m_maxPresetsが初期化されていない問題を修正
- BUG:349346 (gmic) 選択がある場合に、画像サイズとの同期を行わない
- BUG:348887 塗りつぶしツールでの自動スクロールを禁止
- BUG:348914 フィルレイヤーの名前変更ができない問題の修正

**ダウンロード**

- Linux:
    
    - 各ディストリビューションは各ディストリビューションのbleeding edgeレポジトリ向けにパッケージを作成することを期待されています。
    - UbuntuとUbuntu派生ディストリビューションでは通常通りKrita Limeを使用できます:[https://launchpad.net/~dimula73/+archive/ubuntu/krita](https://launchpad.net/~dimula73/+archive/ubuntu/krita).
    
    - OpenSUSEユーザはKDE:Extraレポジトリ:[http://download.opensuse.org/repositories/KDE:/Extra/](http://download.opensuse.org/repositories/KDE:/Extra/) もしくはVcサポート付でビルドされたKrita(ペイントが高速化)を含むLeinir’s OBS repositoriesを使用できます:
        - [http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_13.1/](http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_13.1/)
        - [http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_13.2/](http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_13.2/)
        - [http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_Factory/](http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_Factory/)
- WindowsとOSX
    - 更新された[ダウンロードページ](https://jp.krita.org/download/krita-desktop/ "Krita Desktop")から新しいビルドがダウンロードできます。MSIインストーラを使いたくない場合は、[files.kde.org](http://files.kde.org/krita) からWindows向けKritaのポータブルなzip版をダウンロードできます。
    - [Steam版Krita](http://store.steampowered.com/app/280680)では「Desktop29」オプションをプロパティのベータとして選ぶことで最新バージョンを入手できます！Steamユーザは自動的に更新を入手することができます。

---
title: "Krita 2.9.11・3.0アルファ第2版リリース！"
date: "2016-02-04"
categories: 
  - "uncategorized-jp"
tags: 
  - "japanese"
---

本日、Krita 2.9の11回目のバグ修正版及びKrita 3.0の2回目の開発版をリリースします！2.9についてはこれが最後のバグ修正版リリースとなる予定ですが、Windows 10上で発生するどうやら回避可能な問題があるためもう一つリリースを行えるだけのバグが集まる可能性もあります。ですのでKritaをWindows 10で使用している場合は注意深く確認をお願いします。

- **ウィンドウが真っ黒になった**：設定＞Kritaを設定＞表示でOpenGLを無効にしてください。これはKritaが必要な全機能を実装していない新しいIntelのGPUドライバが最近のWindows updateでインストールされたことにより発生したものです。
- **筆圧が働かない**：Windows 10において最近のWindows updateによって筆圧感知が壊れる場合があります。タブレットドライバの再インストールこの問題を修正されるかを確認してください。されない場合はKritaを閉じ、ユーザーフォルダ以下のAppData\\Roamingフォルダに行き、kritaフォルダの名前をkrita\_oldに変えてください。もしそれでKritaの筆圧が戻った場合はそのkrita\_oldフォルダをZIP圧縮してfoundation@krita.orgにメール添付で送ってください。

そして以下が2.9.11での修正です！

2.9.11変更ログ

- 画像がクリップボードにコピーされている時に起こるメモリリークを修正
- ドキュメントを保存する前に長時間の演算についてそのまま待つか演算をやめるかを選択できるようにしました
- G’Micを1.6.9-preに更新
- レイヤースタイルのレンダリングを修正
- 複製レイヤーを持つファイルを読み込んだ際発生する可能性のある問題を修正
- もし負の数を持つモニターがあってもクラッシュしないよう修正
- 切り取りツールが常に正しい画像サイズを使用するように修正
- 長時間の演算を行っている途中に画像を閉じた時にクラッシュする問題を修正
- 正しいJPEGライブラリにリンクするように修正
- アプリケーションのアイコンを修正
- 色をV使用後にXに切り替えると一時的に直線ツールが有効になる問題を修正
- light theme使用時にスプラッシュ画面の「閉じる」ボタンが見えづらくなっている問題を修正
- Pencil 2Bブラシプリセットを修正
- 16f grayscale colorspaceが正しいチャンネル位置を使用するように修正
- 現在のレイヤーを上に/下に移動へのショートカットを追加

3.0プリアルファ版更新内容

3.0では、数多くの新機能追加とバグ修正を行っています。

まだ1つ、熱心に作業を続けている大きな問題があります。OSXと最新のIntelGPUドライバがKritaのOpenGLサポートを壊しているという問題です。OSXでは、まだブラシアウトライン、対称軸、アシスタントといったものが表示されません。Windowsでは、Intelのグラフィックカードを使っているとKritaのウィンドウが完全に黒画面になることがあります。これらの問題については報告の必要はありません。

- キャンバス上でShift+R+クリックをすると、複数のレイヤーを選択することができるようになりました!このキーと、複数プロパティ編集を組み合わせて、簡単に複数のレイヤー名を一度に変更したり、Ctrl+Gでグループ化したりできます! [![krita_shiftr_layerselect](/images/posts/2016/krita_shiftr_layerselect.gif)](https://krita.org/wp-content/uploads/2016/02/krita_shiftr_layerselect.gif)
- ポップアップパレットの改良。プリセットのアイコンが見やすくなりました(アイコンサイズは設定したプリセット表示数によって決まります。) [![krita-new-popuppalette](/images/posts/2016/krita-new-popuppalette.png)](https://krita.org/wp-content/uploads/2016/02/krita-new-popuppalette.png)
- カラースペースブラウザの数多くの改良:トーンカーブが表示されるようになり、リニア空間を見つけやすくなりました。CMYKのようなカラールックアップテーブルプロファイルのフィードバック、情報ボックスへのコピーライト表示、変換の説明が追加され、一部の情報はツールチップに移動されてすっきりとした見た目になりました。PNG16bitインポートもアルファベット順になっています。 [![krita-new-gamuts](/images/posts/2016/krita-new-gamuts.png)](https://krita.org/wp-content/uploads/2016/02/krita-new-gamuts.png)
- 色相、彩度のためのホットキーの追加。色への赤み、黄み、青み、緑の追加、輝度を使った明るい色、暗い色への変更が行えます。この新しいホットキーはデフォルトではキーが割り当てられていないため、使用するにはショートカットエディタで自分でキーを割り当てる必要があります: [![LK_hotkey](/images/posts/2016/LK_hotkey.gif)](https://krita.org/wp-content/uploads/2016/02/LK_hotkey.gif)[![hue_hotkeys](/images/posts/2016/hue_hotkeys.gif)](https://krita.org/wp-content/uploads/2016/02/hue_hotkeys.gif)[![sat_hotkeys](/images/posts/2016/sat_hotkeys.gif)](https://krita.org/wp-content/uploads/2016/02/sat_hotkeys.gif)[![rygb_hotkeys](/images/posts/2016/rygb_hotkeys.gif)](https://krita.org/wp-content/uploads/2016/02/rygb_hotkeys.gif)
- HSV/HSL調整フィルタへのHSI、HSY、YCrCbオプションの追加。HSYとYCrCbは大部分のRGB空間で正しい係数を使用していますが、まだリニア化されておらず、正しい輝度にはなっていません。現在の結果比較は以下になります : [![krita-hsvhslhsihsyycrcb](/images/posts/2016/krita-hsvhslhsihsyycrcb.png)](https://krita.org/wp-content/uploads/2016/02/krita-hsvhslhsihsyycrcb.png)
- 色ぼかしブラシの艶消しモードに1ピクセル以下の精度が追加: [![krita-smudge-brush-pixel-precision](/images/posts/2016/krita-smudge-brush-pixel-precision.png)](https://krita.org/wp-content/uploads/2016/02/krita-smudge-brush-pixel-precision.png)
- Kritaが.KRAファイルを保存するときの進行レポートを追加
- Krita 3.0のホイールイベントを修正
- リソースとタグ読み込み順番のサニタイズの追加。これはスタートアップを低速化するため、理想としてリソース、タグシステム全体をより洗練されたもので置き換えたいのですが、3.0では実現しない見込みです。
- ステータスバーのメモリ使用量ポップアップの桁数の追加
- 奇妙なデータを含んだPSDファイルを読み込んだ時のアサートに対して回避策を追加
- BUG: 346430: クロップツールが現在の画像サイズを常に参照するように修正
- BUG:357173 KisSelectionMaskのコピーコンストラクタの修正
- BUG:357987 特定ファイル読み込み時のクラッシュを修正
- XDG\_DATA\_PATHが設定されていない時のKritaの起動を修正

**ソースコード**

ソースコードのZIPファイルより[git](https://phabricator.kde.org/diffusion/KRITA/)からKritaをビルドするのを推奨します。OSX版Kritaは別のブランチからのビルドです。

- [krita3prealpha-3c69a59.zip](http://files.kde.org/krita/3/source/krita3prealpha-3c69a59.zip)

**Windows**

- [krita3prealpha-fa2b0d7.zip](http://files.kde.org/krita/3/windows/krita3-prealpha2-fa2b0d7.zip)

ZIPファイルをダウンロードし、[そのZIPファイルをKritaを置いておきたいところへ解凍してください](http://windows.microsoft.com/en-us/windows-10/zip-and-unzip-files#v1h=tab02)。

まずMicrosoft’s Visual Studio runtimeをインストールするためにこのZIPファイルに入っているvcredist\_x64.exeを動かしてください。

そうしたらこれもこのZIPファイルに入っているショートカットKritaをダブルクリックしてください。

Windows上での既存の問題：

- ウィンドウ全体が真っ黒になったらOpenGLを無効にしてください。我々は既にこのトラブルの原因を把握しており、あとはコードを修正するだけです。これはIntelのグラフィックドライバのバグなのですが、我々はこのバグをどう回避すればいいかを既に探し出しています。

**OSX**

- [krita3-prealpha2-ac4e441.dmg](http://files.kde.org/krita/3/osx/krita3-prealpha2-ac4e441.dmg)

DMGファイルをダウンロードして開いてください。そうしたらkrita app bundleをアプリケーションフォルダ（Applications folder）かそれともどこか自分がいいと思った場所にドラッグしてください。そうしたらダブルクリックしてKritaを起動してください。

OSXでの注意すべき事項：

- 我々はKritaをEl Capitanでビルドしました。このバンドルはMavericksで動くMac mini (Mid 2011)でテストされています。このビルドを動かすにはEl Captitanを動かせるだけのハードウェアが必要と思われるかもしれませんが、別にEl Captitanを使用する必要はありません。それ以前のバージョンのOSXでも動かしてみることが可能です。
- ブラシ輪郭カーソルや、例えばグラデーションツールなどのその他のキャンバス上に描画するツールが表示されないかもしれません。我々はこの問題をすでに把握しており、いくつかのIntelのグラフィックドライバでウィンドウが真っ黒になる問題と同じ修正が必要です。

**Linux**

- [krita3-prealpha2-3c69a59-x86\_64.appimage](http://files.kde.org/krita/3/linux/krita3-prealpha2-3c69a59-x86_64.appimage)

Linuxのビルドには今回からAppimagesを使用することとしました！Appimagesは完全に独立したディストリビューションです。AppImageを使用するにはこれをダウンロードして、ターミナルかファイルマネージャのファイルプロパティダイアログを使ってこれを実行可能にしてください。もう一つの変更点として設定とリソースが今回からは.kdeや.kde4ではなくユーザーホームフォルダ（user home folder）内の.config/krita.org/kritarcと.local/share/krita.org/に保存されるようになりました。

Linuxでの既知の事項：

- このビルドを動かすには使用しているディストリビューションでFuseが有効である必要があります。
- いくつかのディストリビューション、インスタレーションではFuseシステムがロックされているためAppImageがルートとしてしか動かせない場合があります。ですがAppImageはシンプルなisoですのでループバックデバイスとしてマウントしてトップフォルダで実行可能なAppRunを使用してKritaを直接実行することも可能です。

---
title: "Krita 4.0.1がリリースされました"
date: "2018-04-14"
categories: 
  - "news-jp"
  - "officialrelease-jp"
---

KritaチームはKrita4.0.0のバグ修正リリースであるKrita 4.0.1をリリースしました。Krita 4.0.0リリースから50以上のバグを修正しました!修正された問題のリストは以下です。appimageとmacOSビルドで翻訳が再び利用できるようになりました。注意してください:

- 参照画像ドッキングパネルは削除されました。Krita 4.1.0に新しい参照画像ツールが追加されます。作成中のツールはWindowsとLinuxのナイトリービルドでテスト可能です。
- macOSではスクリプト機能は使用できません。ほぼ機能するところまでもっていたところでmacbookが更新で壊れて、すべての作業がなくなってしまいました。G'MicもmacOSでは使用できません。
- ドッキングパネルのロックと折り畳みアイコンは削除されました。多くの人が混乱していたからです。

新しい問題を見つけたときは、報告をする前に、この[バグ報告についてのドラフト](https://phabricator.kde.org/T7492)をまず参照してください。4.0リリースの後、150以上のバグ報告がありましたが、そのほとんどは重複であったり、助けを求めるものや、まったく役に立たないものだったりしました。こうしたものは開発者への大きな負担になります。そして実際にKritaの改善に使う時間を減らしてしまいます。協力をおねがいします!

[![](/images/posts/2018/kiki_4.0_sm-1-1024x463.png)](/images/posts/2018/kiki_4.0_sm-1-1024x463.png)

## 改善点

### Windows

- QSaveFileにパッチを当てて、ネットワーク同期されたフォルダ(dropboxやgoogle drive)での作業を安全になるようにしました

### ショートカット

- Photoshopユーザ向けショートカットの重複を修正しました
- ショートカットをアルファベット順にして、変更時のdiffを読みやすくしました

### UI

- カテゴリーリストビューの三角を大きくしてわかりやすくしました
- マクロ記録と再生のプラグインを無効にしました
- ドッキングパネルのタイトルバー上のロックと折り畳みボタンを削除しました[BUG:385238](https://bugs.kde.org/show_bug.cgi?id=385238) [BUG:392235](https://bugs.kde.org/show_bug.cgi?id=392235)
- ピクセルグリッドが表示されるようになるズーム閾値の初期値を2400%に変更しました[BUG:392161](https://bugs.kde.org/show_bug.cgi?id=392161)
- パレットドッキングパネルのレイアウトを改善
- パレットビューでのドラッグアンドドロップを無効にしました。スウォッチの移動では実際にはパレットは変更されていませんでした[BUG:392349](https://bugs.kde.org/show_bug.cgi?id=392349)
- appimage使用時の新規ドキュメントダイアログでの最後に使ったテンプレート選択を修正しました[BUG:391973](https://bugs.kde.org/show_bug.cgi?id=391973)
- 画像の最上部で補助線を使ったときのキャンバスフリーズを修正しました[BUG:391098](https://bugs.kde.org/show_bug.cgi?id=391098)
- レイヤー表示状態を変更した時にやり直し履歴をリセットしないようにしました[BUG:390581](https://bugs.kde.org/show_bug.cgi?id=390581)
- ポップアップパレットの回転サークルを使った後に、パン位置のずれを修正[BUG:391921](https://bugs.kde.org/show_bug.cgi?id=391921)
- ラップアラウンドモードでのハイトマップから法線マップへの変換を修正[BUG:392191](https://bugs.kde.org/show_bug.cgi?id=392191)

### テキスト

- SVGテキストツールでフォントサイズを編集できるようにしました[BUG:392714](https://bugs.kde.org/show_bug.cgi?id=392714)
- テキストシェイプが空の行を持てるようにしました[BUG:392471](https://bugs.kde.org/show_bug.cgi?id=392471)
- やり直し取り消しアクションの更新を修正[BUG:392257](https://bugs.kde.org/show_bug.cgi?id=392257)
- テキストをパスに変換する機能を実装[BUG:391294](https://bugs.kde.org/show_bug.cgi?id=391294)
- ホバー状態/選択状態の形状を削除するときのSvgTextToolのクラッシュを修正[BUG:392128](https://bugs.kde.org/show_bug.cgi?id=392128)
- テキストエディタをウィンドウアプリケーションモーダルに変更しました[BUG:392248](https://bugs.kde.org/show_bug.cgi?id=392248)
- RTLテキストのアラインメントを修正[BUG:392065](https://bugs.kde.org/show_bug.cgi?id=392065) [BUG:392064](https://bugs.kde.org/show_bug.cgi?id=392064)
- キャンバスバウンディングボックス外のテキストのペイントを修正[BUG:392068](https://bugs.kde.org/show_bug.cgi?id=392068)
- 相対オフセットを設定したテキストのレンダリングを修正[BUG:391160](https://bugs.kde.org/show_bug.cgi?id=391160)
- 変形ツールを2回使ってテキストを変形した時のクラッシュを修正[BUG:392127](https://bugs.kde.org/show_bug.cgi?id=392127)

### アニメーション

- 保存時のキーフレームの扱いを修正[BUG:392233](https://bugs.kde.org/show_bug.cgi?id=392233) [BUG:392559](https://bugs.kde.org/show_bug.cgi?id=392559)
- タイムラインで表示設定とオニオンスキンをレイヤーをマージした時にも保持するように修正[BUG:377358](https://bugs.kde.org/show_bug.cgi?id=377358)
- レイヤーをマージした時にもキーフレーム色ラベルを保持するように修正[BUG:388913](https://bugs.kde.org/show_bug.cgi?id=388913)
- MKV、OGV動画フォーマットでのオーディオ書き出しを修正

### ファイル処理

- レイヤーチャンネルフラグを保存/読み込みしないように変更(Krita2.9でUIからチャンネルフラグは削除されていました)[BUG:392504](https://bugs.kde.org/show_bug.cgi?id=392504)
- 変形マスクをレンダリング結果として保存する形式での保存を修正[BUG:392229](https://bugs.kde.org/show_bug.cgi?id=392229)
- 読み込みが失敗した時のエラー報告を修正[BUG:392413](https://bugs.kde.org/show_bug.cgi?id=392413)
- ファイルレイヤーを読み込む際のメモリリークを修正
- クローンレイヤーの構成でループを含むKritaファイルの読み込みを修正[BUG:384587](https://bugs.kde.org/show_bug.cgi?id=394587)
- PNG画像を読み込んだ後に表示される待機カーソルを修正[BUG:392249](https://bugs.kde.org/show_bug.cgi?id=392249)
- バンドル読み込みのフィードバックをわかりやすく変更

### ベクター関連のバグ

- ベクター選択の作成時のクラッシュを修正[BUG:391292](https://bugs.kde.org/show_bug.cgi?id=391292)
- ベクターのグラデーションフィルストップの不透明度インプットボックスで右クリックした時のクラッシュを修正
- ベクター形状のアスペクト比の設定を修正[BUG:391911](https://bugs.kde.org/show_bug.cgi?id=391911)
- SVG書き出し時に不正な形状があった時のクラッシュを修正[BUG:392240](https://bugs.kde.org/show_bug.cgi?id=392240)
- 表示されないストロークとフィルウィジェットが現在の形状選択をトラッキングしない問題を修正 BUG:391990

### ペイントとブラシエンジン

- 新しいスプレープリセットを作成した時のクラッシュを修正[BUG:392869](https://bugs.kde.org/show_bug.cgi?id=392869)
- 筆圧カーブの丸めの修正
- 透過マスク上への色滲みブラシのペイントを修正[BUG:391268](https://bugs.kde.org/show_bug.cgi?id=391268)
- KisHairyPaintOpの初期化されていない距離情報を修正 [BUG:391940](https://bugs.kde.org/show_bug.cgi?id=391940)
- 中間筆圧値の丸めを修正
- ラップアラウンドモードでペイントする時の色滲みブラシを修正[BUG:392312](https://bugs.kde.org/show_bug.cgi?id=392312)

### レイヤーとマスク

- アルファ継承がオンになったグループレイヤーの統合を修正[BUG:390095](https://bugs.kde.org/show_bug.cgi?id=390095)
- ファイルレイヤーに変形マスクを使用した時のクラッシュを修正[BUG:391270](https://bugs.kde.org/show_bug.cgi?id=391270)
- 変形マスクのパフォーマンスを改善

## ダウンロード

### Windows

Windowsユーザーの皆さんへ：もしクラッシュする事案に遭遇した場合は、[この案内（英語）](https://docs.krita.org/Dr._Mingw_debugger) に従いデバッグシンボルをKritaに追加してください。これによってKritaがクラッシュした原因をログから解析できるようになります。

- 64ビットWindows版: [krita-x64-4.0.1-setup.exe](https://download.kde.org/stable/krita/4.0.1/krita-x64-4.0.1-setup.exe)
- 64ビットWindowsポータブル版: [krita-x64-4.0.1.zip](https://download.kde.org/stable/krita/4.0.1/krita-x64-4.0.1.zip)
- [32ビット版向けデバッグシンボル(Kritaをインストールしたフォルダに展開して使用)](https://download.kde.org/stable/krita/4.0.1/krita-x64-4.0.1-dbg.zip)

- 32ビットWindows版: [krita-4.0.1-x86-setup.exe](https://download.kde.org/stable/krita/4.0.1/krita-x86-4.0.1-setup.exe)
- 32ビットWindowsポータブル版: [krita-x86-4.0.1.zip](https://download.kde.org/stable/krita/4.0.1/krita-x86-4.0.1.zip)
- [32ビット版向けデバッグシンボル(Kritaをインストールしたフォルダに展開して使用)](https://download.kde.org/stable/krita/4.0.1/krita-x86-4.0.1-dbg.zip)

### Linux

- 64ビットLinux用AppImage版: [krita-4.0.1-x86\_64.appimage](https://download.kde.org/stable/krita/4.0.1/krita-4.0.1-x86_64.appimage)

(なぜかFirefoxはテキストとして読み込もうとするようです。ダウンロードするにはリンクの右クリックから保存してください) 更新がされると、Ubuntuと派生ディストリビューションでは[Krita Lime PPA](https://launchpad.net/%7Ekritalime/+archive/ubuntu/ppa)からもKrita 4.0.1をインストールできるようになります。snapの更新については作業中です。

### OSX

- OSXディスクイメージ版: [krita-4.0.1.dmg](https://download.kde.org/stable/krita/4.0.1/krita-4.0.1.dmg)

注意: gmic-qtとPythonプラグインはOSXで利用できません。

### ソースコード

- ソースコード: [krita-4.0.1.tar.gz](https://download.kde.org/stable/krita/4.0.1/krita-4.0.1.tar.gz)

### md5sum

すべてのダウンロード向け:

- [md5sum.txt](https://download.kde.org/stable/krita/4.0.1/md5sum.txt)

### キー

Linux appimageとソースのtarボールは署名されています。パブリックキーをhttps経由で取得できます: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8) 署名は [こちら](http://download.kde.org/stable/krita/4.0.1/)です (.sigのファイルです)

## Kritaを支援してください

Kritaは自由なオープンソースのプロジェクトです。[寄付](https://krita.org/jp/support-us-jp/donations-jp/)や[トレーニングビデオやアートブックの購入](https://krita.org/jp/support-us-jp/shop-jp/)で、プロジェクトを支援することを検討してみてください！皆様の支援によって、コアチームがフルタイムでKritaの開発作業を続けることが可能になります。

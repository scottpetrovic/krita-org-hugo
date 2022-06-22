---
title: "Krita 4.0.2リリース！"
date: "2018-05-13"
categories: 
  - "news-jp"
  - "officialrelease-jp"
---

KritaチームはKrita4.0.0のバグ修正リリースであるKrita 4.0.2をリリースしました。Krita 4.0.0リリースから50以上のバグを修正しました!修正された問題のリストは以下です。また二人の新しい貢献者による修正も含んでいます: Emmet O'NeilさんとSeoras Macdonaldさんです。ようこそ!

注意してください:

- 参照画像ドッキングパネルは削除されました。Krita 4.1.0に新しい参照画像ツールが追加されます。作成中のツールはWindowsとLinuxのナイトリービルドでテスト可能です。Antoine Rouxさんの[reference images docker](https://github.com/antoine-roux/krita-plugin-reference)Pythonプラグインも利用可能です。
- 翻訳がいろいろな意味で壊れています。Linuxでは正しく動いているはずです。Windowsでは、設定の「アプリケーションの言語を切り替え」で予備言語にも設定したい言語を指定する必要があるかもしれません。macOSでも起きているかもしれません。
- macOSバイナリには署名が追加されましたが、G'MicとPythonスクリプト機能はありません。

新しい問題を見つけたときは、報告をする前に、この[バグ報告についてのドラフト](https://phabricator.kde.org/T7492)をまず参照してください。4.0リリースの後、150以上のバグ報告がありましたが、そのほとんどは重複であったり、助けを求めるものや、まったく役に立たないものだったりしました。こうしたものは開発者への大きな負担になります。そして実際にKritaの改善に使う時間を減らしてしまいます。協力をおねがいします!

[![](/images/posts/2018/kiki_4.0_sm-1-1024x463.png)](https://krita.org/wp-content/uploads/2018/03/kiki_4.0_sm-1.png)

## 改善点

### Windows

- QSaveFileにパッチを当てて、ネットワーク同期されたフォルダ(dropboxやgoogle drive)での作業を安全になるようにしました[BUG:392408](https://bugs.kde.org/show_bug.cgi?id=392408)
- WinTabが読み込めない時にWinInkを有効にするか聞くプロンプトを出すようにしました

### アニメーション

- アニメーションがキャッシュにレンダリングされているときのキャンバス更新問題を修正しました。[BUG:392969](https://bugs.kde.org/show_bug.cgi?id=392069)
- 指定レイヤーのみを表示モードでの再生を修正しました[BUG:392559](https://bugs.kde.org/show_bug.cgi?id=392559)
- アニメーションした透明マスク、フィルタマスク、調整レイヤの保存を修正しました [BUG:393302](https://bugs.kde.org/show_bug.cgi?id=393302)
- set size for a few timeline icons as it is painfully small on Windows
- アニメーションを持つレイヤーからのピクセルデータのコピーペーストを修正しました [BUG:364162](https://bugs.kde.org/show_bug.cgi?id=364162)

### ブラシ

- ブラシ保存時に消しゴム切り替えサイズ・透明度オプションを保持するように修正[BUG:393499](https://bugs.kde.org/show_bug.cgi?id=393499)
- デフォルトプリセットを作成したときのプリセットエディタGUIの更新を修正[BUG:392869](https://bugs.kde.org/show_bug.cgi?id=392869)
- ブラシエディタの強度、不透明度スライダを0から100パーセントになるように変更

### ファイル形式サポート

- 選択マスクの状態の.kraへの保存を修正
- Nukeによって保存されたマルチレイヤーEXRファイルの読み込み [BUG:393771](https://bugs.kde.org/show_bug.cgi?id=393771)
- PSD: カラー空間がサポートされていない場合は画像を変換
- オートセーブが実行中のアクションをキャンセルしないように修正

### グリッド

- ピクセルグリッド閾値の範囲を増加
- OpenGLが有効な場合のみ等角投影グリッドが使用できるように変更 [BUG:392526](https://bugs.kde.org/show_bug.cgi?id=392526)

### クラッシュ

- 画像保存時のハングアップを修正 [BUG:393916](https://bugs.kde.org/show_bug.cgi?id=393916)
- アクティブなグローバル選択マスクを複製した時のクラッシュを修正 [BUG:382315](https://bugs.kde.org/show_bug.cgi?id=382315)
- ベクターパスポイント操作のUndo/Redoのクラッシュを修正 [BUG:393209](https://bugs.kde.org/show_bug.cgi?id=393209), [BUG:393087](https://bugs.kde.org/show_bug.cgi?id=393087)
- パレット削除時のクラッシュを修正e [BUG:393353](https://bugs.kde.org/show_bug.cgi?id=393353)
- シェイプ選択ツールのツールオプションのサイズを変更した時のクラッシュを修正 [BUG:393217](https://bugs.kde.org/show_bug.cgi?id=393217)

### ユーザインタフェース

- レイヤプロパティダイアログで実際のレイヤーのバウンドを表示
- 円状ラインを表示するオプションを消失点補助線ツールに追加
- 値が100の色をピックした時に彩度スライダーを更新するように修正 [BUG:391934](https://bugs.kde.org/show_bug.cgi?id=391934)
- 閉じたパスで"セグメントの分割が正しく機能するように修正
- ポップアップパレット上での右クリックを無効化 [BUG:391696](https://bugs.kde.org/show_bug.cgi?id=391696), [BUG:378484](https://bugs.kde.org/show_bug.cgi?id=378484)
- 右ボタンが押されてもカラーラベルウィジェットのラベルが変にならないように修正[BUG:392815](https://bugs.kde.org/show_bug.cgi?id=392815)
- ポップアップパレット回転リセット時のキャンバス位置がおかしくなる問題を修正[BUG:391921](https://bugs.kde.org/show_bug.cgi?id=391921) ( Emmet O'Neilさんによるパッチです、ありがとうございます！)
- レイヤー追加ボタンの挙動の変更 [BUG:385050](https://bugs.kde.org/show_bug.cgi?id=385050) (Seoras Macdonaldさんによるパッチです、ありがとうございます！)
- プレビューボックス外をクリックするとビューがその場所まで移動 [BUG:384687](https://bugs.kde.org/show_bug.cgi?id=384687) (Seoras Macdonaldさんによるパッチです、ありがとうございます！)
- 連続移動モードをキャンセルするダブルESCキー押しのショートカットの実装[BUG:361852](https://bugs.kde.org/show_bug.cgi?id=361852)
- ツールバーでの不透明度の表示を0から1ではなくパーセント表示に変更

### その他

- ARMでのビルドを修正 [BUG:393010](https://bugs.kde.org/show_bug.cgi?id=393010)
- [PVS-Studio](https://www.viva64.com/en/pvs-studio/)による多数の警告を修正

## ダウンロード

### Windows

Windowsユーザーの皆さんへ：もしクラッシュする事案に遭遇した場合は、[この案内（英語）](https://docs.krita.org/Dr._Mingw_debugger) に従いデバッグシンボルをKritaに追加してください。これによってKritaがクラッシュした原因をログから解析できるようになります。

- 64ビットWindows版: [krita-x64-4.0.2-setup.exe](https://download.kde.org/stable/krita/4.0.2/krita-x64-4.0.2-setup.exe)
- 64ビットWindowsポータブル版: [krita-x64-4.0.2.zip](https://download.kde.org/stable/krita/4.0.2/krita-x64-4.0.2.zip)
- [32ビット版向けデバッグシンボル(Kritaをインストールしたフォルダに展開して使用)](https://download.kde.org/stable/krita/4.0.2/krita-x64-4.0.2-dbg.zip)

- 32ビットWindows版: [krita-4.0.2-x86-setup.exe](https://download.kde.org/stable/krita/4.0.2/krita-x86-4.0.2-setup.exe)
- 32ビットWindowsポータブル版: [krita-x86-4.0.2.zip](https://download.kde.org/stable/krita/4.0.2/krita-x86-4.0.2.zip)
- [32ビット版向けデバッグシンボル(Kritaをインストールしたフォルダに展開して使用)](https://download.kde.org/stable/krita/4.0.2/krita-x86-4.0.2-dbg.zip)

### Linux

- 64ビットLinux用AppImage版: [krita-4.0.2-x86\_64.appimage](https://download.kde.org/stable/krita/4.0.2/krita-4.0.2-x86_64.appimage)

(なぜかFirefoxはテキストとして読み込もうとするようです。ダウンロードするにはリンクの右クリックから保存してください) 更新がされると、Ubuntuと派生ディストリビューションでは[Krita Lime PPA](https://launchpad.net/%7Ekritalime/+archive/ubuntu/ppa)からもKrita 4.0.2をインストールできるようになります。snapの更新については作業中です。

### OSX

- OSXディスクイメージ版: [krita-4.0.2.dmg](https://download.kde.org/stable/krita/4.0.2/krita-4.0.2.dmg)

注意: gmic-qtとPythonプラグインはOSXで利用できません。

### ソースコード

- ソースコード: [krita-4.0.2.tar.gz](https://download.kde.org/stable/krita/4.0.2/krita-4.0.2.tar.gz)

### md5sum

すべてのダウンロード向け:

- [md5sum.txt](https://download.kde.org/stable/krita/4.0.2/md5sum.txt)

### キー

Linux appimageとソースのtarボールは署名されています。パブリックキーをhttps経由で取得できます: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8) 署名は [こちら](http://download.kde.org/stable/krita/4.0.2/)です (.sigのファイルです)

## Kritaを支援してください

Kritaは自由なオープンソースのプロジェクトです。[寄付](https://krita.org/jp/support-us-jp/donations-jp/)や[トレーニングビデオやアートブックの購入](https://krita.org/jp/support-us-jp/shop-jp/)で、プロジェクトを支援することを検討してみてください！皆様の支援によって、コアチームがフルタイムでKritaの開発作業を続けることが可能になります。

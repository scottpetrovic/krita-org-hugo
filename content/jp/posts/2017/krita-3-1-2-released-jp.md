---
title: "Krita 3.1.2がリリースされました!"
date: "2017-02-02"
categories: 
  - "uncategorized-jp"
---

Krita 3.1.2は2017年2月1日にリリースされました。3.1シリーズの最初のバグ修正リリースになります。ただバグ修正だけではなく、新しい機能も数個追加されています！

### アニメーションでのオーディオサポート

<iframe src="https://www.youtube.com/embed/s08oHOjxo84" width="100%" height="450" frameborder="0" allowfullscreen="allowfullscreen"></iframe>

オーディオファイルをインポートすると、声や音楽への同期の助けになります。左のデモではTimothée Gietさんがオーディオを使った時のスクラブ、再生を紹介しています。

- 利用できるオーディオ形式はWAV、MP3、OGGとFLACです。
- エクスポート時にオーディオを含めるためのチェックボックスがアニメーション出力ダイアログに追加されました。
- オーディオインポート機能の使い方とセットアップについての詳細は[ドキュメントを参照してください。](https://docs.krita.org/Audio_for_Animation)

オーディオはまだLinux appimageでは使用できません。これは実験段階の機能で、まだ正しく機能するという保証はありません。フィードバックを必要としています！

### その他新機能

- 輪郭選択ツールでのCtrlキーによる継続モード: 輪郭選択を作っている時にCtrlを押すと、タブレットからスタイラスを上げても選択が完了しなくなります。任意の場所から選択範囲の描画を再開できます。
- 選択ツールでのシングルクリックによる選択解除: どの選択ツールでも、シングルクリックで選択解除ができるようになりました。
- 設定ダイアログにHiDPIをオンにするチェックボックスを追加しました。
- PDF出力機能の削除。多くの問題を抱えすぎていました。([BUG:372439](https://bugs.kde.org/show_bug.cgi?id=372439))

また数多くのバグが修正されています。 [リリースノート完全版](https://krita.org/en/release-notes-for-3-1-2/)をチェックしてみてください！

### 本を手に入れましょう!

他の人たちがKritaで何を成し遂げているかを見てみたいのなら、初のKritaのアートブックとなる[**Made with Krita 2016**](https://krita.org/en/item/made-with-krita-2016-the-krita-artbook/)を手に入れましょう。予約開始しています!

\[caption id="attachment\_4645" align="alignleft" width="217"\][![Made with Krita 2016](/images/posts/2017/cover_small-217x300.png)](https://krita.org/wp-content/uploads/2016/12/cover_small.png) Made with Krita 2016\[/caption\]

### フィードバックをお願いします!

2017年Kritaユーザー調査にもう1000年以上が回答しています！[どのようにKritaを使っているか、使用ハードウェア、好きなところと嫌いなところを教えてください！](https://goo.gl/forms/PhiKC9cy3wz6DaxN2)

#### Windows

Windowsユーザーの皆さんへ：もしクラッシュする事案に遭遇した場合は、[この案内（英語）](https://docs.krita.org/Dr._Mingw_debugger)に従いデバッグシンボルをKritaに追加してください。これによってKritaがクラッシュした原因をログから解析できるようになります。

- 32ビットWindows版: [krita-3.1.2.2-x86-setup.exe](http://download.kde.org/stable/krita/3.1.2/krita-3.1.2.2-x86-setup.exe)
- 32ビットWindows用ポータブル版: [krita-3.1.2.2-x86.zip](http://download.kde.org/stable/krita/3.1.2/krita-3.1.2.2-x86.zip)
- [32ビット版向けデバッグシンボル (Kritaをインストールしたフォルダに展開して使用)](http://download.kde.org/stable/krita/3.1.2/krita-3.1.2.2-x86-dbg.zip)
    - （訳注：3.1.2.2パッケージでは32ビット版でQtMultimedia.dllがパッケージされていなかった問題 を解決しています。この記事が出る前にダウンロードしてdllが不足しているというエラーが出た人は、こちらの新しいパッケージを再ダウンロードしてください）

- 64ビットWindows版: [krita-3.1.2.1-x64-setup.exe](http://download.kde.org/stable/krita/3.1.2/krita-3.1.2.1-x64-setup.exe)
- 64ビットWindows用ポータブル版: [krita-3.1.2.1-x64.zip](http://download.kde.org/stable/krita/3.1.2/krita-3.1.2.1-x64.zip)
- [64ビット版向けデバッグシンボル (Kritaをインストールしたフォルダに展開して使用)](http://download.kde.org/stable/krita/3.1.2/krita-3.1.2.1-x64-dbg.zip)

#### Linux

- 64ビットLinux用AppImage版: [krita-3.1.2-x86\_64.appimage](http://download.kde.org/stable/krita/3.1.2/krita-3.1.2-x86_64.appimage)

Ubuntu App Store向けのsnapイメージは近日中に利用可能になります。 Ubuntuと派生ディストリビューションでは[Krita Lime PPA](https://launchpad.net/~kritalime/+archive/ubuntu/ppa)を使ってKrita 3.1.2をインストールすることも可能です。

#### OSX

- OSXディスクイメージ版: [krita-3.1.2.0.dmg](http://download.kde.org/stable/krita/3.1.2/krita-3.1.2.0.dmg)

### ソースコード

- ソースコード: [krita-3.1.2.1.tar.gz](http://download.kde.org/stable/krita/3.1.2/krita-3.1.2.1.tar.gz)

#### md5sums

すべてのダウンロード向け:

- [md5sums.txt](http://download.kde.org/stable/krita/3.1.2/md5sums.txt)

#### 公開鍵

Linux appimageとソースのtarボールは署名されています。パブリックキーをhttps経由で取得できます: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8). 署名は[こちら](http://download.kde.org/stable/krita/3.1.2)。

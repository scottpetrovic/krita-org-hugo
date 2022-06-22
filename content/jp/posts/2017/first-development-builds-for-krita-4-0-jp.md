---
title: "Krita 4.0最初の開発版リリース！"
date: "2017-06-16"
categories: 
  - "uncategorized-jp"
---

まだ開発は途中であり、そしてまず最初に言っておかなければならないことがあります：このビルドは普段の作業にはまだ使えません。これはつまり、ツイていれば何事もなかったということもありえますが、同様にツイてなければ作業データが吹っ飛んだなどということもまたありえるということです。まずはぜひテストと何か問題があれば[bugs.kde.org](https://bugs.kde.org)への報告（ですが自分の問題が既に報告済みでないかどうかは確認してください）をお願いします。そんなわけで…

**こちらがKrita 4.0プレアルファ版最初のビルドです！**

これは2.9から3.0へのバージョンアップより大きな変化とまではいかずとも、同等程度には大きなバージョンアップです。いえ、KritaのQt6への移植はまだですよｗ ですが、Kritaのベクターシステムは完全に入れ替えられました。今まで使っていた[Open Document Graphics](https://docs.oasis-open.org/office/v1.2/OpenDocument-v1.2.html)標準の代わりに、このバージョンからKritaはベクター情報を収納するのに[SVG](https://www.w3.org/TR/SVG/)標準を使用するようになりました。これにより[inkscape](https://inkscape.org)などの他ソフトとの互換性が高まりました。KritaはODGベクターレイヤーを持つ既存のKritaドキュメントの読み込みがまだ可能ですが、SVGベクターレイヤーのみが保存可能となります。**一度Krita 4.0プレアルファ版で保存してしまったファイルに関しては、バージョン3台ではベクターレイヤーの読み込みが出来なくなることにご注意ください。**

[![](/images/posts/2017/vector-934x1024.png)](https://krita.org/wp-content/uploads/2017/06/vector.png)

またベクターレイヤーでの作業をより簡単に、生産的にするべく、ベクター図形の取扱についても多くの部分を書き換えました。そしてそれらの改良に対する皆さんのフィードバックも同様に歓迎です。

勿論、大きな変更というのはこれだけではありません。

Allen Marshallによって開発された全く新しいエアブラシの機構が既存のエアブラシの機構を置換しました。これはエアブラシのオプションを使用するブラシプリセットに影響をあたえることになります。ですが、この新機構は明確な改良であるため、古いものを残しておく理由はありませんでした。

Eugene Ingermanが修復ブラシツールを追加しました。使い方はツールボックスにある絆創膏のアイコンのツールを選択し、修復したい場所を塗るだけです！

https://youtu.be/jI87VzDtkPY

画像の保存に関しても今までのものよりもっと安全な新機構を実装しました。この新機構ではデータの一部が失われるフォーマットについては事前に警告を行うようになっています。

[![](/images/posts/2017/warnings.png)](https://krita.org/wp-content/uploads/2017/06/warnings.png)

パレットドッキングパネルについてもWolthera van Hövell tot Westerflierにより大きく改良がなされました。これによってパレットの色をグループ化したり（訳注：実装が不完全なため現時点では使用不能）色をドラッグ&ドロップで並び替えたり、色をダブルクリックして編集したりできます。

[![](/images/posts/2017/palette_dnd.png)](https://krita.org/wp-content/uploads/2017/06/palette_dnd.png)

新たにSVGシンボルを読み込み、画像上にベクター図形としてドラッグ&ドロップできるドッキングパネルを追加しました。吹き出しにもってこいの機能で、手始めとしてDavid RevoyのPepper and Carrot吹き出しライブラリが既に追加されています！

[![](/images/posts/2017/symbol.png)](https://krita.org/wp-content/uploads/2017/06/symbol.png)

さらにもっとたくさんの変更があります。ぜひ探し出して試してみてください！

現在も新しいテキストツールについては開発中です。基本的な部分についての開発は先週始まったばかりですが、またこの開発ビルドには含まれていません。まだ開発版に入れるのにも出来が甘すぎます！

Pythonプラグインは既にマージされ、いつでもテストに入れる状態にあります、しかし、これについては別の問題にぶち当たりました：Kritaのスクリプトに必要なPythonとPythonモジュールをどうやってバンドルするのか未だに解明できていないのです。対応しているLinuxシステムからKritaをビルドした時は上手くいくのですが、Windows及びOSXではまだ全くビルドが出来ていません。**これについてもし何か心当たりがあれば、ぜひ我々に連絡をお願いします！**

[![](/images/posts/2017/scripter.png)](https://krita.org/wp-content/uploads/2017/06/scripter.png) Scripter―Eliakin Costaによって開発されたKrita付属の簡易スクリプタ

#### ダウンロード

#### Windows

Windowsユーザーの皆さんへ：もしクラッシュする事案に遭遇した場合は、[この案内（英語）](https://docs.krita.org/Dr._Mingw_debugger)に従いデバッグシンボルをKritaに追加してください。これによってKritaがクラッシュした原因をログから解析できるようになります。

- 64ビットWindows用ポータブル版: [krita-4.0.0-prealpha.1-x64.zip](https://download.kde.org/unstable/krita/4.0.0-prealpha/krita-4.0.0-prealpha.1-x64.zip)
- [64ビット版向けデバッグシンボル (Kritaをインストールしたフォルダに展開して使用)](https://download.kde.org/unstable/krita/4.0.0-prealpha/krita-4.0.0-prealpha.1-x64-dbg.zip)
- 32ビットWindows用ポータブル版: [krita-4.0.0-prealpha-x86.zip](https://download.kde.org/unstable/krita/4.0.0-prealpha/krita-4.0.0-prealpha-x86.zip)
- [32ビット版向けデバッグシンボル (Kritaをインストールしたフォルダに展開して使用)](https://download.kde.org/unstable/krita/4.0.0-prealpha/krita-4.0.0-prealpha-x86-dbg.zip)

#### Linux

- 64ビットLinux用AppImage版: [krita-4.0.0-prealpha-x86\_64.appimage](https://download.kde.org/unstable/krita/4.0.0-prealpha/krita-4.0.0-pre-alpha-x86_64.appimage)

#### OSX

- OSXディスクイメージ版: [krita-4.0.0-pre-alpha.dmg](https://download.kde.org/unstable/krita/4.0.0-prealpha/krita-4.0.0-prealpha.dmg)

### ソースコード

- ソースコード: [krita-4.0.0-pre-alpha.tar.gz](https://download.kde.org/unstable/krita/4.0.0-prealpha/krita-4.0.0-prealpha.tar.gz)

#### md5sums

すべてのダウンロード向け:

- [md5sums.txt](https://download.kde.org/stable/krita/3.1.4/md5sums.txt)

#### 公開鍵

Linux appimageとソースのtarボールは署名されています。公開鍵をhttps経由で取得できます: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8). 署名は[こちら](http://download.kde.org/stable/krita/3.1.4/)です。

#### Krita開発への支援をよろしくお願いします。

Kritaは自由でオープンソースのプロジェクトです。[寄付](https://krita.org/en/support-us/donations/)や[トレーニング動画、画集の購入](https://krita.org/wp-admin/%22https://krita.org/en/support-us/shop)でこのプロジェクトを支援することをご検討してはいただけないでしょうか？皆さんの支援があって初めて、我々開発はコアチームにKritaの開発をフルタイムで行わせることが可能になるのです。

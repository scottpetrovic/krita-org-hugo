---
title: "Krita 4.4.0 リリース!"
date: "2020-10-21"
categories: 
  - "officialrelease-jp"
---

Krita 4.4.0をリリースしました!

計画から少しの遅れで済みました。これがKritaの新機能を含む新しいリリースです！非常に多用途なSeExprベースの塗りつぶしを含む様々な新しい塗りつぶしレイヤータイプが追加されました。ブラシのグラデーションマップモード、ブラシテクスチャの明るさ、グラデーションモード、グラデーションでの動的な色の使用のサポートといった面白いブラシオプションが追加され、アニメーションのwebm出力が可能になり、スクリプティング機能も追加されています。もちろん数百のバグ修正も行われて、Kritaはさらに良いものになっています。特に、KritaのChromeOS版、Android版にも様々な修正をしています！

[完全版のリリースノート](https://krita.org/en/krita-4-4-0-release-notes/)からハイライトを紹介します:

## 塗りつぶしレイヤー

このリリースでは塗りつぶしレイヤーに多くの更新と変更があります。

### 塗りつぶしレイヤーのマルチスレッド化

塗りつぶしレイヤーがマルチスレッドを活用するようになりました。複数コアのあるPCでは、複数コアで塗りつぶしレイヤーの計算を分散します。これで塗りつぶしレイヤーが大幅に高速化します。

### パターン塗りつぶしの移動

[![](/images/posts/2020/krita_4_4_texture_example.png)](/images/posts/2020/krita_4_4_texture_example.png)

様々なパターン移動が可能になりました。

[塗りつぶしレイヤーのパターン](https://docs.krita.org/en/reference_manual/layers_and_masks/fill_layer_generators/pattern_fill.html)の移動、回転が可能になりました。これはシェイプ描画ツールとバケツ塗りつぶしでも実装されています。長い間Todoとして存在していたものが実現しました。

### スクリーントーン

[![](/images/posts/2020/fill_layer_screentone_postprocessing.png)](/images/posts/2020/fill_layer_screentone_postprocessing.png)

画面全体をドット、四角、ライン、波などで埋めることに特化した[新しい塗りつぶしレイヤーオプション](https://docs.krita.org/en/reference_manual/layers_and_masks/fill_layer_generators/screentone.html)です。この塗りつぶしレイヤーではその場でシンプルなパターンを簡単に生成できます。コミックイラストや、グラフィックスタイル作りでとても役立ちます。

### マルチグリッド

[![](/images/posts/2020/multigrid-color-examples.png)](/images/posts/2020/multigrid-color-examples.png)

[パターンを生成する塗りつぶしレイヤー](https://docs.krita.org/en/reference_manual/layers_and_masks/fill_layer_generators/multigrid.html)です。[ペンローズタイル](https://en.wikipedia.org/wiki/Penrose_tiling)や準結晶構造などのパターン生成します。回転に対してシンメトリーを持つ結果ですが、周期的ではありません。ひし形パターン自身の繰り返しはありません。. このフィルタは次のアイテムからインスパイアされました…

### SeExpr

[![](/images/posts/2020/1096px-SeExpr_manual_1.jpg)](/images/posts/2020/1096px-SeExpr_manual_1.jpg) SeExpr マニュアル

AmysparkのGoogle Summer of CodeプロジェクトはDisney Animationの[SeExpr](https://docs.krita.org/en/reference_manual/layers_and_masks/fill_layer_generators/seexpr.html)エクスプレッション言語のインテグレーションでした。SeExprはWalt Disney Animation Studiosがアニメーションのためにテクスチャやマテリアルを生成するのに使用している小さなシェーダー言語です。KritaではSeExprで塗りつぶしレイヤーを作れます。また、いい感じのデフォルトサンプルも用意することを試みました。

## ブラシ

4.3での明るさモードの追加に加えて、ブラシエンジンに今回も新機能を追加しました。

[![](/images/posts/2020/flowers_gradients_lightness.png)](/images/posts/2020/flowers_gradients_lightness.png)

トップストローク: 新しい明るさパラメータとミックスパラメータの組み合わせを使います。ボトムストローク: テクスチャ強度パラメータでグラデーションマップのブラシ先端とテクスチャを混ぜ合わせします。

### MyPaint色選択の斜め選択ライン (Shift+M)

斜めラインでアクティブカラーの_明るさと彩度_を同時に変更することが可能です。

[![MyPaint色選択の斜め選択ライン (Shift+M)](/images/posts/2020/mypaint_selector_diagonal.png)](/images/posts/2020/mypaint_selector_diagonal.png) MyPaint色選択の斜め選択ライン (Shift+M)

## 現在選択している色を動的にグラデーションで使用するためのサポート

KritaはGIMPグラデーションフォーマットをサポートしていましたが、現在の前景色、背景色による動的な[グラデーション](https://docs.krita.org/en/reference_manual/resource_management/resource_gradients.html)の変更はサポートしていませんでした。レイヤースタイルでも不可能でした。この機能が今回追加されました。同梱のプリセットでも前景色を使用して、簡単に火花、霧といったエフェクトを簡単に生成できるようになりました。[![](/images/posts/2020/fg_changing_gradients_for_sparkles.png)](/images/posts/2020/fg_changing_gradients_for_sparkles.png)GPS glareデフォルトによる火花。 前景色で色が変わります

## ダウンロード

### Windows

ポータブルZipファイルを使う場合は、Zipファイルをエクスプローラーで開いてフォルダを適当な場所に移動して展開し、フォルダ内のKritaアイコンをダブルクリックして起動してください。インストール済みのKritaには影響はありませんが、設定とカスタムリソースは通常のインストール済みのKritaと共有されることに気を付けてください。. クラッシュの報告をするには、デバッグシンボルフォルダもインストールしてください。

**Windowsユーザーへの注意: マイクロソフトは証明書で署名したアプリケーションの扱いを変更しました。Digicertの証明書だけが自動的に信頼されます。他の証明書は、十分な人数のユーザーがスマートスクリーンをバイパスして署名されたアプリケーションを実行しないと信頼されません。私たちのビルドは安全です。バイバスして実行することは安全です。****「Windows によって PC が保護されました」の画面が出た場合は「詳細情報」をクリックしてから、「実行」を選択します。**

- 64ビットWindowsインストーラー: [krita-x64-4.4.0-setup.exe](https://download.kde.org/stable/krita/4.4.0/krita-x64-4.4.0-setup.exe)
- 64ビットWindowsポータブル版: [krita-x64-4.4.0.zip](https://download.kde.org/stable/krita/4.4.0/krita-x64-4.4.0.zip)
- [デバッグシンボル(Kritaをインストールしたフォルダに展開してください)](https://download.kde.org/stable/krita/4.4.0/krita-x64-4.4.0-dbg.zip)

- 32ビットWindowsインストーラー: [krita-x86-4.4.0-setup.exe](https://download.kde.org/stable/krita/4.4.0/krita-x86-4.4.0-setup.exe)
- 32ビットWindowsポータブル版: [krita-x86-4.4.0.zip](https://download.kde.org/stable/krita/4.4.0/krita-x86-4.4.0.zip)
- [デバッグシンボル(Kritaをインストールしたフォルダに展開して使用)](https://download.kde.org/stable/krita/4.4.0/krita-x86-4.4.0-dbg.zip)

### Linux

- 64ビットLinux: [krita-4.4.0-x86_64.appimage](https://download.kde.org/stable/krita/4.4.0/krita-4.4.0-x86_64.appimage)
- 64ビットLinux [G'Mic-Qt plugin appimage](https://download.kde.org/stable/krita/4.4.0/gmic_krita_qt-x86_64.appimage)

(なぜかFirefoxはテキストとして読み込もうとするようです。ダウンロードするにはリンクの右クリックから保存してください)

### OSX

- OSXディスクイメージ版: [krita-4.4.0.1.dmg](https://download.kde.org/stable/krita/4.4.0/krita-4.4.0.dmg)

注意: gmic-qtはOSXで利用できません。

### ChromeOSとAndroidベータ

今回はAndroidリリースはリリースtarballから作成されたので翻訳も含まれています。ChromeOS版とAndroid版のKritaはまだ **_ベータ_**状態と考えています。動かない部分も多数あり、キーボードがなければ操作できないものもあります。

- [64 ビット Intel CPU APK](https://download.kde.org/stable/krita/4.4.0/krita-x86_64-4.4.0-release.apk)
- [32 ビット Intel CPU APK](https://download.kde.org/stable/krita/4.4.0/krita-x86-4.4.0-release.apk)
- [64 ビット Arm CPU APK](https://download.kde.org/stable/krita/4.4.0/krita-arm64-4.4.0-release.apk)
- [32 ビット Arm CPU APK](https://download.kde.org/stable/krita/4.4.0/krita-arm32-4.4.0-release.apk)

### ソースコード

- [krita-4.4.0.tar.gz](https://download.kde.org/stable/krita/4.4.0/krita-4.4.0.tar.gz)
- [krita-4.4.0.tar.xz](https://download.kde.org/stable/krita/4.4.0/krita-4.4.0.tar.xz)

### md5sum

すべてのダウンロード向け:

- [md5sum.txt](https://download.kde.org/stable/krita/4.4.0/md5sum.txt)

## Kritaを支援してください

Kritaは自由なオープンソースのプロジェクトです。[寄付](https://krita.org/jp/support-us-jp/donations-jp/)や[トレーニングビデオの購入](https://krita.org/en/shop/)で、プロジェクトを支援することを検討してみてください！皆様の支援によって、コアチームがフルタイムでKritaの開発作業を続けることが可能になります。

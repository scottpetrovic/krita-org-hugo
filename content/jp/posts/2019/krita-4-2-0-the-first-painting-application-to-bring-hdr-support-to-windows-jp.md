---
title: "Krita 4.2.0: WindowsでHDRペイントをサポートする最初のペイントアプリケーション"
date: "2019-03-17"
categories: 
  - "uncategorized-jp"
---

今はバグ修正に集中しています。5月に次のメジャーバージョンのKrita 4.2.0をリリースしたいと考えているからです。新しい機能に、大量のバグ修正とパフォーマンス向上に加えて、1つとてもユニークなことがあります。HDRモードでのペイントのサポートです。Kritaは、これをサポートする最初のアプリケーションになります！オープンソースでもプロプライアタリソフトにおいても、これがはじめてです。

HDRサポートが内蔵されたKrita 4.2.0のプレビュー版をリリースするので、あなたもこの機能を試すことができます！

ただし、現時点では[Windows 10のみが](https://support.microsoft.com/en-us/help/4040263/windows-10-hdr-advanced-color-settings)HDRモニタをサポートし、サポートされているハードウェアも特定のものだけです。CPUもGPUもそこそこ最近のもので、[HDRをサポートするモニタ](https://displayhdr.org/certified-products/)も必要です。Intelの勇敢な人たちがLinuxでのHDRサポートについても作業していることは聞いています。

### HDRとは？

HDRはHigh Dynamic Rangeの略です。

その反対はLow Dynamic Rangeです。今では、多くの人はHDRと聞くと電話のカメラのHDRモードを思ってしまうかもしれません。こうしたカメラは様々な露出レベルで撮影された画像を一つにまとめて、通常の画像の小さいダイナミックレンジのでも、高ダイナミックレンジのような幻想を作ります。時には不自然な結果になります。

これは違います！トーンマッピングは古い手法です。. 今では従来のモニタよりはるかに明るい新しいモニタが出てきています。1000 nits（明るさの単位）のものも、プロ用ではもっと明るいものもあります。最近のシステム、Intelの第7世代Core CPUはこうしたモニタをサポートしています。

これは明るさだけの話ではありません。大部分のモニタは [sRGB](https://en.wikipedia.org/wiki/SRGB)の色域を表示するように作られています。これは制限されたもので、緑が欠けています。（プロ用モニタではより広い色域のものもあります）HDRモニタははるかに広い色域を使用します。[Rec. 2020](https://en.wikipedia.org/wiki/Rec._2020)色空間です。そして従来の指数的ガンマコレクションの代わりに、 [Perceptual Quantizer (PQ)](https://en.wikipedia.org/wiki/High-dynamic-range_video#Perceptual_Quantizer)を使用しています。ダイナミックレンジを太陽のような明るい値まで拡張するだけではなく、通常のsRGBでは不可能なようなとても暗いエリアをエンコードすることも可能にします。

[![](/images/posts/2019/image3.png)](/images/posts/2019/image3.png)

そして、多くのラップトップパネルは各チャンネルで6bitのみをサポートし、多くのモニタは8bitでグラフィックプロ向けモニタは10bitですが、HDRモニタはチャンネルごとに10から16bitをサポートします。つまり、グラデーションが向上します。

ただ、まだ歴史が浅く、開発者の視点からいえば、この状況は混沌としています。すべてがどう組み合わさるのか理解することは難しく、将来修正のリリースをする必要もあるかもしれませんし、何か誤解している部分もあるかもしれません。

では... HDRをサポートするのはWindows 10、DirectXのみです。Linuxはなし、OpenGLもダメで、 macOSは多分なしです。Kritaのコードが話すのはOpenGLでDirectXではないので、OpenGLからDirectX互換性レイヤーのAngleをハックしてHDRを動かすための拡張を入れる必要がありました。そしてQtもハックする必要がありました。キャンバスはそのままにしつつ、ボタンやパネルといったUIをsRGBからp2020-pqに変換するためです。もちろん、HDRをサポートした色選択機能も追加する必要がありました。数か月の熱心な仕事でした。

ここまでは技術的な話です。大事なことは、ユーザーが新しいHDR画像を実際に作り出すことができるということです。

### なぜすごいことなのでしょうか？

より広い範囲の色を使えるようになります。より広い範囲の明るさ、暗さを扱えるようになります。純粋な光をペイントすることだってできます。HDR画像を作るときにあなたがすることは、ある意味で、ディスプレイの表示にあわせて何かをペイントするというよりは、シーンに光が落ちる様をペイントすることです。ここには新しい自由度があり、使い方を発見してきているところです！

HDR互換の環境があり、ブラウザがHDRをサポートしていれば、このビデオもHDRで表示できるかもしれません:

https://www.youtube.com/watch?v=4O1kxEL9naw&feature=youtu.be (Image by Wolthera van Hövell tot Westerflier)

### どうやって使うのですか？

HDR互換モニタ、DisplayPort 1.4かHDMI 2.0**a** (この'a'が重要です)以上のケーブル、WDDM 2.4ドライバを持つ最新バージョンのWindows 10とこれをサポートするCPUとGPUがあるとして、有効にする方法は以下です:

[Windows設定ユーティリティでHDRモードの表示を手動で切り替えます](https://support.microsoft.com/en-us/help/4040263/windows-10-hdr-advanced-color-settings)。そうするとWindowsはディスプレイにp2020-pqモードで通信するようになります。すべての表示がおかしくなってびっくりしないようにしてください。デフォルトのSDRブライトネスレベルを選択する必要があります。

[![](/images/posts/2019/hdr_settings.png)](/images/posts/2019/hdr_settings.png)

KritaでもHDRサポートの設定が必要です。 _Settings（設定） → Configure Krita（Kritaの設定を変更） → Display（表示）_ でモニタを設定します。またHDRに対応した**small color selector**を_Settings（設定） → Dockers（ドッキングパネル）_メニューから有効にしたいと思うでしょう。

[![](/images/posts/2019/hdr_krita_settings.png)](/images/posts/2019/hdr_krita_settings.png)

正しいHDR画像を作るには、rec 2020の色域でリニアのトーン反応のキャンバスを作成する必要があります: ここで選択するカラープロファイルは"Rec2020-elle-V4-g10.icc" です。HDR画像は標準としてRec2020色域と、PQ trcを使用します。ただ、リニアTRCの方が画像編集には便利なので、画像編集後に最後にPQに変換します。

Kritaのネイティブの.kraファイルフォーマットは、HDR画像を問題なく保存できます。作業中のフォーマットとしてこの.kraを使うべきです。他の画像編集ソフトとのデータやりとりにはOpenEXRフォーマットを使うべきです。Webでの共有には、拡張されたPNGフォーマットを使用できます。すべて新しいものなので、標準のサポートはまだありません。

HDRアニメーションも作成できます... とてもクールですよ！アニメーションはmp4とH.265で出力できます。H.265をサポートするバージョンの [FFMpeg](https://trac.ffmpeg.org/wiki/Encode/H.265)が必要です。まずKritaにこのFFMpegの場所を教えて、そのあとの手順は以下です。

- アニメーションを開いておきます。
- File（ファイル） → Render Animation（アニメーションを出力）を選びます。
- Videoを選択します。
- 出力をMPEG-4 videoかMatroskaにします。
- 出力フォーマット選択メニューの横の設定ボタンをクリックします。
- 一番上の'H.265, MPEG-H Part 2 (HEVC)'を選択します。
- プロファイルは: 'main10' です。
- これでHDR Modeチェックボックスが有効になります。チェックします。
- 'HDR Metadata' をクリックしてHDR メタデータを設定します。
- 最後に'render'をクリックします。

第7世代以降のコアかIntel Graphics integratedがあればハードウェアエンコードを使って出力時間が短縮されます。ffmpegが自動で使用します。

### ダウンロード

すみません、このバージョンのKritaはWindowsユーザー _のみ_に役立つものです。Linuxのグラフィック開発者は開発を進めていきましょう！

### Windows

- 64 bits Windows: [krita-x64-4.2.0-HDR-setup.exe](https://download.kde.org/unstable/krita/4.2.0-HDR/krita-x64-4.2.0-HDR-setup.exe)
- Portable 64 bits Windows: [krita-4.2.0-HDR.zip](https://download.kde.org/unstable/krita/4.2.0-HDR/krita-x64-4.2.0-HDR.zip)

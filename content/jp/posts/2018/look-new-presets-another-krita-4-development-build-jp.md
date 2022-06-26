---
title: "新しいプリセットを見てください！新しいKrita 4開発ビルドです"
date: "2018-02-18"
categories: 
  - "uncategorized-jp"
---

Krita 4のリリースに向けて非常に集中しています。先月には150くらいのバグをクローズし、Krita 4は多くの人が日々使えるほど安定化してきています。それでも、まだやるべき仕事はあります！これから最低でも4週間の間、問題の修正と調整をするつもりです。

今作業していることの一つは、Kritaに同梱されているブラシプリセットとブラシ先端のデザイン見直しです。ブラシ先端はペイントする際に選択できるブラシ形状の画像で、ブラシプリセットはブラシパレットやブラシポップアップから選択できるブラシです。プリセットは、先端と、設定と、ちょっとしたコードの組み合わせです！

今までのセットも機能していましたが、これは[David Revoy](https://www.davidrevoy.com)さんによるかなり昔のKrita向けブラシバンドルを元にしたもので、Krita 4ではブラシセット全体に手を入れるつもりです。当時に比べて、数多くのブラシの機能や設定が追加されています！というわけで、多くのアーティストが共同作業をして、Krita 4向けのいい見た目で、役に立つ、面白いブラシ群を作成しています。[![](/images/posts/2018/brushj_presets-1024x529.png)](/images/posts/2018/brushj_presets.png)

まだ作業は途中です！ですがフィードバックを欲しいと思っています。ですので... Krita 4の開発ビルドをダウンロードして、落書き、スケッチ、お絵かきなどをしてみてください... そしてどう感じたか教えてください:

[ブラシプリセットサーベイ(英語)に回答してください](https://goo.gl/forms/xRbDIZRnRX005ZOt2)!

新しいブラシとバグ修正以外に、Linuxユーザ向けに新しい情報があります。AppImageビルドスクリプトを更新したので、新しいAppImageにはPythonスクリプト機能とTouch UIドッキングパネルが含まれています。注意: デフォルトではすべてのスクリプトは無効に設定されています。Settings/Configure Krita/Python scripts(設定/Kritaを設定/Python Scripts)から使用したいスクリプトを有効にしてください。

#### リリースを手助けしてください!

プログラミング、バグ修正、マニュアル更新などのタスクで開発チームは手一杯です... というかタスクが溢れています!間に合わないことになりそうなタスクの一つは、Krita 4の新機能を紹介するクールなビデオの作成です。もしビデオの作成が得意で、手助けしたい、ということであれば、 irc.freenode.net の#kritaチャンネルで開発チームにコンタクトしてください!

#### Windows

Windowsユーザーの皆さんへ：もしクラッシュする事案に遭遇した場合は、[この案内（英語）](https://docs.krita.org/Dr._Mingw_debugger) に従いデバッグシンボルをKritaに追加してください。これによってKritaがクラッシュした原因をログから解析できるようになります。Windowsではgmic-qtが含まれています。

- 64ビットWindows版:[krita-nightly-x64-v4.0.0.51-325-g2126cec79f-setup.exe](https://download.kde.org/unstable/krita/4.0.0.52/krita-nightly-x64-v4.0.0.51-325-g2126cec79f-setup.exe)
- 64ビットWindowsポータブル版: [krita-nightly-x64-v4.0.0.51-325-g2126cec79f.zip](https://download.kde.org/unstable/krita/4.0.0.52/krita-nightly-x64-v4.0.0.51-325-g2126cec79f.zip)
- [64ビット版向けデバッグシンボル(Kritaをインストールしたフォルダに展開して使用)](https://download.kde.org/unstable/krita/4.0.0.52/krita-nightly-x64-v4.0.0.51-325-g2126cec79f-dbg.zip)

#### Linux

Linuxっではgmix-qtは別のappimageとしてダウンロードする必要があります。Kritaの設定でgmic-qtの場所を指定します。Kritaを使うには"XDG_DATA_DIRS"環境変数の設定が必須です。大部分のディストリビューションでは設定済みですが、もし設定がされていない場合は、回避策として "XDG_DATA_DIRS"を"/usr/local/share/:/usr/share/"に設定してください。次のビルドではKritaはこれを自動的に行います。

- 64ビットLinux用AppImage版: [krita-4.0.0-beta1-b322ae6-x86_64.appimage](https://download.kde.org/unstable/krita/4.0.0.52/krita-4.0.0-beta1-b322ae6-x86_64.appimage)
- AppImage: [gmic_krita_qt-x86_64-2.2.0.appimage](https://download.kde.org/unstable/krita/4.0.0.52/gmic_krita_qt-x86_64-2.2.0.appimage)

(なぜかFirefoxはテキストとして読み込もうとするようです。ダウンロードするにはリンクの右クリックから保存してください)

#### OSX/macOS

OSX/macOSの最小バージョンは10.11です。

- OSXディスクイメージ版: [https://download.kde.org/unstable/krita/4.0.0.52/krita-4.0.0-g2126cec79f.dmg](https://download.kde.org/unstable/krita/4.0.0.52/krita-4.0.0-g2126cec79f.dmg)

注意: Python、gmic-qtとpdfプラグインはOSXで利用できません。

#### md5sums

すべてのダウンロード向け:

- [md5sum.txt](https://download.kde.org/unstable/krita/4.0.0.52/md5sum.txt)

#### Kritaを支援してください

Kritaは自由なオープンソースのプロジェクトです。[寄付](https://krita.org/jp/support-us-jp/donations-jp/)や[トレーニングビデオやアートブックの購入](https://krita.org/jp/support-us-jp/shop-jp/)で、プロジェクトを支援することを検討してみてください！皆様の支援によって、コアチームがフルタイムでKritaの開発作業を続けることが可能になります。

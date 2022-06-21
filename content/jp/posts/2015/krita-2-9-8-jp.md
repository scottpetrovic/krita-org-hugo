---
title: "Krita 2.9.8リリース"
date: "2015-10-14"
categories: 
  - "uncategorized-jp"
tags: 
  - "japanese"
---

Krita 2.9の8個目のバグ修正リリースです! まだバグ修正と機能追加も行っていますが、KickstarterゴールとKrita3.0の移植作業にも多くの労力を注ぎ込んでいます。Ubuntu Linuxユーザは[Krita Lime repository](https://launchpad.net/~dimula73/+archive/ubuntu/krita) から「krita-lod-unstable」パッケージをインストールして、初期のアニメーションサポートとLODパフォーマンス向上のテストを行うことができます。表示(View)メニューのLODオプションにチェックすると、多くのブラシや機能が、大きな画像でもパフォーマンスが改善するはずです！

とはいえ、普段の作業については、Krita 2.9.8にアップデートをお願いします!Photoshopスタイルのレイヤースタイル機能、および、OpenEXR、TIFF、PNGとJPEGの読み込み書き出しについて、重要な修正が含まれています。

- 新しいレイヤー追加のパフォーマンスを向上(空の新しいレイヤを追加してもKritaが画像全体を更新する必要はない)
- 明るいテーマ、暗いテーマに合わせてパススルーのアイコンを修正。また、いくつかのアイコンを縮小
- BUG:353261: 画像回転とレイヤー回転の用語を統一
- BUG:353248: 特定種類のグラフィックタブレットを使った時のクラッシュを防止
- BUG:352916: ケージ変形処理のクラッシュを修正
- レイヤーを隠した時の描画速度の向上
- シェイプ/ベクターレイヤー使用時のクラッシュを修正
- BUG:352734: 単独レイヤーのEXRファイルの保存を修正
- BUG:352983: 複数レイヤーのEXRファイルの読み込み時のレイヤー順番を修正
- BUG:352734: 複数レイヤーとトップレベルチャンネルがあるEXRファイルの読み込みと保存の両方をサポート
- BUG:310359: L\*a\*b TIFF画像の読み込みと保存を修正
- TIFFとJPG書き出しフィルタに「Save Profile」(プロファイル保存)のチェックボックスを追加。これでTIFF、JPG、PNGにプロファイルを埋め込まずに帆zんすることが可能になります。
- BUG:352845: スムージングオプションの保存を１回だけに修正
- ランダムノイズを使ったPhotoshopのレイヤースタイルを修正
- Photoshopスタイルのレイヤースタイルのパフォーマンス向上

### ダウンロード

- Linux
    - ディストリビューションはそれぞれ自分のブリーディングエッジリポジトリにパッケージを出すはずです。
    - Ubuntu及びその系列ディストリビューションではいつも通りKrita Limeが利用可能です：[https://launchpad.net/~dimula73/+archive/ubuntu/krita](https://launchpad.net/~dimula73/+archive/ubuntu/krita)
    - OpenSUSEユーザーはKDE:Extra repo:[http://download.opensuse.org/repositories/KDE:/Extra/](http://download.opensuse.org/repositories/KDE:/Extra/)、あるいはVcをサポートしたKritaのビルドを持つLeinir氏のOBSリポジトリが使用可能です。
        - [http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE\_13.1/](http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_13.1/)
        - [http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE\_13.2/](http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_13.2/)
        - [http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE\_Factory/](http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_Factory/)
- Windows及びOSX
    - [ダウンロードページ](https://jp.krita.org/download/krita-desktop/ "Krita Desktop")が更新されましたので新ビルドをご確認ください。MSIインストーラを使用したくないという場合は[files.kde.org](http://files.kde.org/krita)からWindows版KritaのZipファイルのポータブル版をダウンロードできます。
    - またベータチャンネルにDesktop29オプションを使用する[Steam版Krita](http://store.steampowered.com/app/280680)の最新バージョンも利用可能になっています。Steam版Kritaのユーザーは自動でアップデートがなされます。

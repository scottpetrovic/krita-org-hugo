---
title: "Krita 3.0リリース"
date: "2016-05-31"
categories: 
  - "uncategorized-jp"
tags: 
  - "japanese"
---

本日、アニメーション製作機能を目玉とするKrita 3.0をリリースしました。1年間の開発の結果、3.0はKritaのコアに統合されたアニメーションのサポート、大きなブラシを大きなキャンバスで使用した際のパフォーマンスを大幅に向上させる高速プレビュー、最新版のQtへの移植、そして非常にたくさんの新機能及び改良からなる非常に大きなリリースとなっています！

[![krita-3.0](/images/posts/2016/krita-3.0-1024x559.png)](https://krita.org/wp-content/uploads/2016/05/krita-3.0.png)

これらの新機能の多くが[2015年のKickstarterキャンペーン](https://www.kickstarter.com/projects/krita/krita-free-paint-app-lets-make-it-faster-than-phot?ref=users)での支援によるものです。残りの追加目標は今年の後半を使ってKrita 3.1で実装されることになります。そして[今年のKickstarterキャンペーン](https://krita.org/krita-kickstarter-2016-jp/)は後7日間です！目標金額30000ユーロ達成に後一歩のところまで来ています。皆さんの支援があれば今年も追加目標を加えられる可能性もまだ残っています！

この記事に改良点の一覧の全ては収まりきりませんでした。[今回の3.0での追加機能、改良点の完全な一覧](https://krita.org/jp/krita-3-0-release-notes-jp/)を別ページに用意したのでぜひそちらをご覧ください！

※Krita 3.0は設定とリソースを2.9とは異なる場所から読み込んでいるため、二つのバージョンを競合なしに一緒に使うことが可能になっています。[リソースの移動についてのチュートリアル(訳注：英語)](https://docs.krita.org/KritaFAQ#My_resource_dissapeared_with_installing_3.0.21_Did_Krita_delete_them.3F)を用意したのでぜひご覧ください。

### ダウンロード

#### Windows

Windowsでは、KritaはWacom、Huion、Yiynova製のペンタブレット及びSurface Proシリーズのタブレットをサポートしています。Trust、Bosto、Genius、Peritab及びそれと同様のペンタブレットについては報告されたバグを再現するために必要なハードウェアが開発にないため、現時点ではサポートしていません。

ZIP版は解凍したのち、フォルダ内のショートカットファイルkritaをダブルクリックしてください。インストーラ版を使いたい場合はまずKrita 2.9のアンインストールをお願いします。

Windows版にはAlvin Hochungさんによるファイルエクスプローラでkritaのネイティブフォーマットである.kraファイルのサムネイルを表示させる[シェル拡張](https://github.com/alvinhochun/KritaShellExtension)が用意されています。インストール版ではオプションとしてKritaのインストールと同時にインストールできます。ZIP版の場合は下のリンクから別個にインストールしてください。

もしウィルススキャナーやその他のセキュリティソフトにインストールが待ったをかけられた場合は下に書かれている[SHA-1チェックサム](https://ja.wikipedia.org/wiki/SHA-1#.E3.83.87.E3.83.BC.E3.82.BF.E5.AE.8C.E5.85.A8.E6.80.A7)を確認してください。もしこのチェックサムを通過するなら、そのファイルは安全ということです。

Windows版KritaはWindows 7、Windows 8及びWindows 10の動作が確認されています。

- [krita-3.0-x64.zip](http://files.kde.org/krita/3/windows/krita-3.0-x64.zip) (8d0b3819a94e2731bfa6265a573526bb65f0e568)
- [krita-3.0-x86.zip](http://files.kde.org/krita/3/windows/krita-3.0-x86.zip) (0cd0ebb41e17163e26928affc9bf4bfbe7b315c0)
- [krita-3.0-x64-setup.exe](http://files.kde.org/krita/3/windows/krita-3.0-x64-setup.exe) (c47285e1457c1492c7ee184835ea70d9ac26fdc5)
- [krita-3.0-x86-setup.exe](http://files.kde.org/krita/3/windows/krita-3.0-x86-setup.exe) (82f68755eeeb28dbbaa7f29db15338a98b07f4a6)
- [kritashellex\_1.1.0.1\_setup.exe](http://files.kde.org/krita/3/windows/kritashellex-1.1.0.2-setup.exe) (4fb24f073b0dfccae79050423bc8596e3218ae7d)

#### Linux

Linuxでは最近のあらゆるLinuxディストリビューションで動く[AppImage](http://appimage.org/)版を提供します。Ubuntu 12.04及びCentOS 6.xではOpenMPのサポートのないAppImage版を使用する必要があります。Krita Limeレポジトリについては現在作業中です。今のところ、Krita Limeレポジトリからはkrita3-testing buildをインストールすることができます。Helio Castroさんによる[Redhat/CentOS/Fedora向けのKritaパッケージ](http://www.heliocastro.info/?p=241)もあります。

AppImageをダウンロードしたら、実行可能にしてその場で起動してください。インストールは必要ありません。現在のところ、AppImage版の提供は64ビット版のみです。

- [krita-3.0-x86\_64.appimage](http://files.kde.org/krita/3/linux/krita-3.0-x86_64.appimage)  (cc4d007aff15369d7ae90160649f9594f256ec2c)
- [krita-3.0-no-openmp-x86\_64.appimage](http://files.kde.org/krita/3/linux/krita-3.0-no-openmp-x86_64.appimage) (39d6d14d0607b7db37ea70b7057ebbaebca19a27)

Michael HallさんによってUbuntu Snap Image版のKritaが提供されています。Snap Imageを「snap install krita\_3.0-snap7\_amd64.snap」でターミナルからインストールできます。このSnap Image版は型落ちのQt 5.6を使用しているため、ペンタブのサポートは完璧なものではないことに注意してください。

- [krita\_3.0-snap7\_amd64.snap](http://files.kde.org/krita/3/linux/krita_3.0-snap7_amd64.snap) (f80852826e2dd58ca3615744940aa63371078dbf)

#### OSX

KritaのOSXでのフルサポートはバージョン3.1で実現する予定です。OSX版Krita 3.0はまだ高速プレビューと高品質でのキャンバスの表示倍率変更がない状態です。また画像のレンダリングに一部問題があります―この問題はApple社が自社製品のディスプレイドライバへのOpenGL 3.0互換性プロファイルのサポートを打ち切ったことによって発生しているものです。現在我々はこれらの機能をOpenGL 3.0コアプロファイルを使って再実装すべく開発を続行中です。現在のところ、OSX版Kritaを創作作業に使用する際は設定からOpenGLを無効にしておくことを推奨します。OSX版Kritaは10.9(Mavericks)及び10.11(El Capitan)のみでテストされています。これは我々が他のバージョンのOSXにアクセスできないからです。 6/4追記：日本語環境のOSXでKrita3.0が起動時に「プリセットが見つからない」エラーで終了してしまう問題に対応した[開発中ビルド](http://files.kde.org/krita/3/osx/devbuilds/)が利用可能です。

- [krita-3.0.dmg](http://files.kde.org/krita/3/osx/krita-3.0.dmg) (dcf9a5bd31efe3a2ce89dff77f7e10e23b704f54)

#### ソースコード

Krita 3.0をパッケージしたいディストリビューションの皆さん用にソースアーカイブを用意されています。もし興味があるならソースアーカイブの代わりにgitレポジトリから直接Kritaをビルドしてみることをお勧めします。これによって日々の修正が反映された最新のコードにアクセスできます。David Revoyさんの[初めてKritaをビルドするに当たってのガイド](http://www.davidrevoy.com/article193/guide-building-krita-on-linux-for-cats)もご覧ください。Kritaをソースコードからビルドするにあたって自分の持っているQtのバージョンがQt 5.6.1より古い場合はkrita/3rdparty/ext\_qtにあるパッチを使ってQtもリビルドする必要があります。

- [krita-3.0.tgz](http://download.kde.org/stable/krita/3.0/krita-3.0.tgz.mirrorlist) (6e0f7763e2ed5e266d916e7f76fadbaaf2c84eb5)

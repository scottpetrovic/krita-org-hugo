---
title: "Krita 3.13ベータ第1版リリース"
date: "2017-04-22"
categories: 
  - "uncategorized-jp"
---

アルファ版リリースから1週間経ちましたが、Krita 3.13ベータ版のリリースを行いました。Krita 3.13はバグ修正を目的とした安定版となる予定です。Krita 4.0にはベクター機能の大幅改善とPythonスクリプト機能が含まれることになる予定です。3.13の安定版リリースは4月末の計画となっています。

現在も3.13安定版リリースに向けバグ修正の作業を続行中ですので、ぜひベータ版を試してみて、何か問題を発見したら[バグトラッカー](https://bugs.kde.org/buglist.cgi?bug_severity=critical&bug_severity=grave&bug_severity=major&bug_severity=crash&bug_severity=normal&bug_severity=minor&bug_status=UNCONFIRMED&bug_status=CONFIRMED&bug_status=ASSIGNED&bug_status=REOPENED&list_id=1431433&product=krita&query_format=advanced)に既に報告が上がっていないか確認し、上がっていなければ報告をお願いします！

3.13アルファ版から今回のリリースまでに修正された箇所です。:

- About Kritaのダイアログに2016年度Kickstarterへの投資者のクレジットを追加
- フィルタダイアログからフィルタマスクを新規作成した時、その名前を「effect」ではなく、使用しているフィルタの名前を使うように変更
- スタートアップダイアログ（例えばpdfインポートフィルタなど）をスプラッシュスクリーンで隠してしまわないように変更
- 変形マスクで歪み変形を使用した時、競合状態で不安定になる問題を修正
- 表示倍率を大きくした状態で歪みツールを使用した時、キャンバスが真っ暗になる問題を修正
- 再生のキャッシュの読み込みを修正
- OSXにおいてはOSXの色選択を使用するように変更:Kritaのカスタム色選択ではOSXの画面の色を選択できていませんでした。
- PNGの圧縮のデフォルトを9から3に変更：これによってPNG画像のサイズを変更することなくその保存をもっと早くすることが出来ました。
- 直線を描くショートカットVを押した時にクラッシュする問題を修正
- インストールが完全でない時に表示される警告画面に未だにCalligraに関する記述があった問題を修正
- タブレットでの基準線ドラッグ移動が正しくできるように修正

#### Windows版のユーザーの皆さんへの注意

**我々はIntelのGPUドライバによる問題をまだ解決できていません。最近のWindowsアップデートがどうやら一部のシステムでKritaのOpenGLキャンバスを壊してしまったようなのです。そして我々の手元のシステムではこの問題が発生していないため、我々はこの問題の回避策を作成できない状況にあります。**今のところ、もし皆さんのシステムでこの問題が発生した場合、メニューの設定→Kritaを設定→表示からOpenGLを無効にする必要があります。

#### Windows

Windows版のユーザーの皆さんへ：もしクラッシュした場合、この案内に従って[デバッグシンボル](https://docs.krita.org/Dr._Mingw_debugger)を使ってください。これによってKritaのどこでクラッシュが発生したかを我々が解明できるようになります。

- 32ビットWindows版: [krita-3.1.3-beta.1-x86-setup.exe](http://download.kde.org/unstable/krita/3.1.3-beta.1/krita-3.1.3-beta.1-x86-setup.exe)
- 32ビットWindowsポータブル版: [krita-3.1.3-beta.1-x86.zip](http://download.kde.org/unstable/krita/3.1.3-beta.1/krita-3.1.3-beta.1-x86.zip)
- [デバッグシンボル（Kritaをインストールしたフォルダに解凍してください）](http://download.kde.org/unstable/krita/3.1.3-beta.1/krita-3.1.3-beta.1-x86-dbg.zip)

- 62ビットWindows版: [krita-3.1.3-beta.1-x64-setup.exe](http://download.kde.org/unstable/krita/3.1.3-beta.1/krita-3.1.3-beta.1-x64-setup.exe)
- 62ビットWindowsポータブル版: [krita-3.1.3-beta.1-x64.zip](http://download.kde.org/unstable/krita/3.1.3-beta.1/krita-3.1.3-beta.1-x64.zip)
- [デバッグシンボル（Kritaをインストールしたフォルダに解凍してください）](http://download.kde.org/unstable/krita/3.1.3-beta.1/krita-3.1.3-beta.1-x64-dbg.zip)

#### Linux

- 64ビットLinux版: [krita-3.1.3-beta.1-x86\_64.appimage](http://download.kde.org/unstable/krita/3.1.3-beta.1/krita-3.1.3-beta.1-x86_64.appimage)

Ubuntu App StoreからSnap Image版も利用可能です。Ubuntu系ディストーションでは[Krita Lime PPA](https://launchpad.net/~kritalime/+archive/ubuntu/ppa)を使ってKrita 3.13ベータ第1版をインストールすることも可能です。

#### OSX

- OSXディスクイメージ版: [krita-3.1.3-beta.1.dmg](http://download.kde.org/unstable/krita/3.1.3-beta.1/krita-3.1.3-beta.1.dmg)

### ソースコード

- ソースコード: [krita-3.1.3-beta.1.tar.gz](http://download.kde.org/unstable/krita/3.1.3-beta.1/krita-3.1.3-beta.1.tar.gz)

#### md5sums

すべてのダウンロード向け:

- [md5sums.txt](http://download.kde.org/unstable/krita/3.1.3-beta.1/md5sums.txt)

#### Key

Linux appimageとソースのtarは署名されています。公開鍵は以下の場所から: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8). 署名は[こちら](http://download.kde.org/unstable/krita/3.1.3-beta.1)です。

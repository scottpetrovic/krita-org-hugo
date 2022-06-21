---
title: "Krita 3.1.3アルファ版リリース"
date: "2017-04-03"
categories: 
  - "uncategorized-jp"
---

次のバージョンのKrita、3.1.3と4.0に向けてクレイジーなほど作業を続けています。Krita3.1.3は安定版のバグ修正リリースで、4.0はベクターとPythonスクリプティングを含む新バージョンです。今週はテスト用の3.1.3アルファ版を用意しました！3.1.3の正式リリースは4月の終わりを予定しています。

3.1.3のリリースに向けてさらなるバグ修正を行っています。このビルドを試して、もし問題を見つけた場合は[バグトラッカー](https://bugs.kde.org/buglist.cgi?bug_severity=critical&bug_severity=grave&bug_severity=major&bug_severity=crash&bug_severity=normal&bug_severity=minor&bug_status=UNCONFIRMED&bug_status=CONFIRMED&bug_status=ASSIGNED&bug_status=REOPENED&list_id=1431433&product=krita&query_format=advanced)に報告されているかを確認し、報告されていない問題は是非報告してください！

#### Windowsユーザ向けの注意

まだIntelのGPUドライバでの問題に苦しんでいます。最近のWindowsアップデートで一部のPCではKritaのOpenGLキャンバスがうまく機能しなくなっているようです。問題が起きているPCが開発チームにないため、回避策を見つけられていません。

#### Windows

Windowsユーザーの皆さんへ：もしクラッシュする事案に遭遇した場合は、[この案内（英語）](https://docs.krita.org/Dr._Mingw_debugger)に従いデバッグシンボルをKritaに追加してください。これによってKritaがクラッシュした原因をログから解析できるようになります。

- 32ビットWindows版: [krita-3.1.3-alpha.2-x86-setup.exe](http://download.kde.org/unstable/krita/3.1.3-alpha.2/krita-3.1.3-alpha.2-x86-setup.exe)
- 32ビットWindows用ポータブル版: [krita-3.1.3-alpha.2-x86.zip](http://download.kde.org/unstable/krita/3.1.3-alpha.2/krita-3.1.3-alpha.2-x86.zip)
- [32ビット向けデバッグシンボル(Kritaをインストールしたフォルダに展開して使用)](http://download.kde.org/unstable/krita/3.1.3-alpha.2/krita-3.1.3-alpha.2-x86-dbg.zip)

- 64ビットWindows版: [krita-3.1.3-alpha.2-x64-setup.exe](http://download.kde.org/unstable/krita/3.1.3-alpha.2/krita-3.1.3-alpha.2-x64-setup.exe)
- 64ビットWindows用ポータブル版: [krita-3.1.3-alpha.2-x64.zip](http://download.kde.org/unstable/krita/3.1.3-alpha.2/krita-3.1.3-alpha.2-x64.zip)
- [64ビット版向けデバッグシンボル (Kritaをインストールしたフォルダに展開して使用)](http://download.kde.org/unstable/krita/3.1.3-alpha.2/krita-3.1.3-alpha.2-x64-dbg.zip)

#### Linux

- 64ビットLinux用AppImage版: [krita-3.1.3-alpha.2-x86\_64.appimage](http://download.kde.org/unstable/krita/3.1.3-alpha.2/krita-3.1.3-alpha.2-x86_64.appimage)

Ubuntu App Store向けのsnapイメージは近日中に利用可能になります。 Ubuntuと派生ディストリビューションでは[Krita Lime PPA](https://launchpad.net/~kritalime/+archive/ubuntu/ppa)を使ってKrita 3.1.3-alpha.2をインストールすることも可能です。

#### OSX

- OSXディスクイメージ版: [krita-3.1.3-alpha.2.dmg](http://download.kde.org/unstable/krita/3.1.3-alpha.2/krita-3.1.3-alpha.2.dmg)

### ソースコード

- ソースコード: [krita-3.1.3-alpha.2.tar.gz](http://download.kde.org/unstable/krita/3.1.3-alpha.2/krita-3.1.3-alpha.2.tar.gz)

#### md5sums

すべてのダウンロード向け:

- [md5sums.txt](http://download.kde.org/unstable/krita/3.1.3-alpha.2/md5sums.txt)

#### Key

Linux appimageとソースのtarボールは署名されています。パブリックキーをhttps経由で取得できます: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8). 署名は [こちら](http://download.kde.org/unstable/krita/3.1.3-alpha.2).

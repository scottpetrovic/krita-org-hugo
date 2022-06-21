---
title: "Krita 4.1.7 リリース"
date: "2018-12-15"
categories: 
  - "news-jp"
  - "officialrelease-jp"
---

Krita 4.1シリーズのバグ修正リリースであるKrita 4.1.7をリリースしました。

最も大事な修正はちょっと変なものです。Wifi接続が改善するかもしれません。Krita.orgからのニュースを表示するウィジェットを開発しようとしたところから問題が起きました。ウィジェットはアクティブにはなっていない上、ネットワーク接続もしていないのですが…それでもQtのネットワークマネージャークラスは常にWifi設定を確認していました。詳細についてはこちらを参照してください: [https://bugreports.qt.io/browse/QTBUG-46015](https://bugreports.qt.io/browse/QTBUG-46015) と [https://bugreports.qt.io/browse/QTBUG-40332](https://bugreports.qt.io/browse/QTBUG-40332)です。

それ以外では、Qt 5.12がタブレット使用時に即座にクラッシュするバグへの回避策を追加しました。ビルド済みのパッケージはこのQtバージョンを使っていないので、WindowsとMacOSとLinux appimageには影響していない話です。ただ、ArchのようなLinuxでのリリースのユーザーは影響を受ける可能性がありました。

その他のバグ修正内容は以下です:

- Fix showing wrongly that there is no audio support in the animation timeline audio menu
- Disable the disk-based animation cache rendering backend on Windows: this would give problems with animations bigger than about 150 frames. ([BUG 401326](https://bugs.kde.org/show_bug.cgi?id=401326))
- Don't hang when trying to load recent files thumbnails for files in a location that's no longer accessible. ([BUG:401939](https://bugs.kde.org/show_bug.cgi?id=401939))
- Make it possible to use the LUT docker when Angle is enabled on Windows. We have also updated the OpenColorIO library to the latest release.
- Remember whether anti-aliasing was enabled in selection tools ([BUG:401730](https://bugs.kde.org/show_bug.cgi?id=401730))
- Add a shortcut to activate the text tool ([BUG:401655](https://bugs.kde.org/show_bug.cgi?id=401655))
- Make the toolbars movable again
- Make Select by Color Range check the entire image ([BUG:346138](https://bugs.kde.org/show_bug.cgi?id=346138))
- Enable HiDPI support by default: the problems with the canvas scaling have been solved.
- Allow krita to import more than file at a time when started from a file manager ([BUG:401476](https://bugs.kde.org/show_bug.cgi?id=401476))
- Fix using the scrollwheel in comboboxes on Linux ([BUG:399379](https://bugs.kde.org/show_bug.cgi?id=399379)) Patch by Mykola Krachkovsky.
- Fix the calculation of Average Desaturation ([BUG:400493](https://bugs.kde.org/show_bug.cgi?id=))
- Do not crash when exporting Compositions ([BUG:400627](https://bugs.kde.org/show_bug.cgi?id=400627))
- Make the move tool show the correct cursor in all modes
- Let the move tool move invisible layers
- Fix a crash in the artistic color selector ([BUG:399860](https://bugs.kde.org/show_bug.cgi?id=399860))

## ダウンロード

### Windows

Windowsユーザーの皆さんへ：もしクラッシュする事案に遭遇した場合は、[この案内（英語）](https://docs.krita.org/en/reference_manual/dr_minw_debugger.html#dr-minw) に従いデバッグシンボルをKritaに追加してください。これによってKritaがクラッシュした原因をログから解析できるようになります。

- 64 bits Windows: [krita-x64-4.1.7-setup.exe](https://download.kde.org/stable/krita/4.1.7/krita-x64-4.1.7-setup.exe)
- Portable 64 bits Windows: [krita-x64-4.1.7.zip](https://download.kde.org/stable/krita/4.1.7/krita-x64-4.1.7.zip)
- [デバッグシンボル(Kritaをインストールしたフォルダに展開して使用)](https://download.kde.org/stable/krita/4.1.7/krita-x64-4.1.7-dbg.zip)

- 32 bits Windows: [krita-x86-4.1.7-setup.exe](https://download.kde.org/stable/krita/4.1.7/krita-x86-4.1.7-setup.exe)
- Portable 32 bits Windows: [krita-x86-4.1.7.zip](https://download.kde.org/stable/krita/4.1.7/krita-x86-4.1.7.zip)
- [デバッグシンボル(Kritaをインストールしたフォルダに展開して使用)](https://download.kde.org/stable/krita/4.1.7/krita-x86-4.1.7-dbg.zip)

### Linux

- 64 bits Linux: [krita-4.1.7-x86\_64.appimage](https://download.kde.org/stable/krita/4.1.7/krita-4.1.7-x86_64.appimage)
- 64ビットLinux [G'Mic-Qt plugin appimage](https://download.kde.org/stable/krita/4.1.7/gmic_krita_qt-x86_64.appimage)

(なぜかFirefoxはテキストとして読み込もうとするようです。ダウンロードするにはリンクの右クリックから保存してください) 更新がされると、Ubuntuと派生ディストリビューションでは[Krita Lime PPA](https://launchpad.net/%7Ekritalime/+archive/ubuntu/ppa)からもKrita 4.1.7をインストールできるようになります。snapの更新については作業中です。

### OSX

- OSX disk image: [krita-4.1.7.1.dmg](https://download.kde.org/stable/krita/4.1.7/krita-4.1.7.1.dmg)

注意: タッチドッキングパネル、gmic-qtとPythonプラグインはmacOSで利用できません。

### ソースコード

- Source code: [krita-4.1.7.101.tar.gz](https://download.kde.org/stable/krita/4.1.7/krita-4.1.7.101.tar.gz)

### md5sum

すべてのダウンロード向け:

- [md5sum.txt](https://download.kde.org/stable/krita/4.1.7/md5sum.txt)

### キー

Linux appimageとソースのtarボールは署名されています。パブリックキーをhttps経由で取得できます: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8) 署名は [こちら](http://download.kde.org/stable/krita/4.1.7/)です (.sigのファイルです)

## Kritaを支援してください

Kritaは自由なオープンソースのプロジェクトです。[寄付](https://krita.org/jp/support-us-jp/donations-jp/)や[トレーニングビデオやアートブックの購入](https://krita.org/jp/support-us-jp/shop-jp/)で、プロジェクトを支援することを検討してみてください！皆様の支援によって、コアチームがフルタイムでKritaの開発作業を続けることが可能になります。

---
title: "Krita 4.1.0 リリース"
date: "2018-06-28"
categories: 
  - "news-jp"
  - "officialrelease-jp"
---

Krita 4.0のリリースから3か月が経ちました。Krita 4.1をリリースします！

https://youtu.be/N6oHLuICrHM

このリリースには以下の大きな機能追加が含まれます:  

- 参照画像ドッキングパネルを置き換えることになる新しい参照画像ツール
- セッションの保存と読み込みができるようになります。作業中に開いていた画像グループとビュー状態を保存できるようになります
- マルチモニターのワークスペースれいアウトを作成できるようになります
- アニメーションフレーム作業ワークフローの向上
- アニメーションタイムライン表示の改善
- レンダリング済みのフレームをディスクにバッファリングすることにより、より大きなアニメーションを扱えるようになります
- カラーピッカーで混色できるオプションの追加
- 消失点補助線ツールの改善。カスタムの色を設定できます
- Kritaのスクリプティング機能をPython 2でもビルドできるようになりました
- ベクター化によるブラシマスクのパフォーマンスを改善するIvan YossiのGoogle Summer of Codeの最初の成果も含まれています！

そして数多くのバグ修正がもちろん含まれ、レンダリングパフォーマンス改善と他にも新機能を含んでいます。**Krita 4.1の新機能についての [完全なリリースノートはこちら](https://krita.org/en/krita-4-1-release-notes/) です！**

[![](/images/posts/2018/krita_41-1024x1024.png)](/images/posts/2018/krita_41.png) Image by RJ Quiralta

## ダウンロード

### Windows

Windowsユーザーの皆さんへ：もしクラッシュする事案に遭遇した場合は、[この案内（英語）](https://docs.krita.org/en/reference_manual/dr_minw_debugger.html#dr-minw) に従いデバッグシンボルをKritaに追加してください。これによってKritaがクラッシュした原因をログから解析できるようになります。

- 64ビットWindows版: [krita-x64-4.1.0-setup.exe](https://download.kde.org/stable/krita/4.1.0/krita-x64-4.1.0-setup.exe)
- 64ビットWindowsポータブル版: [krita-x64-4.1.0.zip](https://download.kde.org/stable/krita/4.1.0/krita-x64-4.1.0.zip)
- [デバッグシンボル(Kritaをインストールしたフォルダに展開して使用)](https://download.kde.org/stable/krita/4.1.0/krita-x64-4.1.0-dbg.zip)

- 32ビットWindows版: [krita-x86-4.1.0-setup.exe](https://download.kde.org/stable/krita/4.1.0/krita-x86-4.1.0-setup.exe)
- 32ビットWindowsポータブル版: [krita-x86-4.1.0.zip](https://download.kde.org/stable/krita/4.1.0/krita-x86-4.1.0.zip)
- [デバッグシンボル(Kritaをインストールしたフォルダに展開して使用)](https://download.kde.org/stable/krita/4.1.0/krita-x86-4.1.0-dbg.zip)

### Linux

- 64ビットLinux用AppImage版: [krita-4.1.0-x86_64.appimage](https://download.kde.org/stable/krita/4.1.0/krita-4.1.0-x86_64.appimage)

(なぜかFirefoxはテキストとして読み込もうとするようです。ダウンロードするにはリンクの右クリックから保存してください) 更新がされると、Ubuntuと派生ディストリビューションでは[Krita Lime PPA](https://launchpad.net/%7Ekritalime/+archive/ubuntu/ppa)からもKrita 4.1.0をインストールできるようになります。snapの更新については作業中です。

### OSX

- OSXディスクイメージ版: [krita-4.1.0.dmg](https://download.kde.org/stable/krita/4.1.0/krita-4.1.0.dmg)

注意: タッチドッキングパネル、gmic-qtとPythonプラグインはmacOSで利用できません。

### ソースコード

- ソースコード: [krita-4.1.0.tar.gz](https://download.kde.org/stable/krita/4.1.0/krita-4.1.0.tar.gz)

### md5sum

すべてのダウンロード向け:

- [md5sum.txt](https://download.kde.org/stable/krita/4.1.0/md5sum.txt)

### キー

Linux appimageとソースのtarボールは署名されています。パブリックキーをhttps経由で取得できます: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8) 署名は [こちら](http://download.kde.org/stable/krita/4.1.0/)です (.sigのファイルです)

## Kritaを支援してください

Kritaは自由なオープンソースのプロジェクトです。[寄付](https://krita.org/jp/support-us-jp/donations-jp/)や[トレーニングビデオやアートブックの購入](https://krita.org/jp/support-us-jp/shop-jp/)で、プロジェクトを支援することを検討してみてください！皆様の支援によって、コアチームがフルタイムでKritaの開発作業を続けることが可能になります。

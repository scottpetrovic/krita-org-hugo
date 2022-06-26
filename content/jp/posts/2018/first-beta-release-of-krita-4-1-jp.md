---
title: "Krita 4.1の最初のベータリリース"
date: "2018-06-23"
categories: 
  - "uncategorized-jp"
---

Krita 4.0のリリースから3か月が経ちました。新しい機能を含むリリースKrita4.1の最初の(そしておそらく最後)のベータ版をリリースします！このリリースには以下の大きな機能追加が含まれます:

https://www.youtube.com/watch?v=LWpjlyUlBiA

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

他にもいろいろです。Krita 4.1の新機能についての[完全なリリースノートはこちら](https://krita.org/en/krita-4-0-release-notes/)です！ただ、このベータリリース時点では、まだリリースノートは作業途中です。

## ダウンロード

### Windows

Windowsユーザーの皆さんへ：もしクラッシュする事案に遭遇した場合は、[この案内（英語）](https://docs.krita.org/en/reference_manual/dr_minw_debugger.html#dr-minw) に従いデバッグシンボルをKritaに追加してください。これによってKritaがクラッシュした原因をログから解析できるようになります。

- 64ビットWindows版: [krita-x64-4.1.0-beta.2-setup.exe](https://download.kde.org/unstable/krita/4.1.0-beta.2/krita-x64-4.1.0-beta.2-setup.exe)
- 64ビットWindowsポータブル版: [krita-x64-4.1.0-beta.2.zip](https://download.kde.org/unstable/krita/4.1.0-beta.2/krita-x64-4.1.0-beta.2.zip)
- [32ビット版向けデバッグシンボル(Kritaをインストールしたフォルダに展開して使用)](https://download.kde.org/unstable/krita/4.1.0-beta.2/krita-x64-4.1.0-beta.2-dbg.zip)

- 32ビットWindows版: [krita-4.1.0-beta.2-x86-setup.exe](https://download.kde.org/unstable/krita/4.1.0-beta.2/krita-x86-4.1.0-beta.2-setup.exe)
- 32ビットWindowsポータブル版: [krita-x86-4.1.0-beta.2.zip](https://download.kde.org/unstable/krita/4.1.0-beta.2/krita-x86-4.1.0-beta.2.zip)
- [32ビット版向けデバッグシンボル(Kritaをインストールしたフォルダに展開して使用)](https://download.kde.org/unstable/krita/4.1.0-beta.2/krita-x86-4.1.0-beta.2-dbg.zip)

### Linux

- 64ビットLinux用AppImage版: [krita-4.1.0-beta.2-x86_64.appimage](https://download.kde.org/unstable/krita/4.1.0-beta.2/krita-4.1.0-beta.2-x86_64.appimage)

(なぜかFirefoxはテキストとして読み込もうとするようです。ダウンロードするにはリンクの右クリックから保存してください) 更新がされると、Ubuntuと派生ディストリビューションでは[Krita Lime PPA](https://launchpad.net/%7Ekritalime/+archive/ubuntu/ppa)からもKrita 4.1.0-beta.2をインストールできるようになります。snapの更新については作業中です。

### OSX

- OSXディスクイメージ版: [krita-4.1.0-beta.2.dmg](https://download.kde.org/unstable/krita/4.1.0-beta.2/krita-4.1.0-beta.2.dmg)

注意: タッチドッキングパネル、gmic-qtとPythonプラグインはmacOSで利用できません。

### ソースコード

- ソースコード: [krita-4.1.0-beta.2.tar.gz](https://download.kde.org/unstable/krita/4.1.0-beta.2/krita-4.1.0-beta.2.tar.gz)

### md5sum

すべてのダウンロード向け:

- [md5sum.txt](https://download.kde.org/unstable/krita/4.1.0-beta.2/md5sum.txt)

### キー

Linux appimageとソースのtarボールは署名されています。パブリックキーをhttps経由で取得できます: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8) 署名は [こちら](http://download.kde.org/unstable/krita/4.1.0-beta.2/)です (.sigのファイルです)

## Kritaを支援してください

Kritaは自由なオープンソースのプロジェクトです。[寄付](https://krita.org/jp/support-us-jp/donations-jp/)や[トレーニングビデオやアートブックの購入](https://krita.org/jp/support-us-jp/shop-jp/)で、プロジェクトを支援することを検討してみてください！皆様の支援によって、コアチームがフルタイムでKritaの開発作業を続けることが可能になります。

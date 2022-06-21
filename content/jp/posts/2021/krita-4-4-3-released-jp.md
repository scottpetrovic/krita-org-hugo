---
title: "Krita 4.4.3がリリースされました"
date: "2021-03-28"
categories: 
  - "news-jp"
  - "officialrelease-jp"
---

Krita 4.4.3をリリースしました。これはバグ修正のみのリリースです。2回のベータを通じて、非常に安定なリリースを目指しました。このあとはKrita 5に集中することになります！

また、これが32ビットWindowsでの最終のKritaリリースになります。これからは64ビット版のみリリースします。

macOSでの初のユニバーサルバイナリリリースになります。DMGにARMビルドとX64ビルドの両方が含まれています。ただ、macOS版のKritaの一番の問題であるOpenGLフレーム再描画が入力キューに割り込むという問題は、どちらのアーキテクチャにおいても依然として起こります。

## 修正されたバグ

### Android

- スプラッシュスクリーンでバックボタンを押したときのクラッシュ
- アプリケーション起動中にファイルを読み込ませた場合のクラッシュ
- アセットコピーにlastUpdateTimeを使用
- pathPatternが有効になるようにホストを提供
- 画面全体をカバーする色選択を修正[BUG:432459](https://bugs.kde.org/show_bug.cgi?id=432459))
- 保存したコンフィグが再起動後に読み込まれない問題 ([BUG:432433](https://bugs.kde.org/show_bug.cgi?id=432433))
- psd\_layer\_effects\_shadow\_baseにキー関数を追加 ([BUG:432904](https://bugs.kde.org/show_bug.cgi?id=432904))
- ユーザーがインポートしたバンドルからのプリセットリロードを修正 ([BUG:432488](https://bugs.kde.org/show_bug.cgi?id=432488))

### クラッシュ

- 不正なポインタにアクセスして起きていたハーフトーンフィルタのクラッシュを修正
- プロンプトを再表示してフィルタを再適用する際のクラッシュを修正
- ベクター選択から作られたフィルタマスクでペイントする際のクラッシュを修正([BUG:432329](https://bugs.kde.org/show_bug.cgi?id=432329))

### MacOS

- MacOS: サムネイル表示やクイックルックプレビューを行うFinderプラグインを修正 ([BUG:432328](https://bugs.kde.org/show_bug.cgi?id=432328))

### スクリプティング

- チャンネルフラグの扱いを修正Chris Venterさんのパッチです、ありがとうございます！([BUG:432226](https://bugs.kde.org/show_bug.cgi?id=432226))

### 安定性とパフォーマンス

- キャンバスとスクラッチパッドのズームレベル同期を修正
- スマートパッチツールの正規化を修正 ([BUG:430953](https://bugs.kde.org/show_bug.cgi?id=430953))
- 前景/背景色ボタンのパフォーマンス問題を修正([BUG:432936](https://bugs.kde.org/show_bug.cgi?id=432936))
- インクリメンタルバックアップ保存を修正([BUG:432701](https://bugs.kde.org/show_bug.cgi?id=432701))
- スクラッチパッドが反応しなくなる問題を修正([BUG:431708](https://bugs.kde.org/show_bug.cgi?id=431708))
- カスタムブラシ、クリップボードブラシでの色をアルファに、アルファ保護を修正([BUG:432274](https://bugs.kde.org/show_bug.cgi?id=432274))
- RGBA\_brushesバンドルを修正し、Kritaが起動時に再生成を試みることがなくなりました [(BUG:431832](https://bugs.kde.org/show_bug.cgi?id=431832))
- KisAngleSelectorのスタイルの扱いを修正。スピンボックスがフラット表示に、新しい角度選択がどこでも使用されるようになりました。

## ダウンロード

### Windows

ポータブルZipファイルを使う場合は、Zipファイルをエクスプローラーで開いてフォルダを適当な場所に移動して展開し、フォルダ内のKritaアイコンをダブルクリックして起動してください。インストール済みのKritaには影響はありませんが、設定とカスタムリソースは通常のインストール済みのKritaと共有されることに気を付けてください。. クラッシュの報告をするには、デバッグシンボルフォルダもインストールしてください。

- 64ビットWindowsインストーラー: [krita-x64-4.4.3-setup.exe](https://download.kde.org/stable/krita/4.4.3/krita-x64-4.4.3-setup.exe)
- 64ビットWindowsポータブル版: [krita-x64-4.4.3.zip](https://download.kde.org/stable/krita/4.4.3/krita-x64-4.4.3.zip)
- [デバッグシンボル(Kritaをインストールしたフォルダに展開して使用)](https://download.kde.org/stable/krita/4.4.3/krita-x64-4.4.3-dbg.zip)

- 32ビットWindowsインストーラー: [krita-x86-4.4.3-setup.exe](https://download.kde.org/stable/krita/4.4.3/krita-x86-4.4.3-setup.exe)
- 32ビットWindowsポータブル版: [krita-x86-4.4.3.zip](https://download.kde.org/stable/krita/4.4.3/krita-x86-4.4.3.zip)
- [デバッグシンボル(Kritaをインストールしたフォルダに展開して使用)](https://download.kde.org/stable/krita/4.4.3/krita-x86-4.4.3-dbg.zip)

### Linux

- 64ビットLinux版: [krita-4.4.3-x86\_64.appimage](https://download.kde.org/stable/krita/4.4.3/krita-4.4.3-x86_64.appimage)
- 64ビットLinux [G'Mic-Qt plugin appimage](https://download.kde.org/stable/krita/4.4.3/gmic_krita_qt-x86_64.appimage)

(もしFirefoがはテキストとして読み込もうとした場合:ダウンロードするにはリンクの右クリックから保存してください)

### OSX

- OSXディスクイメージ版: [krita-4.4.3.dmg](https://download.kde.org/stable/krita/4.4.3/krita-4.4.3.dmg)

注意: gmic-qtはOSXで利用できません。

### Android

今回はAndroidリリースはリリースtarballから作成されたので翻訳も含まれています。ChromeOS版とAndroid版のKritaはまだ **_ベータ_**状態と考えています。動かない部分も多数あり、キーボードがなければ操作できないものもあります。[Google Play](https://play.google.com/store/apps/details?id=org.krita)からのKrita 4.4.3の入手も可能です。

- [64 ビット Intel CPU APK](https://download.kde.org/stable/krita/4.4.3/krita_x86_64_apk-release.apk)
- [32 ビット Intel CPU APK](https://download.kde.org/stable/krita/4.4.3/krita_x86_apk-release.apk)
- [64 ビット Arm CPU APK](https://download.kde.org/stable/krita/4.4.3/krita_arm64-v8a_apk-release.apk)
- [32 ビット Arm CPU APK](https://download.kde.org/stable/krita/4.4.3/krita_armeabi-v7a_apk-release.apk)

### ソースコード

- [krita-4.4.3.tar.gz](https://download.kde.org/stable/krita/4.4.3/krita-4.4.3.tar.gz)
- [krita-4.4.3.tar.xz](https://download.kde.org/stable/krita/4.4.3/krita-4.4.3.tar.xz)

### md5sum

すべてのダウンロード向け:

- [md5sum.txt](https://download.kde.org/stable/krita/4.4.3/md5sum.txt)

### キー

Linux appimageとソースの.tar.gzと.tar.xzのtarballsは署名されています。パブリックキーはgpg経由で取得できます: "gpg --recv-key 7468332F". 署名は <a1>こちら</a1>です (.sigのファイルです)

## Kritaを支援してください

Kritaは自由なオープンソースのプロジェクトです。[寄付](https://krita.org/jp/support-us-jp/donations-jp/)や[トレーニングビデオの購入](https://krita.org/jp/support-us-jp/shop-jp/)で、プロジェクトを支援することを検討してみてください！皆様の支援によって、コアチームがフルタイムでKritaの開発作業を続けることが可能になります。

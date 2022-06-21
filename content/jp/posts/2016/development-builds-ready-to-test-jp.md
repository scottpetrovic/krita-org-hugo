---
title: "開発版がテスト可能になりました"
date: "2016-04-29"
categories: 
  - "uncategorized-jp"
tags: 
  - "japanese"
---

さて…昨日、Dmitryがドッキングパネルとポップアップ、キャンバスの操作性を妨げていた昔からあるバグの修正を試みました：時々倍率がおかしくなり、ドッキングパネルで数値を入力しようとしたり、カーソルが画像上にないときに拡大縮小しようとするとおかしくなってしまうというものです。ええっと…今回の開発版はその修正で、_テスト_が必要です。この修正をKrita 3.0に統合できるようになる前には本当にテストが必要なのです。ですので、Windows、Linux、OSXのビルドを用意しました。ダウンロードして試してみて我々を助けてください。この開発版では他にも十数個の修正が行われていますが、それらに関しては考えなくても大丈夫です。テストを、描画や変形、ブラシの切り替え、色の設定を1時間ほど試してみてください！この開発版のダウンロードと試用でKrita 2.9の設定に影響が出ることはありません。

### ダウンロード

**Windows:** ZIPファイルを解凍してbinフォルダの中にあるkrita.exeを実行してください！

- ZIP版: [Windows 64ビット版ベータ1 (zip版)](http://files.kde.org/krita/3/windows/devbuilds/krita-3.0-Beta-master-4a58260-x64.zip)
- ZIP版: [Windows 32ビット版ベータ1 (zip版)](http://files.kde.org/krita/3/windows/devbuilds/krita-3.0-Beta-master-4a58260-x86.zip)

**OSXディスクイメージ版**にはまだOpenGLを有効にするとブラシ輪郭を表示するカーソル、基準線その他が見えなくなる既存の問題が残っています。現在我々はその問題を解決すべく作業中ですが、3.0リリースまでにキャンバスのコードの書き換えは間に合わないと思われます。

- ディスクイメージ版: [OSX版ベータ1](http://files.kde.org/krita/3/osx/devbuilds/krita3-beta1-75295e0.dmg)

**Linux appimage:**ダウンロードした後、実行可能にして起動してください。インストールは必要ありません。CentOS 6とUbuntu 12.04にはG'Micがないappimage版を配布します：最新版のG'Micをそれらのディストリビューションで動くようにビルドすることはもう不可能になっています。

- AppImage版: [Linux AppImage版ベータ1](http://files.kde.org/krita/3/linux/devbuilds/krita-3.0-Beta-master-no_gmic-4336582-x86_64.appimage) (新しいディストリビューション向け)
- AppImage版: [Linux AppImage版ベータ1](http://files.kde.org/krita/3/linux/krita3-beta1-db1ca07-x86_64.appimage) (古いディストリビューション向け)

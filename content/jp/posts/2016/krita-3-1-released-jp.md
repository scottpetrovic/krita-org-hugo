---
title: "Krita 3.1リリース！"
date: "2016-12-14"
categories: 
  - "uncategorized-jp"
tags: 
  - "japanese"
---

本日Krita teamはKrita 3.1.0をリリースしました！Krita 3.1はOSX（10.9以降）に完全対応する最初のバージョンとなります！Krita 3.1は半年に渡る懸命な開発の成果であり、多数の新機能及びパフォーマンス向上、バグ修正が加わっています。本バージョンからアニメーションをgif動画及び様々な動画フォーマットに出力する（ffmpegを使用）ことが可能になりました。プロパティをカーブエディタでトゥイーンアニメーションさせることも可能になっています。ソフトプルーフが実装され、印刷時に色味がどのように変化するかを事前に確認できるようになっています。新しい色選択が実装され、広色域で色を選択できるようになりました。また大きいキャンバスで滑らかに描画できる新しいブラシエンジンとストップベースのグラデーションエディタも実装されています。

またたくさんの修正及び改良、高速化がなされています。変更の一覧については[Krita 3.1リリースノート（英語）](https://krita.org/en/release-notes-for-krita-3-1/)を御覧ください。

[![krita_animation_3_0_2](/images/posts/2016/krita_animation_3_0_2-1024x826.gif)](/images/posts/2016/krita_animation_3_0_2.gif)

以下が今回のバージョンでの主な変更点になります：

- このバージョンからOSXに完全対応しました。OpenGLキャンバスはどこでも同じように動作するようになります。もちろんOSX固有のバグがまだ存在している可能性はあります。ですがこのバージョンからOSX及びMacOSユーザーの皆さんはKritaを心置きなく使い、もし何か問題があれば臆することなく報告を行えるようになったのです。
- Kritaはこのバージョンから[FFmpeg](https://ffmpeg.org)を使用してgif動画、mp4、mkv、oggファイルを出力できるようになりました。
- 不透明度をフレーム間で自動補完トゥイーンアニメーションさせることが可能になりました。またフレームへの色ラベルの割り振り、フィルタレイヤー、塗りつぶしレイヤー及びマスクのラスター部分のアニメーションも可能になっています。
- ツールバーの描画色・背景色の2色が表示されているボタンから新しい色選択にアクセスできるようになりました。この色選択はHDR色、つまりスクリーンのsRGB色域の外側の色に対応しています。またこの色選択にはKritaのウィンドウから色を採取する機能とパレットへのアクセス機能も追加されています。
- クイックブラシエンジンは非常に高速で実にシンプルなブラシエンジンです。
- 既存のセグメントベースのグラデーションエディタに加え、ストップベースのグラデーションエディタが実装されました
- ハーフトーンフィルタが実装されました

他にもたくさんの新機能が追加されています！

Krita 3.1での重要な新機能と修正についてはこちらの動画にまとめられています。

https://www.youtube.com/watch?v=0eHNll7lPKk

このリリースには2015年度のKickstarterで得られた寄付による開発成果及びGoogle Summer of Codeでの開発成果、ボランティアのプログラマたちによる開発成果が含まれています。知らない人もいるかもしれませんが、Kritaはオープンソースであり、機能実装やバグ修正、その他の支援に関わりたい人はだれでも歓迎しています。[我々と一緒にKritaを盛り上げていきませんか？](https://krita.org/jp/get-involved-jp/overview-jp/)

### Windows

Windowsユーザーの皆さんへ：もしクラッシュする事案に遭遇した場合は、[この案内（英語）](https://docs.krita.org/Dr._Mingw_debugger)に従いデバッグシンボルをKritaに追加してください。これによってKritaがクラッシュした原因をログから解析できるようになります。

- 32ビットWindows版：[krita-3.1.0-x86-setup.exe](http://download.kde.org/stable/krita/3.1.0/krita-3.1.0-x86-setup.exe) (MD5 Hash: ea2ea5ef14382e8b720f5bde72d82867)
- 32ビットWindows用ポータブル版：[krita-3.1.0-x86.zip](http://download.kde.org/stable/krita/3.1.0/krita-3.1.0-x86.zip) (MD5 Hash:97d0051f2574c6fa793259d8f0d871cb )
- [32ビット版向けデバッグシンボル (Kritaをインストールしたフォルダに展開して使用)](http://download.kde.org/stable/krita/3.1.0/krita-3.1.0-x86-dbg.zip) (MD5 Hash: 1a1a3cd918401746c4f409b671a5d0dc)

- 64ビットWindows版：[krita-3.1.0-x64-setup.exe](http://download.kde.org/stable/krita/3.1.0/krita-3.1.0-x64-setup.exe) (MD5 Hash: c11465f8c1234a3e62f6e64a123f3dcb)
- 64ビットWindows用ポータブル版：[krita-3.1.0-x64.zip](http://download.kde.org/stable/krita/3.1.0/krita-3.1.0-x64.zip) (MD5 Hash: e3f9b5f2aa60674cb91886e0a31cec37)
- [64ビット版向けデバッグシンボル (Kritaをインストールしたフォルダに展開して使用)](http://download.kde.org/stable/krita/3.1.0/krita_3.1.0-x64-dbg.zip) (MD5 Hash: 44d184d1534e5871dbe52f3dc2aeae7c)

### Linux

- 64ビットLinux用AppImage版：[krita-3.1.0-x86_64.appimage](http://download.kde.org/stable/krita/3.1.0/krita-3.1.0-x86_64.appimage) (MD5 Hash: 80ecd83f738d7190bae8545981df6044)

Ubuntu App Storeのベータチャンネルからスナップイメージが利用可能です。

### OSX

- OSXディスクイメージ版：[krita-3.1.0.dmg](http://download.kde.org/stable/krita/3.1.0/krita-3.1.0.dmg) (MD5 Hash: 5760c25922a17b61581c693f3dfae067)

### ソースコード

- ソースコード：[krita-3.1.0.tar.gz](http://download.kde.org/stable/krita/3.1.0/krita-3.1.0.tar.gz) (MD5 Hash: 0b4a254161632a91eeb52b9fab924778)

### 画集が出版されました！

Kritaが実際にどんなことが出来るか見てみたいなら、**[Made with Krita 2016](https://krita.org/jp/item/made-with-krita-2016-the-krita-artbook-jp/)**はどうでしょうか？これはKritaの画集としては最初のものであり、現在事前予約を受付中です！

[![Made with Krita 2016](/images/posts/2016/cover_small-217x300.png)](/images/posts/2016/cover_small.png) Made with Krita 2016

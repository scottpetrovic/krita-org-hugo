---
title: "Krita 3.1第2ベータ版が公開されました"
date: "2016-10-22"
categories: 
  - "uncategorized-jp"
tags: 
  - "japanese"
---

我々は現在も狂ったようにバグ修正を続けています…それに加え、幾つかの素晴らしい新機能についても開発を続けていますが、これは次以降のリリースで実装されることになります。ともかく、Krita 3.1第2ベータ版が公開されました！そうです、皆さんの見たとおりです。元々はこのリリースはバージョン3.0.2とする予定でしたが、今回は多数の新機能が実装されたため、大きくバージョンを上げた方がいいと判断しました。加えて、[Julian ThijssensのGoogle Summer of Code](https://codereview.qt-project.org/#/c/166202)での成果がQtプロジェクトに受け入れられた事により、我々は一つの区切りとなる非常に大きな目標へと到達しました：

次のリリースより、Kritaは正式にOSXに完全対応します。

[![krita3osx](/images/posts/2016/krita3osx-1024x793.jpg)](https://krita.org/wp-content/uploads/2016/10/krita3osx.jpg)

 

これはつまりOpenGLキャンバスが完全に働くようになり、そしてOSX固有のバグをWindowsやLinuxと同様に責任を持って修正していくということです。OSX用Krita 3.1は今までのような試験的用途ではなく、ちゃんと制作作業を行うために使用しても大丈夫になります。ですのでこのベータ版をテストして、バグや問題の発見にご協力お願いします！

もちろん、Krita 3.1にはたくさんの新機能が実装されます。大きなサイズでも軽快に描画できる新しいブラシエンジン、JouniのGoogle Summer of Codeの成果であるアニメーション機能へのトウィーンアニメーション制作機能の追加、WoltheraのGoogle Summer of Codeの成果である高深度での色選択と色選択への色管理の追加、ソフトプルーフ機能の追加、ストップベースのグラデーションエディタの追加、[ffmpeg](http://ffmpeg.org/)をベースにしたアニメーションGIF及び動画形式への出力機能、その他様々な機能が追加されます。

※このベータ版にはまだ自動塗り分けマスク/ブラシプラグインが含まれています。ですが現在のアルゴリズムが実用とするにはまだ遅すぎ、それに変わる新アルゴリズムは現在調査・実験中であるため、おそらく3.1の正式リリースからは取り除かれる予定です。現在のベータではユーザーインターフェースがどのように働くかを試してみることができますが、我々も自動塗り分けブラシ機能が実用には動作が遅すぎることを把握しており、現在この問題の修正にあたっているということは心に留めておいてください。

この第2ベータ版は最初のベータ版（3.0.1.90）より遥かに安定で実用に耐えるものとなっており、ぜひ皆さんにこのバージョンを制作作業に使ってみて、バグと問題の発見にご協力お願いします！

### Windows

- 32ビットWindows版: [krita-3.0.91-x86-setup.exe](http://download.kde.org/unstable/krita/3.0.91/krita-3.0.91-x86-setup.exe) (MD5 Hash: ead6024307112f5dd98b3c8c91547a85)
- 32ビットWindows用ポータブル版: [krita-3.0.91-x86.zip](http://download.kde.org/unstable/krita/3.0.91/krita-3.0.91-x86.zip) (MD5 Hash: 4d36a3648f55137b39c4fe9238b1b5d4)

- 64ビットWindows版: [krita-3.0.91-x64-setup.exe](http://download.kde.org/unstable/krita/3.0.91/krita-3.0.91-x64-setup.exe) (MD5 Hash: 56522b839bc04d36730518f2d42ed541)
- 64ビットWindows用ポータブル版: [krita-3.0.91-x64.zip](http://download.kde.org/unstable/krita/3.0.91/krita-3.0.91-x64.zip) (MD5 Hash: 56e88e68a6f113e77e0b58d6fc313a8c)

### Linux

- 64ビットLinux版: [krita-3.0.91-x86\_64.appimage](http://download.kde.org/unstable/krita/3.0.91/krita-3.0.91-x86_64.appimage) (MD5 Hash: 4531ee79eb67d4959b7e4ff91db25681)

またUbuntu App StoreのベータチャンネルからSnapイメージも利用可能です。

### OSX

- OSXディスクイメージ: [krita-3.0.91.dmg](http://download.kde.org/unstable/krita/3.0.91/krita-3.0.91.dmg) (MD5 Hash: 6bd801060b189af0c6efc823a3ac41f4)

### ソースコード

- ソースコード: [krita-3.0.91.tar.gz](http://download.kde.org/unstable/krita/3.0.91/krita-3.0.91.tar.gz) (MD5 Hash: 936d256c7e889485ed4722113b2f2bcd)

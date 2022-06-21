---
title: "Krita 3.1リリース候補版"
date: "2016-12-04"
categories: 
  - "uncategorized-jp"
---

病気のため、一週間予定より遅れてしまいましたが、Krita3.1の最初のリリース候補版を公開できることを嬉しく思います。重要なバグ修正が複数含まれ、最終リリースまでにさらにバグ修正を行う予定です。

- ベクターレイヤーを含むドキュメントをKritaネイティブフォーマット以外で保存しようとした場合のクラッシュの修正 (beta 3でのリグレッション)
- Linuxでのコマンドラインによる画像エクスポートの修正
- OSX QuickLookプラグインが正しいサムネイルサイズを使用するように修正
- ズームメニューアイコンの改良
- すべてのSVGアイコンの色を統一
- 傾き-高度ブラシが回転もしくはミラー表示のキャンバスでも正しく機能するように修正
- スタビライザ（安定化ペン補正）を有効にした時の描画を向上
- ミラーしたキャンパスでの位置スペーシングの修正
- 保存時の競合状態を修正
- マルチウィンドウの使用を修正。ツールオプションパレットが最後に開いたウィンドウだけに用意されていたのと、すべてのウィンドウに追加
- 複数のメモリリークを修正
- アニメーションレンダリングの保存場所選択の修正(まだ残っているバグがありますが作業中です)
- ポップアップカラーセレクタの描画速度の向上

Krita 3.1の新機能については[リリースノート](https://krita.org/en/release-notes-for-krita-3-1)でさらに知ることができます。リリースノートはまだ作業中ですが、それでも機能のスニークピークは可能です！

### Windows

Windowsユーザ向けのお知らせ: クラッシュに遭遇した場合は、[こちらの手順](https://docs.krita.org/Dr._Mingw_debugger) に従ってデバッグシンボルを使い、Kritaがどこでクラッシュしているかを突き止められるようにしてください。

- 32ビットWindows版: [krita-3.0.94-x86-setup.exe](http://download.kde.org/unstable/krita/3.0.94/krita-3.0.94-x86-setup.exe) (MD5 Hash: 1fa424258d455f92aac071c47d820095)
- 32ビットWindows用ポータブル版: [krita\_3.0.94-x86.zip](http://download.kde.org/unstable/krita/3.0.94/krita_3.0.94-x86.zip) (MD5 Hash: fa00cc3575a56083916885626ff97d88)
- [32ビット版向けデバッグシンボル (Kritaをインストールしたフォルダに展開して使用)](http://download.kde.org/unstable/krita/3.0.94/krita-3.0.94-x86-dbg.zip) (MD5 Hash: 538fefc19ca79cec36346a2b2564162e)

- 64ビットWindows版: [krita-3.0.94-x64-setup.exe](http://download.kde.org/unstable/krita/3.0.94/krita-3.0.94-x64-setup.exe) (MD5 Hash: 908f52aee5deee6971783ce3c019e93e)
- 64ビットWindows用ポータブル版: [krita\_3.0.94-x64.zip](http://download.kde.org/unstable/krita/3.0.94/krita_3.0.94-x64.zip) (MD5 Hash: 4af2829289476d172032a68d26e55789)
- [64ビット版向けデバッグシンボル (Kritaをインストールしたフォルダに展開して使用)](http://download.kde.org/unstable/krita/3.0.94/krita_3.0.94-x64-dbg.zip) (MD5 Hash: ee90e2c3e679a74d9fe77eec305f84f4)

### Linux

- 64ビットLinux版: [krita-3.0.94-x86\_64.appimage](http://download.kde.org/unstable/krita/3.0.94/krita-3.0.94-x86_64.appimage) (MD5 Hash: e48aa1a805fbb631ab7d908d41c3ab84)

またUbuntu App Storeのベータチャンネルからsnap imageも利用可能です。

### OSX

- OSX ディスクイメージ: [krita-3.0.94.dmg](http://download.kde.org/unstable/krita/3.0.94/krita-3.0.94.dmg) (MD5 Hash: c8fc18364587481d346009f3921a9142)

### ソースコード

- ソースコード: [krita-3.0.94.tar.gz](http://download.kde.org/unstable/krita/3.0.94/krita-3.0.94.tar.gz) (MD5 Hash: a8822566df7743405b37b72f22a1db53)

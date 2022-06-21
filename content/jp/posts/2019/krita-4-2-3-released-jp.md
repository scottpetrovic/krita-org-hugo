---
title: "Krita 4.2.3リリース"
date: "2019-07-17"
categories: 
  - "officialrelease-jp"
---

Krita 4.2.3をリリースしました。これはほぼバグ修正のみのリリースですが、1つ新機能があります。二本指のタッチジェスチャでキャンバスを回転できるようになりました。この機能は 2019 Google Summer of CodeでKritaのAndroid移植に取り組んでいるSharaf Zamanによって開発されたものです。もちろん、Android以外のプラットフォームでも機能します。

バグ修正の中で最重要だったものは、グラフィックドライバが壊れていたり古かったり十分でないWindows向けの回避策です。この問題の中核は、開発の基盤となっているQtにあります。現在のバージョンのQtは、ユーザインタフェース技術のQMLで一つでもコンポーネントを作成するとその時点で機能しているOpenGLかDirect3Dインストールがあることを要求してしまいます。この問題の回避に成功しました。特に少しガタが来たWindows7システムを使用しているユーザも再びKritaを起動できるようになったはずです。

## 修正されたバグ

- Make it possible for Krita to use a software renderer on Windows ([BUG:408872](https://bugs.kde.org/show_bug.cgi?id=408872))
- Fix the caption of the Background Color color selection dialog ([BUG:407658](https://bugs.kde.org/show_bug.cgi?id=407658))
- Fix the tag selector combobox so it is possible to select resources that have a tag that's longer than fits in the combobox ([BUG:408053](https://bugs.kde.org/show_bug.cgi?id=408053))
- Make it possible for the Krita startup window to become as narrow as before adding the news widget ([BUG:408504](https://bugs.kde.org/show_bug.cgi?id=408504))
- Fix copy/pasting of animation frames ([BUG:408421](https://bugs.kde.org/show_bug.cgi?id=408421), [BUG:404595](https://bugs.kde.org/show_bug.cgi?id=404595))
- Make the polygon and outline selection tool handle the control modifier correctly ([BUG:376007](https://bugs.kde.org/show_bug.cgi?id=376007))
- Add a reload script button to the Python scripter plugin
- Fix a crash in the Overview docker when there is no image open
- Fix drag and drop of fill layers between opened files ([BUG:408019](https://bugs.kde.org/show_bug.cgi?id=408019))
- Fix loading EXR files that have more than one layer with the same name ([BUG:409552](https://bugs.kde.org/show_bug.cgi?id=409552))
- Hide vanishing points preview lines when assistants are hidden ([BUG:396158](https://bugs.kde.org/show_bug.cgi?id=396158))
- Fix the Mirror All Layers Horizontally function
- Fix switching profile to default when changing channel depth in the New Image dialog ([BUG:406700](https://bugs.kde.org/show_bug.cgi?id=406700))
- Disable AVG optimizations for some 32 bit blending modes ([BUG:404133](https://bugs.kde.org/show_bug.cgi?id=404133))
- Fix a crash when pressing cancel when trying to create an 8 bit/channel linear gamma RGB image
- Fix colors drifting when using the native macOS color selection dialog ([BUG:407880](https://bugs.kde.org/show_bug.cgi?id=407880))
- Make sure Stroke Selection paint correctly with the selection border in the middle of the selection ([BUG:409254](https://bugs.kde.org/show_bug.cgi?id=409254))
- Fix saving Krita when perspective assistants are present ([BUG:409249](https://bugs.kde.org/show_bug.cgi?id=409249))
- Fix issues with transformations being pixelated ([BUG:409280](https://bugs.kde.org/show_bug.cgi?id=409280))
- Make it possible to hide all layers except the selected one with shift-click ([BUG:376086](https://bugs.kde.org/show_bug.cgi?id=376086))
- Fix cloning keyframe channels that are not opacity channels
- Fix a hang when trying to paint while playing an animation of an empty image ([BUG:408749](https://bugs.kde.org/show_bug.cgi?id=408749))
- Fix Isolated Mode when multiple windows are open ([BUG:408150](https://bugs.kde.org/show_bug.cgi?id=408150))
- Make the gradient editor show the right editor for stop and segmented gradients (but creating new gradients in Krita is still broken)
- Make Krita use the integrated GPU on dual-GPU Apple computers
- Fix a freeze when pressing delete when making a polygonal selection ([BUG:408843](https://bugs.kde.org/show_bug.cgi?id=408843))
- Fix the --export commandline option to return 0 when the export is successful ([BUG:409133](https://bugs.kde.org/show_bug.cgi?id=409133))
- Fix support for the KDE Plasma global menu ([BUG:408015](https://bugs.kde.org/show_bug.cgi?id=408015))
- Fix a crash when using the shrink option of the deform brush ([BUG:408887](https://bugs.kde.org/show_bug.cgi?id=408887))

## ダウンロード

### Windows

Windowsユーザーの皆さんへ：もしクラッシュする事案に遭遇した場合は、[この案内（英語）](https://docs.krita.org/en/reference_manual/dr_minw_debugger.html#dr-minw) に従いデバッグシンボルをKritaに追加してください。これによってKritaがクラッシュした原因をログから解析できるようになります。

- 64 bits Windows: [krita-x64-4.2.3-setup.exe](https://download.kde.org/stable/krita/4.2.3/krita-x64-4.2.3-setup.exe)
- Portable 64 bits Windows: [krita-x64-4.2.3.zip](https://download.kde.org/stable/krita/4.2.3/krita-x64-4.2.3.zip)
- [デバッグシンボル(Kritaをインストールしたフォルダに展開して使用)](https://download.kde.org/stable/krita/4.2.3/krita-x64-4.2.3-dbg.zip)

- 32 bits Windows: [krita-x86-4.2.3-setup.exe](https://download.kde.org/stable/krita/4.2.3/krita-x86-4.2.3-setup.exe)
- Portable 32 bits Windows: [krita-x86-4.2.3.zip](https://download.kde.org/stable/krita/4.2.3/krita-x86-4.2.3.zip)
- [デバッグシンボル(Kritaをインストールしたフォルダに展開して使用)](https://download.kde.org/stable/krita/4.2.3/krita-x86-4.2.3-dbg.zip)

### Linux

- 64 bits Linux: [krita-4.2.3-x86\_64.appimage](https://download.kde.org/stable/krita/4.2.3/krita-4.2.3-x86_64.appimage)
- 64ビットLinux [G'Mic-Qt plugin appimage](https://download.kde.org/stable/krita/4.2.3/gmic_krita_qt-x86_64.appimage)

(なぜかFirefoxはテキストとして読み込もうとするようです。ダウンロードするにはリンクの右クリックから保存してください)

### OSX

- OSX disk image: [krita-4.2.3.dmg](https://download.kde.org/stable/krita/4.2.3/krita-4.2.3.dmg)

注意: gmic-qtはOSXで利用できません。

### ソースコード

- [krita-4.2.3.tar.gz](https://download.kde.org/stable/krita/4.2.3/krita-4.2.3.tar.gz)
- [krita-4.2.3.tar.xz](https://download.kde.org/stable/krita/4.2.3/krita-4.2.3.tar.xz)

### md5sum

すべてのダウンロード向け:

- [md5sum.txt](https://download.kde.org/stable/krita/4.2.3/md5sum.txt)

### キー

The Linux appimage and the source .tar.gz tarball are signed. パブリックキーをhttps経由で取得できます: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8) 署名は [こちら](http://download.kde.org/unstable/krita/4.2.0-beta2/)です (.sigのファイルです)

## Kritaを支援してください

Kritaは自由なオープンソースのプロジェクトです。[寄付](https://krita.org/jp/support-us-jp/donations-jp/)や[トレーニングビデオやアートブックの購入](https://krita.org/jp/support-us-jp/shop-jp/)で、プロジェクトを支援することを検討してみてください！皆様の支援によって、コアチームがフルタイムでKritaの開発作業を続けることが可能になります。

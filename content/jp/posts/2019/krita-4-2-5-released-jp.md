---
title: "Krita 4.2.5リリース"
date: "2019-08-05"
categories: 
  - "officialrelease-jp"
---

Krita 4.2.4には特定のツールがアクティブな場合においてショートカットの処理のバグが残っていることが判明しました。できる限り早くそのバグを修正するよう作業しました。その結果のKrita 4.2.5をリリースします。この新しいリリースへの更新を強く推奨します。

## 修正されたバグ

- Fix an assert in the transform tool when working with a tablet and touch
- Fix continued transformation in the transform tool
- Fix updates in the transform tool
- Show the publication time in the welcome page news ticker in the user's preferred short date/time format
- Fix using the tangent-normal brush when the canvas is rotated or mirrored ([BUG:404408](https://bugs.kde.org/show_bug.cgi?id=404408))
- Make it possible again to create new palettes and save them in the resource folder, instead of the current document ([BUG:410137](https://bugs.kde.org/show_bug.cgi?id=410137))
- Make Krita not gobble up all available memory when loading a JPG file with specific metadata ([BUG:410242](https://bugs.kde.org/show_bug.cgi?id=410242))
- Constrain assistant editors to the viewport, so they can always be manipulated
- Make sure Krita stores changes to brush presets in the current session by default ([BUG:410463](https://bugs.kde.org/show_bug.cgi?id=410463))
- Remove an assert that could be triggered when opening the first image in a session
- Update the version of the default input settings profile, so the rotate/zoom action will be activated even if the user already had a local kritadefault.profile file
- Fix a crash on using the move tool while the image is being opened ([BUG:398968](https://bugs.kde.org/show_bug.cgi?id=398968))
- Make sure the painting tools don't block anymore (BUG:409968,408826,409275)
- Make the shortcut handling system more tolerant when shortcuts overlap ([BUG:409968](https://bugs.kde.org/show_bug.cgi?id=409968))
- Fix a crash in the transform tool
- Make the transform tool and the move tool more responsive

## ダウンロード

### Windows

Windowsユーザーの皆さんへ：もしクラッシュする事案に遭遇した場合は、[この案内（英語）](https://docs.krita.org/en/reference_manual/dr_minw_debugger.html#dr-minw) に従いデバッグシンボルをKritaに追加してください。これによってKritaがクラッシュした原因をログから解析できるようになります。

- 64 bits Windows: [krita-x64-4.2.5-setup.exe](https://download.kde.org/stable/krita/4.2.5/krita-x64-4.2.5-setup.exe)
- Portable 64 bits Windows: [krita-x64-4.2.5.zip](https://download.kde.org/stable/krita/4.2.5/krita-x64-4.2.5.zip)
- [デバッグシンボル(Kritaをインストールしたフォルダに展開して使用)](https://download.kde.org/stable/krita/4.2.5/krita-x64-4.2.5-dbg.zip)

- 32 bits Windows: [krita-x86-4.2.5-setup.exe](https://download.kde.org/stable/krita/4.2.5/krita-x86-4.2.5-setup.exe)
- Portable 32 bits Windows: [krita-x86-4.2.5.zip](https://download.kde.org/stable/krita/4.2.5/krita-x86-4.2.5.zip)
- [デバッグシンボル(Kritaをインストールしたフォルダに展開して使用)](https://download.kde.org/stable/krita/4.2.5/krita-x86-4.2.5-dbg.zip)

### Linux

- 64 bits Linux: [krita-4.2.5-x86\_64.appimage](https://download.kde.org/stable/krita/4.2.5/krita-4.2.5-x86_64.appimage)
- 64ビットLinux [G'Mic-Qt plugin appimage](https://download.kde.org/stable/krita/4.2.5/gmic_krita_qt-x86_64.appimage)

(なぜかFirefoxはテキストとして読み込もうとするようです。ダウンロードするにはリンクの右クリックから保存してください)

### OSX

- OSX disk image: [krita-4.2.5.dmg](https://download.kde.org/stable/krita/4.2.5/krita-4.2.5.dmg)

注意: gmic-qtはOSXで利用できません。

### ソースコード

- [krita-4.2.5.tar.gz](https://download.kde.org/stable/krita/4.2.5/krita-4.2.5.tar.gz)
- [krita-4.2.5.tar.xz](https://download.kde.org/stable/krita/4.2.5/krita-4.2.5.tar.xz)

### md5sum

すべてのダウンロード向け:

- [md5sum.txt](https://download.kde.org/stable/krita/4.2.5/md5sum.txt)

### キー

Linux appimageとソースの.tar.gz tarballは署名されています。パブリックキーをhttps経由で取得できます: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8) 署名は [こちら](http://download.kde.org/unstable/krita/4.2.0-beta2/)です (.sigのファイルです)

## Kritaを支援してください

Kritaは自由なオープンソースのプロジェクトです。[寄付](https://krita.org/jp/support-us-jp/donations-jp/)や[トレーニングビデオやアートブックの購入](https://krita.org/jp/support-us-jp/shop-jp/)で、プロジェクトを支援することを検討してみてください！皆様の支援によって、コアチームがフルタイムでKritaの開発作業を続けることが可能になります。

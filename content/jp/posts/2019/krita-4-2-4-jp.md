---
title: "Krita 4.2.4"
date: "2019-08-02"
categories: 
  - "officialrelease-jp"
---

Krita 4.2.4をリリースしました。最も重要な修正はショートカット入力システムと保存システムの修正です。Krita 4.2.3には、ショートカットが正しく完了しなかったというメッセージが出るバグがありました。これはもう起こりません。Anna Medonosovaが保存システムをさらに堅牢にしました。特に保存操作を始めてからKritaを閉じるケースに対応しています。

他にも修正作業中で約2週間後Kritaスプリントの後に4.2.5をリリースする予定です。

さらに

## 既知の問題

タッチによるズームと回転が動かなくなってしまったら、あなたのローカルPCのdefault.inputrcを削除してください。設定/リソースを管理に、リソースフォルダを開くボタンがあります。inputフォルダを開いて、そのフォルダのファイルをすべて削除してください。

新機能は、Painttool SaiにインスパイアされたLuminosity合成モードです。([BUG:409627](https://bugs.kde.org/show_bug.cgi?id=409627))

## 修正されたバグ

- Make it possible to use dots in filenames (note that that still might confuse your OS) ([BUG:409765](https://bugs.kde.org/show_bug.cgi?id=409765))
- Fix regression on softness sensor on Default Circle autobrush tip ([BUG:409758](https://bugs.kde.org/show_bug.cgi?id=409758))
- Clear any leftover points in the line tool on each use so there are no false starts ([BUG:408439](https://bugs.kde.org/show_bug.cgi?id=408439))
- Do not reset the opacity to zero when moving more than one shape at a time ([BUG:409131](https://bugs.kde.org/show_bug.cgi?id=409131))
- Do not ignore rotation in the bristle brush engine ([BUG:384231](https://bugs.kde.org/show_bug.cgi?id=384231))
- Fix cursor drift when using pan/zoom/rotate ([BUG:409460](https://bugs.kde.org/show_bug.cgi?id=409460))
- Fix a crash when creating an RGB image after the last used color model was CMYK ([BUG:409916](https://bugs.kde.org/show_bug.cgi?id=409916))
- Use Qt's QImageIO image import/export filter for PPM files instead of our own, broken implementation. ([BUG:409714](https://bugs.kde.org/show_bug.cgi?id=409714))
- Fix updating the brush size in the toolbar using shortcuts or drag ([BUG:408331](https://bugs.kde.org/show_bug.cgi?id=408331))
- Make generated gradient names translatable ([BUG:410034](https://bugs.kde.org/show_bug.cgi?id=410034))
- Fix a crash that could happen when closing Krita after deleting a session ([BUG:409909](https://bugs.kde.org/show_bug.cgi?id=409909))
- Fix a bug in the color picker that made it possible for the active foreground color to be transparent
- Fix a logic error in the Separate Image plugin ([BUG:410308](https://bugs.kde.org/show_bug.cgi?id=410308))
- Update the notes for the LargeRGB color profile ([BUG:410023](https://bugs.kde.org/show_bug.cgi?id=410023))
- Fix the filename reference for Rec.709 profiles
- Add a workaround for the KisShortcutsMatcher assert ([BUG:408826](https://bugs.kde.org/show_bug.cgi?id=408826))

## ダウンロード

### Windows

Windowsユーザーの皆さんへ：もしクラッシュする事案に遭遇した場合は、[この案内（英語）](https://docs.krita.org/en/reference_manual/dr_minw_debugger.html#dr-minw) に従いデバッグシンボルをKritaに追加してください。これによってKritaがクラッシュした原因をログから解析できるようになります。

- 64 bits Windows: [krita-x64-4.2.4-setup.exe](https://download.kde.org/stable/krita/4.2.4/krita-x64-4.2.4-setup.exe)
- Portable 64 bits Windows: [krita-x64-4.2.4.zip](https://download.kde.org/stable/krita/4.2.4/krita-x64-4.2.4.zip)
- [デバッグシンボル(Kritaをインストールしたフォルダに展開して使用)](https://download.kde.org/stable/krita/4.2.4/krita-x64-4.2.4-dbg.zip)

- 32 bits Windows: [krita-x86-4.2.4-setup.exe](https://download.kde.org/stable/krita/4.2.4/krita-x86-4.2.4-setup.exe)
- Portable 32 bits Windows: [krita-x86-4.2.4.zip](https://download.kde.org/stable/krita/4.2.4/krita-x86-4.2.4.zip)
- [デバッグシンボル(Kritaをインストールしたフォルダに展開して使用)](https://download.kde.org/stable/krita/4.2.4/krita-x86-4.2.4-dbg.zip)

### Linux

- 64 bits Linux: [krita-4.2.4-x86\_64.appimage](https://download.kde.org/stable/krita/4.2.4/krita-4.2.4-x86_64.appimage)
- 64ビットLinux [G'Mic-Qt plugin appimage](https://download.kde.org/stable/krita/4.2.4/gmic_krita_qt-x86_64.appimage)

(なぜかFirefoxはテキストとして読み込もうとするようです。ダウンロードするにはリンクの右クリックから保存してください)

### OSX

- OSX disk image: [krita-4.2.4.dmg](https://download.kde.org/stable/krita/4.2.4/krita-4.2.4.dmg)

注意: gmic-qtはOSXで利用できません。

### ソースコード

- [krita-4.2.4.tar.gz](https://download.kde.org/stable/krita/4.2.4/krita-4.2.4.tar.gz)
- [krita-4.2.4.tar.xz](https://download.kde.org/stable/krita/4.2.4/krita-4.2.4.tar.xz)

### md5sum

すべてのダウンロード向け:

- [md5sum.txt](https://download.kde.org/stable/krita/4.2.4/md5sum.txt)

### キー

Linux appimageと.tar.gz tarballは署名されています。パブリックキーをhttps経由で取得できます: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8) 署名は [こちら](http://download.kde.org/unstable/krita/4.2.0-beta2/)です (.sigのファイルです)

## Kritaを支援してください

Kritaは自由・無料でオープンソースのプロジェクトです。 [寄付](https://krita.org/jp/support-us-jp/donations-jp/)や[トレーニングビデオやアートブックの購入](https://krita.org/jp/support-us-jp/shop-jp/)で、プロジェクトを支援することを検討してみてください！皆様の支援によって、コアチームがフルタイムでKritaの開発作業を続けることが可能になります。

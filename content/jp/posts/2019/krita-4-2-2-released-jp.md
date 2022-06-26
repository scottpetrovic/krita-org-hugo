---
title: "Krita 4.2.2 リリース"
date: "2019-06-30"
categories: 
  - "officialrelease-jp"
---

Krita 4.2.1が今月出たばかりですが、Krita 4.2.2をリリースします。これもバグ修正リリースです。新機能も含むKrita 4.3のリリース時期まで、毎月Krita 4.2のバグ修正リリースを出そうと考えています。修正されたバグのリストはこちらです。

- Text editor: make sure the background color is the one set in the settings ([BUG:408344](https://bugs.kde.org/show_bug.cgi?id=408344))
- Fix a crash when creating a text shape ([BUG:407554](https://bugs.kde.org/show_bug.cgi?id=407554))
- Make sure the text style is not reset when removing the last character in the text editor ([BUG:408441](https://bugs.kde.org/show_bug.cgi?id=408441))
- Fix an issue on macOS where some libraries could not be loaded (BUG:408343)
- Use a highlighted tool button in the selection tool option dockers so it's easier to see which selection action is active
- Fix the nearest neighbour transform algorithm ([BUG:408182](https://bugs.kde.org/show_bug.cgi?id=408182))
- Fix a styling issue in the filter layers properties dialog ([BUG:408171](https://bugs.kde.org/show_bug.cgi?id=408171))
- Fix an issue where if Krita was set to use a language other than English, vector strokes were drawn wrongly
- Fix selecting colors from the combobox in the palette docker
- Fix a crash when loading a broken KPL file ([BUG:408447](https://bugs.kde.org/show_bug.cgi?id=408447))
- Fix an issue where a transparent pattern fill loader was loaded incorrectly ([BUG:408169](https://bugs.kde.org/show_bug.cgi?id=408169))
- Make it possible to make the onion skin docker smaller ([BUG:407646](https://bugs.kde.org/show_bug.cgi?id=407646))
- Improve loading GPL palettefiles with thousands of columns
- Fix the slider widget to make it impossible to get negative values
- Improve the tiff import/export filter ([BUG:408177](https://bugs.kde.org/show_bug.cgi?id=408177))
- Fix loading the scripter Python plugin when using a language other than English
- Improve the reference image tool and optimize loading images from clipboard
- Make the camera raw import filter honor batch mode
- Fix rendering of clone layers if the source layer is not visible ([BUG:408167](https://bugs.kde.org/show_bug.cgi?id=408167), [BUG:405536](https://bugs.kde.org/show_bug.cgi?id=405536))
- Fix move and transform tools after a quick layer duplication ([BUG:408593](https://bugs.kde.org/show_bug.cgi?id=408593))
- Fix a crash when selecting the opaque pixels on a transform mask ([BUG:408618](https://bugs.kde.org/show_bug.cgi?id=408618))
- Fix loading sRGB EXR files ([BUG:408485](https://bugs.kde.org/show_bug.cgi?id=408485))
- Make the new image dialog choose the last used option even when the user's language has changed
- Fix the "Enforce Palette Colors" feature ([BUG:408256](https://bugs.kde.org/show_bug.cgi?id=408256))
- Update the brush preview on every brush stamp creation ([BUG:389432](https://bugs.kde.org/show_bug.cgi?id=389432))
- Make it possible to edit vector shapes on duplicated vector layers ([BUG:408028](https://bugs.kde.org/show_bug.cgi?id=408028))
- Hide the color picker button in the vector object properties docker, it's unimplemented
- Fix color as mask export in GIH and GBR brush tip export ([BUG:389928](https://bugs.kde.org/show_bug.cgi?id=389928))
- Restore the default favorite blending modes
- Add a header to all right-click menus on the canvas so the first thing under the cursor isn't something dangerous, like 'cut' ([BUG:408696](https://bugs.kde.org/show_bug.cgi?id=408696))
- Fix an incorrect condition when rendering animations where Krita would complain to be out of memory
- Keep the community links in the welcome screen visible when changing theme ([BUG:408686](https://bugs.kde.org/show_bug.cgi?id=408686))
- Check after saving whether the saved file can be opened and has correct contents
- Improve the import/export error handling and reporting
- Make sure the filter dialog shows up in front of Krita's main window ([BUG:408867](https://bugs.kde.org/show_bug.cgi?id=408867))
- Make sure that the contiguous selection tool provides the antialiasing switch ([BUG:408733](https://bugs.kde.org/show_bug.cgi?id=408733))
- Fix the fuzziness setting in the contiguous selection tool
- Fix putting the text shape behind every other shape on a vector layer after editing text ([BUG:408693](https://bugs.kde.org/show_bug.cgi?id=408693))
- Fix switching the pointer type by stylus tip ([BUG:408454](https://bugs.kde.org/show_bug.cgi?id=408454), [BUG:405747](https://bugs.kde.org/show_bug.cgi?id=405747))
- Fix an issue on Linux where switching from pen to mouse would prevent the mouse from drawing on the canvas ([BUG:407595](https://bugs.kde.org/show_bug.cgi?id=407595))
- Fix a crash when the user undoes creating layers too quickly ([BUG:408484](https://bugs.kde.org/show_bug.cgi?id=408484))
- Fix using .KRA and .ORA files as file layers ([BUG:408087](https://bugs.kde.org/show_bug.cgi?id=408087))
- Clear all points in the outline selection on clicking ([BUG:408439](https://bugs.kde.org/show_bug.cgi?id=408439))
- Fix a crash when using the fill tool in fast mode on a pixel selection mask
- Fix merging layers with inactive selection masks ([BUG:402070](https://bugs.kde.org/show_bug.cgi?id=402070))
- Remove default actions from the Reference Image tool that were inappropriate ([BUG:408427](https://bugs.kde.org/show_bug.cgi?id=408427))
- Fix undo/redo not restoring the document to unmodified ([BUG:402263](https://bugs.kde.org/show_bug.cgi?id=402263))
- Fix the deform tool leaving darkish traces when scrubbing a lot on a 16 bit canvas ([BUG:290383](https://bugs.kde.org/show_bug.cgi?id=290383))
- Updated Qt to 5.12.4

**注意**: 一部のWindowsシステムで、Krita 4.2.xが起動しないことがあります。開発チームでこの問題を再現するシステムがない状態です。機能するOpenGLドライバやDirect3Dドライバがないシステムで問題が主に起きているようです。解決に向けて作業を行っています。

## ダウンロード

### Windows

Windowsユーザーの皆さんへ：もしクラッシュする事案に遭遇した場合は、[この案内（英語）](https://docs.krita.org/en/reference_manual/dr_minw_debugger.html#dr-minw) に従いデバッグシンボルをKritaに追加してください。これによってKritaがクラッシュした原因をログから解析できるようになります。

- 64ビットWindows版: [krita-x64-4.2.2-setup.exe](https://download.kde.org/stable/krita/4.2.2/krita-x64-4.2.2-setup.exe)
- 64ビットWindowsポータブル版: [krita-x64-4.2.2.zip](https://download.kde.org/stable/krita/4.2.2/krita-x64-4.2.2.zip)
- [デバッグシンボル(Kritaをインストールしたフォルダに展開して使用)](https://download.kde.org/stable/krita/4.2.2/krita-x64-4.2.2-dbg.zip)

- 32ビットWindows版: [krita-x86-4.2.2-setup.exe](https://download.kde.org/stable/krita/4.2.2/krita-x86-4.2.2-setup.exe)
- 32ビットWindowsポータブル版: [krita-x86-4.2.2.zip](https://download.kde.org/stable/krita/4.2.2/krita-x86-4.2.2.zip)
- [デバッグシンボル(Kritaをインストールしたフォルダに展開して使用)](https://download.kde.org/stable/krita/4.2.2/krita-x86-4.2.2-dbg.zip)

### Linux

- 64ビットLinux用AppImage版: [krita-4.2.2-x86_64.appimage](https://download.kde.org/stable/krita/4.2.2/krita-4.2.2-x86_64.appimage)
- 64ビットLinux [G'Mic-Qt plugin appimage](https://download.kde.org/stable/krita/4.2.2/gmic_krita_qt-x86_64.appimage)

(なぜかFirefoxはテキストとして読み込もうとするようです。ダウンロードするにはリンクの右クリックから保存してください)

### OSX

- OSXディスクイメージ版: [krita-4.2.2.3.dmg](https://download.kde.org/stable/krita/4.2.2/krita-4.2.2.3.dmg)

注意: gmic-qtはOSXで利用できません。

### ソースコード

- [krita-4.2.2.tar.gz](https://download.kde.org/stable/krita/4.2.2/krita-4.2.2.tar.gz)
- [krita-4.2.2.tar.xz](https://download.kde.org/stable/krita/4.2.2/krita-4.2.2.tar.xz)

### md5sum

すべてのダウンロード向け:

- [md5sum.txt](https://download.kde.org/stable/krita/4.2.2/md5sum.txt)

### キー

Linux appimageとソースのtarボールは署名されています。パブリックキーをhttps経由で取得できます: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8) 署名は [こちら](http://download.kde.org/unstable/krita/4.2.0-beta2/)です (.sigのファイルです)

## Kritaを支援してください

Kritaは自由なオープンソースのプロジェクトです。[寄付](https://krita.org/jp/support-us-jp/donations-jp/)や[トレーニングビデオやアートブックの購入](https://krita.org/jp/support-us-jp/shop-jp/)で、プロジェクトを支援することを検討してみてください！皆様の支援によって、コアチームがフルタイムでKritaの開発作業を続けることが可能になります。

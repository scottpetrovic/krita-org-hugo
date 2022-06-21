---
title: "Krita 3.0 ベータビルドリリース！"
date: "2016-04-27"
categories: 
  - "uncategorized-jp"
tags: 
  - "japanese"
---

最後のアルファビルドから80以上のバグ修正が行われ、20日が経過した今こそ我々はベータの段階に入るべき時だと判断しました！また、[Windowsビルド](https://jp.krita.org/item/new-krita-3-0-windows-builds/)の改善にも時間を割いています。Windows上で長らく大きな問題となっていたG'Micのクラッシュが修正されたはずです。

### 重要な修正

- G’Micが修正され、LinuxとWindowsでマルチスレッド処理のためOpenMPを使うようになりました！シングルスレッド処理だったKrita2.9のG'Micに比べて大きなパフォーマンス増加が期待されます。G'MicはおそらくまだOSXでは壊れています。そのバグを報告する必要はありません。
- マスク更新問題にも厳密な対応を行っています!
- 変形マスクと変形のバグについても同様です!
- 大きな問題となっていた保存と読み込みのバグが修正されました。Kritaで保存と読み込みのバグに遭遇した場合、直ぐに開発者に報告をお願いします!
- 変形ブラシと接線法線ブラシのクラッシュと挙動のバグを修正しました!
- 色や一貫性に関する小さなUI修正を各所で行いました。
- ショートカットに関する複数の修正。これでショートカットの保存と読み込みが正しく機能するはずです。
- アニメーションに関するタブレット修正。フレームの複製が簡単になり、使いやすくなるツールもあるはずです。
- グリッドと基準線に関する修正
- その他数多くの修正… [バグ修正リストの完全版はこちら(英語)](https://community.kde.org/Krita/Krita3dot1releasenotes#3.0_BETA_.2822nd_of_April.29)!
- LinuxとWindowsビルドでは、すべての翻訳へのアクセスが追加され、すべてのメニューが翻訳されているはずです。

これから、さらにバグ修正を行う予定です。新しいビルドをテストして、[チャットルーム](https://jp.krita.org/irc/) や [バグトラッカー](https://jp.krita.org/get-involved/report-a-bug/)にフィードバックをお願いします。テストによってこれからKrita3.0が数週間のうちにリリースされた時に問題が突然現れることを防ぐことができます。

### Kickstarter!

次のKickstarterの前に3.0がリリースできる状態にすることを目指していましたが、バグ修正にもう一か月使うことの方が重要と考えています。Kickstarterは予定通り行うつもりで、5月のKickstarterとKrita3.0の5月のリリースは同時期になる見込みです。

### 既知の問題

バグを熱心に修正していますが、まだ[既知の問題もあります。](https://bugs.kde.org/buglist.cgi?bug_severity=critical&bug_severity=grave&bug_severity=major&bug_severity=crash&bug_severity=normal&bug_severity=minor&bug_status=UNCONFIRMED&bug_status=CONFIRMED&bug_status=ASSIGNED&bug_status=REOPENED&list_id=1348442&product=krita&query_format=advanced) このベータリリースを試して、まだ報告されている問題が起こるかテストする手助けをしていただけると助かります![バグの分類](https://jp.krita.org/item/ways-to-help-krita-bug-triaging/)はコミュニティの一員となる素晴らしい協力方法です。

### ダウンロード

今回MSIインストーラは作成していません。ただ、64bit版だけではなく32bit版も用意しました。新しいビルド環境でビルド作成が速く簡単になっています。これらのビルドには、カメラRAWインポータープラグインとPDFインポートエクスポートプラグインがはじめて同梱されています。

- Zip archive: [Windows 64-bit Beta 1 (zip)](http://files.kde.org/krita/3/windows/krita-3.0-Beta-master-25ecbaf-x64.zip) (sha1: 5d45b2ec82aeedf797620a8388ab4e2c8765e376)
- Zip archive: [Windows 32-bit Beta 1 (zip)](http://files.kde.org/krita/3/windows/krita-3.0-Beta-master-301a139-x86.zip) (sha1: 35ced3a2be5eed59b4afb071fc9748669d4c4101)

デバッグ情報つきのWindowsビルドも実験的に用意しています。ダウンロードはこちらからお願いします [http://files.kde.org/krita/3/windows](http://files.kde.org/krita/3/windows).

**OSXディスクイメージ版**にはまだOpenGLを有効にするとブラシ輪郭を表示するカーソル、基準線その他が見えなくなる既存の問題が残っています。現在我々はその問題を解決すべく作業中ですが、3.0リリースまでにキャンバスのコードの書き換えは間に合わないと思われます。

- ディスクイメージ版: [OSX Beta 1](http://files.kde.org/krita/3/osx/krita3-beta1-83b444b.dmg) (sha1: 32098758addbda2971bfbf81420a9bfa70e1b981)

**The Linux appimage** は2012年以降にリリースされたあらゆるLinuxディストリビューションで動くはずです。ダウンロードした後に、AppImageを実行可能にして動かしてください。インストールの必要はありません

- AppImage [Linux AppImage Beta 1](http://files.kde.org/krita/3/linux/krita3-beta1-db1ca07-x86_64.appimage) (sha1: 4c8af3492d80c3ccc8b7ad4086815583e6231b64)

**ソースコード**:

- [krita\_2.99.90](http://download.kde.org/unstable/krita/2.99.90/)

**Gitリポジトリ:**

- [https://phabricator.kde.org/diffusion/KRITA/](https://phabricator.kde.org/diffusion/KRITA/)

---
title: "Krita 2.9.5.1リリースとバグウィークエンド！"
date: "2015-06-19"
categories: 
  - "uncategorized-jp"
tags: 
  - "japanese"
---

前回のKritaのビルドからしばらくぶりになります。新しいビルドKrita 2.9.5.1をリリースしました！目まぐるしいKickstarterキャンペーンの中、新機能、改良と修正を全力で行い、多くのコード変更がありました。そのため、2.9.5.0は、多少、小数点の.0の状態でした！2.9.5.1には以下の改良が含まれています。

### 新機能:

- カーブフィルタにコンポジットRGBカーブを実装
- 魚眼消失点描画ガイドを追加
- 同心円ガイドを追加
- 設定ダイアログの標準設定(Default)ボタンが、そのカテゴリの設定だけ初期化するように変更
- メモリ設定オプションを追加。一時スクラッチファイルの位置を指定可能に
- プロファイラオプションの追加:[https://userbase.kde.org/Krita/Manual/Preferences/Performance](https://userbase.kde.org/Krita/Manual/Preferences/Performance)(注：英語)
- 現在開いている画像のコピーの作成(要望348256)
- 一方向圧力センサーを追加(要望344753)
- ステータスバーにメモリ使用量を表示

### バグ修正:

- 解像度のtiffタグが存在する時のみ解像度を指定するように変更。JPEGファイルの.kraへの保存で問題が起きていました
- BUG:349078 フィルタレイヤーの下の画像トリミング問題の修正
- BUG:324505,294122 調整レイヤーの合成を修正
- Bug 349185 安定化をオンにした時のカーソル表示の修正
- MDIサブウィンドウを切り替えたときのフローティングメッセージ表示の修正
- BUG:348533 新しいドキュメントを作成した時にツールがオフになるバグの修正
- BUG:331708,349108 アクションのやり直し時のクラッシュを修正
- BUG:348737 センサー名の修正: fadeはspeedとは違う
- BUG:345762 どのサブウィンドウがミラー表示状態か正しく記憶するように修正
- BUG:349058 定規ガイドがオプションが最初にオンになった時のキャンバスにしか表示されないバグの修正。ミラー表示、ラップ表示モードの同様のバグも修正
- BUG:331708 ストロークをキャンセルしたあとのやり直しで起こるクラッシュを修正
- 一部の設定ファイルが設定システムで検出されない問題を修正
- BUG:299555 アクティブレイヤーがロックされているか、現在アクティブなツールで編集できない場合、カーソルを「編集禁止」に変更
- BUG:345564 Kritaの設定時に、背景画像の設定をやめたときに画像ファイルが不正であるという警告を出さないように変更
- BUG: 348886:バンドルにリソースを追加、削除するときのリストスクロールを修正
- bristleエンジンのデフォルトプリセットを修正、スケール値を1に戻しました
- レイヤープロパティダイアログでカラープロファイルが正しく表示されないwdglayerproperties.uiのバグを修正。Amadiroさんのパッチです。ありがとう！
- BUG: 348507 PDFインポートダイアログの解像度の問題を修正
- BUG:347004 フィルタープレビューボタンの状態がわかりにくい
- BUG:345754 パースガイドでのフリーズの修正
- 現在のメタデータ作成者を記憶するように修正
- BUG:348726 メタデータの「スマート」マージを注意深く行う
- BUG:348652 一時スワップファイルの正しい初期化
- OpenCanvasで保存されたPSDの読み込みを修正
- （訳注：2.9.5.0で日本語含む翻訳UI使用時にグラデーション、パターン、ワークスペース選択が空になっている問題は報告済みですが、2.9.5.1ではまだ修正されていません。BUG 349026）

**ダウンロード**

- Linux:
    - 各ディストリビューションは各ディストリビューションでのbleeding edgeレポジトリからパッケージを作成することを期待されています。
    - UbuntuとUbuntu派生ディストリビューションでは通常通りKrita Limeを使用できます:[https://launchpad.net/~dimula73/+archive/ubuntu/krita](https://launchpad.net/~dimula73/+archive/ubuntu/krita).
    - OpenSUSEユーザはKDE:Extraレポジトリ: [http://download.opensuse.org/repositories/KDE:/Extra/](http://download.opensuse.org/repositories/KDE:/Extra/) もしくはVcサポート付でビルドされたKrita(ペイントが高速化)を含むLeinir’s OBS repositoriesを使用できます:
        - [http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_13.1/](http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_13.1/)
        - [http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_13.2/](http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_13.2/)
        - [http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_Factory/](http://download.opensuse.org/repositories/home:/leinir:/calligragemini/openSUSE_Factory/)
- WindowsとOSX
    - 更新された[ダウンロードページ](https://jp.krita.org/download/krita-desktop/ "Krita Desktop")から新しいビルドがダウンロードできます。

**バグについて…**

修正はありますが2.9.5.1が完璧だということはありません…Kritaへの関心が高まるにつれて、バグ報告も増えています！現在、今までの最高記録となる315個のバグがオープン状態でベータベースに存在します！

開発チームはバグのトリアージ作業への協力を必要としています。他のバグ報告と同じ内容をまとめ、再現方法を確認し、そして不具合と機能追加要望を振り分ける、といった作業です。

この作業で現在も起こっている再現方法があるバグリストが出来上がったら、対応をしていくことになります！

Kritaでは今週末に2015バグウィークエンドを行います。参加者はKrita2.9.5.1をインストールして、バグリストを確認してトリアージ作業に協力します！

トリアージ作業が必要なバグリストは以下です:

[**Unconfirmed, reopened, need-info Krita Bugs**](https://bugs.kde.org/buglist.cgi?bug_severity=critical&bug_severity=grave&bug_severity=major&bug_severity=crash&bug_severity=normal&bug_severity=minor&query_format=advanced&product=krita&bug_status=UNCONFIRMED&bug_status=REOPENED&bug_status=NEEDSINFO)(再現していない、再発していない、情報が足りていないKritaのバグリスト)

このリストを0にすることを目標にしています!

もちろん、上のリストには既に確認のとれたバグと同じものも含まれているかもしれません:

[**Confirmed Krita Bugs**](https://bugs.kde.org/buglist.cgi?bug_status=CONFIRMED&bug_status=ASSIGNED&bug_severity=critical&bug_severity=grave&bug_severity=major&bug_severity=crash&bug_severity=normal&bug_severity=minor&query_format=advanced&product=krita)(開発が再現を確認したKritaのバグリスト)

今回のトリアージは既存のバグを対象としたものですが、もし新規のバグを見つけた場合は、Dmitryさんによる[バグ報告ガイドライン(英語)](https://community.kde.org/Krita/docs/Bug_Writing_Guidelines)を読んで登録をしていただけると助かります。

[バグハンターHowto](https://community.kde.org/Krita/Docs/Bug_Hunting_Day#Developers)(英語)を読んで、この週末のバグリストの整理にご協力ください！(訳注：今回のバグハントは英語ベースです)そして、その後2週間、開発チームはバグ修正に専念し、これからKickstarterでの新機能を追加していく上での安定した土台を作り上げたいと思っています！

[![Mosquitoes-hunter_by_David-Revoy](/images/posts/2015/Mosquitoes-hunter_by_David-Revoy-238x300.jpg)](/images/posts/2015/Mosquitoes-hunter_by_David-Revoy-238x300.jpg)

Bug hunter by David Revoy

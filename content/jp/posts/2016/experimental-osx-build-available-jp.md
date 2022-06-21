---
title: "開発版OSXビルドが公開されました"
date: "2016-09-07"
categories: 
  - "uncategorized-jp"
tags: 
  - "japanese"
---

今年の夏休み期間、Google Summer of Code参加学生の[Julian Thijssen](http://kritadev.blogspot.nl/)（IRC等でのHNはNimmy）はKritaとQt5をOpenGL 3.0コアプロファイルで正常に動作させるべく開発を行っていました。その理由は特定のシステム、とりわけOSXではOpenGL 3.0互換性プロファイルを使うことが出来ず、加えてKritaではOpenGL 3.0の機能が必要だったことによります。

これは目的の達成のためにはQtの描画バックグラウンドから既存のOpenGLのコードを全て除去しなければならないことを意味していました（その過程で過去に誰かが同じことをしようとし、そして失敗していたことが判明しました。しかしそのせいで中途半端なわかりづらいコードがそこらじゅうに散らかっていたのです）

この作業は遂に完了し、Qtプロジェクトに提出されました：[https://codereview.qt-project.org/#/c/166202/](https://codereview.qt-project.org/#/c/166202/)

同時にKritaを近代化させる作業も行われ、その成果はいつメインブランチへ統合しても大丈夫な状態にあります。次のリリースにこの開発の成果も含まれる予定です。

_ですが、_ まずはテストが必要です！そしてそのために、OSXユーザーの皆さんへ特別なディスクイメージを作成しました。そしてこのディスクイメージを使ってみて、bugzillaにバグを報告する前にまず話し合いをできるよう、専用のトピックもフォーラムに設置しておきました。

フォーラム：[https://forum.kde.org/viewtopic.php?f=137&t=135853](https://forum.kde.org/viewtopic.php?f=137&t=135853)

**更新：3.0.1の全機能を搭載し、ポップアップパレットの問題を修正した新ビルドです**

ディスクイメージ：[http://files.kde.org/krita/3/osx/devbuilds/krita-3.0.1-nimmy2.dmg](http://files.kde.org/krita/3/osx/devbuilds/krita-3.0.1-nimmy2.dmg)

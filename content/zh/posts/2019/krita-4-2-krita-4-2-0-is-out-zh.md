---
title: "Krita 4.2.0 正式版和中文翻译近况报告"
date: "2019-05-29"
categories: 
  - "officialrelease-zh"
---

今天我们为大家带来了 Krita 4.2.0 正式版。这是 Krita 的一次重大更新，修复了超过 1000 个程序问题，还带来了大量新功能、软件和文档中文翻译的显著改进等。

\[embed width="800" height="550"\]https://youtu.be/ZbnQn6h5q0g\[/embed\]

Krita 4.2.0 的新功能包括但不限于：数位板支持的改进、在 Windows 下支持 HDR 显示器、重新编写的调色板工具面板、动画用脚本 API、色域蒙版显示、选区功能的改进、不透明度和流量协同工作的改进，还有更多更新详情请查看[发行日志](https://krita.org/en/krita-4-2-release-notes/)。正式版和最后一个 [beta](https://krita.org/en/item/krita-4-2-0-beta-released/) 版本相比有 30 处左右的改进。

Tyson Tan (钛山) 也为 Krita 4.2.0 绘制了全新的启动图：

[![](/images/posts/2019/electrichearts_20190316_kiki_a_sm-2.png)](/images/posts/2019/electrichearts_20190316_kiki_a_sm-2.png)

## Krita 中文翻译近况报告

在 2019 年的第二季度，Krita 4.2.0 版的软件和文档的中文翻译得到了大量改进。我们通过对[使用手册](https://docs.krita.org/zh_CN/user_manual.html)和[参考手册](https://docs.krita.org/zh_CN/reference_manual.html)的翻译工作，增进了对软件功能的理解，改正了大量旧版软件中翻译得不甚理想的字串。最为重要的笔刷引擎、选区、图层、调整滤镜、绘画辅助尺、矢量工具、色彩管理、各核心对话框、上下文菜单的中文翻译已经接近完善。翻译工作主要由 [Tyson Tan](https://crowdin.com/profile/tysontan/activity)、[Aster Wang](https://crowdin.com/profile/Aster-the-Med-Stu/activity) 进行 (点击链接可查看两人翻译工作的记录)，特别感谢 KDE 中国的 [Guo Yunhe](https://crowdin.com/profile/guoyunhe/activity) 协助解决翻译相关的程序问题和提供翻译环境。

由于 KDE 翻译的组织、技术层面的一些限制，Krita 中文版的软件、文档翻译面临许多不便和困难。例如每次文档的英文版更新后，哪怕是一段话中的一个字符发生了变化，整段话的已有中文翻译就会被抛弃掉不再显示。部分软件的字符串的设置对中文不友好，无法进行最优翻译，甚至根本不支持翻译——这可以理解，毕竟软件的界面程序员基本都是使用西文为母语的。这些问题意味着在可见的将来，Krita 软件将长期面临少数字串的翻译缺失，而 Krita 的文档则可能长期面临大块段落翻译的缺失，甚至以往被翻译过的段落也会随时丢失。我们为此深表歉意，我们一方面将试图寻找更好的翻译手段，与 KDE 基础翻译团队增进沟通改进条件，另一方面我们将尽可能在这些限制下面把中文翻译做到最好。

由于 Tyson Tan 家庭的一些变故，现在他只能提供 Krita 软件的翻译工作，保持软件所有能翻译的字符串能及时得到 100% 的翻译，但他在短期内无法提供如同今年第二季度的那种强度的文档翻译工作。请见谅。

如果你希望对 Krita 的中文翻译提出建议，可通过 [Twitter](https://twitter.com/TysonTanX)、[电子邮件](mailto:tysontanx@gmail.com)、[留言板](https://tysontan.com/message-board/) 联系 Tyson Tan。

## 加入 Krita 社区，与其他画手互助成长

Krita 的用户正在快速增长，其年下载量已经已数百万计。这一方面当然是一件好事，但另一方面我们团队的有限力量已经无法为每位用户遇到的问题逐一作答了。我们希望使用 Krita 的用户们能在 [Reddit](https://reddit.com/r/krita)、[Ask](https://ask.krita.org)、[论坛](https://forum.kde.org/viewforum.php?f=136)、[知乎](https://www.zhihu.com/search?q=krita&type=content)、[贴吧](https://tieba.baidu.com/f?kw=krita&ie=utf-8) 等处积极帮助其他遇到困难的用户！

## 下载

### Windows 版本

注意：如果 Windows 版本用户遇到程序崩溃现象，请 [按照此说明](https://docs.krita.org/en/reference_manual/dr_minw_debugger.html#dr-minw) 使用调试符号包协助我们找到 Krita 崩溃的原因。

- 64 位安装包：[krita-x64-4.2.0-setup.exe](https://download.kde.org/stable/krita/4.2.0/krita-x64-4.2.0-setup.exe)
- 64 位压缩包：[krita-x64-4.2.0.zip](https://download.kde.org/stable/krita/4.2.0/krita-x64-4.2.0.zip)
- 64 位调试符号包：[调试符号包 (解压到 Krita 的安装文件夹)](https://download.kde.org/stable/krita/4.2.0/krita-x64-4.2.0-dbg.zip)

- 32 位安装包：[krita-x86-4.2.0-setup.exe](https://download.kde.org/stable/krita/4.2.0/krita-x86-4.2.0-setup.exe)
- 32 位压缩包：[krita-x86-4.2.0.zip](https://download.kde.org/stable/krita/4.2.0/krita-x86-4.2.0.zip)
- 32 位调试符号包：[调试符号包 (解压到 Krita 的安装文件夹)](https://download.kde.org/stable/krita/4.2.0/krita-x86-4.2.0-dbg.zip)

### Linux 版本

- 64 位 AppImage 包：[krita-4.2.0-x86\_64.appimage](https://download.kde.org/stable/krita/4.2.0/krita-4.2.0-x86_64.appimage)
- 64 位 G'Mic AppImage 包：[G'Mic-Qt 插件包](https://download.kde.org/stable/krita/4.2.0/gmic_krita_qt-x86_64.appimage)

注意：如果 Firefox 将软件包作为文本打开，请在链接上点击右键，选择“另存为”。

### OSX 版本

- OSX 磁盘镜像：[krita-4.2.0.dmg](https://download.kde.org/stable/krita/4.2.0/krita-4.2.0.dmg)

注意：在 OSX 下面，触摸工具面板、G'Mic-Qt 插件包和 Python 插件暂不可用。

### 源代码

- [krita-4.2.0.tar.gz](https://download.kde.org/stable/krita/4.2.0/krita-4.2.0.tar.gz)
- [krita-4.2.0.tar.xz](https://download.kde.org/stable/krita/4.2.0/krita-4.2.0.tar.xz)

### md5sum

所有软件包的 md5sum：

- [md5sum.txt](https://download.kde.org/stable/krita/4.2.0/md5sum.txt)

### 软件包签名和密钥

由于项目主管正在旅行途中，本次发布尚未提供 .sig 文件。我们将在下周准备。

## 支持 Krita

Krita 是一个自由和开源的软件项目。请通过 [捐款](https://krita.org/en/support-us/donations/) 或者 [购买培训教程和画册](https://krita.org/en/support-us/shop) 等方式支持我们，这样我们才能为 Krita 的开发全职工作。

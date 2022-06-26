---
title: "Krita 4.2.4 发布"
date: "2019-08-01"
categories: 
  - "officialrelease-zh"
---

今天我们为大家带来 Krita 4.2.4 版。 此版最重要的修复与快捷键输入系统和保存系统有关。Krita 4.2.3 有一个 bug 会弹出消息窗口提示快捷键没有正常执行，此问题现已修正。Anna Medonosova 进一步加强了保存系统的可靠性，尤其是在发起保存操作后关闭 Krita 时。

更多的问题修正预计在两周后 Krita 开发冲刺活动结束后随 Krita 4.2.5 发布。

根据[知乎社区 Belleve 的评论反馈](https://www.zhihu.com/question/58662017/answer/415291523)，对 SAI 的发光（Luminosity/Shine）图层混色模式进行了初步分析和实验性的支持，请使用该混色模式的用户为我们提供反馈。 ([BUG:409627](https://bugs.kde.org/show_bug.cgi?id=409627))

## 已知问题

如果触控旋转缩放不能工作，请移除本机的 default.inputrc 文件。你可以到菜单>>设定>>管理资源，点击“打开资源文件夹”按钮，进入 input 文件夹，移除全部文件。

## 修复问题清单

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

## 下载

### Windows

提示：如果在 Windows 下遇到程序崩溃，请根据 [相关指引](https://docs.krita.org/en/reference_manual/dr_minw_debugger.html#dr-minw) 使用 debug symbols 协助我们分析崩溃原因。

- 64 位 Windows 安装包: [krita-x64-4.2.4-setup.exe](https://download.kde.org/stable/krita/4.2.4/krita-x64-4.2.4-setup.exe)
- 64 位 Windows 压缩包: [krita-x64-4.2.4.zip](https://download.kde.org/stable/krita/4.2.4/krita-x64-4.2.4.zip)
- [Debug symbols. (解压到 Krita 安装目录)](https://download.kde.org/stable/krita/4.2.4/krita-x64-4.2.4-dbg.zip)

- 32 位 Windows 安装包: [krita-x86-4.2.4-setup.exe](https://download.kde.org/stable/krita/4.2.4/krita-x86-4.2.4-setup.exe)
- 32 位 Windows 压缩包: [krita-x86-4.2.4.zip](https://download.kde.org/stable/krita/4.2.4/krita-x86-4.2.4.zip)
- [Debug symbols. (解压到 Krira 安装目录)](https://download.kde.org/stable/krita/4.2.4/krita-x86-4.2.4-dbg.zip)

### Linux

- 64 位 Linux: [krita-4.2.4-x86_64.appimage](https://download.kde.org/stable/krita/4.2.4/krita-4.2.4-x86_64.appimage)
- 64 位 Linux [G'Mic-Qt plugin appimage](https://download.kde.org/stable/krita/4.2.4/gmic_krita_qt-x86_64.appimage).

(如果 Firefox 把链接作为文本打开，请右键另存为)

### OSX

- OSX disk image: [krita-4.2.4.dmg](https://download.kde.org/stable/krita/4.2.4/krita-4.2.4.dmg)

提示：gmic-qt 在 OSX 下暂不可用。

### 源代码

- [krita-4.2.4.tar.gz](https://download.kde.org/stable/krita/4.2.4/krita-4.2.4.tar.gz)
- [krita-4.2.4.tar.xz](https://download.kde.org/stable/krita/4.2.4/krita-4.2.4.tar.xz)

### md5sum

所有软件包的 md5sum:

- [md5sum.txt](https://download.kde.org/stable/krita/4.2.4/md5sum.txt)

### 软件包签名和密钥

Linux 的 Appimage 包和源代码 tarball 文件已签名，你可以通过 https 来下载公共密钥:

[0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8)、[.sig 签名文件](http://download.kde.org/unstable/krita/4.2.0-beta2/)。

## 支持 Krita

Krita 是一个自由和开源的软件项目。请通过 [捐款](https://krita.org/en/support-us/donations/) 或者 [购买培训教程和画册](https://krita.org/en/support-us/shop) 等方式支持我们，这样我们才能为 Krita 的开发全职工作。

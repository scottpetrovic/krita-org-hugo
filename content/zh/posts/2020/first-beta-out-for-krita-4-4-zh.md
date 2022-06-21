---
title: "Krita 4.4 公开测试第 1 版"
date: "2020-09-23"
categories: 
  - "development-builds-zh"
---

经过了 Krita 4.3 发布后一整个夏季的忙碌，我们于今天推出了 Krita 4.4.0 beta 1，它是 4.4 系列的第一个公开测试版本，我们将在 2 周内推出 4.4 正式版本。请协助我们测试这一版本，并报告你遇到的问题。

Krita 项目参加谷歌编程之夏的全部学生均已完成各自的工程，其中 SeExpr 填充图层工程的成果将会被包含在 4.4 版中。除此之外，填充图层的多个图案填充功能也得到了进一步的扩展，并支持画布视图预览填充效果。Krita 现在还自带了一个用于配合 Godot 使用的插件。笔刷引擎还新增了包括更丰富的笔尖图像选项在内的诸多功能。

Krita 4.4 版还修复了大量的程序缺陷，欲知详情，请查阅：[Krita 4.4 完整版本说明 (已翻译成中文)](https://krita.org/zh/krita-4-4-0-release-notes-zh/)。

<iframe src="https://diode.zone/videos/embed/b441f360-0b94-470a-8365-5a5f44b3a617" width="560" height="315" frameborder="0" sandbox="allow-same-origin allow-scripts allow-popups" allowfullscreen="allowfullscreen" data-mce-fragment="1"></iframe>

## 下载

### 中文版信息

- 中文支持：Krita 的正式版本、通过官方新闻发布的公开测试版本 (beta) 均已内建中文支持。
- 自动检测：Krita 在首次安装时会自动设置为操作系统的语言。
- 手动设置：菜单栏 --> Settings 菜单 --> Switch Application Language (倒数第二项) --> 下拉选单 --> 中文 (底部)，重启程序生效。
- 插件翻译：部分内置，G'MIC 插件[需要下载翻译包](https://share.weiyun.com/SBopNjOn)
- 网盘下载：请在官网下载缓慢时使用。

### Windows 版本

- **64 位 Windows 安装程序** (推荐) [本站下载](https://download.kde.org/unstable/krita/4.4.0-beta1/krita-x64-4.4.0-beta1-setup.exe) | [网盘下载](https://share.weiyun.com/60HLzj6I)
- **64 位 Windows 免安装包** [本站下载](https://download.kde.org/unstable/krita/4.4.0-beta1/krita-x64-4.4.0-beta1.zip) | [网盘下载](https://share.weiyun.com/60HLzj6I)
- **64 位程序崩溃调试包** [本站下载](https://download.kde.org/unstable/krita/4.4.0-beta1/krita-x64-4.4.0-beta1-dbg.zip) | [网盘下载](https://share.weiyun.com/60HLzj6I)

- **32 位 Windows 安装程序** [本站下载](https://download.kde.org/unstable/krita/4.4.0-beta1/krita-x86-4.4.0-beta1-setup.exe) | [网盘下载](https://share.weiyun.com/Otvc2tpi)
- **32 位 Windows 免安装包** [本站下载](https://download.kde.org/unstable/krita/4.4.0-beta1/krita-x86-4.4.0-beta1.zip) | [网盘下载](https://share.weiyun.com/Otvc2tpi)
- **32 位程序崩溃调试包** [本站下载](https://download.kde.org/unstable/krita/4.4.0-beta1/krita-x86-4.4.0-beta1-dbg.zip) | [网盘下载](https://share.weiyun.com/Otvc2tpi)

- 免安装包：解压到任意位置，运行目录中的 Krita 快捷方式。不带文件管理器缩略图插件。与已安装版本共用配置文件和资源，但程序本身相互独立。
- 程序崩溃调试包：解压到 Krita 的安装目录，在报告程序崩溃问题时用于获取回溯追踪数据。日常使用无需下载此包。

### Linux 版本

- **64 位 Linux AppImage 主程序包** [本站下载](https://download.kde.org/unstable/krita/4.4.0-beta1/krita-4.4.0-beta1-x86_64.appimage) | [网盘下载](https://share.weiyun.com/C0gZ6joR)
- **64 位 Linux AppImage G'Mic-Qt 插件包** [本站下载](https://download.kde.org/unstable/krita/4.4.0-beta1/gmic_krita_qt-x86_64.appimage) | [网盘下载](https://share.weiyun.com/C0gZ6joR)
- 如果浏览器把链接作为文本打开，请右键点击链接另存为文件。

### macOS 版本

- **macOS 主程序映像** [本站下载](https://download.kde.org/unstable/krita/4.4.0-beta1/krita-4.4.0-beta1.dmg) | [网盘下载](https://share.weiyun.com/gVg0CI53)

- G'Mic-qt 软件包、触摸屏辅助面板在 macOS 下不可用。

### 安卓版本

4.4 beta 1 并未来得及准备安卓版本，因为我们正在设法修复一系列影响安卓版本打开、保存图像的程序缺陷。我们希望赶在 4.4 正式版发布前合并这些更改。

### 源代码

- [TAR.GZ 格式源代码包](https://download.kde.org/unstable/krita/4.4.0-beta1/krita-4.4.0-beta1.tar.gz)
- [TAR.XZ 格式源代码包](https://download.kde.org/unstable/krita/4.4.0-beta1/krita-4.4.0-beta1.tar.xz)

### md5sum 校验码

适用于上述所有软件包，用于校验下载文件的完整性，不了解文件校验请忽略：

- [ms5sum 校验码文本文件](https://download.kde.org/unstable/krita/4.4.0-beta1/md5sum.txt)

## 支持 Krita

Krita 是一个自由和开源的软件项目。如果条件允许，请考虑通过 [捐款](https://krita.org/zh/support-us-zh/donation-zh/) 或者 [购买培训教程和画册](https://krita.org/en/support-us/shop) 等方式支持我们的存续和发展，这样我们才能支持开发人员为 Krita 全职工作。

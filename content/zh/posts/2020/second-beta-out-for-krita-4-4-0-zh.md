---
title: "Krita 4.4.0 公开测试第 2 版已经推出"
date: "2020-09-30"
categories: 
  - "development-builds-zh"
---

我们于今天推出了 Krita 4.4.0 beta 2 版，修复了在 beta 1 版中发现的一些功能退化和阻碍正式版发布的程序缺陷。

此版软件提供了安卓版本，它已经修复了安卓平台下读写文件有关的一系列程序缺陷。同时从此版开始安卓版本将内建多语言支持，但由于包含翻译文件的 APK 文件超出了 Google Play Store 的限制，我们以后将在本站 (也就是 KDE 项目的download.kde.org 服务器集群提供本地下载。

**注意：微软最近更改了 Windows 的数字安全证书信任策略，仅默认信任 Digicert 颁发的证书。Krita 的证书并非由 Digicert 颁发，因此新版软件的软件包会在一段时间内遭到系统的 SmartScreen 智能安全筛选功能阻止。如果在下载、运行软件时见到“Windows 已经保护了你的电脑”、“此下载可能危害你的电脑”之类的信息，请点击“更多信息”或者“...”展开，然后点击“保留”或者“仍要运行”按钮。在一定数量的用户通过上述方式允许 Krita 下载运行后，SmartScreen 将不会再阻止它，直到下一个新版发布。**

欲知详情，请查阅：[Krita 4.4 完整版本说明 (已翻译成中文)](https://krita.org/zh/krita-4-4-0-release-notes-zh/)。

<iframe src="https://diode.zone/videos/embed/b441f360-0b94-470a-8365-5a5f44b3a617" width="560" height="315" frameborder="0" sandbox="allow-same-origin allow-scripts allow-popups" allowfullscreen="allowfullscreen" data-mce-fragment="1"></iframe>

## 已修复的程序缺陷列表 (Beta 1 版后)

- 停用 DDS 文件格式
- 修复在载入包含参考图像的图像时造成的崩溃 ([BUG:426839](https://bugs.kde.org/show_bug.cgi?id=426839))
- 修复颜色涂抹笔刷引擎的亮度模式效果强度选项功能 ([BUG:426874](https://bugs.kde.org/show_bug.cgi?id=426874))
- 修复图案的截断选项 [BUG:426874](https://bugs.kde.org/show_bug.cgi?id=426874)
- 安卓版本：矢量图形和参考图像不能正常显示 ([BUG:422312](https://bugs.kde.org/show_bug.cgi?id=422312))
- 修复拾色器的颜色预览更新 ([BUG:426867](https://bugs.kde.org/show_bug.cgi?id=))
- Windows 版本：新增相关的 .LNK 文件，以便在 Minimal (最小界面元素) 和 Animation (动画制作) 工作区模式下启动 Krita
- 修复在建立矩形选区后撤销时造成的崩溃
- 修复在移动局部选区蒙版时造成的崩溃 ([BUG:426816](https://bugs.kde.org/show_bug.cgi?id=426816))
- 修复多边形选区工具的快捷键功能 ([BUG:426916](https://bugs.kde.org/show_bug.cgi?id=426916))
- 修复 MyPaint 拾色器在鼠标点击时的颜色预览更新
- SeExpr：将 assert isDirty 指向正确的 preset 进程 ([BUG:426911](https://bugs.kde.org/show_bug.cgi?id=426911))
- 修复曲线工具的辅助线吸附功能 ([BUG:426514](https://bugs.kde.org/show_bug.cgi?id=426514))
- 安卓版本：通过安卓的 Storage Access Framework (存储访问程序框架) 进行所有读写操作 ([BUG:424541](https://bugs.kde.org/show_bug.cgi?id=424541), [BUG:423670](https://bugs.kde.org/show_bug.cgi?id=423670))
- 安卓版本：在欢迎界面显示最近使用的图像列表
- 安卓版本：修复读写文件图层的相关问题
- 安卓版本：修复保存不带扩展名的文件的相关问题
- 安卓版本：修复保存带有选区的图像
- 安卓版本：修复日志无法被保存到文件的缺陷 ([BUG:427043](https://bugs.kde.org/show_bug.cgi?id=427043))

## 下载

### 中文版信息

- 中文支持：Krita 的正式版本、通过官方新闻发布的公开测试版本 (beta) 均已内建中文支持。
- 自动检测：Krita 在首次安装时会自动设置为操作系统的语言。
- 手动设置：菜单栏 --> Settings 菜单 --> Switch Application Language (倒数第二项) --> 下拉选单 --> 中文 (底部)，重启程序生效。
- 插件翻译：部分内置，G'MIC 插件[需要下载翻译包](https://share.weiyun.com/SBopNjOn)
- 网盘下载：请在官网下载缓慢时使用。

### Windows 版本

- **64 位 Windows 安装程序** (推荐) [本站下载](https://download.kde.org/unstable/krita/4.4.0-beta2/krita-x64-4.4.0-beta2-setup.exe) | [网盘下载](https://share.weiyun.com/60HLzj6I)
- **64 位 Windows 免安装包** [本站下载](https://download.kde.org/unstable/krita/4.4.0-beta2/krita-x64-4.4.0-beta2.zip) | [网盘下载](https://share.weiyun.com/60HLzj6I)
- **64 位程序崩溃调试包** [本站下载](https://download.kde.org/unstable/krita/4.4.0-beta2/krita-x64-4.4.0-beta2-dbg.zip) | [网盘下载](https://share.weiyun.com/60HLzj6I)

- **32 位 Windows 安装程序** [本站下载](https://download.kde.org/unstable/krita/4.4.0-beta2/krita-x86-4.4.0-beta2-setup.exe) | [网盘下载](https://share.weiyun.com/Otvc2tpi)
- **32 位 Windows 免安装包** [本站下载](https://download.kde.org/unstable/krita/4.4.0-beta2/krita-x86-4.4.0-beta2.zip) | [网盘下载](https://share.weiyun.com/Otvc2tpi)
- **32 位程序崩溃调试包** [本站下载](https://download.kde.org/unstable/krita/4.4.0-beta2/krita-x86-4.4.0-beta2-dbg.zip) | [网盘下载](https://share.weiyun.com/Otvc2tpi)

- 免安装包：解压到任意位置，运行目录中的 Krita 快捷方式。不带文件管理器缩略图插件。与已安装版本共用配置文件和资源，但程序本身相互独立。
- 程序崩溃调试包：解压到 Krita 的安装目录，在报告程序崩溃问题时用于获取回溯追踪数据。日常使用无需下载此包。

### Linux 版本

- **64 位 Linux AppImage 主程序包** [本站下载](https://download.kde.org/unstable/krita/4.4.0-beta2/krita-4.4.0-beta2-x86_64.appimage) | [网盘下载](https://share.weiyun.com/C0gZ6joR)
- **64 位 Linux AppImage G'Mic-Qt 插件包** [本站下载](https://download.kde.org/unstable/krita/4.4.0-beta2/gmic_krita_qt-x86_64.appimage) | [网盘下载](https://share.weiyun.com/C0gZ6joR)
- 如果浏览器把链接作为文本打开，请右键点击链接另存为文件。

### macOS 版本

- **macOS 主程序映像** [本站下载](https://download.kde.org/unstable/krita/4.4.0-beta2/krita-4.4.0-beta2.dmg) | [网盘下载](https://share.weiyun.com/gVg0CI53)

- G'Mic-qt 软件包、触摸屏辅助面板在 macOS 下不可用。

### 安卓版本

安卓版本目前尚处于早期测试阶段，它的功能和普通版本完全相同，仅为平板设备和 ChromeBook 进行了初步优化，许多功能依然必须搭配键盘使用。由于屏幕比例和大小造成界面显示不全，尽管它能够在一般智能手机上安装，我们依然不建议你在智能手机上使用它。从此版开始，安卓版本已经合并到主源代码分支，且通过统一流程进行构建，因此它包含多语言支持。

- **64 位 Intel CPU APK 安装包** [本站下载](https://download.kde.org/unstable/krita/4.4.0-beta2/krita-x86_64-4.4.0-beta2-release.apk) | [网盘下载](https://share.weiyun.com/he1kczpd)
- **32 位 Intel CPU APK 安装包** [本站下载](https://download.kde.org/unstable/krita/4.4.0-beta2/krita-x86-4.4.0-beta2-release.apk) | [网盘下载](https://share.weiyun.com/he1kczpd)
- **64 位 ARM CPU APK 安装包** [本站下载](https://download.kde.org/unstable/krita/4.4.0-beta2/krita-arm64-4.4.0-beta2-release.apk) | [网盘下载](https://share.weiyun.com/he1kczpd)
- **32 位 ARM CPU APK 安装包** [本站下载](https://download.kde.org/unstable/krita/4.4.0-beta2/krita-arm64-4.4.0-beta2-release.apk) | [网盘下载](https://share.weiyun.com/he1kczpd)

### 源代码

- [TAR.GZ 格式源代码包](https://download.kde.org/unstable/krita/4.4.0-beta2/krita-4.4.0-beta2.tar.gz)
- [TAR.XZ 格式源代码包](https://download.kde.org/unstable/krita/4.4.0-beta2/krita-4.4.0-beta2.tar.xz)

### md5sum 校验码

适用于上述所有软件包，用于校验下载文件的完整性，不了解文件校验请忽略：

- [ms5sum 校验码文本文件](https://download.kde.org/unstable/krita/4.4.0-beta2/md5sum.txt)

## 支持 Krita

Krita 是一个自由和开源的软件项目。如果条件允许，请考虑通过 [捐款](https://krita.org/zh/support-us-zh/donation-zh/) 或者 [购买培训教程和画册](https://krita.org/en/support-us/shop) 等方式支持我们的存续和发展，这样我们才能支持开发人员为 Krita 全职工作。

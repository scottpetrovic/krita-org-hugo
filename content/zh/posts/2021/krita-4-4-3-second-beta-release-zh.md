---
title: "Krita 4.4.3 公开测试第 2 版已经推出"
date: "2021-03-12"
categories: 
  - "news-zh"
  - "development-builds-zh"
---

今天 Krita 开发团队发布了 Krita 4.4.3 的第 2 个公开测试版。此版软件主要在公开测试第 1 版的基础上修复了少量造成体验退步的程序缺陷。欢迎大家下载测试。

- Krita 4.4.3 beta 2 现在使用 GCC 11 进行编译。感谢 Jonathan Wakely 的工作。
- 修复了在 Linux 下屏幕缩放倍率为 125% 时呼叫右键面板会造成崩溃的程序缺陷。 ([BUG:431944](https://bugs.kde.org/show_bug.cgi?id=431944))
- 修复了油画滤镜的分块绘制缺陷。
- 修复了在使用最新版本软件时在欢迎画面依然提示有新版软件可用的问题。
- 如果图像的文件名太长，标签页的右侧文字会被省略，而不是中间文字。
- 修复了使用带有特殊按键的非美式键盘的快捷键 ([BUG:430479](https://bugs.kde.org/show_bug.cgi?id=430479))

## 下载

### 中文版信息

- 中文支持：Krita 的正式版本、通过官方新闻发布的公开测试版本 (beta) 均已内建中文支持。
- 自动检测：Krita 在首次安装时会自动设置为操作系统的语言。
- 手动设置：菜单栏 --> Settings 菜单 --> Switch Application Language (倒数第二项) --> 下拉选单 --> 中文 (底部)，重启程序生效。
- 插件翻译：部分内置，G'MIC 插件[需要下载翻译包](https://share.weiyun.com/SBopNjOn)
- 网盘下载：请在官网下载困难时使用。

### Windows 版本

- **64 位 Windows 安装程序** (推荐) [本站下载](https://download.kde.org/unstable/krita/4.4.3-beta2/krita-x64-4.4.3-beta2-setup.exe) | [网盘下载](https://share.weiyun.com/60HLzj6I)
- **64 位 Windows 免安装包** [本站下载](https://download.kde.org/unstable/krita/4.4.3-beta2/krita-x64-4.4.3-beta2.zip) | [网盘下载](https://share.weiyun.com/60HLzj6I)
- **64 位程序崩溃调试包** [本站下载](https://download.kde.org/unstable/krita/4.4.3-beta2/krita-x64-4.4.3-beta2-dbg.zip) | [网盘下载](https://share.weiyun.com/60HLzj6I)

- **32 位 Windows 安装程序** [本站下载](https://download.kde.org/unstable/krita/4.4.3-beta2/krita-x86-4.4.3-beta2-setup.exe) | [网盘下载](https://share.weiyun.com/Otvc2tpi)
- **32 位 Windows 免安装包** [本站下载](https://download.kde.org/unstable/krita/4.4.3-beta2/krita-x86-4.4.3-beta2.zip) | [网盘下载](https://share.weiyun.com/Otvc2tpi)
- **32 位程序崩溃调试包** [本站下载](https://download.kde.org/unstable/krita/4.4.3-beta2/krita-x86-4.4.3-beta2-dbg.zip) | [网盘下载](https://share.weiyun.com/Otvc2tpi)

- **配套网盘资源 (中文社区维护)** [中文离线文档](https://share.weiyun.com/Dea2uj0M) | [FFmpeg 软件包](https://share.weiyun.com/6tH13bVC) | [G'Mic 滤镜汉化](https://share.weiyun.com/SBopNjOn) |

- 免安装包：解压到任意位置，运行目录中的 Krita 快捷方式。不带文件管理器缩略图插件。与已安装版本共用配置文件和资源，但程序本身相互独立。
- 程序崩溃调试包：解压到 Krita 的安装目录，在报告程序崩溃问题时用于获取回溯追踪数据。日常使用无需下载此包。

### Linux 版本

- **64 位 Linux AppImage 主程序包** [本站下载](https://download.kde.org/unstable/krita/4.4.3-beta2/krita-4.4.3-beta2-x86_64.appimage) | [网盘下载](https://share.weiyun.com/C0gZ6joR)
- **64 位 Linux AppImage G'Mic-Qt 插件包** [本站下载](https://download.kde.org/unstable/krita/4.4.3-beta2/gmic_krita_qt-x86_64.appimage) | [网盘下载](https://share.weiyun.com/C0gZ6joR)
- 如果浏览器把链接作为文本打开，请右键点击链接另存为文件。

### macOS 版本

- **macOS 主程序映像** [本站下载](https://download.kde.org/unstable/krita/4.4.3-beta2/krita-4.4.3-beta2.dmg) | [网盘下载](https://share.weiyun.com/gVg0CI53)

- G'Mic-qt 软件包、触摸屏辅助面板在 macOS 下不可用。

### 安卓版本

安卓版本目前尚处于早期测试阶段，整体功能与桌面版本几乎完全相同。它仅为安卓平板和 ChromeBook 类设备进行了初步适配，大部分功能依然需要搭配键盘使用。尽管它也能够在一般智能手机上安装，但受屏幕大小和宽高比所限会造成界面显示不全，我们不建议你在智能手机上使用它。随正式版发布的安卓版本现在可以正常显示中文界面。

- **64 位 Intel CPU APK 安装包** [本站下载](https://download.kde.org/unstable/krita/4.4.3-beta2/krita_x86_64_apk-4.4.3-beta2.apk) | [网盘下载](https://share.weiyun.com/tEkbnO1K)
- **32 位 Intel CPU APK 安装包** [本站下载](https://download.kde.org/unstable/krita/4.4.3-beta2/krita_x86_apk-4.4.3-beta2.apk) | [网盘下载](https://share.weiyun.com/tEkbnO1K)
- **64 位 ARM CPU APK 安装包** [本站下载](https://download.kde.org/unstable/krita/4.4.3-beta2/krita_arm64-v8a_apk-4.4.3-beta2.apk) | [网盘下载](https://share.weiyun.com/tEkbnO1K)
- **32 位 ARM CPU APK 安装包** [本站下载](https://download.kde.org/unstable/krita/4.4.3-beta2/krita_armeabi-v7a_apk-4.4.3-beta2.apk) | [网盘下载](https://share.weiyun.com/tEkbnO1K)

### 源代码

- [TAR.GZ 格式源代码包](https://download.kde.org/unstable/krita/4.4.3-beta2/krita-4.4.3-beta2.tar.gz)
- [TAR.XZ 格式源代码包](https://download.kde.org/unstable/krita/4.4.3-beta2/krita-4.4.3-beta2.tar.xz)

### md5sum 校验码

适用于上述所有软件包，用于校验下载文件的完整性，不了解文件校验请忽略：

- [ms5sum 校验码文本文件](https://download.kde.org/unstable/krita/4.4.3-beta2/md5sum.txt)

### 文件完整性验证密钥

Linux 的 Appimage 可执行文件包和源代码的 .tar.gz 和 .tar.xz tarballs 压缩包已经经过数字签名。你可以通过 GPG 取回公共密钥，命令为 gpg --recv-key 7468332F 。你可以在此下载 [数字签名的 SIG 文件](https://download.kde.org/unstable/krita/4.4.3-beta2/)。

## 支持 Krita

Krita 是一个自由和开源的软件项目。如果条件允许，请考虑通过 [捐款](https://krita.org/zh/support-us-zh/donation-zh/) 或者 [购买培训教程和画册](https://krita.org/en/shop/) 等方式支持我们的存续和发展，这样我们才能支持开发人员为 Krita 全职工作。

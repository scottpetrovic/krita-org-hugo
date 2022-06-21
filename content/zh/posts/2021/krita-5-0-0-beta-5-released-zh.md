---
title: "Krita 5.0 公开测试第 5 版已经推出"
date: "2021-12-03"
categories: 
  - "news-zh"
  - "development-builds-zh"
---

今天我们为大家带来了 Krita 5.0 公开测试第 5 版。由于 Krita 5.0 beta 3 的 macOS 程序映像构建失败，我们在 beta 3 发布后立即修复了问题并开始构建 beta 4。但在 beta 4 构建途中 Dmitry Kazakov 又修复了一个我们希望能立即投入测试的问题，于是我们决定直接跳过 beta 4，发布 beta 5。

![](images/2021-11-16_kiki-piggy-bank_krita5.png) Krita 是一个自由开源的软件项目，如果条件允许，请考虑通过[捐款](https://fund.krita.org)或[购买视频教程](https://krita.org/en/shop/)等方式为我们提供资金支持，这可以确保 Krita 的核心开发团队成员为项目全职工作。

Krita 5 beta 5 在 beta 3 的基础上的新增了下列程序缺陷修复：

- 又双叒叕一次修复了 macOS 版本的构建……（叹气）
- 修复了一个资源选择器会选择错误资源的问题。
- 只在色板发生改变后才保存它们。
- 修复文字形状的行高过大的问题。
- 修复了文字形状中的文字大小与 Krita 4 不一致的问题。
- 移除了亮度/对比度滤镜的无用快捷键。
- 在 KDE 的可执行程序构建平台中添加 Krita 的 MSIX 软件包构建任务。
- 修复预设保存对话框的错误动画。
- 修复在新版资源从资源文件夹中删除后的资源加载。
- 修复图层组的色彩模型。
- 修复软件色彩校样的问题。
- 修复使用渐变映射模式的笔刷预设。

## 下载

### 中文版信息

- 中文支持：Krita 的所有软件包均内建中文支持，首次安装时会自动设置为操作系统的语言。
- 手动设置：菜单栏 --> Settings --> Switch Application Language (倒数第二项) --> 下拉选单 --> 中文 (底部)，重启程序生效。
- 插件翻译：G'MIC 插件[需要下载翻译包](https://share.weiyun.com/SBopNjOn)
- 网盘下载：请在官网下载困难时使用，更新时间可能滞后。

### Windows 版本

- **64 位 Windows 安装程序** [本站下载](https://download.kde.org/unstable/krita/5.0.0-beta5/krita-x64-5.0.0-beta5-setup.exe) | [网盘下载](https://share.weiyun.com/60HLzj6I)
- **64 位 Windows 免安装包** [本站下载](https://download.kde.org/unstable/krita/5.0.0-beta5/krita-x64-5.0.0-beta5.zip) | [网盘下载](https://share.weiyun.com/60HLzj6I)
- **64 位程序崩溃调试包** [本站下载](https://download.kde.org/unstable/krita/5.0.0-beta5/krita-x64-5.0.0-beta5-dbg.zip) | [网盘下载](https://share.weiyun.com/60HLzj6I)

- **配套网盘资源 (中文社区维护)** [中文离线文档](https://share.weiyun.com/Dea2uj0M) | [FFmpeg 软件包](https://share.weiyun.com/6tH13bVC) | [G'Mic 滤镜汉化](https://share.weiyun.com/SBopNjOn) |

- 32 位支持：最后一版支持 32 位 Windows 的 Krita 为 4.4.3，[本站下载](https://download.kde.org/stable/krita/4.4.3/krita-x86-4.4.3-setup.exe) | [网盘下载](https://share.weiyun.com/wdMnx1WB)。
- 免安装包：解压到任意位置，运行目录中的 Krita 快捷方式。不带文件管理器缩略图插件，与已安装版本共用配置文件和资源，但程序本身相互独立。
- 程序崩溃调试包：解压到 Krita 的安装目录，在报告程序崩溃问题时用于获取回溯追踪数据。日常使用无需下载此包。

### Linux 版本

- **64 位 Linux AppImage 程序包** [本站下载](https://download.kde.org/unstable/krita/5.0.0-beta5/krita-5.0.0-beta5-x86_64.appimage) | [网盘下载](https://share.weiyun.com/C0gZ6joR)
- 从此版开始，G'Mic 插件已经整合到主程序包中
- 如果浏览器把链接作为文本打开，请右键点击链接另存为文件。

### macOS 版本

- **macOS 程序映像** [本站下载](https://download.kde.org/unstable/krita/5.0.0-beta5/krita-5.0.0-beta5.dmg) | [网盘下载](https://share.weiyun.com/gVg0CI53)

- 如果您还在使用 OSX Sierra 或者 High Sierra，请[观看此视频](https://www.youtube.com/watch?v=3py0kgq95Hk)了解如何启动由开发人员签名的可执行软件包。

### 安卓版本

安卓版本目前尚处于早期测试阶段，整体功能与桌面版本几乎完全相同。它仅为安卓平板和 ChromeBook 类设备进行了初步适配，大部分功能依然需要搭配键盘使用，还有不少功能无法正常工作。

- **64 位 Intel CPU APK 安装包** [本站下载](https://download.kde.org/unstable/krita/5.0.0-beta5/krita-x86_64-5.0.0-beta5-release-signed.apk) | [网盘下载](https://share.weiyun.com/AKSomiNJ)
- **32 位 Intel CPU APK 安装包** [本站下载](https://download.kde.org/unstable/krita/5.0.0-beta5/krita-x86-5.0.0-beta5-release-signed.apk) | [网盘下载](https://share.weiyun.com/AKSomiNJ)
- **64 位 ARM CPU APK 安装包** [本站下载](https://download.kde.org/unstable/krita/5.0.0-beta5/krita-arm64-v8a-5.0.0-beta5-release-signed.apk) | [网盘下载](https://share.weiyun.com/GCKrtN0F)
- **32 位 ARM CPU APK 安装包** [本站下载](https://download.kde.org/unstable/krita/5.0.0-beta5/krita-armeabi-v7a-5.0.0-beta5-release-signed.apk) | [网盘下载](https://share.weiyun.com/GCKrtN0F)

### 源代码

- [TAR.GZ 格式源代码包](https://download.kde.org/unstable/krita/5.0.0-beta5/krita-5.0.0-beta5.tar.gz)
- [TAR.XZ 格式源代码包](https://download.kde.org/unstable/krita/5.0.0-beta5/krita-5.0.0-beta5.tar.xz)

### md5sum 校验码

适用于上述所有软件包，用于校验下载文件的完整性，不了解文件校验请忽略：

- [ms5sum 校验码文本文件](https://download.kde.org/unstable/krita/5.0.0-beta5/md5sum.txt)

### 文件完整性验证密钥

Linux 的 Appimage 可执行文件包和源代码的 .tar.gz 和 .tar.xz tarballs 压缩包已经经过数字签名。您可以[在此下载公钥](https://files.kde.org/krita/4DA79EDA231C852B)，还可以在此下载[数字签名的 SIG 文件](https://download.kde.org/unstable/krita/5.0.0-beta5/)。

## 请支持 Krita

Krita 是一个自由和开源的软件项目。如果条件允许，请考虑通过 [捐款](https://fund.krita.org/) 或者 [购买培训教程和画册](https://krita.org/en/shop/) 等方式支持我们的存续和发展，这样我们才能支持开发人员为 Krita 全职工作。

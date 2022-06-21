---
title: "Krita 4.4.7 正式版已经推出"
date: "2021-08-07"
categories: 
  - "officialrelease-zh"
---

Krita 4.4.7 版已经发布。它修复了一些程序缺陷，其中最值得一提的是修复了在 4.4.5 版的一个会造成性能下降的缺陷。此版本还包括以下缺陷修复：

- 修复在某些版本的 Qt 和 PyQt 会造成程序退出时崩溃的缺陷
- 修复磁性选区工具的选区移动功能 ([BUG:433633](https://bugs.kde.org/show_bug.cgi?id=433633))
- 修复磁性选区工具在删除节点时的崩溃 ([BUG:439896](https://bugs.kde.org/show_bug.cgi?id=439896))
- 修复一个从 Python 进行图像色彩空间转换时的 assert 错误 ([BUG:437980](https://bugs.kde.org/show_bug.cgi?id=437980))
- 修复关闭色域蒙版图像时的崩溃 ([BUG:438914](https://bugs.kde.org/show_bug.cgi?id=438914))
- 修复在图像之间进行克隆图层拖放的功能 ([BUG:414699](https://bugs.kde.org/show_bug.cgi?id=414699))
- 修复在启用裁切时保存图像会崩溃的问题 ([BUG:437626](https://bugs.kde.org/show_bug.cgi?id=437626))

提示：Krita 4.4.6 版仅在 Epic 游戏商城中发布。

点击查看：[Krita 4.4.x 系列的完整版本说明](https://krita.org/zh/krita-4-4-0-release-notes-zh/)

## 下载

### 中文版信息

- 中文支持：Krita 的所有软件包均已内建中文支持。
- 自动检测：Krita 在首次安装时会自动设置为操作系统的语言。
- 手动设置：菜单栏 --> Settings 菜单 --> Switch Application Language (倒数第二项) --> 下拉选单 --> 中文 (底部)，重启程序生效。
- 插件翻译：部分内置，G'MIC 插件[需要下载翻译包](https://share.weiyun.com/SBopNjOn)
- 网盘下载：请在官网下载困难时使用。

### Windows 版本

- **64 位 Windows 安装程序** (推荐) [本站下载](https://download.kde.org/stable/krita/4.4.7/krita-x64-4.4.7-setup.exe) | [网盘下载](https://share.weiyun.com/aVyf2PXQ)
- **64 位 Windows 免安装包** [本站下载](https://download.kde.org/stable/krita/4.4.7/krita-x64-4.4.7.zip) | [网盘下载](https://share.weiyun.com/aVyf2PXQ)
- **64 位程序崩溃调试包** [本站下载](https://download.kde.org/stable/krita/4.4.7/krita-x64-4.4.7-dbg.zip) | [网盘下载](https://share.weiyun.com/aVyf2PXQ)

- **配套网盘资源 (中文社区维护)** [中文离线文档](https://share.weiyun.com/Dea2uj0M) | [FFmpeg 软件包](https://share.weiyun.com/6tH13bVC) | [G'Mic 滤镜汉化](https://share.weiyun.com/SBopNjOn) |

- 32 位支持：Krita 从 4.4.5 版开始不再支持 32 位 Windows。最后一版支持 32 位 Windows 的 Krita 为 4.4.3，[本站下载](https://download.kde.org/stable/krita/4.4.3/krita-x86-4.4.3-setup.exe) | [网盘下载](https://share.weiyun.com/wdMnx1WB)。
- 免安装包：解压到任意位置，运行目录中的 Krita 快捷方式。不带文件管理器缩略图插件。与已安装版本共用配置文件和资源，但程序本身相互独立。
- 程序崩溃调试包：解压到 Krita 的安装目录，在报告程序崩溃问题时用于获取回溯追踪数据。日常使用无需下载此包。

### Linux 版本

- **64 位 Linux AppImage 主程序包** [本站下载](https://download.kde.org/stable/krita/4.4.7/krita-4.4.7-x86_64.appimage) | [网盘下载](https://share.weiyun.com/j7Vrjx2m)
- **64 位 Linux AppImage G'Mic-Qt 插件包** [本站下载](https://download.kde.org/stable/krita/4.4.7/gmic_krita_qt-x86_64.appimage) | [网盘下载](https://share.weiyun.com/j7Vrjx2m)
- 如果浏览器把链接作为文本打开，请右键点击链接另存为文件。

### macOS 版本

- **macOS 主程序映像** [本站下载](https://download.kde.org/stable/krita/4.4.7/krita-4.4.7.dmg) | [网盘下载](https://share.weiyun.com/jc82ykle)

- G'Mic-qt 软件包、触摸屏辅助面板在 macOS 下不可用。
- 如果您还在使用 OSX Sierra 或者 High Sierra，请[观看此视频](https://www.youtube.com/watch?v=3py0kgq95Hk)了解如何启动由开发人员签名的可执行软件包。

### 安卓版本

安卓版本目前尚处于早期测试阶段，整体功能与桌面版本几乎完全相同。它仅为安卓平板和 ChromeBook 类设备进行了初步适配，大部分功能依然需要搭配键盘使用，还有不少功能不能正常工作。您还可以通过 [Google Play](https://play.google.com/store/apps/details?id=org.krita) 安装 Krita。

- **64 位 Intel CPU APK 安装包** [本站下载](https://download.kde.org/stable/krita/4.4.7/krita-x86_64-4.4.7-release.apk) | [网盘下载](https://share.weiyun.com/he1kczpd)
- **32 位 Intel CPU APK 安装包** [本站下载](https://download.kde.org/stable/krita/4.4.7/krita-x86-4.4.7-release.apk) | [网盘下载](https://share.weiyun.com/he1kczpd)
- **64 位 ARM CPU APK 安装包** [本站下载](https://download.kde.org/stable/krita/4.4.7/krita-arm64-v8a-4.4.7-release.apk) | [网盘下载](https://share.weiyun.com/he1kczpd)
- **32 位 ARM CPU APK 安装包** [本站下载](https://download.kde.org/stable/krita/4.4.7/krita-armeabi-v7a-4.4.7-release.apk) | [网盘下载](https://share.weiyun.com/he1kczpd)

### 源代码

- [TAR.GZ 格式源代码包](https://download.kde.org/stable/krita/4.4.7/krita-4.4.7.tar.gz)
- [TAR.XZ 格式源代码包](https://download.kde.org/stable/krita/4.4.7/krita-4.4.7.tar.xz)

### md5sum 校验码

适用于上述所有软件包，用于校验下载文件的完整性，不了解文件校验请忽略：

- [ms5sum 校验码文本文件](https://download.kde.org/stable/krita/4.4.7/md5sum.txt)

### 文件完整性验证密钥

Linux 的 Appimage 可执行文件包和源代码的 .tar.gz 和 .tar.xz tarballs 压缩包已经经过数字签名。您可以通过 GPG 取回公共密钥，命令为 gpg --recv-key 7468332F 。您可以在此下载 [数字签名的 SIG 文件](https://download.kde.org/stable/krita/4.4.7/)。

## 请支持 Krita

Krita 是一个自由和开源的软件项目。如果条件允许，请考虑通过 [捐款](https://fund.krita.org/) 或者 [购买培训教程和画册](https://krita.org/en/shop/) 等方式支持我们的存续和发展，这样我们才能支持开发人员为 Krita 全职工作。

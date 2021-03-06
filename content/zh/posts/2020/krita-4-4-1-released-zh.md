---
title: "Krita 4.4.1 正式版已经推出"
date: "2020-10-29"
categories: 
  - "officialrelease-zh"
---

Krita 4.4.0 版发布后不久，我们从用户社区的反馈了解到软件出现了一些会造成使用体验倒退的缺陷。这些问题并未出现在 4.3.0 版中。我们在 4.4.1 版中修复了下列问题：

- Android 和 ChromeOS 版：
    - 使用第 29 版 SDK，这样 Krita 便不再需要额外的权限也能运行，而且访问外部存储装置上的文件时也更加方便。Krita 本身也改为使用 NDK 20或更高版本。
    - 修复拾色器 ([BUG:423254](https://bugs.kde.org/show_bug.cgi?id=423254))
    - 修复在显示浮动消息时事件发送至画布视图时发生的问题
    - 使用本机的区域设置，让翻译可以加载。现在安卓版可以显示中文了。 ([BUG:427692](https://bugs.kde.org/show_bug.cgi?id=427692))
    - 修复安卓设备的复制粘贴 ([BUG:423199](https://bugs.kde.org/show_bug.cgi?id=423199))
- 全部版本：
    - 修复在载入带有图案填充图层的图像文件时发生的崩溃 ([BUG:427866](https://bugs.kde.org/show_bug.cgi?id=427866))
    - 修复载入带有矢量选区的蒙版 ([BUG:428332](https://bugs.kde.org/show_bug.cgi?id=428332))
    - 修复在双击文字对象打开编辑器时文字工具发生的崩溃 ([BUG:427858](https://bugs.kde.org/show_bug.cgi?id=427858))
    - 修复使用在像素选区中使用移动工具时发生的崩溃 ([BUG:428260](https://bugs.kde.org/show_bug.cgi?id=428260))

## 下载

### 中文版信息

- 中文支持：Krita 的正式版本、通过官方新闻发布的公开测试版本 (beta) 均已内建中文支持。
- 自动检测：Krita 在首次安装时会自动设置为操作系统的语言。
- 手动设置：菜单栏 --> Settings 菜单 --> Switch Application Language (倒数第二项) --> 下拉选单 --> 中文 (底部)，重启程序生效。
- 插件翻译：部分内置，G'MIC 插件[需要下载翻译包](https://share.weiyun.com/SBopNjOn)
- 网盘下载：请在官网下载困难时使用。

### Windows 版本

**注意：微软最近更改了 Windows 的数字安全证书信任策略，仅默认信任 Digicert 颁发的证书。Krita 的证书并非由 Digicert 颁发，因此软件包会可能在刚刚发布时遭到系统的 SmartScreen 智能安全筛选功能阻止。如果在下载、运行软件时见到“Windows 已经保护了你的电脑”、“此下载可能危害你的电脑”之类的信息，请点击“更多信息”或者“...”展开，然后点击“保留”或者“仍要运行”按钮。在一定数量的用户通过上述方式允许 Krita 下载运行后，SmartScreen 将不会再阻止它，直到下一个新版发布。**

- **64 位 Windows 安装程序** (推荐) [本站下载](https://download.kde.org/stable/krita/4.4.1/krita-x64-4.4.1-setup.exe) | [网盘下载](https://share.weiyun.com/aVyf2PXQ)
- **64 位 Windows 免安装包** [本站下载](https://download.kde.org/stable/krita/4.4.1/krita-x64-4.4.1.zip) | [网盘下载](https://share.weiyun.com/aVyf2PXQ)
- **64 位程序崩溃调试包** [本站下载](https://download.kde.org/stable/krita/4.4.1/krita-x64-4.4.1-dbg.zip) | [网盘下载](https://share.weiyun.com/aVyf2PXQ)

- **32 位 Windows 安装程序** [本站下载](https://download.kde.org/stable/krita/4.4.1/krita-x86-4.4.1-setup.exe) | [网盘下载](https://share.weiyun.com/wdMnx1WB)
- **32 位 Windows 免安装包** [本站下载](https://download.kde.org/stable/krita/4.4.1/krita-x86-4.4.1.zip) | [网盘下载](https://share.weiyun.com/wdMnx1WB)
- **32 位程序崩溃调试包** [本站下载](https://download.kde.org/stable/krita/4.4.1/krita-x86-4.4.1-dbg.zip) | [网盘下载](https://share.weiyun.com/wdMnx1WB)

- **配套网盘资源 (中文社区维护)** [中文离线文档](https://share.weiyun.com/Dea2uj0M) | [FFmpeg 软件包](https://share.weiyun.com/6tH13bVC) | [G'Mic 滤镜汉化](https://share.weiyun.com/SBopNjOn) |

- 免安装包：解压到任意位置，运行目录中的 Krita 快捷方式。不带文件管理器缩略图插件。与已安装版本共用配置文件和资源，但程序本身相互独立。
- 程序崩溃调试包：解压到 Krita 的安装目录，在报告程序崩溃问题时用于获取回溯追踪数据。日常使用无需下载此包。

### Linux 版本

- **64 位 Linux AppImage 主程序包** [本站下载](https://download.kde.org/stable/krita/4.4.1/krita-4.4.1-x86_64.appimage) | [网盘下载](https://share.weiyun.com/j7Vrjx2m)
- **64 位 Linux AppImage G'Mic-Qt 插件包** [本站下载](https://download.kde.org/stable/krita/4.4.1/gmic_krita_qt-x86_64.appimage) | [网盘下载](https://share.weiyun.com/j7Vrjx2m)
- 如果浏览器把链接作为文本打开，请右键点击链接另存为文件。

### macOS 版本

- **macOS 主程序映像** [本站下载](https://download.kde.org/stable/krita/4.4.1/krita-4.4.1.dmg) | [网盘下载](https://share.weiyun.com/jc82ykle)

- G'Mic-qt 软件包、触摸屏辅助面板在 macOS 下不可用。

### 安卓版本

安卓版本目前尚处于早期测试阶段，可以认为与桌面版本没有差别。它仅为安卓平板和 ChromeBook 类设备进行了初步适配，大部分功能依然需要搭配键盘使用。尽管它也能够在一般智能手机上安装，但会由于屏幕比例和大小等限制而造成界面显示不全，因此我们不建议你在智能手机上使用它。现在安卓版本已经合并到源代码主分支，通过统一流程进行构建，因此它尽管是测试版本，也能正常显示中文界面。

- **64 位 Intel CPU APK 安装包** [本站下载](https://download.kde.org/stable/krita/4.4.1/krita-x86_64-4.4.1-release.apk) | [网盘下载](https://share.weiyun.com/he1kczpd)
- **32 位 Intel CPU APK 安装包** [本站下载](https://download.kde.org/stable/krita/4.4.1/krita-x86-4.4.1-release.apk) | [网盘下载](https://share.weiyun.com/he1kczpd)
- **64 位 ARM CPU APK 安装包** [本站下载](https://download.kde.org/stable/krita/4.4.1/krita-arm64-4.4.1-release.apk) | [网盘下载](https://share.weiyun.com/he1kczpd)
- **32 位 ARM CPU APK 安装包** [本站下载](https://download.kde.org/stable/krita/4.4.1/krita-arm32-4.4.1-release.apk) | [网盘下载](https://share.weiyun.com/he1kczpd)

### 源代码

- [TAR.GZ 格式源代码包](https://download.kde.org/stable/krita/4.4.1/krita-4.4.1.tar.gz)
- [TAR.XZ 格式源代码包](https://download.kde.org/stable/krita/4.4.1/krita-4.4.1.tar.xz)

### md5sum 校验码

适用于上述所有软件包，用于校验下载文件的完整性，不了解文件校验请忽略：

- [ms5sum 校验码文本文件](https://download.kde.org/stable/krita/4.4.1/md5sum.txt)

## 支持 Krita

Krita 是一个自由和开源的软件项目。如果条件允许，请考虑通过 [捐款](https://krita.org/zh/support-us-zh/donation-zh/) 或者 [购买培训教程和画册](https://krita.org/en/shop/) 等方式支持我们的存续和发展，这样我们才能支持开发人员为 Krita 全职工作。

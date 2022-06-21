---
title: "Krita 5.0.2 正式版已经推出"
date: "2022-01-07"
categories: 
  - "news-zh"
  - "officialrelease-zh"
---

紧随 Krita 5.0.0 的步伐，我们今天为大家带来了 Krita 5.0 系列的第一个程序缺陷修复更新：Krita 5.0.2。

为什么跳过了 5.0.1 版发布 5.0.2 版呢？这是因为 Microsoft Store 平台的奇葩机制造成的——我们之前先在 Microsoft Store 上发布过 5.0.0 测试版，然后它就不允许我们发布版本号同为 5.0.0 的正式版了……于是我们不得不把 Microsoft Store 上的 5.0.0 正式版发布为 5.0.1 版，然后真正的 5.0.1 版就这样变成了 5.0.2 版了。

Krita 5.0.2 版包括以下程序缺陷修复：

- 修复了在更改笔刷预设的快速预览设置时的崩溃。
- 修复了存在大写 ABR 扩展名的 ABR 笔刷库预设时的崩溃。[BUG:447454](https://bugs.kde.org/show_bug.cgi?id=447454)
- 修复了存在大写 BUNDLE 扩展名的 Krita 资源包时的崩溃。
- 修复了 macOS 的权利信息以便将 Krita 上传到 Steam。
- 修复了 macOS 的权利信息以便将 Krita 发布到 macOS 应用商店。
- 使 Krita 默认使用 macOS 原生文件对话框。
- 移除 macOS 版内嵌 Python 程序库中的 tkInter 模块。
- 修复 macOS 版在 M1 架构下渲染 16 位整数通道图像。
- 修复了撤销多个图层操作过快时的崩溃。[BUG:447462](https://bugs.kde.org/show_bug.cgi?id=447462)
- 临时应对变形蒙版应用到穿透模式图层组时造成的崩溃。[BUG:447506](https://bugs.kde.org/show_bug.cgi?id=447506)
- 过滤掉 2 个新的 Epic Store 单折线多字符命令行选项。Epic 的弟兄们，通过这种方式传递命令行参数会出事的啊！
- 修复了工具箱箭头按钮在启动 Krita 时不可见。
- 修复了 Photoshop 兼容快捷键方案。[BUG:447771](https://bugs.kde.org/show_bug.cgi?id=447771)
- 修复了将 AppimageUpdate 打包到 appimages。
- 恢复了用 QImageIO 加载 WebP 图像的备用方案。
- 使面板标题栏可以更小。
- 禁用面板的所有快捷键。
- 修复了图像元数据系统中的一处 race 状况。
- 修复了工具选项空间布局偶尔出错的现象。[BUG:447522](https://bugs.kde.org/show_bug.cgi?id=447522)
- 使从 Python 脚本更改选项时正确更新所有填充图层。[BUG:447807](https://bugs.kde.org/show_bug.cgi?id=447807)
- 修复内建文件对话框的图像预览。[BUG:447806](https://bugs.kde.org/show_bug.cgi?id=447806)
- 修复了存在大量资源包时打开和关闭文档的拖慢现象。[BUG:447298](https://bugs.kde.org/show_bug.cgi?id=447298)
- 修复在安卓版中点击外部链接。
- 临时应对安卓版因 Qt 无障碍辅助程序框架造成的一处可能的崩溃。
- 修复了在安卓版中导入资源包。
- 临时应对 ChromeOS 没有正确设置文件权限时造成的问题。

![](images/2021-11-16_kiki-piggy-bank_krita5.png) Krita 是一个自由开源的软件项目，如果条件允许，请考虑通过[捐款](https://fund.krita.org)或[购买视频教程](https://krita.org/en/shop/)等方式为我们提供资金支持。您的支持可以确保 Krita 的核心开发团队成员能够为 Krita 全职工作。

## 下载

### 中文版信息

- 中文支持：Krita 的所有软件包均内建中文支持，首次安装时会自动设置为操作系统的语言。
- 手动设置：菜单栏 --> Settings --> Switch Application Language (倒数第二项) --> 下拉选单 --> 中文 (底部)，重启程序生效。
- 插件翻译：G'MIC 插件[需要下载翻译包](https://share.weiyun.com/SBopNjOn)
- 网盘下载：请在官网下载困难时使用，更新时间可能滞后。

### Windows 版本

- **64 位 Windows 安装程序** [本站下载](https://download.kde.org/stable/krita/5.0.2/krita-x64-5.0.2-setup.exe) | [网盘下载](https://share.weiyun.com/aVyf2PXQ)
- **64 位 Windows 免安装包** [本站下载](https://download.kde.org/stable/krita/5.0.2/krita-x64-5.0.2.zip) | [网盘下载](https://share.weiyun.com/aVyf2PXQ)
- **64 位程序崩溃调试包** [本站下载](https://download.kde.org/stable/krita/5.0.2/krita-x64-5.0.2-dbg.zip) | [网盘下载](https://share.weiyun.com/aVyf2PXQ)

- **配套网盘资源 (中文社区维护)** [中文离线文档](https://share.weiyun.com/Dea2uj0M) | [FFmpeg 软件包](https://share.weiyun.com/6tH13bVC) | [G'Mic 滤镜汉化](https://share.weiyun.com/SBopNjOn) | [Krita 配置文件和资源清理工具](https://share.weiyun.com/SCCloC47)

- 32 位支持：最后一版支持 32 位 Windows 的 Krita 为 4.4.3，[本站下载](https://download.kde.org/stable/krita/4.4.3/krita-x86-4.4.3-setup.exe) | [网盘下载](https://share.weiyun.com/wdMnx1WB)。
- 免安装包：解压到任意位置，运行目录中的 Krita 快捷方式。不带文件管理器缩略图插件，与已安装版本共用配置文件和资源，但程序本身相互独立。
- 程序崩溃调试包：解压到 Krita 的安装目录，在报告程序崩溃问题时用于获取回溯追踪数据。日常使用无需下载此包。

### Linux 版本

- **64 位 Linux AppImage 程序包** [本站下载](https://download.kde.org/stable/krita/5.0.2/krita-5.0.2-x86_64.appimage) | [网盘下载](https://share.weiyun.com/j7Vrjx2m)
- G'Mic 插件已经整合到主程序包中
- 如果浏览器把链接作为文本打开，请右键点击链接另存为文件。

### macOS 版本

- **macOS 程序映像** [本站下载](https://download.kde.org/stable/krita/5.0.2/krita-5.0.2.dmg) | [网盘下载](https://share.weiyun.com/jc82ykle)

- 如果您还在使用 OSX Sierra 或者 High Sierra，请[观看此视频](https://www.youtube.com/watch?v=3py0kgq95Hk)了解如何启动由开发人员签名的可执行软件包。

### 安卓版本

Krita 现在已经能够在 ChromeOS 下正常运行，但其他安卓系统的支持目前尚处于测试阶段。安卓版的整体功能与桌面版本几乎完全相同，它尚未对手机等屏幕狭小细长的设备进行优化，也尚未开发平板专属的模式，因此建议搭配键盘使用。

- **64 位 Intel CPU APK 安装包** [本站下载](https://download.kde.org/stable/krita/5.0.2/krita-x86_64-5.0.2-release-signed.apk) | [网盘下载](https://share.weiyun.com/KXRP4Ec0)
- **32 位 Intel CPU APK 安装包** [本站下载](https://download.kde.org/stable/krita/5.0.2/krita-x86-5.0.2-release-signed.apk) | [网盘下载](https://share.weiyun.com/KXRP4Ec0)
- **64 位 ARM CPU APK 安装包** [本站下载](https://download.kde.org/stable/krita/5.0.2/krita-arm64-v8a-5.0.2-release-signed.apk) | [网盘下载](https://share.weiyun.com/AxnO4CZZ)
- **32 位 ARM CPU APK 安装包** [本站下载](https://download.kde.org/stable/krita/5.0.2/krita-armeabi-v7a-5.0.2-release-signed.apk) | [网盘下载](https://share.weiyun.com/AxnO4CZZ)

### 源代码

- [TAR.GZ 格式源代码包](https://download.kde.org/stable/krita/5.0.2/krita-5.0.2.tar.gz)
- [TAR.XZ 格式源代码包](https://download.kde.org/stable/krita/5.0.2/krita-5.0.2.tar.xz)

### md5sum 校验码

适用于上述所有软件包，用于校验下载文件的完整性。如果您不了解文件校验，忽略即可：

- [ms5sum 校验码文本文件](https://download.kde.org/stable/krita/5.0.2/md5sum.txt)

### 文件完整性验证密钥

Linux 的 Appimage 可执行文件包和源代码的 .tar.gz 和 .tar.xz tarballs 压缩包已经经过数字签名。您可以[在此下载公钥](https://files.kde.org/krita/4DA79EDA231C852B)，还可以在此下载[数字签名的 SIG 文件](https://download.kde.org/stable/krita/5.0.2/)。

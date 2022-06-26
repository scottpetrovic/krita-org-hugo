---
title: "Krita 4.4.2 公开测试第 2 版已经推出"
date: "2020-12-25"
categories: 
  - "development-builds-zh"
---

Krita 开发团队今天推出了 Krita 4.4.2 的公开测试第 2 版。与此同时，Ramon Miranda 也制作了一段视频，专门介绍 4.4.2 的重要新功能之一——曲线网格渐变 (大陆用户需要科学上网)：

https://www.youtube.com/watch?v=DLXWynZT_8s&feature=youtu.be

本版软件在 [公开测试第 1 版](https://krita.org/en/item/first-beta-of-krita-4-4-2/) 的基础上又修复了下列程序缺陷：

- 修复了在应用曲线网格变形时，矢量图层的显示异常问题
- 等角网格能够正常绘制并更新 ([BUG:427833](https://bugs.kde.org/show_bug.cgi?id=427833))
- 三角形拾色器在按比例缩放的显示环境下能够正确响应鼠标事件
- Mypaint 渐变色拾色器的性能和外观都得到了改进
- 修复了在图层组中的动画帧上的变形预览 ([BUG:413968](https://bugs.kde.org/show_bug.cgi?id=413968))
- Krita 现在可以执行连续变形：在变形操作完成后，Shift + 点击图层即可在第一次变形的基础上进行第二次变形
- 新增一个选项，用于反转曲线网格的控制点位置
- 新增一个警告，在 Qt Wayland 平台插件下启动 Krita 时告知用户 Krita 暂时不支持此模式 ([BUG:430426](https://bugs.kde.org/show_bug.cgi?id=430426), [BUG:429079](https://bugs.kde.org/show_bug.cgi?id=429079))
- 修复了选区工具的辅助性界面装饰显示 ([BUG:427658](https://bugs.kde.org/show_bug.cgi?id=427658))
- 修复了在曲线网格功能重写后编辑贝塞尔曲线线段 ([BUG:430377](https://bugs.kde.org/show_bug.cgi?id=430377))
- 修复了填充生成器类图层的加载 ([BUG:430246](https://bugs.kde.org/show_bug.cgi?id=430246), [BUG:430244](https://bugs.kde.org/show_bug.cgi?id=430244))
- 拖放空图层不再造成 Krita 的崩溃 ([BUG:429049](https://bugs.kde.org/show_bug.cgi?id=429049))
- macOS 的 QuickLook 缩略图生成器在此版被暂时停用，因为它可能造成 macOS 访达崩溃 ([BUG:430553](https://bugs.kde.org/show_bug.cgi?id=430553))
- Krita 欢迎界面的图像缩略图可以显示正确的大小 ([BUG:430359](https://bugs.kde.org/show_bug.cgi?id=430359))

Ramon Miranda 为此版软件中提供了 6 组全新笔刷预设：

[![](/images/posts/2020/rgba_brushes.png)](/images/posts/2020/rgba_brushes.png)

## 下载

### 中文版信息

- 中文支持：Krita 的正式版本、通过官方新闻发布的公开测试版本 (beta) 均已内建中文支持。
- 自动检测：Krita 在首次安装时会自动设置为操作系统的语言。
- 手动设置：菜单栏 --> Settings 菜单 --> Switch Application Language (倒数第二项) --> 下拉选单 --> 中文 (底部)，重启程序生效。
- 插件翻译：部分内置，G'MIC 插件[需要下载翻译包](https://share.weiyun.com/SBopNjOn)
- 网盘下载：请在官网下载困难时使用。

### Windows 版本

- **64 位 Windows 安装程序** (推荐) [本站下载](https://download.kde.org/unstable/krita/4.4.2-beta2/krita-x64-4.4.2-beta2-setup.exe) | [网盘下载](https://share.weiyun.com/60HLzj6I)
- **64 位 Windows 免安装包** [本站下载](https://download.kde.org/unstable/krita/4.4.2-beta2/krita-x64-4.4.2-beta2.zip) | [网盘下载](https://share.weiyun.com/60HLzj6I)
- **64 位程序崩溃调试包** [本站下载](https://download.kde.org/unstable/krita/4.4.2-beta2/krita-x64-4.4.2-beta2-dbg.zip) | [网盘下载](https://share.weiyun.com/60HLzj6I)

- **32 位 Windows 安装程序** [本站下载](https://download.kde.org/unstable/krita/4.4.2-beta2/krita-x86-4.4.2-beta2-setup.exe) | [网盘下载](https://share.weiyun.com/Otvc2tpi)
- **32 位 Windows 免安装包** [本站下载](https://download.kde.org/unstable/krita/4.4.2-beta2/krita-x86-4.4.2-beta2.zip) | [网盘下载](https://share.weiyun.com/Otvc2tpi)
- **32 位程序崩溃调试包** [本站下载](https://download.kde.org/unstable/krita/4.4.2-beta2/krita-x86-4.4.2-beta2-dbg.zip) | [网盘下载](https://share.weiyun.com/Otvc2tpi)

- **配套网盘资源** [中文离线文档](https://share.weiyun.com/Dea2uj0M) | [FFmpeg 软件包](https://share.weiyun.com/6tH13bVC) | [G'Mic 滤镜中文翻译包](https://share.weiyun.com/SBopNjOn) |

- 64 位和 32 位：首先尝试 64 位版本，如果无法运行，则尝试 32 位版本
- 免安装包：解压到任意位置，运行目录中的 Krita 快捷方式。不带文件管理器缩略图插件。与已安装版本共用配置文件和资源，但程序本身相互独立。
- 程序崩溃调试包：解压到 Krita 的安装目录，在报告程序崩溃问题时用于获取回溯追踪数据。日常使用无需下载此包。

### Linux 版本

- **64 位 Linux AppImage 主程序包** [本站下载](https://download.kde.org/unstable/krita/4.4.2-beta2/krita-4.4.2-beta2-x86_64.appimage) | [网盘下载](https://share.weiyun.com/C0gZ6joR)
- **64 位 Linux AppImage G'Mic-Qt 插件包** [本站下载](https://download.kde.org/unstable/krita/4.4.2-beta2/gmic_krita_qt-x86_64.appimage) | [网盘下载](https://share.weiyun.com/C0gZ6joR)
- 如果浏览器把链接作为文本打开，请右键点击链接另存为文件。

### macOS 版本

- **macOS 主程序映像** [本站下载](https://download.kde.org/unstable/krita/4.4.2-beta2/krita-4.4.2-beta2.dmg) | [网盘下载](https://share.weiyun.com/gVg0CI53)

- G'Mic-qt 软件包、触摸屏辅助面板在 macOS 下不可用。

### 安卓版本

安卓版本目前尚处于早期测试阶段，也已经自带中文翻译。它仅为安卓平板类、ChromeBook 类设备进行了初步适配，程序功能有诸多不完善之处，大部分功能依然需要搭配键盘使用。

- **64 位 Intel CPU APK 安装包** [本站下载](https://download.kde.org/unstable/krita/4.4.2-beta2/krita-x86_64-4.4.2-beta2.apk) | [网盘下载](https://share.weiyun.com/tEkbnO1K)
- **32 位 Intel CPU APK 安装包** [本站下载](https://download.kde.org/unstable/krita/4.4.2-beta2/krita-x86-4.4.2-beta2.apk) | [网盘下载](https://share.weiyun.com/tEkbnO1K)
- **64 位 ARM CPU APK 安装包** [本站下载](https://download.kde.org/unstable/krita/4.4.2-beta2/krita-arm64-4.4.2-beta2.apk) | [网盘下载](https://share.weiyun.com/tEkbnO1K)
- **32 位 ARM CPU APK 安装包** [本站下载](https://download.kde.org/unstable/krita/4.4.2-beta2/krita-arm32-4.4.2-beta2.apk) | [网盘下载](https://share.weiyun.com/tEkbnO1K)

### 源代码

- [TAR.GZ 格式源代码包](https://download.kde.org/unstable/krita/4.4.2-beta2/krita-4.4.2-beta2.tar.gz)
- [TAR.XZ 格式源代码包](https://download.kde.org/unstable/krita/4.4.2-beta2/krita-4.4.2-beta2.tar.xz)

### md5sum 校验码

适用于上述所有软件包，用于校验下载文件的完整性，不了解文件校验请忽略：

- [ms5sum 校验码文本文件](https://download.kde.org/unstable/krita/4.4.2-beta2/md5sum.txt)

## 支持 Krita

Krita 是一个自由和开源的软件项目。如果条件允许，请考虑通过 [捐款](https://krita.org/zh/support-us-zh/donation-zh/) 或者 [购买培训教程和画册](https://krita.org/en/shop/) 等方式支持我们的存续和发展，这样我们才能支持开发人员为 Krita 全职工作。

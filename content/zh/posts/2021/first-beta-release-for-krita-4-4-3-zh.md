---
title: "Krita 4.4.3 公开测试第 1 版已经推出"
date: "2021-02-24"
categories: 
  - "news-zh"
  - "development-builds-zh"
---

Krita 开发团队已经推出了 Krita 4.4.3 公开测试第 1 版。此版软件修复了一些程序缺陷。

## 程序缺陷修复

### 安卓版本

- 在启动图显示时按后退键会造成程序崩溃
- 在程序正在启动时加载文件会造成程序崩溃
- 为程序资源复制使用 lastUpdateTime
- 为 pathPattern 提供宿主以提高其执行效率
- 修复拾色器覆盖整个屏幕的问题 ([BUG:432459](https://bugs.kde.org/show_bug.cgi?id=432459))
- 已保存的配置文件在重启后不被加载 ([BUG:432433](https://bugs.kde.org/show_bug.cgi?id=432433))
- 添加键函数到 psd_layer_effects_shadow_base ([BUG:432904](https://bugs.kde.org/show_bug.cgi?id=432904))
- 修复重新加载用户导入的资源包中的预设 ([BUG:432488](https://bugs.kde.org/show_bug.cgi?id=432488))

### 程序崩溃

- 修复半调滤镜因无效指针造成的崩溃
- 修复重新应用滤镜并显示对话框时的崩溃
- 修复在通过矢量选区创建的滤镜蒙版上绘制时的崩溃 ([BUG:432329](http://432329))

### macOS 版本

- macOS：修复访达插件显示缩略图或快速预览时的问题 ([BUG:432328](https://bugs.kde.org/show_bug.cgi?id=432328))

### 脚本功能

- 修复通道标记处理。感谢 Chris Venter (克里斯·文特) 提供补丁 ([BUG:432226](https://bugs.kde.org/show_bug.cgi?id=432226))

### 稳定性和性能增强

- 修复画布视图和 F5 面板绘图区的缩放率同步
- 修复智能补丁工具的归一化 ([BUG:430953](https://bugs.kde.org/show_bug.cgi?id=430953))
- 修复前景色/背景色按钮的性能问题 ([BUG:432936](https://bugs.kde.org/show_bug.cgi?id=432936))
- 修复增量备份的保存 ([BUG:432701](https://bugs.kde.org/show_bug.cgi?id=432701))
- 修复 F5 面板绘图区无响应 ([BUG:431708](https://bugs.kde.org/show_bug.cgi?id=431708))
- 修复自定义笔尖和剪贴板笔尖的颜色作为透明度和保持透明度模式 ([BUG:432274](https://bugs.kde.org/show_bug.cgi?id=432274))
- 修复 RGBA_brushes 资源包，让 Krita 在启动时不再尝试重新创建它 [(BUG:431832](https://bugs.kde.org/show_bug.cgi?id=431832))
- 修复在 KisAngleSelector 中当数字输入框必须扁平显示并在所有位置使用新型角度选择器时的显示风格问题

## 下载

### 中文版信息

- 中文支持：Krita 的正式版本、通过官方新闻发布的公开测试版本 (beta) 均已内建中文支持。
- 自动检测：Krita 在首次安装时会自动设置为操作系统的语言。
- 手动设置：菜单栏 --> Settings 菜单 --> Switch Application Language (倒数第二项) --> 下拉选单 --> 中文 (底部)，重启程序生效。
- 插件翻译：部分内置，G'MIC 插件[需要下载翻译包](https://share.weiyun.com/SBopNjOn)
- 网盘下载：请在官网下载困难时使用。

### Windows 版本

- **64 位 Windows 安装程序** (推荐) [本站下载](https://download.kde.org/unstable/krita/4.4.3-beta1/krita-x64-4.4.3-beta1-setup.exe) | [网盘下载](https://share.weiyun.com/60HLzj6I)
- **64 位 Windows 免安装包** [本站下载](https://download.kde.org/unstable/krita/4.4.3-beta1/krita-x64-4.4.3-beta1.zip) | [网盘下载](https://share.weiyun.com/60HLzj6I)
- **64 位程序崩溃调试包** [本站下载](https://download.kde.org/unstable/krita/4.4.3-beta1/krita-x64-4.4.3-beta1-dbg.zip) | [网盘下载](https://share.weiyun.com/60HLzj6I)

- **32 位 Windows 安装程序** [本站下载](https://download.kde.org/unstable/krita/4.4.3-beta1/krita-x86-4.4.3-beta1-setup.exe) | [网盘下载](https://share.weiyun.com/Otvc2tpi)
- **32 位 Windows 免安装包** [本站下载](https://download.kde.org/unstable/krita/4.4.3-beta1/krita-x86-4.4.3-beta1.zip) | [网盘下载](https://share.weiyun.com/Otvc2tpi)
- **32 位程序崩溃调试包** [本站下载](https://download.kde.org/unstable/krita/4.4.3-beta1/krita-x86-4.4.3-beta1-dbg.zip) | [网盘下载](https://share.weiyun.com/Otvc2tpi)

- **配套网盘资源 (中文社区维护)** [中文离线文档](https://share.weiyun.com/Dea2uj0M) | [FFmpeg 软件包](https://share.weiyun.com/6tH13bVC) | [G'Mic 滤镜汉化](https://share.weiyun.com/SBopNjOn) |

- 免安装包：解压到任意位置，运行目录中的 Krita 快捷方式。不带文件管理器缩略图插件。与已安装版本共用配置文件和资源，但程序本身相互独立。
- 程序崩溃调试包：解压到 Krita 的安装目录，在报告程序崩溃问题时用于获取回溯追踪数据。日常使用无需下载此包。

### Linux 版本

- **64 位 Linux AppImage 主程序包** [本站下载](https://download.kde.org/unstable/krita/4.4.3-beta1/krita-4.4.3-beta1-x86_64.appimage) | [网盘下载](https://share.weiyun.com/C0gZ6joR)
- **64 位 Linux AppImage G'Mic-Qt 插件包** [本站下载](https://download.kde.org/unstable/krita/4.4.3-beta1/gmic_krita_qt-x86_64.appimage) | [网盘下载](https://share.weiyun.com/C0gZ6joR)
- 如果浏览器把链接作为文本打开，请右键点击链接另存为文件。

### macOS 版本

- **macOS 主程序映像** [本站下载](https://download.kde.org/unstable/krita/4.4.3-beta1/krita-4.4.3-beta1.dmg) | [网盘下载](https://share.weiyun.com/gVg0CI53)

- G'Mic-qt 软件包、触摸屏辅助面板在 macOS 下不可用。

### 安卓版本

安卓版本目前尚处于早期测试阶段，整体功能与桌面版本几乎完全相同。它仅为安卓平板和 ChromeBook 类设备进行了初步适配，大部分功能依然需要搭配键盘使用。尽管它也能够在一般智能手机上安装，但受屏幕大小和宽高比所限会造成界面显示不全，我们不建议你在智能手机上使用它。随正式版发布的安卓版本现在可以正常显示中文界面。

- **64 位 Intel CPU APK 安装包** [本站下载](https://download.kde.org/unstable/krita/4.4.3-beta1/krita_build_apk-release-x86_64-unsigned.apk) | [网盘下载](https://share.weiyun.com/tEkbnO1K)
- **32 位 Intel CPU APK 安装包** [本站下载](https://download.kde.org/unstable/krita/4.4.3-beta1/krita_build_apk-release-x86_unsigned.apk) | [网盘下载](https://share.weiyun.com/tEkbnO1K)
- **64 位 ARM CPU APK 安装包** [本站下载](https://download.kde.org/unstable/krita/4.4.3-beta1/krita_build_apk-release-arm64-v8a-unsigned.apk) | [网盘下载](https://share.weiyun.com/tEkbnO1K)
- **32 位 ARM CPU APK 安装包** [本站下载](https://download.kde.org/unstable/krita/4.4.3-beta1/krita_build_apk-release-armeabi-v7a-unsigned.apk) | [网盘下载](https://share.weiyun.com/tEkbnO1K)

### 源代码

- [TAR.GZ 格式源代码包](https://download.kde.org/unstable/krita/4.4.3-beta1/krita-4.4.3-beta1.tar.gz)
- [TAR.XZ 格式源代码包](https://download.kde.org/unstable/krita/4.4.3-beta1/krita-4.4.3-beta1.tar.xz)

### md5sum 校验码

适用于上述所有软件包，用于校验下载文件的完整性，不了解文件校验请忽略：

- [ms5sum 校验码文本文件](https://download.kde.org/unstable/krita/4.4.3-beta1/md5sum.txt)

### 文件完整性验证密钥

Linux 的 Appimage 可执行文件包和源代码的 .tar.gz 和 .tar.xz tarballs 压缩包已经经过数字签名。你可以通过 GPG 取回公共密钥，命令为 gpg --recv-key 7468332F 。你可以在此下载 [数字签名的 SIG 文件](https://download.kde.org/unstable/krita/4.4.3-beta1/)。

## 支持 Krita

Krita 是一个自由和开源的软件项目。如果条件允许，请考虑通过 [捐款](https://krita.org/zh/support-us-zh/donation-zh/) 或者 [购买培训教程和画册](https://krita.org/en/shop/) 等方式支持我们的存续和发展，这样我们才能支持开发人员为 Krita 全职工作。

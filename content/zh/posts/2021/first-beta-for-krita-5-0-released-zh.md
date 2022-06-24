---
title: "Krita 5.0 公开测试第 1 版已经推出"
date: "2021-08-18"
categories: 
  - "news-zh"
  - "development-builds-zh"
---

今天 Krita 开发团队为大家带来了 Krita 5.0 的公开测试第 1 版。Krita 5.0 是一次重大更新版本，它包含了大量新功能和程序功能的变更。

[![](/images/posts/2021/electrichearts_20201224A_kiki_c1_1080P-1024x512.png)](/images/posts/2021/electrichearts_20201224A_kiki_c1_1080P.png) Krita 5.0 新版启动图，由 Tyson Tan (钛山) 绘制

### Krita 5.0 使用前注意事项

- Krita 5 完全重写了资源管理系统。Krita 不再需要在每次启动时扫描并加载全部笔刷、图案、渐变和其他资源，而是在首次启动时扫描资源，然后将资源信息写入一个缓存数据库中以便日后直接调用。这意味着 Krita 会在首次启动时耗费较长时间，但日后的启动将明显变快。
- Krita 5 会为用户编辑的资源保存一组版本历史数据，此功能与 Krita 4 不兼容。如果您升级到了 Krita 5，之后又降级回 Krita 4，将可能造成 Krita 4 显示重复的资源。
- Krita 5 不再支持加载 Krita 3 和更早版本的矢量图层。
- Krita 5 创建的 Krita 图像文件 (.kra) 和 Krita 笔刷预设文件 (.kpp) 不能保证与 Krita 4 兼容。
- Krita 5 修复了[一个与图像内嵌文字大小有关的程序缺陷](https://krita.org/en/krita-5-0-release-notes/#text_size_dpi_issue_fix)，但是打开旧版 Krita 创建的图像时可能需要[手动更改一处设置](https://docs.krita.org/en/reference_manual/preferences/general_settings.html#miscellaneous)才能显示文字的原先大小。
- Krita 5 的 G'Mic 插件存在一处程序缺陷，执行 G'Mic 滤镜将造成 Krita 设置暂时重置为默认值。此时重新启动 Krita 即可恢复之前设置状态。
- 如果您在使用色彩管理功能并使用了显示器的特性文件，多功能拾色器的三角形区域可能会无法显示。请在菜单栏-设置-色彩管理页面关闭“允许 LittleCMS 优化”，或者在拾色器设置页面改用四方形拾色器形状。
- 相似颜色选区工具的“颜色容差”选项显示的数值不是实际记忆的数值，请在每次使用时拖动一次滑动条以初始化它。

### Krita 5.0 的新功能

Krita 5.0 带来了众多新功能，详情请查看[完整发行日志](https://krita.org/zh/krita-5-0-release-notes-zh/)。下面仅介绍一些比较重要的方面：

- 开发历时 5 年的全新资源管理系统
- 渐变抖动和宽色域渐变
- 通过 LittleCMS fastfloat 插件提高了程序性能
- 新增 MyPaint 笔刷引擎
- 颜色涂抹笔刷引擎完全重写
- 动画时间轴面板重新设计
- 动画克隆帧功能
- 动画曲线面板更新
- 动画可使用变形蒙版
- 全新分镜头面板
- 图标设计更新和界面打磨
- 支持 HEIF、AVIF、WebP 图像文件格式
- TIFF 图像支持改进
- 全新的绘画过程录像工具
- 全新的两点透视辅助尺，以及辅助尺的限制工作区域功能
- 变形工具预览可以按照图层组混合后的效果显示
- 粘贴到当前图层而不是粘贴为新图层功能
- G'Mic 插件现已支持 macOS

对中文用户而言，Krita 5.0 全面改进了中文支持：

- 支持中文标签
- 支持中文资源名称
- 鼠标悬停于资源时显示资源的中文译名
- 所有输入框均可输入中文
- 调整了默认字体，改善可读性
- 之前不显示中文翻译的少数按钮现已全部正常显示中文
- 欢迎画面的新闻板块可以选择显示中文文章
- 帮助菜单的使用手册链接可以自动跳转到中文文档
- 中文文档网站的搜索框可以有限搜索中文关键词

除此之外，Krita 5.0 还包括了许多功能和性能方面的小幅改进。在此不再赘述。

[![Krita in the old oxygen style](/images/posts/2021/krita-style-change-1024x533.png)](/images/posts/2021/krita-style-change.png)

我们希望能在今年 9 月份发布 Krita 5.0 的正式版本，但我们无法确保能按期发布。我们接下来将要继续修复在测试版中发现的问题，尽可能保证 Krita 5.0 正式发布时的可靠性。为了支持 Krita 的开发工作，请在条件允许时考虑向 [Krita 发展基金](https://fund.krita.org/)捐款：

[![](/images/posts/2021/devfund-1024x346.png)](https://fund.krita.org)

## 下载

### 中文版信息

- 中文支持：Krita 的所有软件包均内建中文支持，首次安装时会自动设置为操作系统的语言。
- 手动设置：菜单栏 --> Settings --> Switch Application Language (倒数第二项) --> 下拉选单 --> 中文 (底部)，重启程序生效。
- 插件翻译：G'MIC 插件[需要下载翻译包](https://share.weiyun.com/SBopNjOn)
- 网盘下载：请在官网下载困难时使用，更新时间可能滞后。

### Windows 版本

- **64 位 Windows 安装程序** [本站下载](https://download.kde.org/unstable/krita/5.0.0-beta1/krita-x64-5.0.0-beta1-setup.exe) | [网盘下载](https://share.weiyun.com/60HLzj6I)
- **64 位 Windows 免安装包** [本站下载](https://download.kde.org/unstable/krita/5.0.0-beta1/krita-x64-5.0.0-beta1.zip) | [网盘下载](https://share.weiyun.com/60HLzj6I)
- **64 位程序崩溃调试包** [本站下载](https://download.kde.org/unstable/krita/5.0.0-beta1/krita-x64-5.0.0-beta1-dbg.zip) | [网盘下载](https://share.weiyun.com/60HLzj6I)

- **配套网盘资源 (中文社区维护)** [中文离线文档](https://share.weiyun.com/Dea2uj0M) | [FFmpeg 软件包](https://share.weiyun.com/6tH13bVC) | [G'Mic 滤镜汉化](https://share.weiyun.com/SBopNjOn) |

- 32 位支持：最后一版支持 32 位 Windows 的 Krita 为 4.4.3，[本站下载](https://download.kde.org/stable/krita/4.4.3/krita-x86-4.4.3-setup.exe) | [网盘下载](https://share.weiyun.com/wdMnx1WB)。
- 免安装包：解压到任意位置，运行目录中的 Krita 快捷方式。不带文件管理器缩略图插件，与已安装版本共用配置文件和资源，但程序本身相互独立。
- 程序崩溃调试包：解压到 Krita 的安装目录，在报告程序崩溃问题时用于获取回溯追踪数据。日常使用无需下载此包。

### Linux 版本

- **64 位 Linux AppImage 程序包** [本站下载](https://download.kde.org/unstable/krita/5.0.0-beta1/krita-5.0.0-beta1-x86_64.appimage) | [网盘下载](https://share.weiyun.com/C0gZ6joR)
- 从此版开始，G'Mic 插件已经整合到主程序包中
- 如果浏览器把链接作为文本打开，请右键点击链接另存为文件。

### macOS 版本

- **macOS 程序映像** [本站下载](https://download.kde.org/unstable/krita/5.0.0-beta1/krita-5.0.0-beta1.dmg) | [网盘下载](https://share.weiyun.com/gVg0CI53)

- 如果您还在使用 OSX Sierra 或者 High Sierra，请[观看此视频](https://www.youtube.com/watch?v=3py0kgq95Hk)了解如何启动由开发人员签名的可执行软件包。

### 安卓版本

安卓版本目前尚处于早期测试阶段，整体功能与桌面版本几乎完全相同。它仅为安卓平板和 ChromeBook 类设备进行了初步适配，大部分功能依然需要搭配键盘使用，还有不少功能无法正常工作。

- **64 位 Intel CPU APK 安装包** [本站下载](https://download.kde.org/unstable/krita/5.0.0-beta1/krita-x86_64-5.0.0-beta1-release-signed.apk) | [网盘下载](https://share.weiyun.com/tEkbnO1K)
- **32 位 Intel CPU APK 安装包** [本站下载](https://download.kde.org/unstable/krita/5.0.0-beta1/krita-x86-5.0.0-beta1-release-signed.apk) | [网盘下载](https://share.weiyun.com/tEkbnO1K)
- **64 位 ARM CPU APK 安装包** [本站下载](https://download.kde.org/unstable/krita/5.0.0-beta1/krita-arm64-v8a-5.0.0-beta1-release-signed.apk) | [网盘下载](https://share.weiyun.com/tEkbnO1K)
- **32 位 ARM CPU APK 安装包** [本站下载](https://download.kde.org/unstable/krita/5.0.0-beta1/krita-armeabi-v7a-5.0.0-beta1-release-signed.apk) | [网盘下载](https://share.weiyun.com/tEkbnO1K)

### 源代码

- [TAR.GZ 格式源代码包](https://download.kde.org/unstable/krita/5.0.0-beta1/krita-5.0.0-beta1.tar.gz)
- [TAR.XZ 格式源代码包](https://download.kde.org/unstable/krita/5.0.0-beta1/krita-5.0.0-beta1.tar.xz)

### md5sum 校验码

适用于上述所有软件包，用于校验下载文件的完整性，不了解文件校验请忽略：

- [ms5sum 校验码文本文件](https://download.kde.org/unstable/krita/5.0.0-beta1/md5sum.txt)

### 文件完整性验证密钥

Linux 的 Appimage 可执行文件包和源代码的 .tar.gz 和 .tar.xz tarballs 压缩包已经经过数字签名。您可以[在此下载公钥](https://files.kde.org/krita/4DA79EDA231C852B)，还可以在此下载[数字签名的 SIG 文件](https://download.kde.org/unstable/krita/5.0.0-beta1/)。

## 请支持 Krita

Krita 是一个自由和开源的软件项目。如果条件允许，请考虑通过 [捐款](https://fund.krita.org/) 或者 [购买培训教程和画册](https://krita.org/en/shop/) 等方式支持我们的存续和发展，这样我们才能支持开发人员为 Krita 全职工作。

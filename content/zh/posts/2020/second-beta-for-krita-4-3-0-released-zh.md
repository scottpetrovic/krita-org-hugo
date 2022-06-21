---
title: "Krita 4.3.0 第 2 测试版和中文翻译改进"
date: "2020-06-02"
categories: 
  - "development-builds-zh"
---

今天我们发布了 Krita 4.3.0 beta 2 测试版。这次发布晚于我们的时间表，这是因为 KDE 的开发平台迁移至 GitLab 时造成了延误。请试用此版本软件，并向我们反馈遇到的问题。

### 程序改进

和 beta 1 相比，beta 2 有下列改进：

- 修复在使用手绘路径工具和曲线工具时拾取颜色 ([BUG:373037](https://bugs.kde.org/show_bug.cgi?id=373037))
- 修复更改图像分辨率后的缩放 ([BUG:421797](https://bugs.kde.org/show_bug.cgi?id=421797))
- 防抖和平滑 - 最强模式现在强制距离与视图缩放成比例 ([BUG:421314](https://bugs.kde.org/show_bug.cgi?id=421314))
- 确保 CMYK 图像的通道缩略图不反相显示 ([BUG:421442](https://bugs.kde.org/show_bug.cgi?id=421442))
- 确保增量备份可保存在与增量备份文件名相同的文件夹中 ([BUG:421792](https://bugs.kde.org/show_bug.cgi?id=421792))
- 处理图像和节点对象的 Python API 现在是 synchronous 的，再也无需加入额外的 waitForDone 呼叫 ([BUG:401497](https://bugs.kde.org/show_bug.cgi?id=401497))
- 改进了在 macOS 下的画布快捷键的修饰键工作 ( [BUG:372646](https://bugs.kde.org/show_bug.cgi?id=372646), [BUG:373299](https://bugs.kde.org/show_bug.cgi?id=373299), [BUG:391088](https://bugs.kde.org/show_bug.cgi?id=391088))
- 实现了对 Wacom 数位板的原生触摸模式的支持。感谢 P. Varet 提供程序补丁 ([BUG:421295](https://bugs.kde.org/show_bug.cgi?id=4221295))
- 修复某些情况下图像需要很长时间才能保存 ([BUG:421584](https://bugs.kde.org/show_bug.cgi?id=421584))
- 让文字工具的默认文字更加简短且可翻译 ([BUG:421663](https://bugs.kde.org/show_bug.cgi?id=421663))
- 按住 Shift 点击图层单独显示时不会再更改全部图层的显示/隐藏状态
- 不再渲染在性能设置页指定区域外的动画帧
- 让自动保存恢复对话框更易读 ([BUG:420014](https://bugs.kde.org/show_bug.cgi?id=420014))
- 在单独显示图层时正确回放动画和显示洋葱皮视图 ([BUG:394199](https://bugs.kde.org/show_bug.cgi?id=394199))
- 修复 Windows 下文字工具对话框的默认位置 ([BUG:419529](https://bugs.kde.org/show_bug.cgi?id=419529))
- 修复色域蒙版渲染 ([BUG:421142](https://bugs.kde.org/show_bug.cgi?id=421142))
- 修复小面积或者复杂选区轮廓的蚂蚁线显示效果 ([BUG:407868](https://bugs.kde.org/show_bug.cgi?id=407868), [BUG:419240](https://bugs.kde.org/show_bug.cgi?id=419240), [BUG:413220](https://bugs.kde.org/show_bug.cgi?id=413220))
- 载入图像后动画时间轴依然可以正确高亮当前帧 ([BUG:403854](https://bugs.kde.org/show_bug.cgi?id=403854))
- 裁切图像后依然可以正确对齐洋葱皮视图 ([BUG:419462](https://bugs.kde.org/show_bug.cgi?id=419462))
- 修复某些尺寸的动画渲染 ([BUG:396128](https://bugs.kde.org/show_bug.cgi?id=396128))
- 将拆分图层对话框的默认值调整得更加合理
- 修复从画布拾取同一颜色时对橡皮擦模式进行重置 ([BUG:415476](https://bugs.kde.org/show_bug.cgi?id=415476))
- 修复图层和通道缩略图的宽高比
- 将被挤压的复选框的未挤压文字显示为工具提示 ([BUG:415117](https://bugs.kde.org/show_bug.cgi?id=415117))
- 新增多处翻译上下文数据
- 修复在选区描边对话框选择颜色 ([BUG:411482](https://bugs.kde.org/show_bug.cgi?id=411482))
- 修复由 Python 创建的图像的内存管理问题 ([BUG:412740](https://bugs.kde.org/show_bug.cgi?id=412740))

特别感谢 Rafał Mikrut 针对内存管理和指针访问编写的大量修复。

### 中文翻译改进

Krita 4.3.0 beta 2 已经合并了大部分简体中文翻译的改进：

- 以简明、易读和易懂为标准，重新翻译了几乎所有的菜单项、工具选项、面板、对话框和混合模式。
- 除少数情况，绝大多数与 PS/SAI 对应的项目已经与它们统一翻译，或者同时注释两者翻译。如工具箱图标悬停信息、混合模式名称等。
- 过长的菜单项和选项名称被缩减、分节，更加易读。如从外部拖放图像进窗口的对话框和文件对话框。
- 并列显示的项目尽可能翻译为相等字数，如欢迎页面、新建图像对话框的模板列表等。
- 大部分文字以中文重写而非翻译。如手绘笔刷工具的工具选项、各个面板、设置对话框、工具栏的空白占位符翻译等。
- 原文因为英文字数限制过于简练的，添加中文注释。如工具箱工具图标的悬停信息、设置对话框的选项等。
- 官方网站的中文翻译已大幅改进，特别辟出[中文社区页面](https://krita.org/zh/get-involved-zh/overview-zh/)。
- Krita 的文档已经完成翻译 90% 以上，但因为 KDE 翻译 SVN 正在调整，成果尚未同步到文档网站。
- [中文翻译参与指南](https://krita.org/zh/get-involved-zh/krita-chinese-translation/)已经完成。我们欢迎有志之士参与 Krita 的中文翻译工作，尤其是文档剩余的实例教程。

[![Kiki among the waterlilies](images/kiki_4.3.3_sm-1024x512.png)](https://krita.org/wp-content/uploads/2020/05/kiki_4.3.3_sm.png)

[你还可以查看完整的 4.3 版新功能介绍页面](https://krita.org/en/krita-4-3-release-notes/)了解更全面的情况。

## 下载

### 中文版信息

- 中文支持：Krita 的正式版本、通过官方新闻发布的 beta 测试版本均已内建中文支持。
- 自动检测：Krita 在首次安装时会自动设置为操作系统的语言。
- 手动设置：菜单栏 --> Settings 菜单 --> Switch Application Language (倒数第二项) --> 下拉选单 --> 中文 (底部)，重启程序生效。
- 微云下载：非官方维护，请仅在官网下载缓慢、同步滞后时使用。

### Windows 版本

- **64 位 Windows 安装程序** (推荐) [本站下载](https://download.kde.org/unstable/krita/4.3.0-beta2/krita-x64-4.3.0-beta2-setup.exe) | [微云下载](https://share.weiyun.com/60HLzj6I)
- **64 位 Windows 免安装包** [本站下载](https://download.kde.org/unstable/krita/4.3.0-beta2/krita-x64-4.3.0-beta2.zip) | [微云下载](https://share.weiyun.com/60HLzj6I)
- **64 位调试包** [本站下载](https://download.kde.org/unstable/krita/4.3.0-beta2/krita-x64-4.3.0-beta2-dbg.zip) | [微云下载](https://share.weiyun.com/60HLzj6I)

- **32 位 Windows 安装程序** [本站下载](https://download.kde.org/unstable/krita/4.3.0-beta2/krita-x86-4.3.0-beta2-setup.exe) | [微云下载](https://share.weiyun.com/Otvc2tpi)
- **32 位 Windows 免安装包** [本站下载](https://download.kde.org/unstable/krita/4.3.0-beta2/krita-x86-4.3.0-beta2.zip) | [微云下载](https://share.weiyun.com/Otvc2tpi)
- **32 位调试包** [本站下载](https://download.kde.org/unstable/krita/4.3.0-beta2/krita-x86-4.3.0-beta2-dbg.zip) | [微云下载](https://share.weiyun.com/Otvc2tpi)

- 免安装包：解压到任意位置，运行目录中的 Krita 快捷方式。不带文件管理器缩略图插件。与已安装版本共用配置文件和资源，但程序本身相互独立。
- 调试包：解压到 Krita 的安装目录，在报告程序崩溃问题时用于获取回溯追踪数据。日常使用无需下载此包。

### Linux 版本

- **64 位 Linux AppImage 主程序包** [本站下载](https://download.kde.org/unstable/krita/4.3.0-beta2/krita-4.3.0-beta2-x86_64.appimage) | [微云下载](https://share.weiyun.com/C0gZ6joR)
- **64 位 Linux AppImage G'Mic-Qt 插件包** [本站下载](https://download.kde.org/unstable/krita/4.3.0-beta2/gmic_krita_qt-x86_64.appimage) | [微云下载](https://share.weiyun.com/C0gZ6joR)
- Appimage 包不支持在动画中使用音频。
- 如果浏览器把链接作为文本打开，请右键点击链接另存为文件。

### macOS 版本

- **macOS 主程序映像** [本站下载](https://download.kde.org/unstable/krita/4.3.0-beta2/krita-4.3.0-beta2.dmg) | [微云下载](https://share.weiyun.com/gVg0CI53)

- G'Mic-qt 软件包、触摸屏辅助面板在 macOS 下不可用。

### 安卓版本

安卓版本目前尚处于早期测试阶段，它的功能和普通版本完全相同，仅为平板设备和 ChromeBook 进行了初步优化。尽管它能够在一般智能手机上安装，我们依然不建议你在智能手机上使用它。它通过 Git 源代码直接构建，不包含正式版的翻译文件，因此只能显示英文界面。此版除了版本号外，功能和 beta 2 一致。新版改进包括：可以从 Google Drive 载入 KRA 文件，修复了一些三星设备的菜单栏问题，支持 三星 Air 手势。

- [64 bits Intel CPU APK 安装包](https://download.kde.org/unstable/krita/4.3.0-beta2/krita-x86_64-signed.apk) | [微云下载](https://share.weiyun.com/tEkbnO1K)
- [32 bits Intel CPU APK 安装包](https://download.kde.org/unstable/krita/4.3.0-beta2/krita-x86-signed.apk) | [微云下载](https://share.weiyun.com/tEkbnO1K)
- [64 bits Arm CPU APK 安装包](https://download.kde.org/unstable/krita/4.3.0-beta2/krita-arm64-signed.apk) | [微云下载](https://share.weiyun.com/tEkbnO1K)
- [32 bits Arm CPU APK 安装包](https://download.kde.org/unstable/krita/4.3.0-beta2/krita-arm32-signed.apk) | [微云下载](https://share.weiyun.com/tEkbnO1K)
- [Google Play Store 页面](https://play.google.com/store/apps/details?id=org.krita)

### 源代码

- [TAR.GZ 格式源代码包](https://download.kde.org/unstable/krita/4.3.0-beta2/krita-4.3.0-beta2.tar.gz)
- [TAR.XZ 格式源代码包](https://download.kde.org/unstable/krita/4.3.0-beta2/krita-4.3.0-beta2.tar.xz)

### md5sum 校验码

适用于上述所有软件包，用于校验下载文件的完整性，不了解文件校验请忽略：

- [ms5sum 校验码文本文件](https://download.kde.org/unstable/krita/4.3.0-beta2/md5sum.txt)

## 支持 Krita

Krita 是一个自由和开源的软件项目。如果条件允许，请考虑通过 [捐款](https://krita.org/en/support-us/donations/) 或者 [购买培训教程和画册](https://krita.org/en/support-us/shop) 等方式支持我们的存续和发展，这样我们才能支持开发人员为 Krita 全职工作。

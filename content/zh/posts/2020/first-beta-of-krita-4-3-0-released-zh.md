---
title: "Krita 4.3.0 第 1 测试版和中文翻译动向"
date: "2020-05-04"
categories: 
  - "development-builds-zh"
---

Krita 4.3.0 将是 Krita 的下一个大版本更新。我们的开发人员已经努力了整整一年，重点关注提高程序的性能和稳定性。包括手绘笔刷工具和选区工具在内的大量工具将在此版本得到显著的性能提升。我们还将在此版带来一些新功能，其中有不少是由各国的志愿者打造的。我们正在准备的[新版说明](https://krita.org/en/krita-4-3-release-notes/)已经列出了详尽的更新内容。

与此同时，Krita 软件、文档、网站的中文版本也将迎来一次全面更新。Krita 全套文档的中文翻译工作已经接近尾声。在完全掌握了软件全部功能设计思路的情况下，中文版的写作指导思想已从“逐字翻译”转向“按照实际条件和语言习惯重新组织语言”，和“对接行业标准软件习惯用词”，力求减轻新老用户的自学难度。使用指南 (文档) 虽然已经接近翻译完毕，但目前尚未完全同步到网站，且同步后的早期可能会有大量条目与软件更新后的状态不符，估计会在今年内陆续修订完毕。在官方网站设计师 Scott Petrovic 的协助下，曾经困扰官方网站中文版的各种技术问题正在被陆续解决，还加入了专门为中文用户准备的各种体贴功能。我们会在现有框架下尽可能创造条件，让 Krita 的中文用户用得更加舒心。

[![Kiki among the waterlilies](/images/posts/2020/kiki_4.3.3_sm-1024x512.png)](https://krita.org/wp-content/uploads/2020/05/kiki_4.3.3_sm.png)

请大家下载体验，并协助我们测试 Krita 4.3.0 的第一个 beta 测试版吧！

## 下载

### 中文版信息

- 中文支持：Krita 的正式版本、通过官方新闻发布的 beta 测试版本均已内建中文支持。
- 自动检测：Krita 在首次安装时会自动设置为操作系统的语言。
- 手动设置：菜单栏 --> Settings 菜单 --> Switch Application Language (倒数第二项) --> 下拉选单 --> 中文 (底部)，重启程序生效。
- 微云下载：非官方维护，请仅在官网下载缓慢、同步滞后时使用。

### Windows 版本

- **64 位 Windows 安装程序** (推荐) [本站下载](https://download.kde.org/unstable/krita/4.3.0-beta1/krita-x64-4.3.0-beta1-setup.exe) | [微云下载](https://share.weiyun.com/uHKk36c3)
- **64 位 Windows 免安装包** [本站下载](https://download.kde.org/unstable/krita/4.3.0-beta1/krita-x64-4.3.0-beta1.zip) | [微云下载](https://share.weiyun.com/uHKk36c3)
- **64 位调试包** [本站下载](https://download.kde.org/unstable/krita/4.3.0-beta1/krita-x64-4.3.0-beta1-dbg.zip) | [微云下载](https://share.weiyun.com/uHKk36c3)

- **32 位 Windows 安装程序** [本站下载](https://download.kde.org/unstable/krita/4.3.0-beta1/krita-x86-4.3.0-beta1-setup.exe) | [微云下载](https://share.weiyun.com/uHKk36c3)
- **32 位 Windows 免安装包** [本站下载](https://download.kde.org/unstable/krita/4.3.0-beta1/krita-x86-4.3.0-beta1.zip) | [微云下载](https://share.weiyun.com/uHKk36c3)
- **32 位调试包** [本站下载](https://download.kde.org/unstable/krita/4.3.0-beta1/krita-x86-4.3.0-beta1-dbg.zip) | [微云下载](https://share.weiyun.com/uHKk36c3)

- 免安装包：解压到任意位置，运行目录中的 Krita 快捷方式。不带文件管理器缩略图插件。与已安装版本共用配置文件和资源，但程序本身相互独立。
- 调试包：解压到 Krita 的安装目录，在报告程序崩溃问题时用于获取回溯追踪数据。日常使用无需下载此包。

### Linux 版本

- **64 位 Linux AppImage 主程序包** [本站下载](https://download.kde.org/unstable/krita/4.3.0-beta1/krita-4.3.0-beta1-x86_64.appimage) | [微云下载](https://share.weiyun.com/uHKk36c3)
- **64 位 Linux AppImage G'Mic-Qt 插件包** [本站下载](https://download.kde.org/unstable/krita/4.3.0-beta1/gmic_krita_qt-x86_64.appimage) | [微云下载](https://share.weiyun.com/uHKk36c3)

- Appimage 包不支持在动画中使用音频。
- 如果浏览器把链接作为文本打开，请右键点击链接另存为文件。

### macOS 版本

- **macOS 主程序映像** [本站下载](https://download.kde.org/unstable/krita/4.3.0-beta1/krita-4.3.0-beta1.dmg) | [微云下载](https://share.weiyun.com/uHKk36c3)

- G'Mic-qt 软件包、触摸屏辅助面板在 macOS 下不可用。

### 源代码

- [TAR.GZ 格式源代码包](https://download.kde.org/unstable/krita/4.3.0-beta1/krita-4.3.0-beta1.tar.gz)
- [TAR.XZ 格式源代码包](https://download.kde.org/unstable/krita/4.3.0-beta1/krita-4.3.0-beta1.tar.xz)

### md5sum 校验码

适用于上述所有软件包，用于校验下载文件的完整性，不了解文件校验请忽略：

- [ms5sum 校验码文本文件](https://download.kde.org/unstable/krita/4.3.0-beta1/md5sum.txt)

## 支持 Krita

Krita 是一个自由和开源的软件项目。如果条件允许，请考虑通过 [捐款](https://krita.org/en/support-us/donations/) 或者 [购买培训教程和画册](https://krita.org/en/support-us/shop) 等方式支持我们的存续和发展，这样我们才能支持开发人员为 Krita 全职工作。

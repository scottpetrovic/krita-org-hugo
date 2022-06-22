---
title: "Krita 4.1.0 发布"
date: "2018-06-27"
categories: 
  - "news-zh"
  - "officialrelease-zh"
---

在发布 Krita 4.0 三个月后，今天我们再次为大家带来 Krita 4.1 版本。

https://youtu.be/N6oHLuICrHM

本版 Krita 软件带来了下列重要的新功能：

- 全新的参考图像工具，它将取代旧有的参考图像工具面板。
- 用户可以保存并载入对话。对话指的是一系列指定的图像，还有这些图像的视图。
- 用户可以创建多显示器环境下的工作空间布局。
- 改进了用于处理动画帧的工作流程。
- 改进了动画时间线的显示方式。
- Krita 现在可以将帧数据缓存到硬盘以处理尺寸更大的动画。
- 拾色器新增混色选项。
- 改进了消失点辅助尺，辅助尺可用自定义颜色绘制。
- Krita 的脚本模块现在也可以通过 Python 2 进行编译。
- 整合了 Ivan Yossi 的 Google Summer of Code 工作成果的第一部分：通过矢量化改进笔刷蒙版性能。
- 中文版的翻译已大致完成，但依然有个别位置翻译不生效，我们正在处理：[BUG 395338](https://bugs.kde.org/show_bug.cgi?id=395338)

另外还有大量的问题已被修正，渲染性能的改进以及其他改进。**请阅读[完整的更新日志](https://krita.org/en/krita-4-1-release-notes/)以发现 Krita 4.1 的全部改进！**

[![](/images/posts/2018/krita_41-1024x1024.png)](https://krita.org/wp-content/uploads/2018/06/krita_41.png)图像作者：RJ Quiralta

## 下载

### Windows 版本

Windows 用户请注意：如果你遇到了崩溃，请遵循[此处的说明](https://docs.krita.org/en/reference_manual/dr_minw_debugger.html#dr-minw)使用软件调试符号包，这样可以帮助我们找到崩溃的原因。

- 64 位 Windows 安装程序：[krita-x64-4.1.0-setup.exe](https://download.kde.org/stable/krita/4.1.0/krita-x64-4.1.0-setup.exe)
- 64 位 Windows 压缩包：[krita-x64-4.1.0.zip](https://download.kde.org/stable/krita/4.1.0/krita-x64-4.1.0.zip)
- [64 位软件调试符号包](https://download.kde.org/stable/krita/4.1.0/krita-x64-4.1.0-dbg.zip) (解压到 Krita 的安装目录)

- 32 位 Windows 安装程序：[krita-x86-4.1.0-setup.exe](https://download.kde.org/stable/krita/4.1.0/krita-x86-4.1.0-setup.exe)
- 32 位 Windows 压缩包：[krita-x86-4.1.0.zip](https://download.kde.org/stable/krita/4.1.0/krita-x86-4.1.0.zip)
- [32 位软件调试符号包](https://download.kde.org/stable/krita/4.1.0/krita-x86-4.1.0-dbg.zip) (解压到 Krita 的安装目录)

### Linux 版本

- 64 位 AppImage：[krita-4.1.0-x86\_64.appimage](https://download.kde.org/stable/krita/4.1.0/krita-4.1.0-x86_64.appimage)

(如果 Firefox 把下载文件当作文本打开，请在连接上点击右键/另存为)

你也可以在 [Krita Lime PPA](https://launchpad.net/%7Ekritalime/+archive/ubuntu/ppa) 更新之后用它在 Ubuntu 以及它的派生版本上面安装最新版本的 Krita。我们也在准备 Snap 形式的更新版本。

### OSX 版本

- OSX 磁盘映像文件：[krita-4.1.0.dmg](https://download.kde.org/stable/krita/4.1.0/krita-4.1.0.dmg)

注意：触控工具面板、gmic-qt、Python 插件在 OSX 上暂不可用。

### 源代码

- 源代码：[krita-4.1.0.tar.gz](https://download.kde.org/stable/krita/4.1.0/krita-4.1.0.tar.gz)

### md5sum

所有下载文件的 md5sum：

- [md5sum.txt](https://download.kde.org/stable/krita/4.1.0/md5sum.txt)

### 密钥和签名

Linux 的 AppImage 软件包和源代码 Tar 压缩包都已签名。 你可以在此通过 https 连接下载公共密钥：[0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8) 和 [签名文件](http://download.kde.org/stable/krita/4.1.0/) (文件名后缀为.sig)。

## 资助 Krita 项目

Krita 是一个自由、免费、开源的软件项目。请通过[捐款](https://krita.org/en/support-us/donations/)、[购买教学材料和画册](https://krita.org/en/support-us/shop)等方式资助我们。有了你的资助，我们才能保持核心开发团队为项目全职工作。

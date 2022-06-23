---
title: "Krita 4.0.3 版软件发布"
date: "2018-05-12"
categories: 
  - "news-zh"
  - "officialrelease-zh"
---

Krita 开发小组在今天发布了 Krita 4.0.3 版。这是 Krita 4.0.0 系列的一个问题修复版本。它修复了在 Krita 4.0.2 版中出现的在同一窗口内打开的多个文件之间复制粘贴时会发生崩溃的错误 ([BUG:394068](https://bugs.kde.org/show_bug.cgi?id=394068))。

[![](/images/posts/2018/kiki_4.0_sm-1-1024x463.png)](/images/posts/2018/kiki_4.0_sm-1-1024x463.png)

## 其他改进

- Krita 在 Windows 平台下面会尝试加载系统的色彩配置文件。
- Krita 可以打开 .rw2 RAW 文件了。
- 启动画面对 HiDPI 模式或者 Retina 显示器进行了优化。([BUG:392282](https://bugs.kde.org/show_bug.cgi?id=392282))
- OpenEXR 导出过滤器会在保存文件之前将图像通道转换为整数格式而不是给出错误。
- OpenEXR 导出过滤器在给出警告时不再自称为 TIFF 过滤器。
- 修复了在导出一定次数之后会弹出一个空白错误信息的问题。([BUG:393850](https://bugs.kde.org/show_bug.cgi?id=393850)).
- Python API 中的 setBackGroundColor 方式更名为 setBackgroundColor 以提高一致性。
- 修复 KisColorizeMask 里的一个会造成崩溃的问题 ([BUG:393753](https://bugs.kde.org/show_bug.cgi?id=393753))

## 下载软件

### Windows 版本

Windows 用户请注意：如果你遇到了崩溃，请遵循[此处的说明](https://docs.krita.org/Dr._Mingw_debugger)来使用软件调试符号包，这样可以帮助我们找到崩溃的原因。

- 64 位 Windows 安装程序：[krita-x64-4.0.3-setup.exe](https://download.kde.org/stable/krita/4.0.3/krita-x64-4.0.3-setup.exe)
- 64 位 Windows 压缩包：[krita-x64-4.0.3.zip](https://download.kde.org/stable/krita/4.0.3/krita-x64-4.0.3.zip)
- [64 位软件调试符号包](https://download.kde.org/stable/krita/4.0.3/krita-x64-4.0.3-dbg.zip) (解压到 Krita 的安装目录)

- 32 位 Windows 安装程序：[krita-4.0.3-x86-setup.exe](https://download.kde.org/stable/krita/4.0.3/krita-x86-4.0.3-setup.exe)
- 32 位 Windows 压缩包：[krita-x86-4.0.3.zip](https://download.kde.org/stable/krita/4.0.3/krita-x86-4.0.3.zip)
- [32 位软件调试符号包](https://download.kde.org/stable/krita/4.0.3/krita-x86-4.0.3-dbg.zip) (解压到 Krita 的安装目录)

### Linux 版本

- 64 位 AppImage：[krita-4.0.3-x86\_64.appimage](https://download.kde.org/stable/krita/4.0.3/krita-4.0.3-x86_64.appimage)

(如果 Firefox 把下载文件当作文本打开，请在连接上点击右键/另存为)

你也可以在 [Krita Lime PPA](https://launchpad.net/%7Ekritalime/+archive/ubuntu/ppa) 更新之后用它在 Ubuntu 以及它的派生版本上面安装最新版本的 Krita。我们也在准备 Snap 形式的更新版本。

### OSX 版本

- OSX 映像文件：[krita-4.0.3.1.dmg](https://download.kde.org/stable/krita/4.0.3/krita-4.0.3.1.dmg)

注意：触控工具面板、gmic-qt、Python 插件在 OSX 上暂不可用。

### 源代码

- 源代码：[krita-4.0.3.tar.gz](https://download.kde.org/stable/krita/4.0.3/krita-4.0.3.tar.gz)

### md5sum

所有下载文件的 md5sum：

- [md5sum.txt](https://download.kde.org/stable/krita/4.0.3/md5sum.txt)

### 密钥和签名

Linux 的 AppImage 软件包和源代码 Tar 压缩包都已签名。你可以在此通过 https 连接下载公共密钥： [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8) 和[下载签名文件](http://download.kde.org/stable/krita/4.0.3/) (文件名后缀为.sig)。

## 资助 Krita 项目

Krita 是一个自由、免费、开源的软件项目。请通过[捐款](https://krita.org/en/support-us/donations/)、[购买教学材料和画册](https://krita.org/en/support-us/shop)等方式资助我们。有了你的资助，我们才能保持核心开发团队为项目全职工作。

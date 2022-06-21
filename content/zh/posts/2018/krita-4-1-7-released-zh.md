---
title: "Krita 4.1.7 发布"
date: "2018-12-15"
categories: 
  - "news-zh"
  - "officialrelease-zh"
---

今天我们为大家带来 Krita 4.1.7，Krita 4.1 系列的又一个问题修复版本。

此版最重要的一项更新看上去很奇怪——它跟你的 WiFi 连接有关。事情的来龙去脉是这样的：我们正在为 Krita 的启动画面开发一个能显示 Krita.org 网页新闻的组件，该组件尚未被激活，所以理应不会建立任何网络连接。然而 Qt 的网络管理器类却依然会不停地检测你的 WiFi 设置。详见：[https://bugreports.qt.io/browse/QTBUG-46015](https://bugreports.qt.io/browse/QTBUG-46015) 和 [https://bugreports.qt.io/browse/QTBUG-40332](https://bugreports.qt.io/browse/QTBUG-40332)。

除此之外，我们还为一个会造成在使用数位板时瞬间崩溃的 Qt 5.12 问题开发了临时应对方案。我们构建的程序版本并没有使用该版本的 Qt，所以我们网站上提供的 Windows、macOS和 Linux AppImage 程序包不受该问题的影响。该问题主要影响那些采用滚动更新模式的 Linux 发行版——如 ArchLinux 等——在它们的官方软件库中提供的 Krita 版本。

当然还有一些其他的更新：

- 修复了在动画时间线的音频菜单中错误地显示不支持音频功能的信息
- 在 Windows 下面停用基于磁盘的动画缓存渲染后端：它在动画超过 150 帧时会造成问题 ([BUG 401326](https://bugs.kde.org/show_bug.cgi?id=401326))
- 在尝试加载最近文档的缩略图时如果文档不在原位，不会造成挂起 ([BUG:401939](https://bugs.kde.org/show_bug.cgi?id=401939))
- 在 Windows 下使用 Angle 渲染模式时可以使用 LUT 工具面板了。我们还为最新版本更新了 OpenColorIO 库
- 在选区工具中记忆抗锯齿选项的启用状况 ([BUG:401730](https://bugs.kde.org/show_bug.cgi?id=401730))
- 添加了激活文字工具的快捷键 ([BUG:401655](https://bugs.kde.org/show_bug.cgi?id=401655))
- 重新让工具栏可以被拖动
- 在按颜色区间建立选区时，对整个图像进行检查 ([BUG:346138](https://bugs.kde.org/show_bug.cgi?id=346138))
- 默认启用 HiDPI： 画布缩放的有关问题已被解决
- 从文件管理器启动 Krita 时允许一次导入多个文件 ([BUG:401476](https://bugs.kde.org/show_bug.cgi?id=401476))
- 修复在 Linux 下面的单选框中使用鼠标滚轮 ([BUG:399379](https://bugs.kde.org/show_bug.cgi?id=399379)) 该补丁由 Mykola Krachkovsky 开发
- 修复均值去饱和的计算方式 ([BUG:400493](https://bugs.kde.org/show_bug.cgi?id=))
- 导出构图时不再崩溃 ([BUG:400627](https://bugs.kde.org/show_bug.cgi?id=400627))
- 让移动工具在所有模式下面均能显示正确的光标
- 让移动工具可以移动隐藏图层
- 修复一个会在艺术颜色选择器中造成崩溃的问题 ([BUG:399860](https://bugs.kde.org/show_bug.cgi?id=399860))

## 下载

### Windows 版本

Windows 用户请注意：如果你遇到了崩溃，请[按此说明](https://docs.krita.org/en/reference_manual/dr_minw_debugger.html#dr-minw)使用软件调试符号包，这样可以帮助我们找到崩溃的原因。

- 64 位 Windows 安装程序：[krita-x64-4.1.7-setup.exe](https://download.kde.org/stable/krita/4.1.7/krita-x64-4.1.7-setup.exe)
- 64 位 Windows 压缩包：[krita-x64-4.1.7.zip](https://download.kde.org/stable/krita/4.1.7/krita-x64-4.1.7.zip)
- [64 位软件调试符号包](https://download.kde.org/stable/krita/4.1.7/krita-x64-4.1.7-dbg.zip) (解压到 Krita 的安装目录)

- 32 位 Windows 安装程序：[krita-x86-4.1.7-setup.exe](https://download.kde.org/stable/krita/4.1.7/krita-x86-4.1.7-setup.exe)
- 32 位 Windows 压缩包：[krita-x86-4.1.7.zip](https://download.kde.org/stable/krita/4.1.7/krita-x86-4.1.7.zip)
- [32 位软件调试符号包](https://download.kde.org/stable/krita/4.1.7/krita-x86-4.1.7-dbg.zip) (解压到 Krita 的安装目录)

### Linux 版本

- 64 位 AppImage：[krita-4.1.7-x86\_64.appimage](https://download.kde.org/stable/krita/4.1.7/krita-4.1.7-x86_64.appimage)
- 64 位 G’Mic-Qt 插件 AppImage：[G'Mic-Qt plugin appimage](https://download.kde.org/stable/krita/4.1.7/gmic_krita_qt-x86_64.appimage).

（如果 Firefox 将文件当成文本加载，请在链接上点击右键，另存为）

[Krita Lime PPA](https://launchpad.net/%7Ekritalime/+archive/ubuntu/ppa) 中的版本更新后即可在 Ubuntu 及其派生版本中安装 Krita 4.1.7。我们也在准备更新的 Snap 包。

### OSX 版本

- OSX 磁盘映像文件：[krita-4.1.7.1.dmg](https://download.kde.org/stable/krita/4.1.7/krita-4.1.7.1.dmg)

注意：触控工具面板、gmic-qt、Python 插件在 OSX 上暂不可用。

### 源代码

- 源代码：[krita-4.1.7.101.tar.gz](https://download.kde.org/stable/krita/4.1.7/krita-4.1.7.101.tar.gz)

### md5sum 值

所有下载文件的 md5sum 值：

- [md5sum.txt](https://download.kde.org/stable/krita/4.1.7/md5sum.txt)

### 文件一致性验证密钥和签名

Linux appimage 和源代码的 tarball 文件均已签名。 通过 https 链接下载公共密钥：[0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8) 和 [签名文件](http://download.kde.org/stable/krita/4.1.7/)（扩展名为 .sig 的文件）

## 支持 Krita

Krita 是一个自由、免费、开源的软件项目。请通过[捐助](https://krita.org/en/support-us/donations/)、[购买教学材料和画册](https://krita.org/en/support-us/shop)等方式资助我们。有了你的资助，我们才能保持核心开发团队为项目全职工作。

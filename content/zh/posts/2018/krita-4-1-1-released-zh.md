---
title: "Krita 4.1.1 发布"
date: "2018-07-19"
categories: 
  - "news-zh"
  - "officialrelease-zh"
---

今天我们为大家带来了 Krita 4.1.1，这是 Krita 4.1.0 系列的第一个问题修正版本。

- 修复了在使用 PyQt 5.11 时 PyKrita 的加载问题 (补丁由 Antonio Rojas 提供，谢谢!) ([BUG:396381](https://bugs.kde.org/show_bug.cgi?id=396381))
- 修复了在处理矢量对象时可能发生的崩溃 ([BUG:396145](https://bugs.kde.org/show_bug.cgi?id=396145))
- 修复了在笔刷编辑器中缩放像素笔刷大小时的一个问题 ([BUG:396136](https://bugs.kde.org/show_bug.cgi?id=396136))
- 修复了在 macOS 下启用了多个语言时加载系统语言
- 在矢量对象属性工具面板中不显示尚未实现的拾色器按钮 ([BUG:389525](https://bugs.kde.org/show_bug.cgi?id=389525))
- 修复了在一次修改、保存、修改周期后自动保存时间的激活问题 ([BUG:393266](https://bugs.kde.org/show_bug.cgi?id=393266))
- 修复了跨通道曲线滤镜的超出范围的数据抬头 ([BUG:396244](https://bugs.kde.org/show_bug.cgi?id=396244))
- 修复了一个当按下 PageUp 切换至参考图像图层时的判断参数
- 修复了在孤立图层模式下合并图层时的一个崩溃 ([BUG:395981](https://bugs.kde.org/show_bug.cgi?id=395981))
- 修复了使用自由变形模式的变形蒙版的文件加载问题 ([BUG:395979](https://bugs.kde.org/show_bug.cgi?id=395979))
- 修复了自由变形模式被选中时变形工具的激活问题 ([BUG:395979](https://bugs.kde.org/show_bug.cgi?id=395979))
- 当使用不受支持的 Windows 版本时警告用户
- 修复了在隐藏最近一个可见通道时的崩溃问题 ([BUG:395301](https://bugs.kde.org/show_bug.cgi?id=395301))
- 实现了对非规范 GPL 调色板的加载，如 https://lospec.com/palette-list/endesga-16
- 简化了网面变形模式下的网格显示
- 修复了反向选择菜单项的显示 ([BUG:395764](https://bugs.kde.org/show_bug.cgi?id=395764))
- 使用 KFormat 显示带格式的数字 (补丁由 Pino Toscano 提供，谢谢!)
- 隐藏颜色滑动条的设置页面
- 不从完全透明的参考图像上拾取颜色 ([BUG:396358](https://bugs.kde.org/show_bug.cgi?id=396358))
- 修复了嵌入参考图像时的一个崩溃
- 修复了保存和加载参考图像时的一些问题 ([BUG:396143](https://bugs.kde.org/show_bug.cgi?id=396143))
- 修复了拾色器工具在参考图像上不工作的问题 ([BUG:396144](https://bugs.kde.org/show_bug.cgi?id=396144))
- 将画布视图的平移范围扩展至包含参考图像

## 下载

### Windows 版本

Windows 用户请注意：如果你遇到了崩溃，请遵循[此处的说明](https://docs.krita.org/en/reference_manual/dr_minw_debugger.html#dr-minw)使用软件调试符号包，这样可以帮助我们找到崩溃的原因。

- 64 位 Windows 安装程序：[krita-x64-4.1.1-setup.exe](https://download.kde.org/stable/krita/4.1.1/krita-x64-4.1.1-setup.exe)
- 64 位 Windows 压缩包：[krita-x64-4.1.1.zip](https://download.kde.org/stable/krita/4.1.1/krita-x64-4.1.1.zip)
- [64 位软件调试符号包](https://download.kde.org/stable/krita/4.1.1/krita-x64-4.1.1-dbg.zip) (解压到 Krita 的安装目录)

- 32 位 Windows 安装程序：[krita-x86-4.1.1-setup.exe](https://download.kde.org/stable/krita/4.1.1/krita-x86-4.1.1-setup.exe)
- 32 位 Windows 压缩包：[krita-x86-4.1.1.zip](https://download.kde.org/stable/krita/4.1.1/krita-x86-4.1.1.zip)
- [32 位软件调试符号包](https://download.kde.org/stable/krita/4.1.1/krita-x86-4.1.1-dbg.zip) (解压到 Krita 的安装目录)

### Linux 版本

- 64 位 AppImage：[krita-4.1.1-x86_64.appimage](https://download.kde.org/stable/krita/4.1.1/krita-4.1.1-x86_64.appimage)
- 64 位 G'Mic-Qt 插件 AppImage：[G'Mic-Qt 插件 appimage](https://download.kde.org/stable/krita/4.1.1/gmic_krita_qt-x86_64.appimage)

(如果 Firefox 把下载文件当作文本打开，请在连接上点击右键/另存为)

你也可以在 [Krita Lime PPA](https://launchpad.net/%7Ekritalime/+archive/ubuntu/ppa) 更新之后用它在 Ubuntu 以及它的派生版本上面安装最新版本的 Krita。我们也在准备 Snap 形式的更新版本。

### OSX 版本

- OSX 磁盘映像文件：[krita-4.1.1.dmg](https://download.kde.org/stable/krita/4.1.1/krita-4.1.1.dmg)

注意：触控工具面板、gmic-qt、Python 插件在 OSX 上暂不可用。

### 源代码

- 源代码：[krita-4.1.1.tar.gz](https://download.kde.org/stable/krita/4.1.1/krita-4.1.1.tar.gz)

### md5sum

所有下载文件的 md5sum：

- [md5sum.txt](https://download.kde.org/stable/krita/4.1.1/md5sum.txt)

### 密钥和签名

Linux 的 AppImage 软件包和源代码 Tar 压缩包都已签名。 你可以在此通过 https 连接下载公共密钥： [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8) 和 [签名文件](http://download.kde.org/stable/krita/4.1.1/) (文件名后缀为.sig)。

## 资助 Krita 项目

Krita 是一个自由、免费、开源的软件项目。请通过[捐款](https://krita.org/en/support-us/donations/)、[购买教学材料和画册](https://krita.org/en/support-us/shop)等方式资助我们。有了你的资助，我们才能保持核心开发团队为项目全职工作。

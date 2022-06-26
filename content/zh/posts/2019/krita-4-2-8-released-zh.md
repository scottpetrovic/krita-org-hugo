---
title: "Krita 4.2.8 发布"
date: "2019-11-28"
categories: 
  - "officialrelease-zh"
---

Krita 团队为大家带来了 Krita 4.2 分支的又一个问题修复版本：Krita 4.2.8。此版在矢量形状、变形工具和 Windows 下保存文件等方面做了大量工作，但得到修复的问题数量少于上一版，这是因为我们的一部分核心团队需要集中精力重写 Krita 用于管理笔刷和渐变等资源的程序模块。

Windows 系统在一般情况下不会立即将程序保存的数据写入硬盘，而是放在缓存里由系统来决定什么时候写入。如果在 Windows 写完这些数据之前切断了电源，文件很可能会被损坏。统计学上看这个机率虽然很小，但考虑到上个月在 Windows 10 下面我们有约 150 万名用户（无重复统计），遇到这个问题的人数仍然不算少。特别提醒一下那些喜欢画完一整张画才保存的画师们——这是一种很冒险的习惯！为了应对这个问题，我们在此版开始强制 Windows 把保存后的文件立即完成写入硬盘。虽然这会使得保存文件的速度变慢，但它带来的安全性提升是值得的。

我们还重写了笔刷选项面板的自动精确度选项，这将提高绘制速度和品质。

已修复问题清单：

- Fix the sliders in the performance settings page. [BUG:414092](https://bugs.kde.org/show_bug.cgi?id=414092)
- Fix the color space of the onion skin cache. [BUG:407251](https://bugs.kde.org/show_bug.cgi?id=407251)
- Fix transforming layers that have onion skins enabled. [BUG:408152](https://bugs.kde.org/show_bug.cgi?id=408152)
- Also save the preferences when closing the preferences dialog with the titlebar close button
- Fix a bug in the polygon tool that adds an extra point. [BUG:411059](https://bugs.kde.org/show_bug.cgi?id=411059)
- Save the last used export settings. [BUG:409044](https://bugs.kde.org/show_bug.cgi?id=409044)
- Prevent a crash on macOS when closing a dialog that opened the system color dialog. [BUG:413922](https://bugs.kde.org/show_bug.cgi?id=413922)
- Fix an issue on macOS where the native file dialogs would not return a filename. [BUG:413241](https://bugs.kde.org/show_bug.cgi?id=413241)
- Make it possible to save the "All" tag as the current tag. [BUG:409748](https://bugs.kde.org/show_bug.cgi?id=409748)
- Show the correct blending mode in the brush preset editor. [BUG:410136](https://bugs.kde.org/show_bug.cgi?id=410136)
- Fix saving color profiles that are not sRGB to PNG files
- Make the transform tool work correctly with the selection mask's overlay
- Fix a crash when editing the global selection mask. [BUG:412747](https://bugs.kde.org/show_bug.cgi?id=412747)
- Remove the "Show Decorations" option from the transform tool. [BUG:413573](https://bugs.kde.org/show_bug.cgi?id=413573)
- Remove the CSV export filter (it hasn't worked for ages)
- Fix slowdown in the Warp transform tool. [BUG:413157](https://bugs.kde.org/show_bug.cgi?id=413157)
- Fix possible data loss when pressing the escape key multiple times. [BUG:412561](https://bugs.kde.org/show_bug.cgi?id=412561)
- Fix a crash when opening an image with a clone layer when instant preview is active. [BUG:412278](https://bugs.kde.org/show_bug.cgi?id=412278)
- Fix a crash when editing vector shapes. [BUG:413932](https://bugs.kde.org/show_bug.cgi?id=413932)
- Fix visibility of Reference Layer and Global Selection Mask in Timeline. [BUG:412905](https://bugs.kde.org/show_bug.cgi?id=412905)
- Fix random crashes when converting image color space. [BUG:410776](https://bugs.kde.org/show_bug.cgi?id=410776)
- Rewrite the "auto precision" option in the brush preset editor. [BUG:413085](https://bugs.kde.org/show_bug.cgi?id=413085)
- Fix legacy convolution filters on images with non-transparent background. [BUG:411159](https://bugs.kde.org/show_bug.cgi?id=411159)
- Fix an assert when force-autosaving the image right during the stroke. [BUG:412835](https://bugs.kde.org/show_bug.cgi?id=412835)
- Fix crash when using Contionous Selection tool with Feather option. [BUG:412622](https://bugs.kde.org/show_bug.cgi?id=412622)
- Fix an issue where temporary files were created in the folder above the current folder.
- Improve the rendering of the transform tool handles while actually making a transformation
- Use the actual mimetype instead of the extension to identify files when creating thumbnails for the recent files display
- Improve the logging to detect whether Krita has closed improperly
- Fix exporting compositions from the compositions docker. [BUG:412953](https://bugs.kde.org/show_bug.cgi?id=412953), [BUG:412470](https://bugs.kde.org/show_bug.cgi?id=412470)
- Fix Color Adjustment Curves not processing. [BUG:412491](https://bugs.kde.org/show_bug.cgi?id=412491)
- Fix artifacts on layers with colorize mask \*and\* disabled layer styles
- Make Separate Channels work. [BUG:336694](https://bugs.kde.org/show_bug.cgi?id=336694), [BUG:412624](https://bugs.kde.org/show_bug.cgi?id=412624)
- Make it possible to create vector shapes on images that are bigger than QImage's limits. [BUG:408936](https://bugs.kde.org/show_bug.cgi?id=408936)
- Disable adjustmentlayer support on the raindrop filter. [BUG:412522](https://bugs.kde.org/show_bug.cgi?id=412522)
- Make it possible to use .kra files as file layers. [BUG:412549](https://bugs.kde.org/show_bug.cgi?id=412549)
- Fix Crop tool loosing aspect ratio on move. [BUG:343586](https://bugs.kde.org/show_bug.cgi?id=343586)
- Fix Rec2020 display format. [BUG:410918](https://bugs.kde.org/show_bug.cgi?id=410918)
- Improve error messages when loading and saving fails.
- Fix jumping of vector shapes when resizing them
- Add hi-res input events for pan, zoom and rotate. [BUG:409460](https://bugs.kde.org/show_bug.cgi?id=409460)
- Fix crash when using Pencil Tool with a tablet. [BUG:412530](https://bugs.kde.org/show_bug.cgi?id=412530)
- Always ask Windows to synchronize the file systems after saving a file from Krita.
- Fix wrong aspect ratio on loading SVG files. [BUG:407425](https://bugs.kde.org/show_bug.cgi?id=407425)

## 下载

### Windows

如需试用新版或者测试版，可以先下载 zip 压缩包的版本。随便把压缩包解压到你方便的地方，点击文件夹中的 Krita 图标文件即可运行。这样不会影响之前已安装的旧版 Krita，但新旧两个版本会共享配置文件和自定义资源。如需报告程序崩溃问题，请下载 Debug 符号包。

- 64 位 Windows 安装包: [krita-x64-4.2.8-setup.exe](https://download.kde.org/stable/krita/4.2.8/krita-x64-4.2.8-setup.exe)
- 64 位 Windows 压缩: [krita-x64-4.2.8.zip](https://download.kde.org/stable/krita/4.2.8/krita-x64-4.2.8.zip)
- [Debug 符号包 (解压到 Krita 安装目录)](https://download.kde.org/stable/krita/4.2.8/krita-x64-4.2.8-dbg.zip)

- 32 位 Windows 安装: [krita-x86-4.2.80-setup.exe](https://download.kde.org/stable/krita/4.2.8/krita-x86-4.2.8-setup.exe)
- 32 位 Windows 压缩包: [krita-x86-4.2.8.zip](https://download.kde.org/stable/krita/4.2.8/krita-x86-4.2.8.zip)
- [Debug 符号包 (解压到 Krita 安装目录)](https://download.kde.org/stable/krita/4.2.8/krita-x86-4.2.8-dbg.zip)

### Linux

- 64 位 Linux: [krita-4.2.8-x86_64.appimage](https://download.kde.org/stable/krita/4.2.8/krita-4.2.8-x86_64.appimage)
- 64 位 Linux [G'Mic-Qt plugin appimage](https://download.kde.org/stable/krita/4.2.8/gmic_krita_qt-x86_64.appimage).

(如果浏览器把链接作为文本打开，请右键另存为)

### OSX

- OSX 磁盘映像: [krita-4.2.8.dmg](https://download.kde.org/stable/krita/4.2.8/krita-4.2.8.dmg)

注意： gmic-qt 软件包在 OS X 下不可用。

### 源代码

- [krita-4.2.8.2.tar.gz](https://download.kde.org/stable/krita/4.2.8/krita-4.2.8.2.tar.gz)
- [krita-4.2.8.2.tar.xz](https://download.kde.org/stable/krita/4.2.8/krita-4.2.8.2.tar.xz)

### md5sum

适用于全部上述下载文件:

- [md5sum.txt](https://download.kde.org/stable/krita/4.2.8/md5sum.txt)

### Key

Linux 的 Appimage 包和源代码 tarball 文件已签名，你可以通过 https 来下载公共密钥: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8)、[.sig 签名文件](https://download.kde.org/stable/krita/4.2.8/)

## 支持 Krita

Krita 是一个自由和开源的软件项目。请通过 [捐款](https://krita.org/en/support-us/donations/) 或者 [购买培训教程和画册](https://krita.org/en/support-us/shop) 等方式支持我们，这样我们才能为 Krita 的开发全职工作。

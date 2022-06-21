---
title: "Krita 4.2.3 发布"
date: "2019-07-18"
categories: 
  - "officialrelease-zh"
---

我们今天为大家带来 Krita 4.2.3 版。它主要修复了程序的一系列已知问题，同时还带来一项新功能：二指手势画布旋转，这是 Sharaf Zaman 的 2019 年 Google Summer of Code 任务的一环，为移植 Krita 到安卓系统作准备。此功能也支持其他平台的版本。

在此版修复的程序问题中，最重要的一项是为 Windows 下使用老旧、损坏、不完善的显卡驱动时准备的应对方式。这个问题的从根本上是我们目前使用的开发平台 Qt 造成的，只要程序使用了任意的 QML（用于创建界面），Qt 的当前版本就会要求工作环境具备正常的 OpenGL 或者 Direct3D 支持。我们针对这个问题开发了应对方式，之前遇到困难的用户，尤其是 Windows 7 用户，现在应该可以正常运行 Krita 了。

另外，由于中文翻译负责人员的工作生活发生较大变故，导致时间精力不足，从今开始小版本的修复问题清单暂不提供翻译，按照中文语言习惯重新组织词句的细致程度也会适当降低，请谅解。

## 修复问题清单

- Make it possible for Krita to use a software renderer on Windows ([BUG:408872](https://bugs.kde.org/show_bug.cgi?id=408872))
- Fix the caption of the Background Color color selection dialog ([BUG:407658](https://bugs.kde.org/show_bug.cgi?id=407658))
- Fix the tag selector combobox so it is possible to select resources that have a tag that's longer than fits in the combobox ([BUG:408053](https://bugs.kde.org/show_bug.cgi?id=408053))
- Make it possible for the Krita startup window to become as narrow as before adding the news widget ([BUG:408504](https://bugs.kde.org/show_bug.cgi?id=408504))
- Fix copy/pasting of animation frames ([BUG:408421](https://bugs.kde.org/show_bug.cgi?id=408421), [BUG:404595](https://bugs.kde.org/show_bug.cgi?id=404595))
- Make the polygon and outline selection tool handle the control modifier correctly ([BUG:376007](https://bugs.kde.org/show_bug.cgi?id=376007))
- Add a reload script button to the Python scripter plugin
- Fix a crash in the Overview docker when there is no image open
- Fix drag and drop of fill layers between opened files ([BUG:408019](https://bugs.kde.org/show_bug.cgi?id=408019))
- Fix loading EXR files that have more than one layer with the same name ([BUG:409552](https://bugs.kde.org/show_bug.cgi?id=409552))
- Hide vanishing points preview lines when assistants are hidden ([BUG:396158](https://bugs.kde.org/show_bug.cgi?id=396158))
- Fix the Mirror All Layers Horizontally function
- Fix switching profile to default when changing channel depth in the New Image dialog ([BUG:406700](https://bugs.kde.org/show_bug.cgi?id=406700))
- Disable AVG optimizations for some 32 bit blending modes ([BUG:404133](https://bugs.kde.org/show_bug.cgi?id=404133))
- Fix a crash when pressing cancel when trying to create an 8 bit/channel linear gamma RGB image
- Fix colors drifting when using the native macOS color selection dialog ([BUG:407880](https://bugs.kde.org/show_bug.cgi?id=407880))
- Make sure Stroke Selection paint correctly with the selection border in the middle of the selection ([BUG:409254](https://bugs.kde.org/show_bug.cgi?id=409254))
- Fix saving Krita when perspective assistants are present ([BUG:409249](https://bugs.kde.org/show_bug.cgi?id=409249))
- Fix issues with transformations being pixelated ([BUG:409280](https://bugs.kde.org/show_bug.cgi?id=409280))
- Make it possible to hide all layers except the selected one with shift-click ([BUG:376086](https://bugs.kde.org/show_bug.cgi?id=376086))
- Fix cloning keyframe channels that are not opacity channels
- Fix a hang when trying to paint while playing an animation of an empty image ([BUG:408749](https://bugs.kde.org/show_bug.cgi?id=408749))
- Fix Isolated Mode when multiple windows are open ([BUG:408150](https://bugs.kde.org/show_bug.cgi?id=408150))
- Make the gradient editor show the right editor for stop and segmented gradients (but creating new gradients in Krita is still broken)
- Make Krita use the integrated GPU on dual-GPU Apple computers
- Fix a freeze when pressing delete when making a polygonal selection ([BUG:408843](https://bugs.kde.org/show_bug.cgi?id=408843))
- Fix the --export commandline option to return 0 when the export is successful ([BUG:409133](https://bugs.kde.org/show_bug.cgi?id=409133))
- Fix support for the KDE Plasma global menu ([BUG:408015](https://bugs.kde.org/show_bug.cgi?id=408015))
- Fix a crash when using the shrink option of the deform brush ([BUG:408887](https://bugs.kde.org/show_bug.cgi?id=408887))

## 下载

### Windows

提示：如果在 Windows 下遇到程序崩溃，请根据 [相关指引](https://docs.krita.org/en/reference_manual/dr_minw_debugger.html#dr-minw) 使用 debug symbols 协助我们分析崩溃原因。

- 64 位 Windows: [krita-x64-4.2.3-setup.exe](https://download.kde.org/stable/krita/4.2.3/krita-x64-4.2.3-setup.exe)
- 64 位 Windows: [krita-x64-4.2.3.zip](https://download.kde.org/stable/krita/4.2.3/krita-x64-4.2.3.zip)
- [Debug symbols (解压到 Krita 安装目录)](https://download.kde.org/stable/krita/4.2.3/krita-x64-4.2.3-dbg.zip)

- 32 位 Windows: [krita-x86-4.2.3-setup.exe](https://download.kde.org/stable/krita/4.2.3/krita-x86-4.2.3-setup.exe)
- 32 位 Windows: [krita-x86-4.2.3.zip](https://download.kde.org/stable/krita/4.2.3/krita-x86-4.2.3.zip)
- [Debug symbols (解压到 Krita 安装目录)](https://download.kde.org/stable/krita/4.2.3/krita-x86-4.2.3-dbg.zip)

### Linux

- 64 位 Linux: [krita-4.2.3-x86\_64.appimage](https://download.kde.org/stable/krita/4.2.3/krita-4.2.3-x86_64.appimage)
- 64 位 Linux: [G'Mic-Qt plugin appimage](https://download.kde.org/stable/krita/4.2.3/gmic_krita_qt-x86_64.appimage)

(如果 Firefox 把链接作为文本打开，请右键另存为)

### OSX

- OSX disk image: [krita-4.2.3.dmg](https://download.kde.org/stable/krita/4.2.3/krita-4.2.3.dmg)

提示：gmic-qt 在 OSX 下暂不可用

### 源代码

- [krita-4.2.3.tar.gz](https://download.kde.org/stable/krita/4.2.3/krita-4.2.3.tar.gz)
- [krita-4.2.3.tar.xz](https://download.kde.org/stable/krita/4.2.3/krita-4.2.3.tar.xz)

### md5sum

所有软件包的 md5sum:

- [md5sum.txt](https://download.kde.org/stable/krita/4.2.3/md5sum.txt)

### 软件包签名和密钥

Linux 的 Appimage 包和源代码 tarball 文件已签名，你可以通过 https 来下载公共密钥:

 [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8)、[.sig 签名文件](http://download.kde.org/unstable/krita/4.2.0-beta2/)。

## 支持 Krita

Krita 是一个自由和开源的软件项目。请通过 [捐款](https://krita.org/en/support-us/donations/) 或者 [购买培训教程和画册](https://krita.org/en/support-us/shop) 等方式支持我们，这样我们才能为 Krita 的开发全职工作。

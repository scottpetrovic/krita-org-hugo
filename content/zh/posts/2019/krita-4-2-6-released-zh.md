---
title: "Krita 4.2.6 发布"
date: "2019-09-13"
categories: 
  - "officialrelease-zh"
---

Krita 4.2.6 已经发布。由于在 [beta 测试](https://krita.org/en/item/help-beta-test-krita-4-2-6/)中遇到的一些问题，此版更新的时间略有延误。共有 120 位用户参与了本次 beta 测试的问卷调查，我们也将在日后的新版测试中继续通过这种方式收集用户的反馈。

本版软件还针对 AMD Ryzen 5 3500 CPU 进行了一项重要的适配调整。该 CPU 的随机数生成器有一处硬件缺陷，会造成软件崩溃。

### 新功能：

- 新增图层面板右键菜单项“用可见内容新建图层”。
- 在 Windows 环境首次运行 Krita 时将默认使用 Angle 作为渲染器。提示：如在使用 NVidia GPU 时遇到 Krita 的窗口显示为透明的状况，请在 Krita 设置中手动选用 Angle 渲染器；如在使用其他 GPU 时遇到画布不更新的状况，可以尝试手动选用 OpenGL 渲染器。

特别鸣谢 Karl Ove Hufthammer 为可翻译字串所做的细致审校工作。

### 已修复问题清单

- Allow selection overlay to be reset to default. ([BUG:410470](https://bugs.kde.org/show_bug.cgi?id=410470))
- Set date for bundle creation to use ISO-Date. ([BUG:410490](https://bugs.kde.org/show_bug.cgi?id=410490))
- Fix freeze with 32bit float tiff by using our own tiff reader for the thumbnails. ([BUG:408731](https://bugs.kde.org/show_bug.cgi?id=408731))
- Ensure filter mask button is disabled appropriately depending on whether the filter supports it. ([BUG:410374](https://bugs.kde.org/show_bug.cgi?id=410374))
- Enable the small color selector if opengles is available as well ([BUG:410602](https://bugs.kde.org/show_bug.cgi?id=410602))
- Fix mixed Zoom, Pan, Rotate on macOS ([BUG:410698](https://bugs.kde.org/show_bug.cgi?id=410698))
- Ensure that checkboxes are shown in menus even when using the fusion theme
- Isolate Layer Crash ([BUG:408785](https://bugs.kde.org/show_bug.cgi?id=408785))
- Properly fix font resetting when all the text in the editor removed ([BUG:409243](https://bugs.kde.org/show_bug.cgi?id=409243))
- Fix lags in Move Tool when using tablet device ([BUG:410838](https://bugs.kde.org/show_bug.cgi?id=410838))
- Fix Shift and Alt modifiers in Outline Selection Tool ([BUG:410532](https://bugs.kde.org/show_bug.cgi?id=410532))
- Ensure Convert group to Animated Layer shows text in the toolbar. ([BUG:410500](https://bugs.kde.org/show_bug.cgi?id=410500))
- Allow 'Add Clone Layer' to Work on Multiple Layers ([BUG:373338](https://bugs.kde.org/show_bug.cgi?id=373338))
- Fix saving animated transparency masks created through conversion ([BUG:409895](https://bugs.kde.org/show_bug.cgi?id=409895))
- Partially fix the curve change despite 'Share curve across all settings' checked ([BUG:383909](https://bugs.kde.org/show_bug.cgi?id=383909))
- Try harder to make sure that the swap location is writable
- Properly handle timezones in bundles
- Make sure all the settings dialogs pages are always shown in the same order
- Make the settings dialog fit in low-res screens ([BUG:410793](https://bugs.kde.org/show_bug.cgi?id=410793))
- Remove misleading ‘px’ suffix for ‘move amount’ shortcut setting
- Make string for reasons for image export problems translatable ([BUG:406973](https://bugs.kde.org/show_bug.cgi?id=406973))
- Fix crash when creating a bezier curve ([BUG:410572](https://bugs.kde.org/show_bug.cgi?id=410572))
- Fix deadlocks in KoShapeManager ([BUG:410909](https://bugs.kde.org/show_bug.cgi?id=410909), [BUG:410572](https://bugs.kde.org/show_bug.cgi?id=410572))
- Fix a deadlock when using broken Wacom drivers on Linux ([BUG:410797](https://bugs.kde.org/show_bug.cgi?id=410797))
- Fix absolute brush rotation on rotated canvas ([BUG:292726](https://bugs.kde.org/show_bug.cgi?id=292726))
- Fix deadlock when removing reference image ([BUG:411212](https://bugs.kde.org/show_bug.cgi?id=411212))
- Fix a deadlock in handling of vector objects ([BUG:411365](https://bugs.kde.org/show_bug.cgi?id=411365))
- Fix autosave saving only once ([BUG:411631](https://bugs.kde.org/show_bug.cgi?id=411631))

## 下载

### Windows

提示：如果在 Windows 下遇到程序崩溃，请根据 [相关指引](https://docs.krita.org/en/reference_manual/dr_minw_debugger.html#dr-minw) 使用 debug symbols 协助我们分析崩溃原因。

- 64 位 Windows 安装包: [krita-x64-4.2.6-setup.exe](https://download.kde.org/stable/krita/4.2.6/krita-x64-4.2.6-setup.exe)
- 64 位 Windows 压缩包: [krita-x64-4.2.6.zip](https://download.kde.org/stable/krita/4.2.6/krita-x64-4.2.6.zip)
- [Debug symbols. (解压到 Krita 安装目录)](https://download.kde.org/stable/krita/4.2.6/krita-x64-4.2.6-dbg.zip)

- 32 位 Windows 安装包: [krita-x86-4.2.6-setup.exe](https://download.kde.org/stable/krita/4.2.6/krita-x86-4.2.6-setup.exe)
- 32 位 Windows 压缩包: [krita-x86-4.2.6.zip](https://download.kde.org/stable/krita/4.2.6/krita-x86-4.2.6.zip)
- [Debug symbols. (解压到 Krita 安装目录)](https://download.kde.org/stable/krita/4.2.6/krita-x86-4.2.6-dbg.zip)

### Linux

- 64 位 Linux: [krita-4.2.6-x86_64.appimage](https://download.kde.org/stable/krita/4.2.6/krita-4.2.6-x86_64.appimage)
- 64 位 Linux [G'Mic-Qt plugin appimage](https://download.kde.org/stable/krita/4.2.6/gmic_krita_qt-x86_64.appimage).

(如果 Firefox 把链接作为文本打开，请右键另存为)

### OSX

- OSX 磁盘映像: [krita-4.2.6.dmg](https://download.kde.org/stable/krita/4.2.6/krita-4.2.6.dmg)

Note: the gmic-qt is not available on OSX.

### 源代码

- [krita-4.2.6.tar.gz](https://download.kde.org/stable/krita/4.2.6/krita-4.2.6.tar.gz)
- [krita-4.2.6.tar.xz](https://download.kde.org/stable/krita/4.2.6/krita-4.2.6.tar.xz)

### md5sum

适用于全部上述下载文件:

- [md5sum.txt](https://download.kde.org/stable/krita/4.2.6/md5sum.txt)

### 软件包签名和密钥

Linux 的 Appimage 包和源代码 tarball 文件已签名，你可以通过 https 来下载公共密钥: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8)、[.sig 签名文件](http://download.kde.org/unstable/krita/4.2.0-beta2/)

## 支持 Krita

Krita 是一个自由和开源的软件项目。请通过 [捐款](https://krita.org/en/support-us/donations/) 或者 [购买培训教程和画册](https://krita.org/en/support-us/shop) 等方式支持我们，这样我们才能为 Krita 的开发全职工作。

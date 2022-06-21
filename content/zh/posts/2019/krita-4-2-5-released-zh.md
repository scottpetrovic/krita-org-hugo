---
title: "Krita 4.2.5 发布"
date: "2019-08-04"
categories: 
  - "officialrelease-zh"
---

我们发现 Krita 4.2.4 下使用某些工具时依然会发生一个影响快捷键工作的程序问题。我们以最快速度修复了它，并提前发布了 Krita 4.2.5。我们建议所有用户升级到最新版。

## 修复问题清单

- Fix an assert in the transform tool when working with a tablet and touch
- Fix continued transformation in the transform tool
- Fix updates in the transform tool
- Show the publication time in the welcome page news ticker in the user's preferred short date/time format
- Fix using the tangent-normal brush when the canvas is rotated or mirrored ([BUG:404408](https://bugs.kde.org/show_bug.cgi?id=404408))
- Make it possible again to create new palettes and save them in the resource folder, instead of the current document ([BUG:410137](https://bugs.kde.org/show_bug.cgi?id=410137))
- Make Krita not gobble up all available memory when loading a JPG file with specific metadata ([BUG:410242](https://bugs.kde.org/show_bug.cgi?id=410242))
- Constrain assistant editors to the viewport, so they can always be manipulated
- Make sure Krita stores changes to brush presets in the current session by default ([BUG:410463](https://bugs.kde.org/show_bug.cgi?id=410463))
- Remove an assert that could be triggered when opening the first image in a session
- Update the version of the default input settings profile, so the rotate/zoom action will be activated even if the user already had a local kritadefault.profile file
- Fix a crash on using the move tool while the image is being opened ([BUG:398968](https://bugs.kde.org/show_bug.cgi?id=398968))
- Make sure the painting tools don't block anymore (BUG:409968,408826,409275)
- Make the shortcut handling system more tolerant when shortcuts overlap ([BUG:409968](https://bugs.kde.org/show_bug.cgi?id=409968))
- Fix a crash in the transform tool
- Make the transform tool and the move tool more responsive

## 下载

### Windows

提示：如果在 Windows 下遇到程序崩溃，请根据 [相关指引](https://docs.krita.org/en/reference_manual/dr_minw_debugger.html#dr-minw) 使用 debug symbols 协助我们分析崩溃原因。

- 64 位 Windows 安装包: [krita-x64-4.2.5-setup.exe](https://download.kde.org/stable/krita/4.2.5/krita-x64-4.2.5-setup.exe)
- 64 位 Windows 压缩包: [krita-x64-4.2.5.zip](https://download.kde.org/stable/krita/4.2.5/krita-x64-4.2.5.zip)
- [Debug symbols. (解压到 Krita 安装目录)](https://download.kde.org/stable/krita/4.2.5/krita-x64-4.2.5-dbg.zip)

- 32 位 Windows 安装包: [krita-x86-4.2.5-setup.exe](https://download.kde.org/stable/krita/4.2.5/krita-x86-4.2.5-setup.exe)
- 32 位 Windows 压缩包: [krita-x86-4.2.5.zip](https://download.kde.org/stable/krita/4.2.5/krita-x86-4.2.5.zip)
- [Debug symbols. (解压到 Krita 安装目录)](https://download.kde.org/stable/krita/4.2.5/krita-x86-4.2.5-dbg.zip)

### Linux

- 64 位 Linux: [krita-4.2.5-x86\_64.appimage](https://download.kde.org/stable/krita/4.2.5/krita-4.2.5-x86_64.appimage)
- 64 位 Linux [G'Mic-Qt plugin appimage](https://download.kde.org/stable/krita/4.2.5/gmic_krita_qt-x86_64.appimage).

(如果 Firefox 把链接作为文本打开，请右键另存为)

### OSX

- OSX disk image: [krita-4.2.5.dmg](https://download.kde.org/stable/krita/4.2.5/krita-4.2.5.dmg)

提示：gmic-qt 在 OSX 下暂不可用。

### 源代码

- [krita-4.2.5.tar.gz](https://download.kde.org/stable/krita/4.2.5/krita-4.2.5.tar.gz)
- [krita-4.2.5.tar.xz](https://download.kde.org/stable/krita/4.2.5/krita-4.2.5.tar.xz)

### md5sum

所有软件包的 md5sum:

- [md5sum.txt](https://download.kde.org/stable/krita/4.2.5/md5sum.txt)

### 软件包签名和密钥

Linux 的 Appimage 包和源代码 tarball 文件已签名，你可以通过 https 来下载公共密钥:

 [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8)、[.sig 签名文件](http://download.kde.org/unstable/krita/4.2.0-beta2/)。

## 支持 Krita

Krita 是一个自由和开源的软件项目。请通过 [捐款](https://krita.org/en/support-us/donations/) 或者 [购买培训教程和画册](https://krita.org/en/support-us/shop) 等方式支持我们，这样我们才能为 Krita 的开发全职工作。

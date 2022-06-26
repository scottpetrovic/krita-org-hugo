---
title: "Krita 4.2.1 正式版发布"
date: "2019-06-05"
categories: 
  - "officialrelease-zh"
---

## Krita 4.2.1

4.2.0 版才发布了没多久，我们为什么紧接着就发布 4.2.1 版了呢。这主要是因为我们在 4.2.0 版中发现了一个问题，它导致撤销队列无限增长，造成在长时间工作后 Krita 的性能下降。这个问题比较影响使用，所以我们在修复它之后便第一时间发布了新版。除了这个问题之外，我们还在此版中包含了一些其他问题的修复，如修复了保存和载入非 latin1 字符文件名且带有矢量图层的文档等。一些修复是由我们新的代码贡献者 Carl Olsson 和 Dmitry Utkin 编写的，特此感谢！

下面为全部问题修复列表：

- 修复长时间使用性能下降 ([BUG:408255](https://bugs.kde.org/show_bug.cgi?id=408255), [BUG:408133](https://bugs.kde.org/show_bug.cgi?id=408133))
- 修复非 latin1 字符文件名图像的矢量图层载入 ([BUG:408280](https://bugs.kde.org/show_bug.cgi?id=408280))
- 修复矩形网格间距限制在调整画布大小后不正常 ([BUG:408166](https://bugs.kde.org/show_bug.cgi?id=408166))
- 修复图层属性窗口会在在其他程序窗口之上绘制 ([BUG:408170](https://bugs.kde.org/show_bug.cgi?id=408170))
- 确保色调分离滤镜使用非线性 sRGB 进行运算
- 允许动画渲染器在任何时候自帧 0 开始 ([BUG:408198](https://bugs.kde.org/show_bug.cgi?id=408198))
- 在分组图层上启用选择不透明区域操作 ([BUG:408236](https://bugs.kde.org/show_bug.cgi?id=408236))
- 在为动画渲染创建临时文件夹之前先检查驱动器是否存在 ([BUG:408246](https://bugs.kde.org/show_bug.cgi?id=408246))
- 防止用户因为过快按下 Shift + Del 而删除已锁定图层
- 修复对矢量图层的复制和副本创建 ([BUG:408028](https://bugs.kde.org/show_bug.cgi?id=408028))
- 修复 Krita 在 Linux 下面用旧版 Qt 编译时画布显示成透明的问题 ([BUG:408225](https://bugs.kde.org/show_bug.cgi?id=408225))
- 修复笔画起始阶段可能存在的微小延迟 ([BUG:408133](https://bugs.kde.org/show_bug.cgi?id=408133))
- 修复点击图层缩略图时折叠和展开
- 修复在使用导线时的撤销和重做 (补丁由 GSoC 学生 Tusooa Zhu 提供)
- 修复 Python API 导线的锁定和显示状态的调转 ([BUG:408113](https://bugs.kde.org/show_bug.cgi?id=408113))
- 使笔刷的最小值在软件中一致
- 使自动笔刷间距精度数值一致 ([BUG:359453](https://bugs.kde.org/show_bug.cgi?id=359453))
- 改进在图层工具面板中的选区行为 ([BUG:408002](https://bugs.kde.org/show_bug.cgi?id=408002))
- 修复 MacOS 缩放和旋转图标卡住的问题 ([BUG:404321](https://bugs.kde.org/show_bug.cgi?id=404321))
- 修复矢量描边样式波及到其他矢量对象的问题 [(BUG:407683](https://bugs.kde.org/show_bug.cgi?id=407683))
- 修复文件工具插件 ([BUG:408146](https://bugs.kde.org/show_bug.cgi?id=408146))
- 修复在打开图层名称编辑器时图层名称会被取消选择的问题 ([BUG:400357](https://bugs.kde.org/show_bug.cgi?id=400357))

我们提供的 Krita 4.2.1 软件包是使用 Qt 5.12.3 编译的，这版 Qt 应该解决了一些文件拖放的问题，但说不定在 Windows 下面会带来界面缩放方面的新问题，因为我们在 4.2.0 时制作的实验性补丁现在会报告冲突。

## 下载

### Windows 版本

注意：如果 Windows 版本用户遇到程序崩溃现象，请 [按照此说明](https://docs.krita.org/en/reference_manual/dr_minw_debugger.html#dr-minw) 使用调试符号包协助我们找到 Krita 崩溃的原因。

- 64 位安装包：[krita-x64-4.2.1-setup.exe](https://download.kde.org/stable/krita/4.2.1/krita-x64-4.2.1-setup.exe)
- 64 位压缩包：[krita-x64-4.2.1.zip](https://download.kde.org/stable/krita/4.2.1/krita-x64-4.2.1.zip)
- 64 位调试符号包：[调试符号包 (解压到 Krita 的安装文件夹)](https://download.kde.org/stable/krita/4.2.1/krita-x64-4.2.1-dbg.zip)

- 32 位安装包：[krita-x86-4.2.1-setup.exe](https://download.kde.org/stable/krita/4.2.1/krita-x86-4.2.1-setup.exe)
- 32 位压缩包：[krita-x86-4.2.1.zip](https://download.kde.org/stable/krita/4.2.1/krita-x86-4.2.1.zip)
- 32 位调试符号包：[调试符号包 (解压到 Krita 的安装文件夹)](https://download.kde.org/stable/krita/4.2.1/krita-x86-4.2.1-dbg.zip)

### Linux 版本

- 64 位 AppImage 包：[krita-4.2.1-x86_64.appimage](https://download.kde.org/stable/krita/4.2.1/krita-4.2.1-x86_64.appimage)
- 64 位 G'Mic AppImage 包：[G'Mic-Qt 插件包](https://download.kde.org/stable/krita/4.2.1/gmic_krita_qt-x86_64.appimage)

注意：如果 Firefox 将软件包作为文本打开，请在链接上点击右键，选择“另存为”。

### OSX 版本

- OSX 磁盘镜像：[krita-4.2.1.dmg](https://download.kde.org/stable/krita/4.2.1/krita-4.2.1.dmg)

注意：在 OSX 下面，触摸工具面板、G'Mic-Qt 插件包和 Python 插件暂不可用。

### 源代码

- [krita-4.2.1.tar.gz](https://download.kde.org/stable/krita/4.2.1/krita-4.2.1.tar.gz)
- [krita-4.2.1.tar.xz](https://download.kde.org/stable/krita/4.2.1/krita-4.2.1.tar.xz)

### md5sum

所有软件包的 md5sum：

- [md5sum.txt](https://download.kde.org/stable/krita/4.2.1/md5sum.txt)

### 软件包签名和密钥

Linux 的 Appimage 包和源代码 tarball 文件已签名，你可以通过 https 来下载公共密钥： [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8)、[.sig 签名文件](http://download.kde.org/unstable/krita/4.2.0-beta2/)

## 支持 Krita

Krita 是一个自由和开源的软件项目。请通过 [捐款](https://krita.org/en/support-us/donations/) 或者 [购买培训教程和画册](https://krita.org/en/support-us/shop) 等方式支持我们，这样我们才能为 Krita 的开发全职工作。

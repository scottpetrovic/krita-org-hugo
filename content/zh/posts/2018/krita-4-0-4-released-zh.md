---
title: "Krita 4.0.4 正式发布"
date: "2018-06-14"
categories: 
  - "officialrelease-zh"
---

Krita 开发小组在今天正式发布 Krita 4.0.4 版，这是 Krita 4.0.0 的一个问题修正版本，也是该系列的最后一次维护性更新。

Krita 的中文翻译在这一版得到了大幅更新，但是少数字符串因为在源代码中未进行可翻译处理而依然显示英文。我们正在处理这个问题。如果遇到其它翻译缺失也请上报。([BUG:395338](https://bugs.kde.org/show_bug.cgi?id=395338))

以下是在 Krita 4.0.4 版的修复问题列表：

- OpenColorIO 在 Mac OSX 下面可以工作了
- 修复了像素笔刷在透明度图层上绘画时的图像问题 ([BUG:394438](https://bugs.kde.org/show_bug.cgi?id=394438))
- 修复了在使用生成器图层时的竞态紊乱问题
- 修复了编辑变形蒙版时的一个崩溃问题 ([BUG:395224](https://bugs.kde.org/show_bug.cgi?id=395224))
- 添加预设记忆到“十大笔刷”脚本，让来回切换预设变得更为便利。
- 改进描边图层样式的性能 ([BUG:361130](https://bugs.kde.org/show_bug.cgi?id=361130), [BUG:390985](https://bugs.kde.org/show_bug.cgi?id=390985))
- 不允许在.kra 文件中进行嵌套：在一个.kra文件里嵌入一个本身带有文件图层的.kra文件作为文件图层会扰乱文件加载。
- 使用阈值滤镜时保持透明度通道 ([BUG:394235](https://bugs.kde.org/show_bug.cgi?id=394235))
- 不自动将资源包的名称用作标签 ([BUG:394345](https://bugs.kde.org/show_bug.cgi?id=394345))
- 修复在 Python 调色板工具面板中选择颜色 ([BUG:394705](https://bugs.kde.org/show_bug.cgi?id=394705))
- 在启动 Krita 时恢复上次使用的颜色，但在创建新视图时不恢复 ([BUG:394816](https://bugs.kde.org/show_bug.cgi?id=394816))
- 允许在当前选中的节点是蒙版时创建一个分组图层。 ([BUG:394832](https://bugs.kde.org/show_bug.cgi?id=394832))
- 在分段渐变编辑器中显示正确的透明度 ([BUG:394887](https://bugs.kde.org/show_bug.cgi?id=394887))
- 移除旧文本工具和艺术字工具曾经使用过的已过时的快捷键 ([BUG:393508](https://bugs.kde.org/show_bug.cgi?id=393508))
- 允许用分数设定多重笔刷的角度
- 改进 OpenGL 画布的性能，特别时 Mac OSX
- 修复在孤立图层模式下在穿透属性的分组图层里绘画 ([BUG:394437](https://bugs.kde.org/show_bug.cgi?id=394437))
- 改进 OpenEXR 文件的加载性能 (Jeroen Hoolmans 贡献补丁)
- 现在 Krita 在忙碌时依然能够进行自动保存
- 改进默认语言的加载
- 修复双击时的颜色选择问题 ([BUG:394396](https://bugs.kde.org/show_bug.cgi?id=394396))
- 修复呼叫 FFMpeg 时帧数不一致的问题 ([BUG:389045](https://bugs.kde.org/show_bug.cgi?id=389045))
- 修复 Mac OSX 下使用 16 位浮点或者 32 位浮点通道时红蓝通道对调的问题
- 在比较新的 Qt 版本下面修复接受触控事件
- 修复 Breeze 主题整合：Krita 不再尝试在线程中创建小工具 ([BUG:392190](https://bugs.kde.org/show_bug.cgi?id=392190))
- 修复在通过 Python 加载图像时的批处理警告
- 在 Windows 和 Mac OSX 上加载系统色彩配置
- 修复 Mac OSX 的一个崩溃问题 ([BUG:394068](https://bugs.kde.org/show_bug.cgi?id=394068))

## 下载

### Windows 版本

Windows 用户请注意：如果你遇到了崩溃，请遵循[此处的说明](https://docs.krita.org/Dr._Mingw_debugger)来使用软件调试符号包，这样可以帮助我们找到崩溃的原因。

- 64 位 Windows 安装程序：[krita-x64-4.0.4-setup.exe](https://download.kde.org/stable/krita/4.0.4/krita-x64-4.0.4-setup.exe)
- 64 位 Windows 压缩包：[krita-x64-4.0.4.zip](https://download.kde.org/stable/krita/4.0.4/krita-x64-4.0.4.zip)
- [64 位软件调试符号包](https://download.kde.org/stable/krita/4.0.4/krita-x64-4.0.4-dbg.zip) (解压到 Krita 的安装目录)

- 32 位 Windows 安装程序：[krita-4.0.4-x86-setup.exe](https://download.kde.org/stable/krita/4.0.4/krita-x86-4.0.4-setup.exe)
- 32 位 Windows 压缩包：[krita-x86-4.0.4.zip](https://download.kde.org/stable/krita/4.0.4/krita-x86-4.0.4.zip)
- [32 位软件调试符号包](https://download.kde.org/stable/krita/4.0.4/krita-x86-4.0.4-dbg.zip) (解压到 Krita 的安装目录)

### Linux 版本

- 64 位 AppImage：[krita-4.0.4-x86_64.appimage](https://download.kde.org/stable/krita/4.0.4/krita-4.0.4-x86_64.appimage)

(如果 Firefox 把下载文件当作文本打开，请在连接上点击右键/另存为)

你也可以在 [Krita Lime PPA](https://launchpad.net/%7Ekritalime/+archive/ubuntu/ppa) 更新之后用它在 Ubuntu 以及它的派生版本上面安装最新版本的 Krita。我们也在准备 Snap 形式的更新版本。

### OSX 版本

- OSX 映像文件：[krita-4.0.4.dmg](https://download.kde.org/stable/krita/4.0.4/krita-4.0.4.dmg)

注意：触控工具面板、gmic-qt、Python 插件在 OSX 上暂不可用。

### 源代码

- 源代码：[krita-4.0.4.tar.gz](https://download.kde.org/stable/krita/4.0.4/krita-4.0.4.tar.gz)

### md5sum

所有下载文件的 md5sum：

- [md5sum.txt](https://download.kde.org/stable/krita/4.0.4/md5sum.txt)

### 密钥和签名

Linux 的 AppImage 软件包和源代码 Tar 压缩包都已签名。你可以在此通过 https 连接下载公共密钥： [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8) 和[下载签名文件](http://download.kde.org/stable/krita/4.0.4/) (文件名后缀为.sig)。

## 资助 Krita 项目

Krita 是一个自由、免费、开源的软件项目。请通过[捐款](https://krita.org/en/support-us/donations/)、[购买教学材料和画册](https://krita.org/en/support-us/shop)等方式资助我们。有了你的资助，我们才能保持核心开发团队为项目全职工作。

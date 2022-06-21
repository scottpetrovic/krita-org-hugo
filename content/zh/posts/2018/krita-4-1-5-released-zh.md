---
title: "Krita 4.1.5 发布"
date: "2018-10-12"
categories: 
  - "news-zh"
  - "officialrelease-zh"
---

在发布 Krita 4.1.3 之后我们发现 TIFF 插件出了问题，所以我们今天紧随其后发布了 4.1.5 版本。不过这一新版并不仅仅修复了那一个问题，还有大量其他修复。这些都是正在荷兰代芬特尔进行的开发冲刺活动的成果，我们以此来庆祝 Krita 2018 年筹款活动进入尾声。

[![](images/2018-fundraiser-hero2.png)](https://krita.org)

这次更新有许多亮点，如为高分辨率和视网膜屏幕提供大幅改进的界面缩放等，下面是本次更新的详情：

- 关联 Krita 到 .ico 文件
- 在更改屏幕时自动更新设备像素旋转
- 在使用平移工具时禁用自动滚动
- 在最近文档中禁用文件拖放：[BUG:399397](https://bugs.kde.org/show_bug.cgi?id=399397)
- 在富文本模式下编辑文本时禁用缩放操作：[BUG:399157](https://bugs.kde.org/show_bug.cgi?id=399157)
- 不将模板文件添加到最近文档列表：[BUG:398877](https://bugs.kde.org/show_bug.cgi?id=398877)
- 不允许在已锁定的图层中创建蒙版：[BUG:399145](https://bugs.kde.org/show_bug.cgi?id=399145)
- 在搜索快捷键时，按下回车键不再关闭设定对话框：[BUG:399116](https://bugs.kde.org/show_bug.cgi?id=399116)
- 在选中某些填充样式时填充多边形形状：[BUG:399135](https://bugs.kde.org/show_bug.cgi?id=399135)
- 修复 16 位和 32 位浮点图像的切线法线的绘制操作：[BUG:398826](https://bugs.kde.org/show_bug.cgi?id=398826)
- 修复拾色器首次拾取颜色时的一个颜色混合问题：[BUG:394399](http://394399)
- 修复载入 SVG 时的一个 namespaces 问题
- 修复右键点击动画时间线时的一个程序宣称问题：[BUG:399435](https://bugs.kde.org/show_bug.cgi?id=399435)
- 修复浮动颜色选择器的自动隐藏
- 修复 HI-DIP 模式下的画布缩放：[BUG:360541](https://bugs.kde.org/show_bug.cgi?id=360541)
- 修复画布输入设定快捷键的删除操作：[BUG:385662](https://bugs.kde.org/show_bug.cgi?id=385662)
- 修复带有额外标记的多行文本的载入：[BUG:399227](https://bugs.kde.org/show_bug.cgi?id=399227)
- 修复载入 unicode 空白符号：[BUG:392710](https://bugs.kde.org/show_bug.cgi?id=392710)
- 修复载入 Photoshop TIFF 文件的透明度通道：[BUG:376950](https://bugs.kde.org/show_bug.cgi?id=376950)
- 修复填充工具的缺失的工具提示：[BUG:399111](https://bugs.kde.org/show_bug.cgi?id=399111)
- 修复在撤销新建图层后的投射更新：[BUG:399575](https://bugs.kde.org/show_bug.cgi?id=399575)
- 修复图层锁定、透明度锁定、透明度继承的保存：[BUG:399513](https://bugs.kde.org/show_bug.cgi?id=399513)
- 修复在 .kra 文件中保存音频源的位置
- 修复当镜像轴启用时选区和变形工具的覆盖：[BUG:395222](https://bugs.kde.org/show_bug.cgi?id=395222)
- 修复在创建新会话后设定活动会话
- 修复在浮动模式下显示浮动颜色选择器
- 修复在 Windows 下用 Ctrl+W 关闭窗口的快捷键：[BUG:399339](https://bugs.kde.org/show_bug.cgi?id=399339)
- 修复总览图工具面板：[BUG:396922](https://bugs.kde.org/show_bug.cgi?id=396922), [BUG:384033](https://bugs.kde.org/show_bug.cgi?id=384033)
- 修复 Shift+I 颜色选择器快捷键
- 修复对阻止了 Krita 关闭的会话的失败恢复：[BUG:399203](https://bugs.kde.org/show_bug.cgi?id=399203)
- 将 SVG 文件作为矢量图层而不是像素图层导入：[BUG:399166](https://bugs.kde.org/show_bug.cgi?id=399166)
- 改进画布输入设定分类的间隔
- 让并非按照由上至下顺序选择的图层可以被正确合并：[BUG:399146](https://bugs.kde.org/show_bug.cgi?id=399146)
- 让 SVG 文本工具创建的文本被移入一个隐藏分组后重新设为可见时依然可以被选中：[BUG:395412](https://bugs.kde.org/show_bug.cgi?id=395412)
- 让拾色器能够拾取正确的透明通道值：[BUG:399169](https://bugs.kde.org/show_bug.cgi?id=399169)
- 在不可编辑的图层中不打开滤镜对话框：[BUG:398915](https://bugs.kde.org/show_bug.cgi?id=398915)
- 创建新文档后复位笔刷预设工具面板：[BUG:399340](https://bugs.kde.org/show_bug.cgi?id=399340)
- 支持非证书的显示缩放倍数
- 在填充后更新颜色历史：[BUG:379199](https://bugs.kde.org/show_bug.cgi?id=379199)

## 下载

### Windows 版本

Windows 用户请注意：如果你遇到了崩溃，请[按此说明](https://docs.krita.org/en/reference_manual/dr_minw_debugger.html#dr-minw)使用软件调试符号包，这样可以帮助我们找到崩溃的原因。

- 64 位 Windows 安装程序：[krita-x64-4.1.5-setup.exe](https://download.kde.org/stable/krita/4.1.5/krita-x64-4.1.5-setup.exe)
- 64 位 Windows 压缩包：[krita-x64-4.1.5.zip](https://download.kde.org/stable/krita/4.1.5/krita-x64-4.1.5.zip)
- [64 位软件调试符号包](https://download.kde.org/stable/krita/4.1.5/krita-x64-4.1.5-dbg.zip) (解压到 Krita 的安装目录)

- 32 位 Windows 安装程序：[krita-x86-4.1.5-setup.exe](https://download.kde.org/stable/krita/4.1.5/krita-x86-4.1.5-setup.exe)
- 32 位 Windows 压缩包：[krita-x86-4.1.5.zip](https://download.kde.org/stable/krita/4.1.5/krita-x86-4.1.5.zip)
- [32 位软件调试符号包](https://download.kde.org/stable/krita/4.1.5/krita-x86-4.1.5-dbg.zip) (解压到 Krita 的安装目录)

### Linux 版本

- 64 位 AppImage：[krita-4.1.5-x86\_64.appimage](https://download.kde.org/stable/krita/4.1.5/krita-4.1.5-x86_64.appimage)
- 64 位 G’Mic-Qt 插件 AppImage：[G'Mic-Qt plugin appimage](https://download.kde.org/stable/krita/4.1.5/gmic_krita_qt-x86_64.appimage)

（如果 Firefox 将文件当成文本加载，请在链接上点击右键，另存为）

[Krita Lime PPA](https://launchpad.net/%7Ekritalime/+archive/ubuntu/ppa) 中的版本更新后即可在 Ubuntu 及其派生版本中安装 Krita 4.1.5。我们也在准备更新的 Snap 包。

### OSX 版本

- OSX 磁盘映像文件：[krita-4.1.5.1.dmg](https://download.kde.org/stable/krita/4.1.5/krita-4.1.5.1.dmg)

注意：触控工具面板、gmic-qt、Python 插件在 OSX 上暂不可用。

### 源代码

- 源代码：[krita-4.1.5.tar.gz](https://download.kde.org/stable/krita/4.1.5/krita-4.1.5.tar.gz)

### md5sum

所有下载文件的 md5sum：

- [md5sum.txt](https://download.kde.org/stable/krita/4.1.5/md5sum.txt)

### 密钥

Linux 的 AppImage 软件包和源代码 Tar 压缩包都已签名。你可以在此通过 https 连接下载： [公共密钥 0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8) 和[签名文件](http://download.kde.org/stable/krita/4.1.5/) (文件名后缀为.sig)。

## 支持 Krita

Krita 是一个自由、免费、开源的软件项目。请通过[捐助](https://krita.org/en/support-us/donations/)、[购买教学材料和画册](https://krita.org/en/support-us/shop)等方式资助我们。有了你的资助，我们才能保持核心开发团队为项目全职工作。

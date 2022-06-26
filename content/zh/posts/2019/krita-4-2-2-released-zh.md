---
title: "Krita 4.2.2 正式版发布"
date: "2019-06-28"
categories: 
  - "officialrelease-zh"
---

虽然 Krita 4.2.1 版才发布了还不到一个月，我们又要发布 Krita 4.2.2 版了。此版主要修复在旧版程序中存在的问题。在带有新功能的 4.3 版就位之前，我们计划每月为 4.2 分支发布问题修复更新。下面是修复的问题列表：

- 文字编辑器：确保编辑器背景颜色使用设定的颜色 ([BUG:408344](https://bugs.kde.org/show_bug.cgi?id=408344))
- 修复创建文字形状时的一个崩溃问题 ([BUG:407554](https://bugs.kde.org/show_bug.cgi?id=407554))
- 确保文字样式在移除文字编辑器中最后一个字母时不会被复位 ([BUG:408441](https://bugs.kde.org/show_bug.cgi?id=408441))
- 修复在 macOS 某些库无法被加载的问题 (BUG:408343)
- 在选区工具的工具选项面板中使用高亮的工具按钮，方便发现哪个选区功能正被激活
- 修复变形功能的邻近算法 ([BUG:408182](https://bugs.kde.org/show_bug.cgi?id=408182))
- 修复一个滤镜图层属性对话框的样式问题 ([BUG:408171](https://bugs.kde.org/show_bug.cgi?id=408171))
- 修复当 Krita 使用英语之外的语言时矢量笔画绘制异常
- 修复调色板面板中通过单选框选择颜色
- 修复加载损坏 KPL 文件时的一个崩溃问题 ([BUG:408447](https://bugs.kde.org/show_bug.cgi?id=408447))
- 修复透明图案填充加载器加载异常 ([BUG:408169](https://bugs.kde.org/show_bug.cgi?id=408169))
- 让洋葱皮视图面板可以被缩小 ([BUG:407646](https://bugs.kde.org/show_bug.cgi?id=407646))
- 改进加载含有巨量列的 GPL 调色板文件
- 让滑动条模块不会返回负值
- 改进 TIFF 导入/导出过滤器 ([BUG:408177](https://bugs.kde.org/show_bug.cgi?id=408177))
- 修复在使用英语以外语言加载 Python 插件 Scripter
- 改进参考图像工具并优化从剪贴板加载图像
- 让照相机 RAW 导入过滤器遵守批量模式
- 修复源图层隐藏时对克隆图层的渲染 ([BUG:408167](https://bugs.kde.org/show_bug.cgi?id=408167), [BUG:405536](https://bugs.kde.org/show_bug.cgi?id=405536))
- 修复在快速复制图层后使用移动和变形工具 ([BUG:408593](https://bugs.kde.org/show_bug.cgi?id=408593))
- 修复在变形蒙版上选择不透明像素时的崩溃问题 ([BUG:408618](https://bugs.kde.org/show_bug.cgi?id=408618))
- 修复加载 sRGB EXR 文件 ([BUG:408485](https://bugs.kde.org/show_bug.cgi?id=408485))
- 确保在语言更改后新建图像对话框依然选中上次使用的选项
- 修复 "强制调色板颜色" 功能 ([BUG:408256](https://bugs.kde.org/show_bug.cgi?id=408256))
- 每次产生笔刷印迹后更新笔刷预览形状 ([BUG:389432](https://bugs.kde.org/show_bug.cgi?id=389432))
- 使在复制的矢量图层上编辑矢量形状变得可能 ([BUG:408028](https://bugs.kde.org/show_bug.cgi?id=408028))
- 隐藏矢量形状属性面板的拾色器按钮，该功能尚未就位
- 修复在 GUI 和 GBR 笔尖导出中把颜色作为蒙版 ([BUG:389928](https://bugs.kde.org/show_bug.cgi?id=389928))
- 复位默认的常用混色模式
- 为全部画布右键菜单添加标题，确保不会点击后误选第一个比较危险的项目，如剪切等 ([BUG:408696](https://bugs.kde.org/show_bug.cgi?id=408696))
- 修复 Krita 在渲染动画时误以为内存不足
- 在更改主题时保持欢迎屏幕的社区链接 ([BUG:408686](https://bugs.kde.org/show_bug.cgi?id=408686))
- 在保存后检查已保存文件能否被打开并含有正确内容
- 改进导入/导出错误的处理和报告方式
- 确保滤镜对话框在 Krita 的主窗口中显示 ([BUG:408867](https://bugs.kde.org/show_bug.cgi?id=408867))
- 确保相连选区工具提供抗锯齿开关 ([BUG:408733](https://bugs.kde.org/show_bug.cgi?id=408733))
- 修复相连选区中的模糊选项
- 修复在编辑文字后会被放到该矢量图层最后的问题 ([BUG:408693](https://bugs.kde.org/show_bug.cgi?id=408693))
- 修复切换笔尖指针模式 ([BUG:408454](https://bugs.kde.org/show_bug.cgi?id=408454), [BUG:405747](https://bugs.kde.org/show_bug.cgi?id=405747))
- 修复在 Linux 下面从笔切换至鼠标时会无法在画布上绘制 ([BUG:407595](https://bugs.kde.org/show_bug.cgi?id=407595))
- 修复过快撤销创建图层操作时的崩溃 ([BUG:408484](https://bugs.kde.org/show_bug.cgi?id=408484))
- 修复使用 .KRA 和 .ORA 文件作为文件图层 ([BUG:408087](https://bugs.kde.org/show_bug.cgi?id=408087))
- 点击时清空轮廓选区工具的全部节点 ([BUG:408439](https://bugs.kde.org/show_bug.cgi?id=408439))
- 修复在像素选区蒙版中使用填充工具的快速模式的崩溃问题
- 修复合并带有非活动选区蒙版的图层 ([BUG:402070](https://bugs.kde.org/show_bug.cgi?id=402070))
- 从参考图像工具中移除不合用的默认操作 ([BUG:408427](https://bugs.kde.org/show_bug.cgi?id=408427))
- 修复撤销/重做不会把文件恢复为未更改状态 ([BUG:402263](https://bugs.kde.org/show_bug.cgi?id=402263))
- 修复扭曲工具在 16 位画布上反复使用后留下暗色痕迹的问题 ([BUG:290383](https://bugs.kde.org/show_bug.cgi?id=290383))
- 升级到 Qt 5.12.4

**注意**：我们接到报告说在某些 Windows 系统下面 Krita 4.2.x 无法启动，但找不到可以重现此问题的机器。我们怀疑与系统没有安装可用的 OpenGL 或者 D3D 驱动有关。我们正在寻找解决办法。

## 下载

### Windows

注意：如果 Windows 版本用户遇到程序崩溃现象，请 [按照此说明](https://docs.krita.org/zh_CN/reference_manual/dr_minw_debugger.html#dr-minw) 使用调试符号包协助我们找到 Krita 崩溃的原因。

- 64 位安装包: [krita-x64-4.2.2-setup.exe](https://download.kde.org/stable/krita/4.2.2/krita-x64-4.2.2-setup.exe)
- 64 位压缩包: [krita-x64-4.2.2.zip](https://download.kde.org/stable/krita/4.2.2/krita-x64-4.2.2.zip)
- 64 位调试符号包: [调试符号包 (解压到 Krita 的安装文件夹)](https://download.kde.org/stable/krita/4.2.2/krita-x64-4.2.2-dbg.zip)

- 32 位安装包: [krita-x86-4.2.2-setup.exe](https://download.kde.org/stable/krita/4.2.2/krita-x86-4.2.2-setup.exe)
- 32 位压缩包: [krita-x86-4.2.2.zip](https://download.kde.org/stable/krita/4.2.2/krita-x86-4.2.2.zip)
- 32 位调试符号包: [调试符号包 (解压到 Krita 的安装文件夹)](https://download.kde.org/stable/krita/4.2.2/krita-x86-4.2.2-dbg.zip)

### Linux

- 64 位 AppImage 包: [krita-4.2.2-x86_64.appimage](https://download.kde.org/stable/krita/4.2.2/krita-4.2.2-x86_64.appimage)
- 64 位 G'Mic AppImage 包: [G'Mic-Qt plugin appimage](https://download.kde.org/stable/krita/4.2.2/gmic_krita_qt-x86_64.appimage).

注意：如果 Firefox 将软件包作为文本打开，请在链接上点击右键，选择“另存为”。

### OSX

- OSX 磁盘镜像: [krita-4.2.2.3.dmg](https://download.kde.org/stable/krita/4.2.2/krita-4.2.2.3.dmg)

注意：在 OSX 下面，G'Mic-Qt 插件包暂不可用。

### 源代码

- [krita-4.2.2.tar.gz](https://download.kde.org/stable/krita/4.2.2/krita-4.2.2.tar.gz)
- [krita-4.2.2.tar.xz](https://download.kde.org/stable/krita/4.2.2/krita-4.2.2.tar.xz)

### md5sum

所有软件包的 md5sum:

- [md5sum.txt](https://download.kde.org/stable/krita/4.2.2/md5sum.txt)

### 软件包签名和密钥

Linux 的 Appimage 包和源代码 tarball 文件已签名，你可以通过 https 来下载公共密钥: [0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8)、[.sig 签名文件](http://download.kde.org/unstable/krita/4.2.0-beta2/)

## 支持 Krita

Krita 是一个自由和开源的软件项目。请通过 [捐款](https://krita.org/en/support-us/donations/) 或者 [购买培训教程和画册](https://krita.org/en/support-us/shop) 等方式支持我们，这样我们才能为 Krita 的开发全职工作。

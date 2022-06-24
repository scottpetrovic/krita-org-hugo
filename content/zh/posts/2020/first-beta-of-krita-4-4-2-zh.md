---
title: "Krita 4.4.2 公开测试第 1 版已经推出"
date: "2020-12-09"
categories: 
  - "news-zh"
  - "development-builds-zh"
---

今天 Krita 团队推出了 Krita 4.4.2 的第 1 个公开测试版本。此版软件包含了 300 多处代码变更，除了修复程序的缺陷之外，还带来了一些重要的新功能。

请注意：此版软件可能带有一个程序缺陷，[它在某些情况下会造成配合修饰键的快捷键失效](https://bugs.kde.org/show_bug.cgi?id=424319)。虽然我们已经针对此缺陷进行了修复，但该缺陷的报告者尚未确认此修复是否有效。请帮我们测试一下吧！

## 新功能

### 曲线网格渐变

曲线网格渐变功能是 Sharaf Zaman 在 2020 年谷歌编程之夏活动中负责的工程，它现在终于正式合并到 Krita 的主分支了。这是继 Inkscape 之后自由开源软件对 SVG Mesh Gradient 规范的又一次独立实现，它与 Inkscape 的类似功能相兼容。曲线渐变功能可以应用于矢量图形，用来生成自然的复杂渐变效果：

[![Mesh Gradients](/images/posts/2020/Handles-meshgradient-1024x554.png)](/images/posts/2020/Handles-meshgradient.png) 曲线网格渐变的效果

### 曲线网格变形

[![Image showing how useful mesh transforms can be](/images/posts/2020/krita_4_4_2_mesh_gradients.png)](/images/posts/2020/krita_4_4_2_mesh_gradients.png) 曲线网格变形模式是变形工具的一个新模式，它可以更加高效地进行有弧度透视感的复杂变形。在上图的示例中我们用此功能演示了将一组扁平的材质转换为具有外凸感的窗栅。

除了矢量的曲线网格渐变外，此版 Krita 还带来了另一个以“曲线网格”命名的功能——曲线网格变形。“曲线”代表它们都是基于贝塞尔曲线来对图像进行操作的；“网格”意味着变形面被控制点细分成互不干扰的网格。它们可以更加高效地生成复杂的效果，尤其是具有弧面的效果。虽然我们没有在上图中显示出来，但你还可以显示各条贝塞尔曲线的操作点进行精细操控。

下面是曲线网格的相关快捷键 (尚未完全定型)：

1. 曲线网格节点： - 点击+拖动——移动节点
2. 边框节点： - 点击+拖动——移动节点 - Shift+点击+拖动——移动整行/整列节点 - Ctrl+Alt+点击+拖动——拆分/滑动整行/整列节点 - Ctrl+Alt+点击+拖动到画布外——移除整行/整列节点
3. 控制点： - 点击+拖动——同步调整两侧控制点 - Shift+点击+拖动——单独调整一侧控制点 (会让交界处产生棱角感)
4. 节点选择： - Ctrl+点击——选择多个节点
5. 网格操作： - 点击+拖动——对一个网眼进行自由变形 - Shift+点击+拖动——移动整个网格
6. 网格外空间： - 点击+拖动——旋转网格或者选中的节点、控制点、曲线线段 - Ctrl+点击+拖动——缩放网格或者选中的节点、控制点、曲线线段 - Shift+点击+拖动——移动网格或者选中的节点、控制点、曲线线段

### 渐变填充图层和新型渐变编辑器

[![Showing the gradient fill layer and the new gradient editor.](/images/posts/2020/krita_4_4_2_new_gradient_editor_and_fill_layer.png)](/images/posts/2020/krita_4_4_2_new_gradient_editor_and_fill_layer.png) 渐变填充图层和新型渐变编辑器的工作效果

Deif Lou 将单纯渐变模式添加到了填充图层，你可以用它生成简易的渐变并进行非破坏性编辑。他还对渐变编辑器的易用性进行了改进，Krita 的两种渐变类型——“色标渐变(SVG)”和“片段渐变(GIMP)”现在不但可以在同一个编辑器中进行操作，还可以相互转换。

### 半调滤镜改进

Deif Lou 还编写了一个全新的半调滤镜，与旧版滤镜相比，新版滤镜不但速度更快，还能够使用更丰富的网点，并被用作滤镜蒙版。

[![Our splash screen as filtered by the half tone filter](/images/posts/2020/krita_4_4_2_halftone_filter.png)](/images/posts/2020/krita_4_4_2_halftone_filter.png) 新版半调滤镜可以按色彩通道进行颜色过滤，不但可以用来制作怀旧的效果，或许也能在套色印刷场合发挥作用。

新版滤镜可以作为滤镜蒙版使用，支持按色彩通道进行颜色过滤。它可以使用任何一种填充图层的选项来生成网点，带来更丰富的可能性。

### macOS 整合插件更新

Amyspark 改进了 macOS 版的 quicklook 插件，新增了缩略图支持 (需要 macOS 10.15 或者更高版本)，还为 Spotlight 增加了 Krita 元数据支持。

### 新增粘贴矢量形状样式操作

我们新增了一个可以只从复制的矢量形状中粘贴样式到选中形状的操作。尽管这是一个小功能，但对于需要保留形状轮廓而只应用样式的场合非常有用。此功能可在菜单栏的编辑菜单中找到，你也可以给它分配一个快捷键方便使用。

### 四方连续模式的工具栏按钮

四方连续模式是一个 Krita 早就实现的功能，Photoshop 也将在下一版本中支持类似的功能。我们本来给 Krita 的四方连续模式分配的快捷键是 W。

[![](/images/posts/2020/wrap-around-mode.jpg)](/images/posts/2014/wrap-around-mode.jpg)

但因为很多不知情的画师在不小心按到 W 之后被类似上图的谜之光景吓坏了，我们决定移除这个快捷键，却造成新人再也不知道 Krita 居然有这样的功能。为了解决这个问题，我们将四方连续模式加入到工具栏中，成为一个单独的按钮。

[![](/images/posts/2020/wraparound_button.png)](/images/posts/2020/wraparound_button.png)这下你们就不会再按错了吧！

### HiDPI 支持改进

![This image shows the difference between the old popup palette and the new one on 4k display with 200% UI scaling. Note that it also shows a new button and custom UI text.](/images/posts/2020/popup_palette_comparison.png) Agata Cacko 改进了 Krita 的 HiDPI 显示效果 ([BUG:411118](https://bugs.kde.org/show_bug.cgi?id=411118))，包括以下方面：

- 象素画预览
- 参考图像
- 漫画管理工具页面
- 最近图像列表面板中的图像缩略图
- 最近图像缩略图
- 右键工具面板
- 新建图像对话框的剪贴板图像内容
- 拾色器
- 色域蒙版
- 笔刷预设编辑器中的笔刷预设图标
- 图层缩略图和图标
- 资源列表
- 资源包图标

## 已修复的程序缺陷

### 文件读写

- 文件名以数字开头的图像现在可以被正确地自动保存
- 可以载入路径中带有非 ASCII 字符的 EXR 文件
- 禁用将半透明 EXR 图像的背景色设为黑色 ([BUG:427720](https://bugs.kde.org/show_bug.cgi?id=427720))

### 绘画功能

- 压力增量传感器现在能够与色相颜色表达正确配合使用 ([BUG:426234](https://bugs.kde.org/show_bug.cgi?id=426234))
- 绘制速度平滑算法不再产生块状断续笔画 ([BUG:363364](https://bugs.kde.org/show_bug.cgi?id=363364), [375360](https://bugs.kde.org/show_bug.cgi?id=375360))
- 颜色涂抹笔刷引擎在有活动选区时也能正常混色 ([BUG:423851](https://bugs.kde.org/show_bug.cgi?id=423851))
- 笔刷的外轮廓在两个不同缩放倍率的文件之间切换时不再发生异常吸附 ([BUG:427094](https://bugs.kde.org/show_bug.cgi?id=427094))

### 动画功能

除了下面列出的少量改进外，我们还正在为 Krita 5.0 的动画功能准备大量的功能更新。

- 洋葱皮视图在播放动画时将被隐藏 ([BUG:426246](https://bugs.kde.org/show_bug.cgi?id=426246))
- 警告用户他们指定的是 FFmpeg 的压缩包，他们应该先解压缩里面的文件。
- 修复将动画的透明度蒙版转换为颜料图层 ([BUG:419223](https://bugs.kde.org/show_bug.cgi?id=419223))

### 易用性

- 移除用于切换选区工具模式的默认快捷键，它们的功能将被 Ctrl/Shift/Alt 修饰键替代。它们的快捷键操作槽依然保留，你可以随时为它们重新分配快捷键
- 磁性选区工具新增了用来确认和取消选取作业的按钮
- 修复在移动选区时会发生跳跃的问题 ([BUG:426949](https://bugs.kde.org/show_bug.cgi?id=426949))
- 新增缩放到视图高度的快捷键，感谢 Jonathan Colman 提供补丁 ([BUG:410929](https://bugs.kde.org/show_bug.cgi?id=410929))
- 网点生成器的默认值得到了改进
- 为拖放而成的文件图层提供适合的默认名称，感谢 Jonathan Colman 提供补丁 ([BUG:427235](https://bugs.kde.org/show_bug.cgi?id=427235))
- 右键面板新增清除颜色历史按钮，感谢 Emilio Del Castillo 提供补丁
- 报告程序缺陷对话框现在会提供系统信息和使用日志，并引导用户复制/粘贴到缺陷报告中去
- 文件名含有 \\ 的被添加到黑名单的资源会被忽略 ([BUG:421575](https://bugs.kde.org/show_bug.cgi?id=421575))
- 在色彩管理设置页面中显示显示器的设备名称 ([BUG:412943](https://bugs.kde.org/show_bug.cgi?id=412943))
- 为用户定制的模板修复自定义图标的显示，感谢 Evan Thompson 提供补丁  ([BUG:395894](https://bugs.kde.org/show_bug.cgi?id=395894))
- 填充图层和 Seexpr 对话框得到了进一步改进
- 移动工具的  x/y 位置数值框已被修复 ([BUG:420329](https://bugs.kde.org/show_bug.cgi?id=420329), [423452](https://bugs.kde.org/show_bug.cgi?id=423452))
- 为文字形状增加默认的字符间距参数，感谢 Lucid Sunlight 提供补丁
- 为用户安装的配色方案提供支持，感谢 Daniel 提供补丁
- 所有对话框和信息框现已正确与主窗口建立父子关系，感谢 Daniel 提供补丁
- 新增导出图层组为合并图层的功能，感谢 Dmitrij Antsevich 提供补丁
- 修复文字编辑器中的字距调整处理，感谢 Lucid Sunlight 提供补丁
- 为文字编辑器新增颜色不透明度支持，感谢 Lucid Sunlight 提供补丁 ([BUG:342303](https://bugs.kde.org/show_bug.cgi?id=342303))
- 修复在移动被蒙版的图层时变形蒙版被裁剪
- 改进在 SVG 源代码和富文本编辑器之间切换时的体验，感谢 Lucid Sunlight 提供补丁 ([BUG:424213](https://bugs.kde.org/show_bug.cgi?id=424213))
- 修复在笔刷尺寸小于 0 时笔刷外轮廓会被卡住的问题 ([BUG:427751](https://bugs.kde.org/show_bug.cgi?id=427751))
- 改进 Python 插件导入工具，让 action 文件能够被正确导入。感谢Rebecca Breu 提供补丁 ([BUG:429262](https://bugs.kde.org/show_bug.cgi?id=429262))
- 修复在资源选单中滚动时图案的显示发生撕裂的问题
- 矩形选区工具和椭圆选区工具现在有了默认的快捷键：Shift+R 和 Shift+J
- 让相连颜色选区工具正确处理图像外框和透明图层 ([BUG:428441](https://bugs.kde.org/show_bug.cgi?id=428441))
- 修复等角网格模式的显示
- 手绘轮廓选区的英文从 Outline 改为 Freehand, 不影响中文翻译) ([BUG:425894](https://bugs.kde.org/show_bug.cgi?id=425894))

### 滤镜

- 自带的 G'mic 插件更新到 2.9.2 版，修复了 Boost-Fade 滤镜的问题 (BUG:412617)
- 渐变映射滤镜得到了改进和提速，感谢 Deif Lou 提供补丁

### 稳定性和性能

- 修复了大量内存泄漏问题
- 消除了内部颜色信息和 QColor 颜色信息相互传递时的一处性能瓶颈
- 修复漫画管理工具的一处 race 问题 ([BUG:426701](https://bugs.kde.org/show_bug.cgi?id=426701))
- 修复填充图层过于频繁地更新
- 修复在更改网点参数时会发生的随机崩溃 ([BUG:428014](https://bugs.kde.org/show_bug.cgi?id=428014))
- 修复方形渐变策略中的一处崩溃，感谢 Deif Lou 提供补丁
- 修复从 SVG 源代码转换到富文本编辑器时的崩溃，感谢 Lucid Sunlight 提供补丁
- 修复在对空图层应用液化变形时造成的 assert ([BUG:428685](https://bugs.kde.org/show_bug.cgi?id=428685))
- 修复当活动图层隐藏时使用从可见图层创建新图层时造成的 assert ([BUG:428683](https://bugs.kde.org/show_bug.cgi?id=428683))
- 让相似颜色选区工具支持多线程

### macOS 支持

- 在 macOS 下面，Delete 键 (也就是退格键) 现在可以删除选区 ([BUG:425370](https://bugs.kde.org/show_bug.cgi?id=425370))

### 安卓支持

- 支持从外部文件源打开图像，例如文件管理器、Google Drive 或者下载管理器等
- 为 KRA 文件新增 mimetype 和 pathpatter
- 将 Krita 设为 SingleTask 应用：这意味着在 Krita 已经在运行时也能正常打开一个 Krita 支持的图像类型
- 修复在保存 KRA 和 ORA 图像时可能发生的文件损坏现象
- 修复在退出 Krita 时发生的崩溃 ([BUG:426092](https://bugs.kde.org/show_bug.cgi?id=426092))
- 修复“同时保存一份 Krita 格式图像”功能 ([BUG:424612](https://bugs.kde.org/show_bug.cgi?id=424612))
- 正确处理鼠标键状态和触摸事件
- 使安卓下面能够正确另存为其他 MIME 类型的文件 ([BUG:429056](https://bugs.kde.org/show_bug.cgi?id=429056))
- 使主题的背景在 ChromeOS 下面为黑色：这原本是粉色的，在改变窗口大小时很难看
- 在启用 OpenGL 时画布视图的渲染拼贴块不再闪烁 ([BUG:424347](https://bugs.kde.org/show_bug.cgi?id=424347))

## 下载

### 中文版信息

- 中文支持：Krita 的正式版本、通过官方新闻发布的公开测试版本 (beta) 均已内建中文支持。
- 自动检测：Krita 在首次安装时会自动设置为操作系统的语言。
- 手动设置：菜单栏 --> Settings 菜单 --> Switch Application Language (倒数第二项) --> 下拉选单 --> 中文 (底部)，重启程序生效。
- 插件翻译：部分内置，G'MIC 插件[需要下载翻译包](https://share.weiyun.com/SBopNjOn)
- 网盘下载：请在官网下载困难时使用。

### Windows 版本

提示：微软最近更改了 Windows 的数字安全证书信任策略，仅默认信任 Digicert 颁发的证书。Krita 的证书并非由 Digicert 颁发，因此软件包会可能在刚刚发布时遭到系统的 SmartScreen 智能安全筛选功能阻止。如果在下载、运行软件时见到“Windows 已经保护了你的电脑”、“此下载可能危害你的电脑”之类的信息，请点击“更多信息”或者“...”展开，然后点击“保留”或者“仍要运行”按钮。在一定数量的用户通过上述方式允许 Krita 下载运行后，SmartScreen 将不会再阻止它，直到下一个新版发布。

- **64 位 Windows 安装程序** (推荐) [本站下载](https://download.kde.org/unstable/krita/4.4.2-beta1/krita-x64-4.4.2-beta1-setup.exe) | [网盘下载](https://share.weiyun.com/60HLzj6I)
- **64 位 Windows 免安装包** [本站下载](https://download.kde.org/unstable/krita/4.4.2-beta1/krita-x64-4.4.2-beta1.zip) | [网盘下载](https://share.weiyun.com/60HLzj6I)
- **64 位程序崩溃调试包** [本站下载](https://download.kde.org/unstable/krita/4.4.2-beta1/krita-x64-4.4.2-beta1-dbg.zip) | [网盘下载](https://share.weiyun.com/60HLzj6I)

- **32 位 Windows 安装程序** [本站下载](https://download.kde.org/unstable/krita/4.4.2-beta1/krita-x86-4.4.2-beta1-setup.exe) | [网盘下载](https://share.weiyun.com/Otvc2tpi)
- **32 位 Windows 免安装包** [本站下载](https://download.kde.org/unstable/krita/4.4.2-beta1/krita-x86-4.4.2-beta1.zip) | [网盘下载](https://share.weiyun.com/Otvc2tpi)
- **32 位程序崩溃调试包** [本站下载](https://download.kde.org/unstable/krita/4.4.2-beta1/krita-x86-4.4.2-beta1-dbg.zip) | [网盘下载](https://share.weiyun.com/Otvc2tpi)

- **配套网盘资源 (中文社区维护)** [中文离线文档](https://share.weiyun.com/Dea2uj0M) | [FFmpeg 软件包](https://share.weiyun.com/6tH13bVC) | [G'Mic 滤镜汉化](https://share.weiyun.com/SBopNjOn) |

- 免安装包：解压到任意位置，运行目录中的 Krita 快捷方式。不带文件管理器缩略图插件。与已安装版本共用配置文件和资源，但程序本身相互独立。
- 程序崩溃调试包：解压到 Krita 的安装目录，在报告程序崩溃问题时用于获取回溯追踪数据。日常使用无需下载此包。

### Linux 版本

- **64 位 Linux AppImage 主程序包** [本站下载](https://download.kde.org/unstable/krita/4.4.2-beta1/krita-4.4.2-beta1-x86_64.appimage) | [网盘下载](https://share.weiyun.com/C0gZ6joR)
- **64 位 Linux AppImage G'Mic-Qt 插件包** [本站下载](https://download.kde.org/unstable/krita/4.4.2-beta1/gmic_krita_qt-x86_64.appimage) | [网盘下载](https://share.weiyun.com/C0gZ6joR)
- 如果浏览器把链接作为文本打开，请右键点击链接另存为文件。

### macOS 版本

- **macOS 主程序映像** [本站下载](https://download.kde.org/unstable/krita/4.4.2-beta1/krita-4.4.2-beta1.dmg) | [网盘下载](https://share.weiyun.com/gVg0CI53)

- G'Mic-qt 软件包、触摸屏辅助面板在 macOS 下不可用。

### 安卓版本

安卓版本目前尚处于早期测试阶段，可以认为与桌面版本没有差别。它仅为安卓平板和 ChromeBook 类设备进行了初步适配，大部分功能依然需要搭配键盘使用。尽管它也能够在一般智能手机上安装，但会由于屏幕比例和大小等限制而造成界面显示不全，因此我们不建议你在智能手机上使用它。现在安卓版本已经合并到源代码主分支，通过统一流程进行构建，因此它尽管是测试版本，也能正常显示中文界面。

- **64 位 Intel CPU APK 安装包** [本站下载](https://download.kde.org/unstable/krita/4.4.2-beta1/krita-x86_64-4.4.2-beta1.apk) | [网盘下载](https://share.weiyun.com/tEkbnO1K)
- **32 位 Intel CPU APK 安装包** [本站下载](https://download.kde.org/unstable/krita/4.4.2-beta1/krita-x86-4.4.2-beta1.apk) | [网盘下载](https://share.weiyun.com/tEkbnO1K)
- **64 位 ARM CPU APK 安装包** [本站下载](https://download.kde.org/unstable/krita/4.4.2-beta1/krita-arm64-4.4.2-beta1.apk) | [网盘下载](https://share.weiyun.com/tEkbnO1K)
- **32 位 ARM CPU APK 安装包** [本站下载](https://download.kde.org/unstable/krita/4.4.2-beta1/krita-arm32-4.4.2-beta1.apk) | [网盘下载](https://share.weiyun.com/tEkbnO1K)

### 源代码

- [TAR.GZ 格式源代码包](https://download.kde.org/unstable/krita/4.4.2-beta1/krita-4.4.2-beta1.tar.gz)
- [TAR.XZ 格式源代码包](https://download.kde.org/unstable/krita/4.4.2-beta1/krita-4.4.2-beta1.tar.xz)

### md5sum 校验码

适用于上述所有软件包，用于校验下载文件的完整性，不了解文件校验请忽略：

- [ms5sum 校验码文本文件](https://download.kde.org/unstable/krita/4.4.2-beta1/md5sum.txt)

### 文件完整性验证密钥

Linux 的 Appimage 可执行文件包和源代码的 .tar.gz 和 .tar.xz tarballs 压缩包已经经过数字签名。你可以通过 GPG 取回公共密钥，命令为 gpg --recv-key 7468332F 。你可以在此下载 [数字签名的 SIG 文件](https://download.kde.org/unstable/krita/4.4.2-beta1/)。

## 支持 Krita

Krita 是一个自由和开源的软件项目。如果条件允许，请考虑通过 [捐款](https://krita.org/zh/support-us-zh/donation-zh/) 或者 [购买培训教程和画册](https://krita.org/en/shop/) 等方式支持我们的存续和发展，这样我们才能支持开发人员为 Krita 全职工作。

---
title: "Krita 4.1.3 发布"
date: "2018-09-28"
categories: 
  - "news-zh"
  - "officialrelease-zh"
---

今天我们为大家带来 Krita 4.1.3。虽然我们正在进行 [2018 年度筹款活动](https://www.krita.org)，但我们还是抽出时间准备了新版的 Krita。4.1.3 版本是一个较为重要的更新，它包含了近 100 处改进，我们建议所有 Krita 用户更新到这一最新版本。我们也邀请你参加我们的筹款活动，你的点滴帮助将让我们可以继续改进 Krita！

[![](/images/posts/2018/2018-fundraiser-hero2.png)](https://krita.org)

你可能会觉得奇怪——Krita 4.1.2 去哪儿了？事情是这样的：我们原本已经准备好了 Krita 4.1.2，但是我们的编译系统出了一些问题，导致编译出来的 Windows 版本程序出错。在我们调试编译系统的时候，Dmitry 又着手修正了更多的问题，包括一个多行文本编辑后会变成一行的问题。我们决定创建一个更新的 4.1.3 版本，将这些全新的改进包含进去。

[![](/images/posts/2018/text_tool-1024x577.jpg)](https://krita.org/wp-content/uploads/2018/09/text_tool.jpg)

Krita 4.1.3 主要是一个问题修复版本，但它也包含了一些新功能。

首先是新的欢迎屏幕，由 Scott Petrovic 打造。它提供了一组用于快速创建新文件和打开已有文件的链接，一个近期文件列表和其他一些有用的网页链接。你还可以将文件拖到欢迎屏幕区域直接打开已有文件。

[![](/images/posts/2018/welcome_page-1024x781.png)](https://krita.org/wp-content/uploads/2018/09/welcome_page.png)

Dmitry Kazakov 开足了马力对 Krita 进行各种改进。其中一项成果是对即时预览模式的改进。即时预览模式是我们在 2015 年 Kickstarter 众筹活动中得到赞助开发的一项功能，它把用户绘制的笔画先用低分辨率临时绘制到画布上进行显示，同时在后台继续演算实际的高分辨率笔画。在低配置的机器上使用大型笔刷时即时预览模式能够相当可观地提高 Krita 画布的绘图性能。但在使用某些笔刷时笔画的末尾会发生一点延迟，有时画布也会发生闪烁：[BUG:361448](https://bugs.kde.org/show_bug.cgi?id=361448) 。这个问题已经得到修复，绘画的感觉将更加平顺。与此同时 [Ivan Yossi 的Google Summer of Code 工作成果](https://colorathis.wordpress.com/tag/kde/)的绝大部分也已经被整合到这一版本中，它也将改进绘画的流畅程度。

我们也对选区功能进行了改进。Krita 的选区可以被定义为矢量图形或像素蒙版。在使用矢量选区时可以用形状工具把诸如矩形或椭圆形能矢量形状添加到该选区，无需事先像素化该选区。

移动工具也得到了改进。使用移动工具时的每一步移动都可以撤销，而不会一下子跳回到使用移动工具之前。参见：[BUG:392014](https://bugs.kde.org/show_bug.cgi?id=392014)。

贝塞尔曲线工具也得到了改进，新增了自动平滑选项。选中自动平滑时绘制的曲线将不是多边形，而是一条每个点都设为“平滑”的曲线。参见：[BUG:351787](https://bugs.kde.org/show_bug.cgi?id=351787)。

[![](/images/posts/2018/bezier_smoothing-1024x726.png)](https://krita.org/wp-content/uploads/2018/09/bezier_smoothing.png)

最后一个新功能是矩形工具的圆角功能。无论是在像素还是矢量图层上，你都可以为绘制的矩形指定圆角：[BUG:335568](https://bugs.kde.org/show_bug.cgi?id=335568)。

[![](/images/posts/2018/rounded_rectangles-1024x726.png)](https://krita.org/wp-content/uploads/2018/09/rounded_rectangles.png)

漫画项目管理器，一个由 Wolthera van Hövell tot Westerflier 打造的 Python 插件得到了大量改进，尤其是生成符合行业规范的 epub 和 acbf 文件方面。与此有关的软件项目是 KDE 漫画书阅读器 [Peruse](https://peruse.kde.org/)。具体的改进如下：

- 改进生成的 epub 文件内导航功能：
    - 单个 epub 文件内的画框和对话框的区域导航
    - 在 nav.xhtml 和 ncx 中使用“acbf\_title”关键词创建TOC
    - 在 nav.xhtml 和 ncx 中包含页面列表
- 确保生成的 epub 文件能通过 epub 检查验证。包括确保 mimetype 首先被添加到 zip 文件中，还有一些其他作者元数据和 NCX 页面列表的修正.
- 修复语言问题
- 修复与 epub 元数据导出有关的数个问题
    - 为配合'refines'的使用而添加 MARC-relators
    - 为 acbf 和 epub 添加共用的 UUID
    - 添加倍数和正确的日期
- 实现"epub\_spread"、基本颜色 ahl 元数据和其他特性，此外还有：
    - 让对话框的本地化更加可靠
    - 为全部对话框的文字区域命名以提高精确度
    - 设置作者序列
    - 添加大量相关文档
- 让生成的 EPUB 3 文件预先分页，使得漫画可以作为跨页显示，改善显示效果
- 让 epub 使用 QDomDocument 生成文件，将 ncx/opf 分离出去，这让 xml 文件更加有条理，并留出更多空间来生成 epub 2/3/3+
- 更新 ComicBookInfo 和 ComicRack 生成器

[![](/images/posts/2018/Screenshot_20180828_155852-1024x797.png)](https://krita.org/wp-content/uploads/2018/09/Screenshot_20180828_155852.png)

下面是一个完整的更新列表：

**动画**

- 为载入带有负数帧 ID 的 错误文件添加一个变通方式：[BUG:395378](https://bugs.kde.org/show_bug.cgi?id=395378)
- 只在导出范围内删除已有的帧文件：[BUG:377354](https://bugs.kde.org/show_bug.cgi?id=377354)
- 修复插入保持帧操作的一个问题。我们还要平移帧格来确保帧序列的扩充得到正确执行：[BUG:396848](https://bugs.kde.org/show_bug.cgi?id=396848)
- 修复一个在导出 PNG 图像序列时的程序宣称：[BUG:398608](https://bugs.kde.org/show_bug.cgi?id=398608)
- 修复在含有 Scalar 通道的图层中切换帧时的更新问题
- 为自动创建的动画帧使用用户选定的颜色标签：[BUG:394072](https://bugs.kde.org/show_bug.cgi?id=394072)
- 将多帧插入和移除的选项保存到设置文件中

**文件支持改进**

- 修复一个当导入的 SVG 文件链接到不存在的色彩配置文件时的程序宣称：[BUG:398576](https://bugs.kde.org/show_bug.cgi?id=398576)
- 修复调整曲线的向后兼容性。因为旧版支持的可调整通道更少，我们不能假定配置数据的一致性：[BUG:396625](https://bugs.kde.org/show_bug.cgi?id=396635)
- 修复保存带有图层风格的图层：[BUG:396224](https://bugs.kde.org/show_bug.cgi?id=396224)
- 允许 Krita 将所有类型的图层像素化后保存成 PSD：[BUG:399002](https://bugs.kde.org/show_bug.cgi?id=399002)
- PNG 导出：在图像不是 RGB 或 灰阶色彩空间时转换成 RGB：[BUG:398241](https://bugs.kde.org/show_bug.cgi?id=398241)
- 移除与 FAX 有关的 TIFF 选项。FAX 模式只能保存 1 位每通道的图像，Krita 并不支持该图像格式：[BUG:398548](https://bugs.kde.org/show_bug.cgi?id=398548)

**滤镜**

- 为阈值滤镜添加一个快捷方式：[BUG:383818](https://bugs.kde.org/show_bug.cgi?id=383818)
- 修复在 16 位色彩空间下使用加深滤镜：[BUG:387102](https://bugs.kde.org/show_bug.cgi?id=387102)
- 让颜色标签的颜色差异阈值更高
- 修复反相滤镜的快捷方式

**绘画**

- 移除快速笔刷引擎的笔刷尺寸限制：[BUG:376085](https://bugs.kde.org/show_bug.cgi?id=376085)
- 修复变形后镜像的对象的旋转方向：[BUG:398928](https://bugs.kde.org/show_bug.cgi?id=398928)
- 让图章笔刷预览可以正常缩放：[CCBUG:399065](https://bugs.kde.org/show_bug.cgi?id=399065)

**数位板支持**

- 为那些在悬停模式下不报告数位板事件的数位板添加变通方式：[BUG:363284](https://bugs.kde.org/show_bug.cgi?id=363284)

**文本**

- 在文本编辑器中选中对象后不复位文本风格
- 修复保存文本在非左对齐时的换行：[BUG:395769](https://bugs.kde.org/show_bug.cgi?id=395769)

**参考图像工具**

- 修复参考图像缓存更新状态：[BUG:397208](https://bugs.kde.org/show_bug.cgi?id=397208)

**编译系统**

- 修复使用 dcraw 0.19 编译

**画布**

- 当 OpenGL 被禁用时禁用像素网格操作：[BUG:388903](https://bugs.kde.org/show_bug.cgi?id=388903) 补丁由 Shingo Ohtsuka 提供，特此感谢！
- 修复选区修饰符在网格之上的绘制：[BUG:362662](https://bugs.kde.org/show_bug.cgi?id=362662)

**Krita 核心改进**

- 临时修复在 Windows 下保存到 dropbox 或 Google Drive 文件夹，直至 [QTBUG-57299](https://bugreports.qt.io/browse/QTBUG-57299) 得到解决前 QSaveFile 在 Windows 下应被禁用
- 修复透明色彩空间的 to/fromLab16/Rgb16 方式
- 修复在克隆的 KisDocument 中的撤销操作：[BUG:398730](https://bugs.kde.org/show_bug.cgi?id=398730)

**图层**

- 自动回避颜色标签和系统颜色之间的冲突
- 修复图层属性对话框的光标跳跃问题：[BUG:398958](https://bugs.kde.org/show_bug.cgi?id=398958)
- 修复在移动在矢量图层之上图层的活动工具的复位：[BUG:398095](https://bugs.kde.org/show_bug.cgi?id=398095)
- 修复撤销平整图像后选择图层的操作：[BUG:398814](https://bugs.kde.org/show_bug.cgi?id=398814)
- 修复在转换成滤镜图层后显示两个节点：1）如果是滤镜蒙版应先移除源图层，只在那之后显示滤镜选择对话框；2）确保在用户按下取消按钮后操作会回滚
- 修复在节点与 subtree walker 更新时克隆图层更新问题
- 修复图层克隆时的一个伪程序宣称：[BUG:398788](https://bugs.kde.org/show_bug.cgi?id=398788)

**元数据处理**

- 修复 KisExifIO 中的多个内存访问问题
- 在元数据编辑器的都柏林核心页面显示元数据。编辑器插件本身依然有问题，日期和布尔函数不工作，但至少输入的字符串已经可以显示了：[CCBUG:396672](https://bugs.kde.org/show_bug.cgi?id=396672)

**Python 脚本**

- 修复 LibKis 节点 mergeDown 中的 SegFault：[BUG:397043](https://bugs.kde.org/show_bug.cgi?id=397043)
- apidox for Node.position()：[BUG:393035](https://bugs.kde.org/show_bug.cgi?id=393035)
- 添加 modified() getter 到 Document class：[BUG:397320](https://bugs.kde.org/show_bug.cgi?id=397320)
- 添加 resetCache() Python API 到 FileLayer：[BUG:398740](https://bugs.kde.org/show_bug.cgi?id=398740)
- 修复滤镜的 InfoObject 的内存管理：[BUG:392183](https://bugs.kde.org/show_bug.cgi?id=392183)
- 修复通过 Python API 设定文件图层的文件路径：[BUG:398740](https://bugs.kde.org/show_bug.cgi?id=398740)
- 确保程序等待滤镜完成工作

**资源处理**

- 修复以原有文件名保存到一个固有的资源包

**选区**

- 修复在本地选区中使用描边选区：[BUG:398007](https://bugs.kde.org/show_bug.cgi?id=398007)
- 修复在覆盖模式下移动矢量形状时发生崩溃
- 修复在转换形状到形状选区时的崩溃
- 修复撤销选区蒙版时的崩溃
- 修复矩形选区的圆角功能：[BUG:397806](https://bugs.kde.org/show_bug.cgi?id=397806)
- 修复在载入旧版调整图层时的选区默认绑定
- 描边选区：不要在图层没有绘画设备时尝试添加形状：[BUG:398015](https://bugs.kde.org/show_bug.cgi?id=398015)

**其他工具**

- 修复从参考图像中选区颜色。去饱和度现在会影响选取的颜色，取色工具会忽略隐藏状态下的参考图像
- 修复外框变形模式的连接点：[BUG:396788](https://bugs.kde.org/show_bug.cgi?id=396788)
- 修复移动工具的小问题：1）当移动操作正在进行时添加一个明确的帧；2）Ctrl+Z 在没有可撤销的操作时会取消移动操作：[BUG:392014](https://bugs.kde.org/show_bug.cgi?id=392014)
- 修复移动工具拖动操作末尾的位移
- 修复曲线选区工具中的 Shift 修饰键。最终点击的点的修饰键状态将决定选区模式。我们在选区工具中禁用了路径工具的 Shift + 点击闭合路径功能：[BUG:397932](https://bugs.kde.org/show_bug.cgi?id=397932)
- 移动工具按照准确的边缘裁切边缘区域
- 减轻参考图像的锯齿：[BUG:396257](https://bugs.kde.org/show_bug.cgi?id=396257)

**小问题和界面问题**

- 为关闭操作添加默认快捷方式：当用 Krita 打开图像时关闭文档快捷方式曾不可用
- 新功能：新增一个隐藏选项以锁定所有工具面板
- 修复 KMainWindow 不正确地保存小工具设定
- 修复缩放到新尺寸的 Alt-F 指定到 Alt-T：[BUG:396948](https://bugs.kde.org/show_bug.cgi?id=396948)
- 修复 KritaBlender.colors 的 http 链接颜色：现在链接可以在 Krita 的启动页面正确显示，以前的深蓝色和背景色相同使得阅读困难，将其改为青色改善可读性
- 修复载入模板图标
- 修复位移对话框会给出不精确的位移量：[BUG:397218](https://bugs.kde.org/show_bug.cgi?id=397218)
- 让颜色标签选择器能够处理鼠标键释放事件：[CCBUG:394072](https://bugs.kde.org/show_bug.cgi?id=394072)
- 在首选项对话框中记住最近用过的设定页面
- 记住最近用过的过滤镜收藏
- 移除环绕模式的快捷方式：它依然在菜单中可用，也可以放入工具栏，也可以指定一个快捷方式。但默认指定一个快捷方式为用户支持带来太多不必要的麻烦
- 移除多文档界面的系统菜单操作的快捷方式。关闭窗口操作可以指定一个自定义快捷方式，同时不会再与隐藏操作发生冲突：[BUG:398729](https://bugs.kde.org/show_bug.cgi?id=398729) [BUG:375524](https://bugs.kde.org/show_bug.cgi?id=375524) [BUG:352205](https://bugs.kde.org/show_bug.cgi?id=352205)
- 为 compositor 指定提示的颜色方案，它会被 KWin 读取并设定窗口和框架的配色，确保外观的一致性
- 当进入环绕模式时在画布上显示提示信息
- 当切换文档时显示缩放小工具：[BUG:398099](https://bugs.kde.org/show_bug.cgi?id=398099)
- 为图案工具面板和笔刷编辑器中的图案名称使用 KSqueezedTextLabel：[BUG:398958](https://bugs.kde.org/show_bug.cgi?id=398958)
- 按深度对色彩空间的复选框进行排序

## 下载

### Windows 版本

Windows 用户请注意：如果你遇到了崩溃，请[按此说明](https://docs.krita.org/en/reference_manual/dr_minw_debugger.html#dr-minw)使用软件调试符号包，这样可以帮助我们找到崩溃的原因。

- 64 位 Windows 安装程序：[krita-x64-4.1.3-setup.exe](https://download.kde.org/stable/krita/4.1.3/krita-x64-4.1.3-setup.exe)
- 64 位 Windows 压缩包：[krita-x64-4.1.3.zip](https://download.kde.org/stable/krita/4.1.3/krita-x64-4.1.3.zip)
- [64 位软件调试符号包](https://download.kde.org/stable/krita/4.1.3/krita-x64-4.1.3-dbg.zip) (解压到 Krita 的安装目录)

- 32 位 Windows 安装程序：[krita-x86-4.1.3-setup.exe](https://download.kde.org/stable/krita/4.1.3/krita-x86-4.1.3-setup.exe)
- 32 位 Windows 压缩包：[krita-x86-4.1.3.zip](https://download.kde.org/stable/krita/4.1.3/krita-x86-4.1.3.zip)
- [32 位软件调试符号包](https://download.kde.org/stable/krita/4.1.3/krita-x86-4.1.3-dbg.zip) (解压到 Krita 的安装目录)

### Linux 版本

- 64 位 AppImage：[krita-4.1.3-x86\_64.appimage](https://download.kde.org/stable/krita/4.1.3/krita-4.1.3-x86_64.appimage)
- 64 位 G’Mic-Qt 插件 AppImage：[G'Mic-Qt 插件 appimage](https://download.kde.org/stable/krita/4.1.3/gmic_krita_qt-x86_64.appimage)

(如果 Firefox 把下载文件当作文本打开，请在连接上点击右键/另存为)

你也可以在 [Krita Lime PPA](https://launchpad.net/%7Ekritalime/+archive/ubuntu/ppa) 更新之后用它在 Ubuntu 以及它的派生版本上面安装最新版本的 Krita。我们也在准备 Snap 形式的更新版本。

### OSX 版本

- OSX 磁盘映像文件：[krita-4.1.3.dmg](https://download.kde.org/stable/krita/4.1.3/krita-4.1.3.dmg)

注意：触控工具面板、gmic-qt、Python 插件在 OSX 上暂不可用。

### 源代码

- 源代码：[krita-4.1.3.tar.gz](https://download.kde.org/stable/krita/4.1.3/krita-4.1.3.tar.gz)

### md5sum

所有下载文件的 md5sum：

- [md5sum.txt](https://download.kde.org/stable/krita/4.1.3/md5sum.txt)

### 密钥

Linux 的 AppImage 软件包和源代码 Tar 压缩包都已签名。你可以在此通过 https 连接下载： [公共密钥 0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8) 和 [签名文件](http://download.kde.org/stable/krita/4.1.3/) (文件名后缀为.sig)。

## 支持 Krita

Krita 是一个自由、免费、开源的软件项目。请通过[捐助](https://krita.org/en/support-us/donations/)、[购买教学材料和画册](https://krita.org/en/support-us/shop)等方式资助我们。有了你的资助，我们才能保持核心开发团队为项目全职工作。

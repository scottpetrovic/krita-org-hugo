---
title: "Krita 4.2.9 发布"
date: "2020-03-27"
categories: 
  - "officialrelease-zh"
---

Krita 团队为大家带来了新版软件，Krita 4.2.9。题外话，我们在准备本次发布时遇到了各种状况——我们更新了 Krita 的 Python 库，Windows 版的脚本支持出错了；苹果更新了他们的验证手续，Krita 在 macOS 下面构建失败了；我们更新了 Krita 构建所需的其他软件库，Krita 的各种功能换着花样崩掉了；我们学会了用新方式给 Windows 商店版本打包，图标却出错了……

不过我们克服了这些困难！Krita 4.2.9 在测试期间遇到的所有问题都已解决，软件不但非常稳定，还为大家带来了一些全新功能！

- Dmitry 对笔刷轮廓的显示方式作出了改进，它在画布上悬停时不会再闪烁了： \[video width="960" height="540" mp4="https://krita.org/wp-content/uploads/2020/02/2020-02-11\_comparing-outline.mp4"\]\[/video\]
- Dmitry 还为颜色涂抹笔刷引擎加入了“喷枪”、“频率”和“宽高比”参数，“宽高比”参数可以通过映射到传感器来控制笔尖形状的扁度。Ramón Miranda 专门制作了一个视频进行介绍：
    
    <iframe src="https://www.youtube.com/embed/fyc8-qgxAww" width="560" height="315" frameborder="0" allowfullscreen="allowfullscreen" data-mce-fragment="1"></iframe>
    
- 新加入的开发人员 Saurabh Kumar 为软件添加了 "拆分至本地选区蒙版" 功能：[![Layer Split Dialog](/images/posts/2020/Screenshot_20200225_140252.png)](https://krita.org/wp-content/uploads/2020/02/Screenshot_20200225_140252.png)

我们在本版软件中修复了大量问题……下面列出了其中一部分：

- 修复透明度棋盘格在 HDR 显示下发白 [bug 406698](https://bugs.kde.org/show_bug.cgi?id=406698)
- 文件保存对话框改进，包括覆盖已有文件和 JPG 等 [bug 412651](https://bugs.kde.org/show_bug.cgi?id=412651)
- 修复扩大选区时只会在一个方向上扩大的问题 [bug 414647](https://bugs.kde.org/show_bug.cgi?id=414647)
- 修复洋葱皮视图在非动画图层上崩溃 [bug 414668](https://bugs.kde.org/show_bug.cgi?id=414668)
- 图层偏移上限提高到 100k [bug 414625](https://bugs.kde.org/show_bug.cgi?id=414625)
- 修复打开含有错误克隆源的 .kra 文件时崩溃 [bug 414699](https://bugs.kde.org/show_bug.cgi?id=414699)
- 防止在通过拾色器添加颜色到已删除的调色板时造成崩溃 [bug 413548](https://bugs.kde.org/show_bug.cgi?id=413548)
- 在把多重笔刷工具从“克隆基点并发”切换为别的类型时关闭添加子笔刷 [bug 415651](https://bugs.kde.org/show_bug.cgi?id=415651)
- 改进预制笔刷的默认四边形笔尖的渲染效果
- 设置保存文件的默认位置为 QStandardPaths::PicturesLocation [bug 415810](https://bugs.kde.org/show_bug.cgi?id=415810)
- 如果没有 mainwindow 时，不要在请求 remoteArguments 时崩溃 [bug 415794](https://bugs.kde.org/show_bug.cgi?id=415794)
- 在安卓环境，默认把拖拽滚动设为触控手势
- 延迟笔刷 paintop 小部件状态的初始化 [bug 415033](https://bugs.kde.org/show_bug.cgi?id=415033)
- 重新启用 breeze 主题，选框问题已经在新版被解决
- 如果尚未创建着色蒙版，显示手掌光标 [bug 415935](https://bugs.kde.org/show_bug.cgi?id=415935)
- 修复在笔画选择对话框的启用/停用逻辑 [bug 415896](https://bugs.kde.org/show_bug.cgi?id=415896)
- 导出 ORA 文件时，写入整个图层而不是裁切它们
- 修复在文件中指定特性文件时的无限循环问题 [bug 414818](https://bugs.kde.org/show_bug.cgi?id=414818)
- 修复在取消变形工具时崩溃 [bug 414672](https://bugs.kde.org/show_bug.cgi?id=414672)
- 修复渐变中的一处明显错误的 assert [bug 414550](https://bugs.kde.org/show_bug.cgi?id=414550)
- 修复直线工具的 1px 笔刷偏移 [bug 407405](https://bugs.kde.org/show_bug.cgi?id=407405)
- 修复 Breeze 主题的图层滤镜选框 [bug 406595](https://bugs.kde.org/show_bug.cgi?id=406595)
- 修复双数字设定框的比较
- 修复调色板工具面板不显示调色板 [bug 414890](https://bugs.kde.org/show_bug.cgi?id=414890)
- 修复替换矢量选区时的撤销操作 [bug 412808](https://bugs.kde.org/show_bug.cgi?id=412808)
- 把 Krita 的日志从系统信息日志中分离出来
- 在资源包中把 assert 改为 check [bug 399008](https://bugs.kde.org/show_bug.cgi?id=399008)
- 修复 Python 的 Canvas.setRotation 方式 [bug 416126](https://bugs.kde.org/show_bug.cgi?id=416126)
- 保存和恢复 SVG 编辑器窗口的形状 [bug 416097](https://bugs.kde.org/show_bug.cgi?id=416097)
- 修复持续变形的 assert 数 [bug 415625](https://bugs.kde.org/show_bug.cgi?id=415625)
- 修复在新文件中触控面板的保存按钮不工作 [bug 407905](https://bugs.kde.org/show_bug.cgi?id=407905)
- 修复模糊滤镜的不一致性 [bug 416241](https://bugs.kde.org/show_bug.cgi?id=416241)
- 修复图层样式的描边伪像 [bug 414582](https://bugs.kde.org/show_bug.cgi?id=414582)
- 为拾色器的浮动小部件使用 Qt::Popup [bug 410959](https://bugs.kde.org/show_bug.cgi?id=410959)
- 永远在光标下方显示浮动拾色器小部件 [bug 394139](https://bugs.kde.org/show_bug.cgi?id=394139)
- 移除强度数值与旧版 paintop 预设的兼容性 [bug 416335](https://bugs.kde.org/show_bug.cgi?id=416335)
- 修复在渲染动画时的多余错误信息 [bug 412599](https://bugs.kde.org/show_bug.cgi?id=412599)
- 修复画布偏移计算 [bug 416352](https://bugs.kde.org/show_bug.cgi?id=416352)
- 为 ORA 文件将带有已正确停用的透明度通道的图层导出为 "svg:src-atop"
- 在“关于 Krita”对话框添加关闭按钮
- 修复预设历史面板的内存泄漏
- 启用/停用插件后提醒需要重启 Krita [bug 416575](https://bugs.kde.org/show_bug.cgi?id=416575)
- 针对 Qt 5.14 因颜色管理问题阻止 PNG 保存的临时应对 [bug 416515](https://bugs.kde.org/show_bug.cgi?id=416515)
- 修复最近使用操作命令 [bug 416706](https://bugs.kde.org/show_bug.cgi?id=416706)
- 修复增大/减小笔刷大小和切换到上一个预设的按钮
- 在 master 分支修复网面和外框变形 [bug 416505](https://bugs.kde.org/show_bug.cgi?id=416505)
- 修复在调整形状大小时的抽搐性吸附 [bug 414336](https://bugs.kde.org/show_bug.cgi?id=414336)
- 修复在进行画布操作时的问题 [bug 414576](https://bugs.kde.org/show_bug.cgi?id=414576), [415773](https://bugs.kde.org/show_bug.cgi?id=415773)
- 修复小于 100px 的小图像的动画渲染问题 [bug 415367](https://bugs.kde.org/show_bug.cgi?id=415367)
- 修复矢量形状在使用变形工具后的显示 [bug 417016](https://bugs.kde.org/show_bug.cgi?id=417016)
- 修复载入带有自动生成功能的图层和文件图层时挂起 [bug 415891](https://bugs.kde.org/show_bug.cgi?id=415891)
- 修复与 Shift + 点击图层显示/隐藏图标的快速隐藏功能有关的拖慢
- 修复画布边缘的颜色问题
- 修复在保存配置时的问题
- 在 masOS 下隐藏 SubWindow 装饰
- 对 L\*A\*B\* 和 CMYK 模型的一系列修复，感谢 L.E Segovia 在本季 KDE 工作中的贡献
- 在安卓环境可以选择 OpenGL ES
- 按照 KDE 邮件列表中的讨论设置 setRedirectPolicy
- 修复载入带有 tdta OSType 的 asl 时的崩溃
- 使“保存增量版本”更新最近使用文件列表
- 用于确定是否请求了多个备份的正确逻辑 [bug 417914](https://bugs.kde.org/show_bug.cgi?id=417914)
- 修复了老旧预设中的错误共用曲线 [bug 417748](https://bugs.kde.org/show_bug.cgi?id=417748)
- 修复历史面板中的布局问题
- 修复由于次像素精度造成的笔刷轮廓闪烁 [bug 374551](https://bugs.kde.org/show_bug.cgi?id=374551)
- 在转换自选区蒙版的图层上使本地选区轮廓可见
- 修复矢量图层的卡死 [bug 412746](https://bugs.kde.org/show_bug.cgi?id=412746)
- 修复滤镜图层在应用到调整图层时的伪像 [bug 417673](https://bugs.kde.org/show_bug.cgi?id=417673)
- 修复低精度笔刷的宽高比选项
- 修复 Appimages 的启动 [bug 418230](https://bugs.kde.org/show_bug.cgi?id=418230)
- 在进行传统操作后把图像设为已修改 (修复颜色通道面板在某些情况下不更新) [bug 417992](https://bugs.kde.org/show_bug.cgi?id=417992)

## 下载

### Windows

如需试用新版或者测试版，可以先下载 zip 压缩包的版本。随便把压缩包解压到你方便的地方，点击文件夹中的 Krita 图标文件即可运行。这样不会影响之前已安装的旧版 Krita，但新旧两个版本会共享配置文件和自定义资源。如需报告程序崩溃问题，请下载调试符号包。

- 64 位 Windows 安装包：[krita-x64-4.2.9-setup.exe](https://download.kde.org/stable/krita/4.2.9/krita-x64-4.2.9-setup.exe)
- 64 位 Windows 压缩包：[krita-x64-4.2.9.zip](https://download.kde.org/stable/krita/4.2.9/krita-x64-4.2.9.zip)
- [64 位调试符号包 (解压到 Krita 安装目录)](https://download.kde.org/stable/krita/4.2.9/krita-x64-4.2.9-dbg.zip)

- 32 位 Windows 安装包：[krita-x86-4.2.9-setup.exe](https://download.kde.org/stable/krita/4.2.9/krita-x86-4.2.9-setup.exe)
- 32 位 Windows 压缩包：[krita-x86-4.2.9.zip](https://download.kde.org/stable/krita/4.2.9/krita-x86-4.2.9.zip)
- [32 位调试符号包 (解压到 Krita 安装目录)](https://download.kde.org/stable/krita/4.2.9/krita-x86-4.2.9-dbg.zip)

### Linux

- 64 位 Linux Appimage 包：[krita-4.2.9-x86\_64.appimage](https://download.kde.org/stable/krita/4.2.9/krita-4.2.9-x86_64.appimage)
- 64 位 Linux：[G'Mic-Qt 插件 appimage 包](https://download.kde.org/stable/krita/4.2.9/gmic_krita_qt-x86_64.appimage)

(如果浏览器把链接作为文本打开，请右键另存为)

### OSX

- OSX 磁盘映像：[krita-4.2.9.dmg](https://download.kde.org/stable/krita/4.2.9/krita-4.2.9.dmg)

请留意：gmic-qt 软件包在 OS X 下不可用。

### 源代码

- [krita-4.2.9.tar.gz](https://download.kde.org/stable/krita/4.2.9/krita-4.2.9.tar.gz)
- [krita-4.2.9.tar.xz](https://download.kde.org/stable/krita/4.2.9/krita-4.2.9.tar.xz)

### md5sum 验证码

适用于所有下载版本：

- [md5sum.txt](https://download.kde.org/stable/krita/4.2.9/md5sum.txt)

### 签名和密钥

Linux 的 Appimage 包和源代码 tarball 文件已签名，你可以通过 https 来下载公共密钥：[0x58b9596c722ea3bd.asc](https://share.kde.org/index.php/s/fJ99V5mZvuyD0z8)、[.sig 签名文件](https://download.kde.org/stable/krita/4.2.9/)

## 支持 Krita

Krita 是一个自由和开源的软件项目。请通过 [捐款](https://krita.org/en/support-us/donations/) 或者 [购买培训教程和画册](https://krita.org/en/support-us/shop) 等方式支持我们，这样我们才能为 Krita 的开发全职工作。

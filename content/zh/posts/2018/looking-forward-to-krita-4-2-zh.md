---
title: "Krita 4.2 预览版本和未来展望"
date: "2018-10-06"
categories: 
  - "news-zh"
  - "development-builds-zh"
---

在大家的通力协作下，我们终于可以为大家带来 Krita 4.2 的预览版本了！请留意这是一个开发途中的版本，比起稳定版本会有更多的问题，使用时请做好准备以防丢失数据。我们还计划在下周发布 Krita 4.1.4。

[![](/images/posts/2018/2018-fundraiser-hero2.png)](https://krita.org) 请支持 Krita 2018 年的开发筹款活动！

虽然预览版本会比较不稳定，但它也具备大量的改动和新功能。我们邀请你放胆一试，帮助我们进行测试和反馈所遇到的问题！当然，还有更多 Krita 4.2 计划内的新特性还在开发途中，它们尚未在这一预览版本中实现。下面我们将会为大家详细讲解 Krita 4.2 的新特性展望。

## 已经实现的特性

**蒙版和选区。**我们围绕着蒙版和选区功能进行了大量的工作，其中有一部分成果已经反馈到了 Krita 4.1.3 版本中。Krita 4.2 将会让绘制选区蒙版变得更加便捷，带来对选区本身进行移动和变形的全新方式，并全面提高相关的性能表现。选择不透明区域功能也新增了一些选项。

https://youtu.be/gWv--Do9L0E

**色域蒙版。**这是一个许多用户期待已久的新功能。它可以在颜色选择器中隐藏部分颜色。[James Gurney 的文章介绍了如何使用色域蒙版的概念](http://gurneyjourney.blogspot.com/2011/09/part-1-gamut-masking-method.html)来帮助你更加和谐地使用颜色。你可以在 Krita 中直接创建和编辑色域蒙版，并将它们应用到艺术颜色选择器和高级颜色选择器中。你还可以在颜色选择器中旋转色域蒙版。

![](/images/posts/2018/gamut-masking.png)

**更快的性能。**我们一直致力于让 Krita 运行得更快，我们相信在这一方面总会找到改进的空间。这一预览版本包含了 Andrey Kamakin 的 Google Summer of Code 工作成果，它与 Krita 的核心部件——分块引擎有关。分块引擎用于处理图层的像素数据。目前相关的开发工作尚未完全结束，如果你使用非常大的笔刷，你可能会遇到崩溃等问题。这一预览版本还包括了 Ivan Yossi 的 Summer of Code work 工作成果：使用 CPU 的矢量指令来创建笔刷蒙版，从而提升绘画性能。Dmitry 也在努力改进图层样式的性能，尤其是描边的性能。现在渲染的结果会更加准确，填充图层也变得更加快速。

**获取 Krita 的最新资讯。**欢迎屏幕现在可以显示来自 Krita 官方网站的最新资讯。此功能默认关闭，因为它需要互联网连接。目前这一功能只在 Linux 上正常工作。我们正在处理在 Windows 和 macOS 所需的程序库。

[![](/images/posts/2018/news_widget-1024x566.png)](/images/posts/2018/news_widget.png)

**绘画辅助尺着色。**这项功能让你可以分别为绘画辅助尺指定不同的颜色，并且可以被保存到 .kra 文件中后在下一次加载时复原。

**粘贴后自动切换到变形工具。**在 Krita 中，每次当你进行粘贴操作时都会将粘贴的内容新建为一个图层。在绝大多数情况下人们在粘贴之后都会立即进行移动或者变形操作。为此我们在 Krita 的首选项中新增了一个新选项，勾选后 Krita 将在粘贴操作之后立即切换到变形工具。

**移动工具改进。**在使用 Krita 的移动工具时进行撤销和重做曾经不太正常，现在相关的操作得到了改进。这虽然不是一项大的改进，但对用户的工作流程却相当有帮助。

**用户界面改进。**Krita 将会带来许多与改进工作流程有关的小修正，如实现更改图层工具面板预览图大小、改进的调色板交互方式、实现 Python 插件的翻译等等。除此之外还有一系列全新的混合模式正在陆续被添加进来，G'Mic 插件也被更新到了最新版本。

\[video width="344" height="502" mp4="/images/posts/2018/resize-thumbnail.mp4"\]\[/video\]

**大量的问题修复。**目前我们已经为 Krita 4.2 修复了近 200 个问题，这个数字每天都在增长。

## 正在开发的特性

我们的工作还没有做完。Krita 4.2 计划在今年的 12 月份发布，但我们还没有完成功能冻结。下面我们会介绍一些有机会进入 4.2 的特性。

**笔刷编辑器界面的重新设计。**这项改进尚未在此预览版本中实现，但我们的 UX 专家 Scott 正在为此努力。在下面的视频里你可以看出我们正在设法把界面变得更为紧凑，这是因为我们希望可以把笔刷编辑器放到一个工具面板上，或者作为一个浮动面板显示在另一个显示器上。

https://youtu.be/2hWPzNFPIxY

**文本工具界面的重新编写。**Dmitry 正在改进文本工具的可靠性，Scott 则在改进其易用性。

https://youtu.be/pNsifPZJsjw

**新的调色板系统。**Michael 的 Summer of Code 工程尚未被合并进来，但我们非常希望能够在正式版本中包含他的成果。这会让调色板相关的操作变得更加可靠，并将调色板保存到 .kra 文件中。

**资源管理框架的重建。**这里指的是为包括笔刷预设、笔刷头、渐变和图案等进行载入、编辑、标签、保存和分享的相关功能。这是一个规模庞大的工程，但它会为 Krita 带来更快的启动速度，更小的内存消耗，并根绝围绕着资源管理的一系列疑难杂症。

现在，请尽情试用 Krita 4.2 预览版吧！

[![](/images/posts/2018/4.2-preview-1024x693.png)](https://www.krita.org)

## Download

### Windows 版本

- 64 位 Windows 安装程序：[krita-x64-4.2.0-preview-setup.exe](https://download.kde.org/unstable/krita/4.2.0-preview/krita-x64-4.2.0-preview-setup.exe)
- 64 位 Windows 压缩包：[krita-x64-4.2.0-preview.zip](https://download.kde.org/unstable/krita/4.2.0-preview/krita-x64-4.2.0-preview.zip)
- [64 位软件调试符号包](https://download.kde.org/unstable/krita/4.2.0-preview/krita-x64-4.2.0-preview-dbg.zip) (解压到 Krita 的安装目录)

- 32 位 Windows 安装程序：[krita-x86-4.2.0-preview-setup.exe](https://download.kde.org/unstable/krita/4.2.0-preview/krita-x86-4.2.0-preview-setup.exe)
- 32 位 Windows 压缩包：[krita-x86-4.2.0-preview.zip](https://download.kde.org/unstable/krita/4.2.0-preview/krita-x86-4.2.0-preview.zip)
- [32 位软件调试符号包](https://download.kde.org/unstable/krita/4.2.0-preview/krita-x86-4.2.0-preview-dbg.zip) (解压到 Krita 的安装目录)

### Linux 版本

- 64 位 AppImage：[krita-4.2.0-preview-x86_64.appimage](https://download.kde.org/unstable/krita/4.2.0-preview/krita-4.2.0-preview-x86_64.appimage)
- 64 位 G’Mic-Qt 插件 AppImage：[G'Mic-Qt plugin appimage](https://download.kde.org/unstable/krita/4.2.0-preview/gmic_krita_qt-x86_64.appimage).

(如果 Firefox 把下载文件当作文本打开，请在连接上点击右键/另存为)

### OSX 版本

- OSX 磁盘映像文件：[krita-4.2.0-preview.dmg](https://download.kde.org/unstable/krita/4.2.0-preview/krita-4.2.0-preview.dmg)

注意：触控工具面板、gmic-qt、Python 插件在 OSX 上暂不可用。

### 源代码

- 源代码：[krita-4.2.0-preview.tar.gz](https://download.kde.org/unstable/krita/4.2.0-preview/krita-4.2.0-preview.tar.gz)

### md5sum

所有下载文件的 md5sum：

- [md5sum.txt](https://download.kde.org/unstable/krita/4.2.0-preview/md5sum.txt)

---
title: "2020 年谷歌代码之夏 Krita 项目课题报告"
date: "2020-09-10"
categories: 
  - "news-zh"
---

2020 年谷歌代码之夏活动已经进入课题评估环节，今年共有 4 位学生负责 Krita 项目课题。现在让我们一览他们的努力成果吧！

## SeExpr 脚本填充图层支持

**Amy Spark** 的课题是 SeExpr 脚本填充图层支持。填充图层是一种按照设置动态生成内容的图层。SeExpr 是迪士尼主导设计的图案生成程序库，它带有一套使用 Qt 编写的界面元素。

Amy Spark 的课题不但让 Krita 可以使用 SeExpr 脚本来生成填充图层，还改善了 SeExpr 表达式编辑器的易用性，并让 SeExpr 可被翻译为其他语言。你还可以保存 SeExpr 脚本为资源，以便日后调用或者与他人分享。(中国大陆用户需要科学上网才能观看下方视频)

<iframe src="https://diode.zone/videos/embed/b441f360-0b94-470a-8365-5a5f44b3a617" width="560" height="315" frameborder="0" sandbox="allow-same-origin allow-scripts allow-popups" allowfullscreen="allowfullscreen" data-mce-fragment="1"></iframe>

SeExpr 脚本填充图层的效果千变万化，可以用来制作各种纹理特效。现在此课题的成果已经包含在每天更新的开发测试版本中，将在 9 月份随 Krita 4.4 版一同正式发布。如果你对课题细节感兴趣，请移步阅读 Amy Spark 的 [课题报告](https://community.kde.org/GSoC/2020/StatusReports/LeonardoEmanuelSegovia)，也可以前往阅读相关的 [参考文档](https://docs.krita.org/zh_CN/reference_manual/layers_and_masks/fill_layer_generators/seexpr.html) (已翻译为中文)：

\[caption id="attachment\_10913" align="aligncenter" width="1024"\][![](/images/posts/2020/1096px-SeExpr_manual_1-1024x840.jpg)](https://docs.krita.org/en/tutorials/seexpr.html) SeExpr 参考文档\[/caption\]

## MyPaint 笔刷引擎整合

**Ashwin Daikata** 的课题是将 [MyPaint](http://mypaint.org/) 的笔刷引擎整合到 Krita。这其实已经是我们第二次整合 MyPaint 的笔刷引擎了，但上一次整合时的程序速度不够理想，而且我们当时必须整合 MyPaint 的内部代码，成本很高却效果不好，最终没能保留下来。现在 MyPaint 的笔刷引擎已经从它的主程序中分离出来成为一个程序库，因此 Krita 再次整合 MyPaint 笔刷引擎变得更加方便易行。

[![](/images/posts/2020/Particules_eraser_2.png)](https://krita.org/wp-content/uploads/2020/08/Particules_eraser_2.png)

Ashwin 出色地完成了他的工作，在默认的 8 位 RGBA 图层上作画时，整合的 MyPaint 笔刷引擎的工作速度和在 MyPaint 中没有差别。

[![](/images/posts/2020/preset_selector.png)](https://krita.org/wp-content/uploads/2020/08/preset_selector.png)整合的 MyPaint 笔刷引擎不但工作正常，你还可以使用它们在 Krita 中制作、编辑笔刷预设。

[![](/images/posts/2020/Preset_editor-1024x568.png)](https://krita.org/wp-content/uploads/2020/08/Preset_editor.png)

MyPaint 笔刷引擎整合工程将很快被合并到主分支，并随今年年底的 Krita 5.0 发布。

欲知课题详情，可阅读 Ashwin 的 [课题报告](https://community.kde.org/GSoC/2020/StatusReports/AshwinDhakaita)。

## 分镜头面板

**Saurabh Kumar** 为 Krita 开发了分镜头面板。它依托于 Krita 的动画功能，可以随时点击分镜头列表切换画布内容，还可以将分镜头列表按照指定的布局导出为 SVG 或者 PDF 格式。

\[caption id="attachment\_10957" align="aligncenter" width="601"\][![](/images/posts/2020/Storyboard_custom_options.png)](https://krita.org/wp-content/uploads/2020/09/Storyboard_custom_options.png) 指定导出分镜头列表布局\[/caption\]

你可以选择仅查看缩略图或者注释，也可以并列显示所有内容：

\[caption id="attachment\_10956" align="aligncenter" width="473"\][![](/images/posts/2020/Storyboard_row_mode.png)](https://krita.org/wp-content/uploads/2020/09/Storyboard_row_mode.png) 多列竖排布局的分镜头列表\[/caption\]

欲知课题详情，请阅读 Saurabh 的 [课题报告](https://community.kde.org/GSoC/2020/StatusReports/SaurabhKumar)。

## SVG 网格渐变

**Sharaf Zaman** 在 2019 年的谷歌编程之夏中将 Krita 移植到了安卓。今年她的课题则是在 Krita 中再一次实现 SVG 网格渐变。此功能前一次是由 Tavmjon Bah 通过 [Inkscape](http://tavmjong.free.fr/blog/?p=316) 实现的。

此课题最棘手的工作是如何对渐变进行渲染：

\[caption id="attachment\_10919" align="aligncenter" width="296"\][![](/images/posts/2020/Screenshot_2020-07-23_11-46-06.png)](https://krita.org/wp-content/uploads/2020/08/Screenshot_2020-07-23_11-46-06.png) 从 Inkscape 导入的网格渐变\[/caption\]

不同的 2D 图形程序库对图形的渲染方式不完全一致，Sharaf 设法克服了这个难题，让 Krita 可以和 Inkscape 以同样的方式渲染网格渐变。

为了使此课题的成果可以派上用场，Sharaf 扩展了 Krita 的 SVG 解析器，让它可以支持网格渐变扩展，同时还要让 Krita 能够在渲染后正确保存生成的图形。

最后她还为网格渐变准备了对应的图形界面以便操作：

[![](/images/posts/2020/Handles-meshgradient-1024x554.png)](https://krita.org/wp-content/uploads/2020/08/Handles-meshgradient.png)

SVG 网格渐变的选项将被包含在矢量形状选择工具的的工具选项面板中：

![](/images/posts/2020/Tooloptions-meshgradient.png)

欲知课题细节，可阅读 Sharaf 的 [课题报告](https://community.kde.org/GSoC/2020/StatusReports/SharafZaman)。

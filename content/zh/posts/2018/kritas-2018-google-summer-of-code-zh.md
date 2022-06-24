---
title: "Krita 2018 年度 Google Summer of Code 工作报告"
date: "2018-09-06"
categories: 
  - "news-zh"
---

今年的 Google Summer of Code 活动中有三位学生参加了 Krita 的项目，他们是 [Ivan](https://colorathis.wordpress.com/), [Andrey](https://lieroz.github.io/) 和 [Michael](https://simeir.github.io/)。他们贡献的代码有一部分已被应用到了 Krita 4.1.1，余下的绝大部分代码也已经整合到了主分支，你可以通过 [Windows](https://binary-factory.kde.org/job/Krita_Nightly_Windows_Build/) 或者 [Linux](https://binary-factory.kde.org/job/Krita_Nightly_Appimage_Build/) 的每夜更新版本进行测试。下面我们将介绍他们在今年 GSoC 中的工作成果。

**Ivan** 负责的工程是通过矢量化来提高笔刷绘制速度。它的原理是利用 CPU 的一项特性——只要运算方式保持不变，仅改变输入的数据，CPU 在同一时间内能够处理大量的数据。例如我们提供 200 个数字给 CPU，然后告诉 CPU 对这些数字全部进行乘法运算，CPU 处理这组运算所需的时间和单个数字的乘法运算所需时间相同。笔刷绘制在本质上和前面的例子是一样的，但想要实现相同的处理逻辑需要克服一些困难。Ivan 已经在预制笔刷引擎中实现了这个目标。我们借用他[博客](https://colorathis.wordpress.com/)上的一则演示动图来说明他的工程带来的速度提升：

[![](/images/posts/2018/avx_cgauss_60.gif)](/images/posts/2018/avx_cgauss_60.gif)

上半部分是以前的处理速度，下半部分是现在的处理速度。

**Andrey** 的项目也是与性能有关。现代 CPU 通常具备多个核心——例如四核心八线程、十核心 20 线程，甚至更多。但许多程序只能利用一个核心，造成了大量的浪费。Krita 对多核心的利用由来已久，其中就包括它的分块引擎。该引擎在 2009 年的 [GSoC](http://dimula73.blogspot.com/2009/08/gsoc-krita-tile-engine-wrap-up.html) 项目中由 Dmitry Kazakov 开发，它可以把一张完整的图像分割成多个小块，分别交给不同的 CPU 进程并行处理，这样可以增加 CPU 的利用率以提升性能。九年后的今天 Dmitry 又指导了 Andrey 进一步改进了该引擎。

去年 Dmitry 在改进 Krita 的多核心支持时发现了一个问题：Krita 在某些情况下会强制多个核心相互等待。Andrey 的工程就是要在分块引擎中解决这个问题。现在这项工作已经大致完成，其中一部分改进已经整合到了 Krita 4.1.1，但余下的部分有一些相当棘手的 bug，需要进行深入测试后留待年底的 Krita 4.2 中整合。下表列出了该工程带来的性能提升幅度：

[![](/images/posts/2018/lockless-1024x506.png)](/images/posts/2018/lockless.png)

**Michael** 的工程是改进 Krita 的调色板系统。调色板是包含有一组预制颜色的资源，用于快速选取颜色。Krita 的调色板的编辑功能原本是和 Calligra 的其他组件共享代码的，这个传统甚至可以追溯到 KOffice 的时代。也是因为这个原因，相关的代码分散在项目的各个角落，关系错综复杂。Micheal 的第一阶段的工作就是重新组织这些代码，让它们变得集中而有条理。Krita 4.1.1 已经整合了这项改进。

Michael 的下一个工程是改进调色板工具面板，详情可参考 [他为此建立的 Phabricator 任务](https://phabricator.kde.org/D14815)。这项工作还未结束，但 GSoC 计划内的部分已经完成了。下面我们预览一下新调色板工具面板的草案：

[![](/images/posts/2018/listanddocker-1024x512.jpg)](/images/posts/2018/listanddocker.jpg)

新调色板编辑对话框草案：

[![](/images/posts/2018/DlgPaletteEditor-1024x517.png)](/images/posts/2018/DlgPaletteEditor.png)

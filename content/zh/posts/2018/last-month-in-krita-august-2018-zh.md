---
title: "Krita 项目 2018 年 8 月开发工作报告"
date: "2018-09-09"
categories: 
  - "news-zh"
---

Krita 项目曾经会每周发布一次开发工作报告，但随着开发任务变得愈发繁重，维持每周报告开始变得不太现实。虽然大家也可以通过 [git 历史](https://github.com/KDE/krita)来查看开发进度，但它欠缺条理。现在我们决定以每月一期的形式来总结开发工作近况。

八月份的一项重要工作是为新一轮大规模筹款活动进行准备，我们将在九月中旬到十月中旬为下一轮的 Krita 开发工作募集资金。我们之前的筹款活动围绕着新功能展开，而这次筹款将围绕着稳定性和细节优化展开。“程序零问题”是我们的口号，尽管实现它不太可能。我们正在迁移到一个新的付款服务提供商，这将带来在 Paypal 和银行汇款之外的更多捐赠途径，如信用卡和其他电子支付系统，甚至包括比特币。部分新功能已经在[我们的捐款页面上线](/support-us/donations/)。

前述的稳定性和细节优化工作已经开始，我们修复了大量曾经失败的单元测试 (unittests)。单元测试是一些短小的代码片段，用于测试 Krita 的各项功能。我们通过运行单元测试来检验开发产生的新代码是否对已有的部分造成负面影响。除此之外我们也修复了近百个程序问题。今年 Krita 在 [Google Summer of Code](https://krita.org/en/item/kritas-2018-google-summer-of-code/) 的开发工作也已经完成。

下面我们展开说明几个较为重要的改进：

### 持续优化代码质量

在将 Krita 移植到 Qt5 之后，我们发现有相当数量的单元测试无法正常工作。它们要么无法编译，要么在运行时挂起，要么给出错误的结果，甚至干脆造成崩溃。八月的高温炙烤着大脑，不利于创造性思维，所以我们把精力主要放在修复这些已知问题上面。

### 改进选区工具

Dmitry 是我们的核心开发人员之一。在大家的捐赠的帮助下，他得以为 Krita 项目全职工作。最近数周他一直在[改进 Krita 的选区工具](https://phabricator.kde.org/T3920)。Krita 的选区与其他同类软件不同，它同时具备本地和全局选区功能，选区可以通过蚂蚁线或蒙版方式进行可视化，选区可以是像素的，也可以是矢量对象。Dmitry 的改进包括：

- 在选区蒙版上实时绘制
- 支持一个以上的本地选区
- 全局选区支持新增、相交、移除不透明区域
- 选中“现实全局选区”后自动创建一个选区
- 支持矢量和像素选区的相互转换
- 支持对选区本身进行调整

https://www.youtube.com/watch?v=gWv--Do9L0E

### 重写资源管理系统

Krita 资源包括笔尖形状、笔刷预设、渐变和图案预设、工作空间预设等。Krita 自带了一些资源，用户也可以创建自己的资源，或者使用网上下载到的现成资源。Krita 的资源管理系统是在遥远的二十世纪编写的老古董了，当时人们加载几个直径 50 px 的笔刷，再加上几块 128 px 见方的图案，就觉得很了不起了。而现在，直径 1000 px 的笔刷，5000 px 见方的图案到处都是，人们把大量的这种巨型资源往资源库里塞。时代已经改变，旧系统已经无法满足新时代用户的需求。

在 Krita 主体一再脱胎换骨的同时，老旧的资源管理系统却被落在了后面。二十几年来我们缝缝补补将就着用，把它的代码搞得乱七八糟。有些程序员认为[重写是不好的习惯](https://www.joelonsoftware.com/2000/04/06/things-you-should-never-do-part-i/)，但我们觉得重写是最好的选择。Boudewijn 已经进行了大量的工作，不过它们尚未进入用户视野，你可以在[相关的 Phabricator 任务](https://phabricator.kde.org/T379)中查看详情。我们已经为此进行了周密的计划和长期的讨论。如果一切按计划进行，与资源的标签、添加、移除、更改相关的程序问题将会被一举解决。

[![](/images/posts/2018/resource_db_explorer-300x145.png)](https://krita.org/wp-content/uploads/2018/09/resource_db_explorer.png)

### 新功能和小惊喜

Anna Medonosova 开发了一个相当有趣的新功能：色域蒙版。它可以被应用到艺术颜色选择器，也可以对已有的色域蒙版进行编辑。详情可参考 [James Gurney 的博客文章](https://gurneyjourney.blogspot.com/2008/01/color-wheel-masking-part-1.html)。

[![](/images/posts/2018/gamut-300x300.png)](https://krita.org/wp-content/uploads/2018/09/gamut.png)

新增调试日志工具面板，这样 Windows 用户就再也不必与 Debug View 打交道了。

[![](/images/posts/2018/log-docker-300x300.png)](https://krita.org/wp-content/uploads/2018/09/log-docker.png)

(图画作者 [Iza Ka](http://LifeFinalEdited.pl))

除此之外，Reptorian 创建了一系列新的混合模式，他现在正在开发新的选区相交模式。Jouni 正在处理参考图像工具面板的问题，并且为动画功能实现了[克隆帧](https://phabricator.kde.org/T8764)。

---
title: "Krita 2018 年度开发冲刺聚会报告"
date: "2018-05-22"
categories: 
  - "news-zh"
---

这个周末，来自世界各地的 Krita 开发人员和绘画作者们齐聚在荷兰代芬特尔这个沉闷的偏僻小镇采购本地特产的奶酪……我的意思是为了 Krita 努力工作！不过话说回来，代芬特尔的本地特产奶酪[在荷兰也算是数一数二](http://www.kaashandel-debrink.nl/)。而 Krita 基金会的总部也设在这里。活动在周四开始，最后一位活动参加者则在今天离开。

\[caption id="attachment\_6665" align="aligncenter" width="1024"\][![](/images/posts/2018/2018-05_Krita-sprint_Deventer-1024x345.jpg)](https://krita.org/wp-content/uploads/2018/05/2018-05_Krita-sprint_Deventer.jpg) David Revoy 摄影\[/caption\]

像这样能让大家齐聚一堂的活动是非常重要的。团队成员们在进行严肃的讨论和开发工作之余共同进餐、闲谈和散步，这样可以增进友谊，让回到 # Krita IRC 聊天室之后的协作变得更加顺畅。我们在 2017 年没有组织大型的开发冲刺聚会，上次举办这样的大型聚会已经是在 [2016 年](https://krita.org/en/item/2016-krita-sprint-day-1/)了。

那么我们都在本次聚会里做了什么呢？我们[首先举行了一场长会](https://files.kde.org/krita/krita_meeting_docs/Other%20Meetings/2018%20Krita%20Sprint%20Meeting.odt)，讨论了以下话题：

- **2018 年度的筹款计划**：我们现在每个月能收到 €2000 左右的捐款，这里面包括了来自 80 多位开发赞助人提供的稳定的每月捐款。这让我们得以资助 Dmitry 开展工作。虽然项目的财务状况有所好转，不过我们还是打算在今年九月份前后举办一次年度筹款活动。筹款活动非常好玩，它让我们能够把 Krita 的社区动员起来。我们打算把这次筹款活动办成一个节日庆祝那样的热闹活动。不过我们这次将不会考虑 Kickstarter 了，它已经显露出疲态。我们也不打算设立新功能之类的开发目标，这是因为……
- **今年的目标是**：“zarro bugs！” (以往 bugzilla 错误追踪系统里要是一个不留地解决了问题，就会显示这个) 在过去的数年里我们实现了大量的新功能，并将 Krita 移植到了 Qt 5。所有这些工作都产生了巨量的新代码。但这并不意味着我们的工作就此结束了——相反：我们尚未处理的问题报告多得数不过来，无法完成的程序的单元测试多得数不过来，[源代码的 PVS 警告](https://www.viva64.com/en/b/0569/)多得数不过来，还没做完的新功能也多得数不过来！解决上述问题便是我们今年想要完成的目标。
- [**未完成工作**](https://phabricator.kde.org/T8758)：我们确定了一些我们尚需解决的未完成工作，然后向绘画作者们征集任务的优先顺序，以下就是我们讨论的结果：
    - Boudewijn 的工作是：
        - [改良资源包管理器](https://phabricator.kde.org/T379)
        - 修复快捷键、画布输入整合以及相关问题
        - 改良 G'MIC 功能集成
    - Dmitry 的工作是：
        - 蒙版和选区
        - 改良文本排版引擎，实现 OpenType 支持、竖排文本以及更多的 SVG2 特性
        - SVG 支持收尾工作：滤镜、图案、缠绕填充、对象组合等
        - 图层样式收尾工作
    - Jouni 的工作是：
        - 动画的帧周期循环以及克隆帧
        - 动画的变形蒙版插值曲线支持
    - Wolthera 的工作是：
        - 收集脚本 API 的遗漏信息
        - 色调分阶滤镜组
- **发布新版软件**。我们计划在 6 月 20 日发布 Krita 4.1.0，它将会包含大量新增动画功能、动画内存交换、会话管理器、参考图像工具等新特性。同时我们将继续每月发布一次问题修复版本。我们已经请求 KDE 的系统管理员们提供了稳定分支的每夜编译版本，在正式版发布之前供用户测试。

我们还讨论了资源包管理器的改良计划、努力使得 OpenGL 画布响应速度更快 (尤其在 Mac OSX 上)、将 FFMpeg 打包进 Windows 版本的安装程序、修正了翻译问题、改善了自动保存功能的可靠性、修复了大量动画相关问题并为色调分阶功能实现了跨通道色彩曲线滤镜。没有来到聚会现场的开发人员也没有闲着。他们改善了 OpenEXR 的加载，实现了包括多线程在内的一些功能、精简了颜色选择器的代码并修复了它的一些问题、还对动画时间线进行了诸多改进。

这还不是全部。Wolthera、Timothee、Raghukamath 三人还将 Krita 的使用手册移植到了 Sphinx，这样我们在进行翻译工作和生成离线版本的时候就方便多了。我们现在才发现，这本使用手册已经有 1000 多页了！

有三位参会人员是第一次出席开发冲刺聚会：绘画作者 Raghukamath、ace windows 开发人员 Alwin Wong、KDE Plasma 数位板设置工具的项目负责人 Valeriy Malov。Valeriy 在这几天里改良了对 Cintiq 一类的数位屏的支持。

当然，我们也留出了时间来散步、采购本地特产奶酪、在我们的老地方 [De Rode Kater (红猫公饭店)](http://www.derodekater.nu/) 里用餐。到了周日，荷兰六月的天空竟然放晴了！继续写代码吧！

\[caption id="attachment\_6669" align="aligncenter" width="1024"\][![](/images/posts/2018/rode_kater-1024x529.jpg)](https://krita.org/wp-content/uploads/2018/05/rode_kater.jpg)David Revoy 摄影\[/caption\]

2018 年度 Krita 开发冲刺聚会的旅行费用由 KDE e.V.赞助；住宿以及餐饮费用由 Krita 基金会赞助。

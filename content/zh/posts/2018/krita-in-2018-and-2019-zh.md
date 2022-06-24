---
title: "Krita 2018 年回顾与 2019 年展望"
date: "2018-12-25"
categories: 
  - "news-zh"
---

转眼间又到了一年的年底，正如我们去年[回顾了 2017 年并展望了 2018 年一样](https://krita.org/en/item/looking-back-looking-forward/)，今天我们将继续这个传统，回顾 2018 年 Krita 项目的工作并对 2019 年的发展进行展望。整体而言，2018 年对 Krita 来说是一个比 2017 年要好的年份，我们在年内设法达成了多个项目的里程碑。

我们发布了 **[Krita 4.0](https://krita.org/en/item/krita-4-0-0-released/)**，它包含了 Python 脚本支持，一个重新编写但尚未羽翼丰满的文字工具，矢量图像从 ODG 格式切换到了 SVG 格式，以及许多其他的新功能与改进。

{{< youtube a-CY4hmkg_I >}}

在那之后，我们陆续发布了版本 [4.0.1](https://krita.org/en/item/krita-4-0-1-released/)、[4.0.2](https://krita.org/en/item/krita-4-0-2-released/)、[4.0.3](https://krita.org/en/item/krita-4-0-3-released/)、[4.0.4](https://krita.org/en/item/krita-4-0-4-released/)、[4.1.0](https://krita.org/en/item/krita-4-1-0-released/)（此版包含全新的[参考图像工具、会话管理功能等新功能](https://krita.org/en/krita-4-1-release-notes/)）、[4.1.1](https://krita.org/en/item/krita-4-1-1-released/)、[4.1.3](https://krita.org/en/item/krita-4-1.3-released/)、[4.1.5](https://krita.org/en/item/krita-4-1.5-released/) 和 [4.1.7](https://krita.org/en/item/krita-4-1.5-released/)。全部加起来我们今年一共发布了 10 次新版软件，颇为接近我们每月发布一个新版本的目标。然而我们并不对这个成绩感到非常满意。我们原本打算在今年年内发布 4.2.0 版，把我们 Google Summer of Code 学生们的贡献全部包含进来。遗憾的是其中一个重要的部分依然没有完工，它会影响程序处理大型图像时的稳定性。与此同时，新代码也在源源不断地进入 Git 的主开发分支，为了不忘记这些变化，我们已经[开始着手准备新版的更新日志](https://krita.org/en/krita-4-2-release-notes/)了。

说起 [**Google Summer of Code**](https://summerofcode.withgoogle.com/archive/)，我们以 [KDE](https://www.kde.org) 项目的名义参加了 GSoC 2018 的活动。分配给我们的三位学生全部成功完成了各自的工程，现在他们贡献的代码已经整合进来，但还有一些打磨需要完成。总的来说今年的 GSoC 活动收获颇丰。

Google Summer of Code 在 2019 年将迎来全新一届的活动。我们现在还不确定 KDE 会不会参与下一届的 GSoC，但我们已经[罗列了一些开发目标供学生们参考](https://community.kde.org/GSoC/2019/Ideas)。这些是颇具挑战性的任务，如果你感兴趣，请尽早和我们的开发人员社区联系！

[![](/images/posts/2018/2018-fundraiser-hero2.png)](/images/posts/2018/2018-fundraiser-hero2.png)

我们还举办了[**一场成功的筹款活动**](https://krita.org/en/fundraising-2018-campaign/)。这次我们并没有使用 Kickstarter，所以[很难为筹款活动带来流量](https://mail.kde.org/pipermail/kde-community/2018q4/004976.html)。但另一方面，除去了 Kickstarter 的分成之后，我们筹得的款项与 2016 年的相当接近，能够确保支持七、八个月的开发工作。

### [![](/images/posts/2018/busy.png)](/images/posts/2018/busy.png)网站访问统计概况（上图）

- 4,292,309 位独立访客
- 12,416,956 次页面点击，9,726,467 次独立页面点击
- 2 分 57 秒的平均访问停留时间
- 140,163 次搜索到本站，通过 1,763 个独立关键词
- 36% 的访问反弹（查看第一页后即离开网站）
- 2,060,689 次下载，1,699,170 次独立下载
- 3.6 次操作每访客（页面点击，下载，外链和站内搜索等）
- 644,797 次外链，568,971 次独立外链
- 0.48 秒平均页面生成时间
- 26,567 次最大单独访客操作数

我们的社区也在继续发展壮大。Krita 在一年里差不多被下载了 200 万次，而这还不包括官方网站之外的下载量。未被统计在内的包括但并不限于 Windows Store、重装出发的 Steam Store、社区运作的 flatpak，各大下载网站收录的 Windows 版和各大 Linux 发行版收录的软件包也越来越接近我们的最新版本。

Krita 的核心团队虽然很乐于与用户互动，但说句实话十几个人很难对来自庞大用户群的提问进行逐一作答。为了不影响我们的开发工作，我们架设了一个[问答网站](https://ask.krita.org)，我们希望通过这种全新的形式鼓励社区用户进行互助。

总的来说，2018 年是一个不错的年份。那么 2019 年会带来怎样的新气象呢？

首先当然是发布新版软件了。我们正在全力以赴准备 Krita 4.2。每日编译的开发版本已经包括了许多新功能和新改动，除此之外我们目前还在进行两个特殊工程：

通过与 Intel 紧密合作，我们正在为 [**HDR 绘画支持**](https://phabricator.kde.org/T9256)进行准备。我们在这里颇为超前，能支持相关功能的硬件相当少见，而唯一支持它的操作系统是 Windows 10（Linux 内核和 X11 的图形驱动也已经有初步的前置开发工作正在进行）。

但在功能验证层面上，我们已经成功地让该功能正常工作了——在 1000 nits 的宽色域显示器下面绘画简直是一种魔幻的体验！我们希望 HDR 视觉支持能够成为 Qt 的组成部分，让其他应用程序也能跟上潮流。当然相关硬件的普及和操作系统的支持也是必不可少的。

另一个在 2018 年耗费了大量时间但尚未完工的大工程则是**资源系统的重新编写**工作了。资源这个概念包括笔尖、预设、图案、渐变等。当 Krita 的前身 KImageShop 在 20 年前起步的时候，电脑的磁盘、内存都非常小。那时候人们觉得 1024x768 像素的图像简直大得不行，图案和笔刷只有一丁点大，人们也只会在程序里放置很少这类资源。

时至今日，资源的体积日渐庞大，人们也倾向于无止境地囤积它们。我们用于处理资源的代码不但显得老旧，也在多年的开发中也变得错综复杂不便维护。我们在 2017 年开始设计一个新的资源系统，在 2018 年投入了大量时间进行实现，这个工程还未完工。我们的目标是让新的资源管理系统更加节约内存，减少程序的启动时间并提高稳定性。

当然我们还会投入相当的精力去修复程序的问题，改进程序的性能并发布新版软件！

随着时间进入 2019 年，[Krita 项目也将迈入它的第 20 周年](https://phabricator.kde.org/R511:3e91e954652b9db5c715b71c717b2a58cfe49bcd)！

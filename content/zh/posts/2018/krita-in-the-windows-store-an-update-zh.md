---
title: "Krita Windows Store 版软件描述调整说明"
date: "2018-07-31"
categories: 
  - "news-zh"
---

这篇文章对 Krita 的 Windows Store 版的软件描述调整情况进行了说明。

Krita 已经在 Windows Store 上面发行了一段时间了。迄今为止绝大多数的用户是在 Krita.org 上下载 Krita 的，下载量为每周约三万次；而 Windows Store 的下载量则是每周约 125 次。Windows Store 版的下载量看起来虽然微不足道，但它产生的收入让 Krita 的项目负责人能够全职为 Krita 工作，免去了曾经一边维护 Krita 一边从事另外一份全职工作的压力。顺便一提：我们每月收到的约 2000 欧元的捐赠只能维持主程序员之一的 Dmitry 为 Krita 全职工作。

通过 Windows Store 版获得一些收入当然是好事，但也不全是好事。在 Windows Store 上发行软件意味着你成了微软的[佃农](https://en.wikipedia.org/wiki/Sharecropping)——活儿都是你干的，然而收成可以留下多少则是微软说了算，你完全没有发言权。Windows Store 对于开发者有一套限制条款，而如何解释这些条款也是微软的管理员们说了算——即便是他们的解释完全不符合人类的逻辑，你也只得乖乖听话，按照他们说的去做。

因为 Windows Store 条款的缘故，我们在不到一年的时间里来来回回更改了差不多有 20 次软件描述。一开始我们曾经在商店的说明里提及用户可以在 Krita.org 网站上免费获取 Krita 软件和源代码：

 

[![](/images/posts/2018/store_listing-1024x980.png)](https://krita.org/wp-content/uploads/2018/07/store_listing.png)对此，微软认为违反了他们的[应用商店条款第 10.8.5 条](https://docs.microsoft.com/en-us/legal/windows/agreements/store-policies#108-financial-transactions)：

[![](/images/posts/2018/Screenshot_20180730_151859.png)](https://krita.org/wp-content/uploads/2018/07/Screenshot_20180730_151859.png)

“你的软件只能通过 Microsoft Store 进行宣传和分发软件。”

然而上述条款是第 10.8 条的一部分：

[![](/images/posts/2018/Screenshot_20180730_151934-1024x138.png)](https://krita.org/wp-content/uploads/2018/07/Screenshot_20180730_151934.png)

“如果你的软件包含内购、订阅、虚拟货币、扣费功能或获取财务信息，则下述要求将被适用：”

我们觉得很明显，只有在你的软件含有第 10.8 条所述的那些东西时，第 10.8.5 条才会被适用。因此只要你的软件没有那些东西，该条文就不应被适用。然而微软并不这么认为，对于 Krita 项目管理人的提问他们回复如下：

[![](/images/posts/2018/mail_microsoft-1024x443.png)](https://krita.org/wp-content/uploads/2018/07/mail_microsoft.png)

“第 10.8.5 条款依然适用于你的软件。请更新软件的元数据并移除在 Windows Store 之外安装软件的有关 URL。如果那些 URL 不被移除，你的软件将会继续遇到与认证相关的困难。”

第 10.8 条所述的“如果”条件并不适用于 Krita 的情况，这个我们在此姑且不论，那个微软想要移除的链接也不是在应用商店之外，而是在应用商店的软件描述处，而第 10.8.5 显然没有对此作出任何限制。

我们认为微软很清楚 Krita 是在 GNU 协议下发行的开源软件，他们对于 Krita 在 Windows Store 之外有另外的发行途径是心知肚明的，毕竟一开始帮助 Krita 上架 Windows Store 的并不是别人，就是他们自己。他们之所以会这么做，大概是因为 Windows Store 至今也没有太多值得一提的产品吧。

说了这么多，但毕竟我们并没有与微软讨价还价的权力，因此我们只得按照他们的要求修改软件描述了。

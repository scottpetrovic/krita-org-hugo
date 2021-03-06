---
title: "Krita 开发冲刺聚会 2018：wacomtablet 项目报告"
date: "2018-06-02"
categories: 
  - "news-zh"
---

在 2018 年度的 Krita 开发冲刺聚会上我们迎来了一位特殊嘉宾： Valeriy Malov，Plasma 桌面环境项目的 Wacom 数位板控制面板模块的项目负责人。我们邀请他分享在这次活动中的体验和成果，下面就是他的总结：

大家好：

以下便是我的 2018 年度 Krita 开发冲刺聚会报告，同时我也将借此机会对 KDE Plasma 的 [wacomtablet](https://userbase.kde.org/Wacomtablet) 项目的近况进行说明，作为该项目新版发布的预热。

### Krita 2018 年度开发冲刺聚会

就在数周前我出席了 Krita 开发冲刺聚会。这是一场既有趣又富有成果的活动。Boudewijn、Timothee 和 Raghukamath 在他们的电脑上测试了 wacomtablet 的 git 版本。我也通过 KCM 测试了一系列 Wacom 设备，收集了一些用户意见并编写了以下修复：

- Cintiq 等数位屏设备的校准得到了大幅改进。由于 Cintiq 数位屏的传感器的面积比屏幕的面积要大，因此传感器的座标体系并非从 0x0 开始计算。之前的 KCM 并没有将此特殊设计考虑在内。
- 初步支持将触控传感器报告为独立 USB ID 的设备。目前这一功能依然需要用户干预。如果你见到一个设备在 KCM 里面被列出两次，请用 Wacom 数位板扫描工具手动标记压感笔和触控输入。
- 其他数个校准方面的改进：锁定比例按钮、校准画面将在数位板映射的屏幕上打开、无需编辑设置文件即可微调校准数值的设置项 (冲刺聚会期间收到请求，聚会之后编写完毕)
- 修复数个小问题：触控跟随数位板整体旋转、快捷键不再重复触发。
- 我们一致认为 KCM 的图形界面存在一定的可用性问题。我打算在 3.1.0 版发布之后向 Krita 团队请求帮助。我们还在讨论关于如何改良默认设置的问题。
- 我对初步的 LED 显示支持进行了测试。它可以工作，但前提是系统被配置为允许用户访问 Wacom LED API (大概是通过 udev 规则实现)。OLED 显示尚未实现，但它也使用了相同的 API。总的来说这项功能尚需改进，而且做起来估计也不难，但因为具备 LED 和 OLED 的设备很少，所以这并不是优先事项。

我要感谢 Boudewijn 和 Irina 承办了这次开发冲刺聚会，还要感谢 Krita 基金会 和 KDE e.V.对这次活动的赞助。没有他们上述问题将不可能在短期内得到解决。

### 新版发布和测试

从 3.0.0 版起还有一个重大变化：libwacom 支持。这会增加能够直接工作的设备种类，但目前的支持还不完整：尚未支持 LED 和多 USB ID 设备；libwacom 提供的按钮布局不太适合现有的图形界面。它还需要 libwacom 0.29 才能支持具有特异按钮的设备，尽管旧版的也能编译，但设备的功能会大打折扣。因此我们的“Wacom 数位板扫描工具”还不能马上光荣退役。

另一个较小的调整则是日志系统被移植到了 QLoggingCategory，这意味着要启用调试日志，你必需运行 **kdebugsettings** 然后找到“wacom”项目。

我准备在近期创建 3.1.0 版的分支，将上面所说的变化包含进去，这意味着新版会在这个月发布。3.0.0 版之后的绝大多数重要的问题修复将很难被向前移植，因此将不会有 3.0.0 版了，不好意思。以后也不会再有 beta 版本的发布，因为 Neon Dev Unstable、Arch 和 Gentoo 等已经提供了 git 编译版本可供测试。

已知问题：

- 没有 Wayland 支持，连一星半点都没有，也没有时间表。我已经在与某位想要在 KWin wayland 实现数位板支持的开发人员进行协作，但我本人在短期内无法为此进行开发工作。
- 自动旋转的定位在多显示器环境下不能正常工作。这个是 Qt 的一个问题。
- 校准窗口在压感笔触碰或者拖拽时会进入拖拽模式。它很烦人但应该不会影响校准结果。这其实是一项 KDE 功能，你可以在小工具样式设定中禁用它。但我现在还不知道如何回避这个问题。

目前有许多问题尚处在开放状态，但在发布 3.1.0 之后我会将下列我认为已经解决的问题关闭。

- [**Bug 334520**](https://bugs.kde.org/show_bug.cgi?id=334520) - 如果 TabletPC 在数位板映射到内置屏幕时连接了一个外置屏幕，校准操作会失败。(应该已在 git/3.1.0 中得到修复)
- [**Bug 336748**](https://bugs.kde.org/show_bug.cgi?id=336748) - 校准在 Cintiq 13HD 下面工作不正常 (应该已在 git/3.1.0 中得到修复)
- [**Bug 322918**](https://bugs.kde.org/show_bug.cgi?id=322918) - Wacom Cintiq 13HD 的校准问题 (应该已在 git/3.1.0 中得到修复)
- [**Bug 327952**](https://bugs.kde.org/show_bug.cgi?id=327952) - Wacom 模块在校准 Cintiq 21UX 时不起作用 (应该已在 git/3.1.0 中得到修复)
- [**Bug 364043**](https://bugs.kde.org/show_bug.cgi?id=364043) - Intuos Pro 无法生成配置方案，也无法配置按钮。
- [**Bug 343666**](https://bugs.kde.org/show_bug.cgi?id=343666) - Device 'Wacom Bamboo One M Pen' is not in wacom_devicelist, not able to configure using tablet configuration (应该已在 git/3.1.0 中得到修复)
- [**Bug 339138**](https://bugs.kde.org/show_bug.cgi?id=339138) - 数位板的屏幕映射在 KDE 重启后会复位
- [**Bug 325520**](https://bugs.kde.org/show_bug.cgi?id=325520) - Dell Latitude XT2 屏幕旋转时触控设备朝相反方向旋转 (应该已在 git/3.1.0 中得到修复)

完整的开放问题/建议列表[在这里](https://bugs.kde.org/buglist.cgi?component=general&list_id=1520931&product=wacomtablet&resolution=---)。

如果遇到了问题，请提交问题报告。如果在 3.1.0 版发布后没有更多的新问题，那么项目接下来的优先事项将转向可用性的改进。

### 程序的打包问题

这是一个我本人无能为力却又非常重要的问题。目前 KDE 的数位板支持是一个可选组件。如果**输入设备**选项中没有**数位板**一项，你需要手动安装它。软件包的名称一般是 **wacomtablet** 或者 **kcm-wacomtablet**。你可以在[这里](https://repology.org/metapackage/kcm-wacomtablet/versions)和[这里](https://repology.org/metapackage/wacomtablet/versions)检查你的发行版有没有将其打包。按照我目前了解的情况，只有 KDE Neon、Arch (及其派生版本)、Gentoo 等提供了最新的 wacomtablet 软件包。Kubuntu 也有提供，但它需要挂载 [实验性功能 PPA](https://launchpad.net/~kubuntu-ppa/+archive/ubuntu/experimental/+packages)。如果你使用的是其他发行版，你还有以下选项：

- 按照源代码中 README.md 的指示进行编译和安装。不过由于许多原因我并不推荐人们那样做。
- 请求别人 (最好是你的发行版的 KDE 小组) 将其打包。一般在发行版的问题追踪系统或支持论坛上进行。

这个项目是插件结构的，因此我不能把它编译成 AppImage 来提供给大家使用。要让它进入你所用的发行版的最佳办法就是让发行版的项目负责人们知道它的存在而你需要它被打包进来。

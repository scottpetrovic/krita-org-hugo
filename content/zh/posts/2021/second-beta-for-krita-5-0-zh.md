---
title: "Krita 5.0 公开测试第 2 版已经推出"
date: "2021-10-11"
categories: 
  - "development-builds-zh"
---

今天我们为大家带来了 Krita 5.0 的第二个公开测试版。此次发布比原计划的要晚，原因是因为一些开发人员在长达一年半的隔离解封后迫不及待地线下碰头，却不小心得了重感冒。

Krita 公开测试第 2 版与第 1 版一样存在[一些需要旧版用户注意的事项](https://krita.org/zh/item/first-beta-for-krita-5-0-released-zh/)，请在充分了解情况后才进行使用。

公开测试第 2 版在第 1 版的基础上修复了超过 700 项程序缺陷。现在我们至少还需要解决[这些程序缺陷](https://bugs.kde.org/buglist.cgi?bug_severity=critical&bug_severity=grave&bug_severity=major&bug_severity=crash&bug_severity=normal&bug_severity=minor&bug_status=UNCONFIRMED&bug_status=CONFIRMED&bug_status=ASSIGNED&bug_status=REOPENED&keywords=regression%2C%20release_blocker%2C%20&keywords_type=anywords&list_id=1918546&product=krita&query_format=advanced)后才能正式发布 Krita 5.0。此版软件还包含了重构的 GPU 加速画布程序，大幅改善了在 HiDPI 和 macOS 环境下的性能。

[![](/images/posts/2021/electrichearts_20201224A_kiki_c1_1080P-1024x512.png)](https://krita.org/wp-content/uploads/2021/08/electrichearts_20201224A_kiki_c1_1080P.png) Tyson Tan (钛山) 绘制的新版启动图

下面是自公开测试第 1 版以来的比较值得一提的更新：

- Dmitry Kazakov 和 Ivan Yossi 实现了一套上传纹理到 GPU 的新方案，改善了画布性能，尤其是 macOS 下的性能。
- Michał Chojnowski 修复了色域蒙版工具栏的一处崩溃 ([BUG:441122](https://bugs.kde.org/show_bug.cgi?id=441122))
- Alvin Wong 大幅改善了 Krita 的可翻译性，并对繁体中文的翻译进行了大量改进。
- Tyson Tan 也大幅改善了 Krita 的可翻译性，并对简体中文的翻译进行了大量改进。
- Amyspark 修复了一个在使用 G'Mic-Qt 插件时会造成设置重置的程序缺陷。G'Mic 也已经更新到了最新版本。
- Deif Lou 修复了滤镜笔刷引擎中存在的数个问题。
- Amyspark 重构了图层元数据框架 ([BUG:410341](https://bugs.kde.org/show_bug.cgi?id=410341))
- Agata Cacko 修复了颜色历史按钮布局 ([BUG:434915](https://bugs.kde.org/show_bug.cgi?id=434915))
- Alan North 修复了笔刷编辑器中调整共享曲线时会发生的问题。
- Agata Cacko 改进了 Adobe 样式库文件支持，现在可以加载唯一 ID 冲突的 ASL 文件。
- Alvin Wong 修复了画布浮动缩放水平消息的问题 ([BUG:429569](https://bugs.kde.org/show_bug.cgi?id=429569))
- Tom Tom Tom 修复了西文书法工具中的一处程序缺陷
- Eoin O'Neill 修复了分镜头脚本面板中的一处崩溃 ([BUG:441592](https://bugs.kde.org/show_bug.cgi?id=441592))
- Emmet O'Neill 改进了分镜头脚本面板的易用性 ([BUG:441593](https://bugs.kde.org/show_bug.cgi?id=441593))
- Sharaf Zaman 修复了安卓/ChromeOS 版的欢迎页面。
- Matthias Wein 修复了面板标题栏的数个问题。
- Alvin Wong 修复了 Windows 版显示弹窗时的一些问题 ([BUG:441935](https://bugs.kde.org/show_bug.cgi?id=441935))
- Alvin Wong 修复了触控平移手势在移动太快时会出错的问题 ([BUG:441706](https://bugs.kde.org/show_bug.cgi?id=441706))
- Wolthera van Hövell tot Westerflier 修复了使用 Lab 色彩空间定义的 KPL 色板的加载失败问题 ([BUG:441139](https://bugs.kde.org/show_bug.cgi?id=441139))
- Alvin Wong 修复了导航器面板的一处性能问题 ([BUG:442075](https://bugs.kde.org/show_bug.cgi?id=442075))
- Wolthera van Hövell tot Westerflier 修复了通道面板的一处崩溃 ([BUG:442117](https://bugs.kde.org/show_bug.cgi?id=442117))
- Matthias Wein 修复了通道面板的一处性能问题
- Alvin Wong 改进了 Krita 在多文档模式下的易用性 ([BUG:441644](https://bugs.kde.org/show_bug.cgi?id=441644))
- Halla Rempt 修复了操作流程面板在执行已禁用操作时的崩溃 ([BUG:441638](https://bugs.kde.org/show_bug.cgi?id=441638))
- Halla Rempt 修复了 Qt 字体数据库在字体名称中角括号中间存在空格时导致解析器出错的问题 ([BUG:430220](https://bugs.kde.org/show_bug.cgi?id=430220))
- Agata Cacko 修复了多种辅助尺形状的预览问题 ([BUG:441212](https://bugs.kde.org/show_bug.cgi?id=441212))
- Alvin Wong 修复了在使用 Windows Ink 或 Wintab 时某些驱动程序会重复发送数位板事件，从而激活一个鼠标事件的问题 ([BUG:441687](https://bugs.kde.org/show_bug.cgi?id=441687))
- Matthias Weind 修复了一个会导致新图像尺寸计算错误的问题 ([BUG:442124](https://bugs.kde.org/show_bug.cgi?id=442124))
- Sharaf Zaman 修复了安卓版的增量备份保存功能 ([BUG:427042](https://bugs.kde.org/show_bug.cgi?id=427042))
- Halla Rempt 修复了系统日志的滚动更新功能
- Halla Rempt 将默认撤销次数从 30 改为 200
- Agata Cacko 修复了渐变编辑后预览的更新问题
- Amyspark 修复了LittleCMS 的 32 位浮点 RGB ([BUG:442004](https://bugs.kde.org/show_bug.cgi?id=442004), [BUG:439947](https://bugs.kde.org/show_bug.cgi?id=439947), [BUG:437429](https://bugs.kde.org/show_bug.cgi?id=437429))
- Wolthera van Hövell tot Westerflier 修复了透明度通道分离到单独图层功能 ([BUG:434288](https://bugs.kde.org/show_bug.cgi?id=434288))
- Halla Rempt 为创建矢量图层新增了一个默认快捷键：CTRL+Insert ([BUG:442585](https://bugs.kde.org/show_bug.cgi?id=442585))
- Wolthera van Hövell tot Westerflier 实现了在作为 Krita 图像编辑笔刷时加载 GIMP 笔刷或 GIMP 图像水管笔刷作为彩色图像，并修复了这类笔刷的保存问题  ([BUG:442316](https://bugs.kde.org/show_bug.cgi?id=442316))
- Wolthera van Hövell tot Westerflier 为自动笔刷空间增加了一个重置选项 ([BUG:437006](https://bugs.kde.org/show_bug.cgi?id=437006))
- Halla Rempt 修复了快捷键定义文件遗失，造成菜单项显示为空白的程序缺陷 ([BUG:428453](https://bugs.kde.org/show_bug.cgi?id=428453))
- Eoin O'Neill 为分镜头脚本面板编写了全新的导出界面。
- Eoin O'Neill 修复了在动画蒙版上使用移动工具时的问题 ([BUG:441974](https://bugs.kde.org/show_bug.cgi?id=441974))
- Eoin O'Neill 修复了裁剪工具在克隆的动画帧中不正常工作的程序缺陷 ([BUG:441369](https://bugs.kde.org/show_bug.cgi?id=441369))
- Wolthera van Hövell tot Westerflier 改进了时间轴面板，现在可以对蒙版分配色标并固定到时间轴面板 ([BUG:438124](https://bugs.kde.org/show_bug.cgi?id=438124))
- Wolthera van Hövell tot Westerflier 修复了操作流程面板的外观问题 ([BUG:442185](https://bugs.kde.org/show_bug.cgi?id=442185))
- Alvin Wong 修复了非正数倍显示缩放倍率的一系列问题
- Sharaf Zaman 修复了安卓版更改光标图标时的问题 ([BUG:431859](https://bugs.kde.org/show_bug.cgi?id=431859))
- Reinold Rojas 为拾色器工具启用了颜色采样预览功能 ([BUG:396490](https://bugs.kde.org/show_bug.cgi?id=396490))
- Reinold Rojas 修复了隐藏面板模式的全屏状态问题 ([BUG:437932](https://bugs.kde.org/show_bug.cgi?id=437932))
- Halla Rempt 为变形工具新增了一个工具预览选项，方便用户在快速预览和图层混合模式之间切换。
- Black Cat 修复了在文字工具中应用字体风格的问题 ([BUG:392343](https://bugs.kde.org/show_bug.cgi?id=392343))
- Agata Cacko 修复了局部辅助尺的预览问题 ([BUG:442619](https://bugs.kde.org/show_bug.cgi?id=442619))
- Wolthera van Hövell tot Westerflier 修复了裁剪工具的一系列文问题 ([BUG:442827](https://bugs.kde.org/show_bug.cgi?id=442827), [BUG:442959](https://bugs.kde.org/show_bug.cgi?id=442959))
- Wolthera van Hövell tot Westerflier 修复了合并克隆阵列的问题，现在合并后的图层能处在正确的位置 ([BUG:437431](https://bugs.kde.org/show_bug.cgi?id=437431))
- Wolthera van Hövell tot Westerflier 修复了颜色调整滤镜蒙版的一处可能的崩溃 ([BUG:428349](https://bugs.kde.org/show_bug.cgi?id=428349))
- Agata Cacko 修复了创建资源包时的渐变预览图
- Agata Cacko 修复了资源标签系统中的一系列问题
- Dmitry Kazakov 改进了蒙版笔刷的性能
- Halla Rempt 实现了用户定义标签的保存功能
- Dmitry Kazakov 改进了当前笔尖非常大时起笔时的性能 ([BUG:436731](https://bugs.kde.org/show_bug.cgi?id=436731))
- Sharaf Zaman 改进了安卓或 ChromeOS 下文字工具的易用性。
- Dmitry Kazakov 修复了属于一个已变形图层组中的形状更新 ([BUG:443161](https://bugs.kde.org/show_bug.cgi?id=443161))
- Dmitry Kazakov 修复了四方连续模式下的画布更新 ([BUG:442796](https://bugs.kde.org/show_bug.cgi?id=442796))
- Dmitry Kazakov 修复了颜色涂抹笔刷引擎的色相感应程序造成的杂色 ([BUG:441755](https://bugs.kde.org/show_bug.cgi?id=441755))
- Matthias Wein 修复了创建新图像对话框的一处内存泄漏问题
- Halla Rempt 修复了通知程序脚本类的一个初始化问题
- Agata Cacko 改进了透视辅助尺的性能

我们将继续修复在公开测试版和每日构建版中发现的问题，以确保在发布 Krita 5.0 正式版时程序的可靠性。

如果条件允许，请考虑通过 [Krita 开发基金](https://fund.krita.org/)支持我们的工作：

[![](/images/posts/2021/devfund-1024x346.png)](https://fund.krita.org)

## 下载

### 中文版信息

- 中文支持：Krita 的所有软件包均内建中文支持，首次安装时会自动设置为操作系统的语言。
- 手动设置：菜单栏 --> Settings --> Switch Application Language (倒数第二项) --> 下拉选单 --> 中文 (底部)，重启程序生效。
- 插件翻译：G'MIC 插件[需要下载翻译包](https://share.weiyun.com/SBopNjOn)
- 网盘下载：请在官网下载困难时使用，更新时间可能滞后。

### Windows 版本

- **64 位 Windows 安装程序** [本站下载](https://download.kde.org/unstable/krita/5.0.0-beta2/krita-x64-5.0.0-beta2-setup.exe) | [网盘下载](https://share.weiyun.com/60HLzj6I)
- **64 位 Windows 免安装包** [本站下载](https://download.kde.org/unstable/krita/5.0.0-beta2/krita-x64-5.0.0-beta2.zip) | [网盘下载](https://share.weiyun.com/60HLzj6I)
- **64 位程序崩溃调试包** [本站下载](https://download.kde.org/unstable/krita/5.0.0-beta2/krita-x64-5.0.0-beta2-dbg.zip) | [网盘下载](https://share.weiyun.com/60HLzj6I)

- **配套网盘资源 (中文社区维护)** [中文离线文档](https://share.weiyun.com/Dea2uj0M) | [FFmpeg 软件包](https://share.weiyun.com/6tH13bVC) | [G'Mic 滤镜汉化](https://share.weiyun.com/SBopNjOn) |

- 32 位支持：最后一版支持 32 位 Windows 的 Krita 为 4.4.3，[本站下载](https://download.kde.org/stable/krita/4.4.3/krita-x86-4.4.3-setup.exe) | [网盘下载](https://share.weiyun.com/wdMnx1WB)。
- 免安装包：解压到任意位置，运行目录中的 Krita 快捷方式。不带文件管理器缩略图插件，与已安装版本共用配置文件和资源，但程序本身相互独立。
- 程序崩溃调试包：解压到 Krita 的安装目录，在报告程序崩溃问题时用于获取回溯追踪数据。日常使用无需下载此包。

### Linux 版本

- **64 位 Linux AppImage 程序包** [本站下载](https://download.kde.org/unstable/krita/5.0.0-beta2/krita-5.0.0-beta2-x86_64.appimage) | [网盘下载](https://share.weiyun.com/C0gZ6joR)
- 从此版开始，G'Mic 插件已经整合到主程序包中
- 如果浏览器把链接作为文本打开，请右键点击链接另存为文件。

### macOS 版本

- **macOS 程序映像** [本站下载](https://download.kde.org/unstable/krita/5.0.0-beta2/krita-5.0.0-beta2.dmg) | [网盘下载](https://share.weiyun.com/gVg0CI53)

- 如果您还在使用 OSX Sierra 或者 High Sierra，请[观看此视频](https://www.youtube.com/watch?v=3py0kgq95Hk)了解如何启动由开发人员签名的可执行软件包。

### 安卓版本

安卓版本目前尚处于早期测试阶段，整体功能与桌面版本几乎完全相同。它仅为安卓平板和 ChromeBook 类设备进行了初步适配，大部分功能依然需要搭配键盘使用，还有不少功能无法正常工作。

- **64 位 Intel CPU APK 安装包** [本站下载](https://download.kde.org/unstable/krita/5.0.0-beta2/krita-x86_64-5.0.0-beta2-release-signed.apk) | [网盘下载](https://share.weiyun.com/AKSomiNJ)
- **32 位 Intel CPU APK 安装包** [本站下载](https://download.kde.org/unstable/krita/5.0.0-beta2/krita-x86-5.0.0-beta2-release-signed.apk) | [网盘下载](https://share.weiyun.com/AKSomiNJ)
- **64 位 ARM CPU APK 安装包** [本站下载](https://download.kde.org/unstable/krita/5.0.0-beta2/krita-arm64-v8a-5.0.0-beta2-release-signed.apk) | [网盘下载](https://share.weiyun.com/GCKrtN0F)
- **32 位 ARM CPU APK 安装包** [本站下载](https://download.kde.org/unstable/krita/5.0.0-beta2/krita-armeabi-v7a-5.0.0-beta2-release-signed.apk) | [网盘下载](https://share.weiyun.com/GCKrtN0F)

### 源代码

- [TAR.GZ 格式源代码包](https://download.kde.org/unstable/krita/5.0.0-beta2/krita-5.0.0-beta2.tar.gz)
- [TAR.XZ 格式源代码包](https://download.kde.org/unstable/krita/5.0.0-beta2/krita-5.0.0-beta2.tar.xz)

### md5sum 校验码

适用于上述所有软件包，用于校验下载文件的完整性，不了解文件校验请忽略：

- [ms5sum 校验码文本文件](https://download.kde.org/unstable/krita/5.0.0-beta2/md5sum.txt)

### 文件完整性验证密钥

Linux 的 Appimage 可执行文件包和源代码的 .tar.gz 和 .tar.xz tarballs 压缩包已经经过数字签名。您可以[在此下载公钥](https://files.kde.org/krita/4DA79EDA231C852B)，还可以在此下载[数字签名的 SIG 文件](https://download.kde.org/unstable/krita/5.0.0-beta2/)。

## 请支持 Krita

Krita 是一个自由和开源的软件项目。如果条件允许，请考虑通过 [捐款](https://fund.krita.org/) 或者 [购买培训教程和画册](https://krita.org/en/shop/) 等方式支持我们的存续和发展，这样我们才能支持开发人员为 Krita 全职工作。

---
title: "Krita 4.4.5 正式版已经推出"
date: "2021-06-09"
categories: 
  - "news-zh"
  - "officialrelease-zh"
---

今天 Krita 团队推出了 Krita 4.4.5，它是 5.0 发布前的最后一个程序缺陷修复版本。我们发布此版的最主要原因是要修复一个 macOS 版的严重缺陷，但我们也顺便把大量其他修复也合并到此版中，希望能提升使用体验。

注意：Krita 4.4.4 只在 Epic 游戏商城发布过，并未在本站发布。

- 为在 mdiarea 中的标签页设置 ([Bug 433640](https://bugs.kde.org/show_bug.cgi?id=433640))
- 如果图像加载频繁失败，则停止重试 ([Bug 433652](https://bugs.kde.org/show_bug.cgi?id=433652))
- 使用 QVersionNumber 来比较版本
- 修复油画滤镜的图块显示错误 [相关代码提交](https://krita.org/zh/item/krita-arrives-in-the-epic-store-zh/)
- 仅在使用 Krita alpha 或 beta 版时打开程序缺陷报告对话框
- 修复在右键面板显示比例为 125% 时的崩溃 ([Bug 431944](https://bugs.kde.org/show_bug.cgi?id=431944))
- 修复 GCC11 的编译，感谢 Jonathan Wakely 提供建议线索 ([Bug 434150](https://bugs.kde.org/show_bug.cgi?id=434150))
- 在 Arm Linux 下使用 OpenGL ES ([Bug 421136](https://bugs.kde.org/show_bug.cgi?id=421136))
- 修复导入损坏的 ICC 色彩特性文件时的崩溃 ([Bug 434273](https://bugs.kde.org/show_bug.cgi?id=434273))
- 移除 hello world 演示插件 ([Bug 422380](https://bugs.kde.org/show_bug.cgi?id=422380))
- 修复缺陷：裁剪工具崩溃 ([Bug 433770](https://bugs.kde.org/show_bug.cgi?id=433770))
- 修复缺陷：变形 (斜切) 的参照点无效 ([Bug 427462](https://bugs.kde.org/show_bug.cgi?id=427462))
- 修复状态栏和导航器中的角度选择器范围 ([Bug 434993](https://bugs.kde.org/show_bug.cgi?id=434993))
- 在曲线网格变形中实现“按比例缩放手柄”
- 修复缺陷：裁剪工具不响应某些事件 ([Bug 435201](https://bugs.kde.org/show_bug.cgi?id=435201))
- 从剪贴板支持图像格式列表中移除 JPG ([Bug 431310](https://bugs.kde.org/show_bug.cgi?id=431310))
- 如果操作为空，则不设置菜单文字 ([Bug 437036](https://bugs.kde.org/show_bug.cgi?id=437036))
- 为 libkis 提供节点的唯一 ID [commit](https://invent.kde.org/graphics/krita/-/commit/57f0af27d358e21ffdaf8af5a38a196df1565dcf)
- 修复 quicklook 生成器 ([Bug 436224](https://bugs.kde.org/show_bug.cgi?id=436224))
- 修复 macOS 下的随机崩溃并修复光标在使用 cmb+tab 切换到其他应用程序并使用鼠标返回 Krita 时的卡死现象 ([Bug 434646](https://bugs.kde.org/show_bug.cgi?id=434646))
- 修复当裁剪操作活动时按下 Ctrl+Z 会造成数据损坏的问题 (CC[Bug 433770](https://bugs.kde.org/show_bug.cgi?id=433770))
- 修复智能填色工具色板的缩放 ([Bug 410997](https://bugs.kde.org/show_bug.cgi?id=410997))
- 修复按下 Shift 修饰键时手绘轮廓选区工具的精确度问题 ([Bug 437048](https://bugs.kde.org/show_bug.cgi?id=437048))
- 修复在某些笔画还在渲染途中时过早关闭 Krita 造成的崩溃 ([Bug 419021](https://bugs.kde.org/show_bug.cgi?id=419021))
- 修复 KisCanvas2::setProofingOptions() 的不正确内存访问
- 修复自发任务开始时的 race 状态 ([Bug 434648](https://bugs.kde.org/show_bug.cgi?id=434648))
- 修复导航器的色彩管理显示 ([Bug 428605](https://bugs.kde.org/show_bug.cgi?id=428605))
- 修复透视变形模式的最近邻插值过滤器 ([Bug 420811](https://bugs.kde.org/show_bug.cgi?id=420811))
- 修复变形后的图像会在移动鼠标过快时造成漂移 ([Bug 416899](https://bugs.kde.org/show_bug.cgi?id=416899))
- 修复自由变形模式的平滑度 ([Bug 416899](https://bugs.kde.org/show_bug.cgi?id=416899))
- 修复 (不限于) 中文输入法无法在某些弹出部件中使用的问题 ([Bug 395598](https://bugs.kde.org/show_bug.cgi?id=395598))
- 修复在命令行模式下 Krita 的导出功能 [相关代码提交](https://invent.kde.org/graphics/krita/-/commit/38b9dfa668494c03a9d11b16e3f619ff3c4f27a8)
- 修复 OpenColorIO 的 include 目录检测 [相关代码提交](https://invent.kde.org/graphics/krita/-/commit/1c55fefecb85366feee7d101a343f31d3cfb8e5d)
- 修复 OverviewThumbnailStrokeStrategy 中的参数顺序 (CID 310957)
- 不要在 psd_image_data 中依赖字节顺序 (CID 35080)
- 在进行计算之前拓宽变量 (CID 248925)
- 用默认值覆盖数值为 0 的 patchWidth 和 patchHeight (CID 248441, CID 248622)
- 在 ConvertColorSpacePr.Vis 中进行动态投射后检查数值 (CID 304985)
- 在转换时正确绑定数值 (CID 248629, CID 248458)
- 在 KisMetaData::TypeInfo::Private 中初始化 propertyType (CID 35498)
- 初始化 KoRuler and KisFullRefreshWalker 中的变量 (CID 35523, CID 35612)
- 初始化 KisImagePyramid 中的成员 (CID 36041)
- 初始化 DlgOffsetImage and DeformBrush 中初始化成员 (CID 36144, CID 36265)
- 初始化 KCanvasPreview 中的成员 (CID 36395)
- 初始化 DlgClonesArray 中的成员 (CID 248509)
- 初始化 KisShadeSelectorLine 中的成员 (CID 36338)
- 初始化 assistant 类 的成员 (CID 248502, CID 248916)
- 初始化数值框相关类的成员 (CID 248555, CID 248871)
- 修复 xyYtoXYZ 色彩转换方程
- 简化三角形拾色器代码 [相关代码提交](https://invent.kde.org/graphics/krita/-/commit/789edc1cf4fe7c2c885368337788c9db7e22d1c6)
- 修复颜色通道面板显示更新 [相关代码提交](https://invent.kde.org/graphics/krita/-/commit/cb81820599f35ffae4c4e41ce8039829ffec37d7)
- 修复直方图面板显示更新 [相关代码提交](https://invent.kde.org/graphics/krita/-/commit/6ddf4a12db10510715b177e71768ea176b6327a2)
- 修复直方图部件的多线程处理 [相关代码提交](https://invent.kde.org/graphics/krita/-/commit/04d8cf6c586877e76c174aff445fb726962a4984)
- 在 HistogramDockerWidget 中更改 typedef 为 using [相关代码提交](https://invent.kde.org/graphics/krita/-/commit/4cfcf5e967a195af07c4f4c238183a147d513899)
- 修复 SvgStyleWriter 中参照空值 (CID 329512)
- 修复在 HistogramDockerWidget 中的未初始化数值 (CID 329509)
- 修复撤销历史记录面板的高分辨率支持模式画布预览 [相关代码提交](https://invent.kde.org/graphics/krita/-/commit/7bfca14742ba2b99c42c33ef3978be1fb7fb868f)
- 修复在保存巨大图像为 .kra 时崩溃 ([Bug 432182](https://bugs.kde.org/show_bug.cgi?id=432182))
- 确保变形工作器不尝试缩放为 0 倍 ([Bug 432182](https://bugs.kde.org/show_bug.cgi?id=432182))
- 修复 KoQuaZipStore 的错误检测 [相关代码提交](https://invent.kde.org/graphics/krita/-/commit/80f43d1ce4bb1305731cffc192c4e9907a88b986)
- 在语言列表中显示国家/地区以便区分 ([Bug 437994](https://bugs.kde.org/show_bug.cgi?id=437994))
- 修复在使用变形工具处理矢量图层时的更新失败 ([Bug 437886](https://bugs.kde.org/show_bug.cgi?id=437886))
- 不为 zh_CN 和 zh_TW 区域设置附加国家/地区标识 ([Bug 437994](https://bugs.kde.org/show_bug.cgi?id=437994))
- 回退“修复 OpenColorIO 的 include 目录检测”
- 保存为 kra 文件时添加更多检测 [相关代码提交](https://invent.kde.org/graphics/krita/-/commit/d47163e4f7e99d790be7905b79b2ca94ef8ef675)
- 为浮点数值修复非浮点数值结果 (CID 329390, CID 329448, CID 329482)
- 修复多个类中的未初始化数值 (CID 329508, CID 329504, CID 329503, CID 329502, CID 329501)
- 不对 0 字节色板进行 assert [相关代码提交](https://invent.kde.org/graphics/krita/-/commit/876d61fc8d2b0a3f76277a814ccc9f595f063c7d)
- 初始化 SVG 符号类成员 (CID 304987)
- 初始化 KisColorSelector 类成员 (CID 36349, CID 248848, CID 248452, CID 248707)
- 安卓版本：让退出时保存的操作更加可靠 [相关代码提交](https://invent.kde.org/graphics/krita/-/commit/f248c032199be64e9ac4e172155434d793fdd212)
- 缺陷修复：在存在不止一个辅助尺时发生显示错误 ([Bug 401940](https://bugs.kde.org/show_bug.cgi?id=401940))
- 安卓版本：发生 TouchCancel 事件时的 SAFE_ASSERT [相关代码提交](https://invent.kde.org/graphics/krita/-/commit/adebed6735b94bbcd7945aeace304975f43e5667)
- 安卓版本：图像属性文字框不响应键盘事件
- 安卓版本：修复旋转时窗口管理器的位置
- 缺陷修复：描边填充和形状填充效果不一致 ([Bug 399127](https://bugs.kde.org/show_bug.cgi?id=399127), [Bug 422204](https://bugs.kde.org/show_bug.cgi?id=422204), [Bug 434828](https://bugs.kde.org/show_bug.cgi?id=434828))

## 下载

### 中文版信息

- 中文支持：Krita 的所有软件包均已内建中文支持。
- 自动检测：Krita 在首次安装时会自动设置为操作系统的语言。
- 手动设置：菜单栏 --> Settings 菜单 --> Switch Application Language (倒数第二项) --> 下拉选单 --> 中文 (底部)，重启程序生效。
- 插件翻译：部分内置，G'MIC 插件[需要下载翻译包](https://share.weiyun.com/SBopNjOn)
- 网盘下载：请在官网下载困难时使用。

### Windows 版本

注意：从此版开始，Krita 不再提供 32 位 Windows 版的软件包。

- **64 位 Windows 安装程序** (推荐) [本站下载](https://download.kde.org/stable/krita/4.4.5/krita-x64-4.4.5-setup.exe) | [网盘下载](https://share.weiyun.com/aVyf2PXQ)
- **64 位 Windows 免安装包** [本站下载](https://download.kde.org/stable/krita/4.4.5/krita-x64-4.4.5.zip) | [网盘下载](https://share.weiyun.com/aVyf2PXQ)
- **64 位程序崩溃调试包** [本站下载](https://download.kde.org/stable/krita/4.4.5/krita-x64-4.4.5-dbg.zip) | [网盘下载](https://share.weiyun.com/aVyf2PXQ)

- **配套网盘资源 (中文社区维护)** [中文离线文档](https://share.weiyun.com/Dea2uj0M) | [FFmpeg 软件包](https://share.weiyun.com/6tH13bVC) | [G'Mic 滤镜汉化](https://share.weiyun.com/SBopNjOn) |

- 免安装包：解压到任意位置，运行目录中的 Krita 快捷方式。不带文件管理器缩略图插件。与已安装版本共用配置文件和资源，但程序本身相互独立。
- 程序崩溃调试包：解压到 Krita 的安装目录，在报告程序崩溃问题时用于获取回溯追踪数据。日常使用无需下载此包。

### Linux 版本

- **64 位 Linux AppImage 主程序包** [本站下载](https://download.kde.org/stable/krita/4.4.5/krita-4.4.5-x86_64.appimage) | [网盘下载](https://share.weiyun.com/j7Vrjx2m)
- **64 位 Linux AppImage G'Mic-Qt 插件包** [本站下载](https://download.kde.org/stable/krita/4.4.5/gmic_krita_qt-x86_64.appimage) | [网盘下载](https://share.weiyun.com/j7Vrjx2m)
- 如果浏览器把链接作为文本打开，请右键点击链接另存为文件。

### macOS 版本

- **macOS 主程序映像** [本站下载](https://download.kde.org/stable/krita/4.4.5/krita-4.4.5.dmg) | [网盘下载](https://share.weiyun.com/jc82ykle)

- G'Mic-qt 软件包、触摸屏辅助面板在 macOS 下不可用。
- 如果您还在使用 OSX Sierra 或者 High Sierra，请[观看此视频](https://www.youtube.com/watch?v=3py0kgq95Hk)了解如何启动由开发人员签名的可执行软件包。

### 安卓版本

安卓版本目前尚处于早期测试阶段，整体功能与桌面版本几乎完全相同。它仅为安卓平板和 ChromeBook 类设备进行了初步适配，大部分功能依然需要搭配键盘使用，还有不少功能不能正常工作。您还可以通过 [Google Play](https://play.google.com/store/apps/details?id=org.krita) 安装 Krita。

- **64 位 Intel CPU APK 安装包** [本站下载](https://download.kde.org/stable/krita/4.4.5/krita-x86_64-4.4.5-release.apk) | [网盘下载](https://share.weiyun.com/he1kczpd)
- **32 位 Intel CPU APK 安装包** [本站下载](https://download.kde.org/stable/krita/4.4.5/krita-x86-4.4.5-release.apk) | [网盘下载](https://share.weiyun.com/he1kczpd)
- **64 位 ARM CPU APK 安装包** [本站下载](https://download.kde.org/stable/krita/4.4.5/krita-arm64-v8a-4.4.5-release.apk) | [网盘下载](https://share.weiyun.com/he1kczpd)
- **32 位 ARM CPU APK 安装包** [本站下载](https://download.kde.org/stable/krita/4.4.5/krita-armeabi-v7a-4.4.5-release.apk) | [网盘下载](https://share.weiyun.com/he1kczpd)

### 源代码

- [TAR.GZ 格式源代码包](https://download.kde.org/stable/krita/4.4.5/krita-4.4.5.tar.gz)
- [TAR.XZ 格式源代码包](https://download.kde.org/stable/krita/4.4.5/krita-4.4.5.tar.xz)

### md5sum 校验码

适用于上述所有软件包，用于校验下载文件的完整性，不了解文件校验请忽略：

- [ms5sum 校验码文本文件](https://download.kde.org/stable/krita/4.4.5/md5sum.txt)

### 文件完整性验证密钥

Linux 的 Appimage 可执行文件包和源代码的 .tar.gz 和 .tar.xz tarballs 压缩包已经经过数字签名。您可以通过 GPG 取回公共密钥，命令为 gpg --recv-key 7468332F 。您可以在此下载 [数字签名的 SIG 文件](https://download.kde.org/stable/krita/4.4.5/)。

## 请支持 Krita

Krita 是一个自由和开源的软件项目。如果条件允许，请考虑通过 [捐款](https://krita.org/zh/support-us-zh/donation-zh/) 或者 [购买培训教程和画册](https://krita.org/en/shop/) 等方式支持我们的存续和发展，这样我们才能支持开发人员为 Krita 全职工作。

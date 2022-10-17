---
layout: default
---
# Getting Started

### 概述
本用户指南旨在为 GameDriver Pro 用户提供关于工具的基本概述、功能和用法。  

### 安装
从Unity的Asset Store下载GameRiver Pro后，请转到：“Assets->Import Package->Custom Package...”。 在“导入资产”窗口中，查找并选择GameDriver Pro UnityPackage文件。 在“导入软件包”窗口中出现Unity之后，请验证所有项目选择导入，然后单击窗口右下方的导入按钮。 GameDriver Pro的全部文件将加入到Assets/GameDriver中。  

您也可以选择所需的部分进行导入。  

如果你觉得安装对你来说并不方便, 请 [file an issue](https://github.com/jekyll/jekyll/issues/new) (或者提交一个 pull request) 来描述一下你的遭遇并告诉我们如何使这个安装过程更加便捷。  

### 支持
如果您想快速了解 GameDriver Pro 中的重要功能，可以直接参考GameDriver/Samples中的示例。  

如果您想详细了解 GameDriver Pro 中的各功能模块的设计思路和细节, 您可以在[在线帮助](http://www.xuzhuoxi.com/GameDriver-Docs/)中找到更多信息和常见问题解答。  

如果您无法要查找您寻求的信息，请 [file an issue](https://github.com/xuzhuoxi/GameDriver-Docs/issues/new)(或者提交一个 pull request) 来描述一下你的遭遇。  

或者联系作者：xuzhuoxi@gmail.com 或 mailxuzhuoxi@163.com  

# 功能
GameDriver Pro中的源代码存放位置是有规律的。  
+ **GameDriver/Runtime/CSharp** 中的源码**只依赖**于C#标准库，**不依赖**Unity标准库。 是对C#的扩展功能。
+ **GameDriver/Runtime/Actions** 中的源码**依赖**于Core和Unity标准库。 是对Unity引擎的扩展功能。
+ **GameDriver/Runtime/Games** 中的源码依赖于Core与Actions。 是游戏开发过程常用的系统功能的通用实现。

**功能目录**：

---
<ul>
{% for p in site.data.manual.cn_pages %}
  <li>
    <a href="{{ site.home }}/{{ p.pattern }}">{{ p.text }}</a>
  </li>
{% endfor %}
</ul>
---

[1. 事件(Event) - 高效的事件模块，支持Unity多线程](manual/Manual-1.Event_cn.html)

[2. 加载管理模块(Loader) - 支持Resources、Editor、Assetbundle三种模式自由切换](manual/Manual-2.Loader_cn.html)

[3. 国际化(i18n) - 轻量级国际化解决方案](manual/Manual-3.i18n_cn.html)

[4. 网络管理扩展模块(NetManager)](manual/Manual-4.Net_cn.html)

[5. 音频管理模块(AudioManager) ](manual/Manual-5.Audio_cn.html)

[6. 面板管理模块(PanelManager)](manual/Manual-6.Panel_cn.html)

[7. 服务框架(Service)](manual/Manual-7.Service_cn.html)

[8. Rpg材料数据系统](manual/Manual-8.RpgMaterial_cn.html)

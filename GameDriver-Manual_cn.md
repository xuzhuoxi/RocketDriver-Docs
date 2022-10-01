## Getting Started

### 概述

本用户指南旨在为 GameDriver Pro 用户提供关于工具的基本概述、功能和用法。

### 安装

从Unity的Asset Store下载GameRiver Pro后，请转到：“Assets->Import Package->Custom Package...”。 在“导入资产”窗口中，查找并选择GameDriver Pro UnityPackage文件。 在“导入软件包”窗口中出现Unity之后，请验证所有项目选择导入，然后单击窗口右下方的导入按钮。 GameDriver Pro的全部文件将加入到Assets/GameDriver中。

您也可以选择所需的部分进行导入。

### 支持

如果您想快速了解 GameDriver Pro 中的重要功能，可以直接参考GameDriver/Samples中的示例。

如果您想详细了解 GameDriver Pro 中的各功能模块的设计思路和细节, 您可以在[在线帮助](http://www.xuzhuoxi.com/GameDriver-Docs/)中找到更多信息和常见问题解答。  

如果您无法要查找您寻求的信息，请随时在Github仓库 [GameDriver-Docs](https://github.com/xuzhuoxi/GameDriver-Docs) 提交Issues, 或者联系xuzhuoxi@gmail.com 或 mailxuzhuoxi@163.com

## 功能

GameDriver Pro中的源代码存放位置是有规律的。

1. GameDriver/Runtime/Core中的源码**只依赖**于C#标准库，**不依赖**Unity标准库。 是对C#的扩展功能。

2. GameDriver/Runtime/Actions中的源码**依赖**于Core和Unity标准库。 是对Unity引擎的扩展功能。

3. GameDriver/Runtime/Games中的源码依赖于Core与Actions。 是游戏开发过程常用的功能系统的通用实现。

### 1. 事件 - 高效的事件模块，支持Unity多线程

事件采用“监听-捕获”机制，监听时支持捕获次数、 捕获优先级的设置。

事件功能包含在JLGames.GameDriver.Event和JLGames.GameDriver.Actions.ThreadEvent两个命令空间下。

JLGames.GameDriver.Event负责事件系统的核心逻辑实现。

JLGames.GameDriver.Actions.ThreadEvent针对多线程提供支持。

#### 核心API

+ IEventListener: `AddEventListener`
  用于添加事件监听

+ IEventListener: `RemoveEventListener`
  用于移除事件监听

+ IEventDispatcher: `DispatchEvent`
  用于分发事件

示例位置：GameDriver/Samples/Event

### Loaderx - 资源加载管理模块, 支持Resources、Editor、Assetbundle三种模式自由切换

### i18n - 轻量级国际化解决方案

### Audio - 完善的音频管理模块，支持场景与UI的音乐音效同时，去除Assetbundle的依赖。

### Panel - UI面板与层级管理模块。

### RpgMaterial - 游戏数据管理模型

### Service - 服务扩展

### Net - 简单易用的网络链接管理模块，并提供一套模拟服务器扩展实现，对单机游戏与独立游戏非常友好。

## Editor功能
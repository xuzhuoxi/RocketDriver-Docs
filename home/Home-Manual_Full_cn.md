---
layout: print
page_id: 'home.manual'
group_id: home
lang: cn
title: '用户手册'
---
# 开始

### 概述
本用户指南旨在为 GameDriver Pro 用户提供关于工具的基本概述、功能和用法。  

### 安装
1. 从Unity的Asset Store下载GameRiver Pro后，请转到：“Assets->Import Package->Custom Package...”。 
2. 在“导入资产”窗口中，查找并选择GameDriver Pro UnityPackage文件。 
3. 在“导入软件包”窗口中出现Unity之后，请验证所有项目选择导入，然后单击窗口右下方的导入按钮。
4. GameDriver Pro的全部文件将加入到Assets/GameDriver中。 

您也可以选择所需的部分进行导入。  

### 支持
如果您想快速了解 GameDriver Pro 中的重要功能，可以直接参考GameDriver/Samples中的示例。  

如果您想详细了解 GameDriver Pro 中的各功能模块的设计思路和细节, 您可以在[在线帮助](https://www.xuzhuoxi.com/GameDriver-Docs/)中找到更多信息和常见问题解答。  

如果您无法要查找您寻求的信息，请 [file an issue](https://github.com/xuzhuoxi/GameDriver-Docs/issues/new)(或者提交一个 pull request) 来描述一下你的遭遇。  

或者联系作者：xuzhuoxi@gmail.com 或 mailxuzhuoxi@163.com  

# 功能
GameDriver Pro中的源代码存放位置是有规律的。  
+ **GameDriver/Runtime/CSharp** 中的源码**只依赖**于C#标准库，**不依赖**Unity标准库。 是对C#的功能扩展。
+ **GameDriver/Runtime/Actions** 中的源码**依赖**于CSharp和Unity标准库。 是对Unity引擎的功能扩展。
+ **GameDriver/Runtime/Games** 中的源码依赖于CSharp与Actions。 是游戏开发过程常用的系统功能的通用实现。

**目录**：  
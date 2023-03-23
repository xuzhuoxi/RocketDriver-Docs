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
+ **GameDriver/Runtime/CSharp** 中的源码**只依赖**于C#标准库，**不依赖**Unity标准库。 是对C#的功能扩展，命名空间为 **JLGames.GameDriver.CSharp**。
+ **GameDriver/Runtime/Actions** 中的源码**依赖**于CSharp和Unity标准库。 是对Unity引擎的功能扩展，命名空间为 **JLGames.GameDriver.Actions**。
+ **GameDriver/Runtime/Games** 中的源码依赖于CSharp与Actions。 是游戏开发过程常用的系统功能的通用实现，命名空间为 **JLGames.GameDriver.Games**。

## 功能概述

### GameDriver/Runtime/CSharp 
命名空间为 **JLGames.GameDriver.CSharp**  
+ Algs  
  通透算法相关功能  
  + AStar  
  A\* 通用算法  
+ Archive  
文件归档相关功能，现包含 zip解压 功能  
+ Buffer  
字节数据缓存功能，支持对大小端设置和基础数据类型的读写。  
+ DateTimex  
时间相关功能。包含时间单位间的计算转换、时间的字符串格式化、支持暂停继续的计时器等。  
+ Event  
事件相关功能。包含事件的监听、移除和调度功能。详细可查看[1.事件(Event)](Manual_1.Event_cn.html)  
+ Extensions  
CSharp中基础数据类型的扩展功能。  
+ Imagex  
图像相关功能。现包含 RGBA数据对象、 滤波器处理功能等。   
+ Mathx  
数学计算相关功能。  
+ Net  
Socket API定义、消息的封包与解包功能等。  
+ Pool  
对象池相关功能。包含 Key-Value对象池、元数据对象池、重用对象池等。  
+ Service  
服务框架基础支持。详细可查看[7.服务框架(Service)](Manual_7.Service_cn.html)  
+ TinyJson  
简单的Json读写库。来自Github开源：[https://github.com/zanders3/json](https://github.com/zanders3/json) .  
+ Utils  
  基于CSharp的常用工具函数  
  + Encrypt  
  **加密解密**相关功能，现包含 Des、Rijandel、RSA  
  + ArrayUtil  
  **数组**相关功能，数组的克隆、合并、类型转换、数组矩阵旋转等功能  
  + BitUtil  
  数值的**位运算**功能。  
  + ConfusedUtil  
  **数据混淆**相关功能。  
  + DirectionUtil  
  文件系统中与**目录**相关功能。  
  + FileUtil  
  文件系统中与**文件**相关功能。  
  + PathUtil  
  文件系统中与**路径**相关功能。  
  + PrintUtil  
  对象信息的**打印**支持。  
  + ReflexUtil  
  **反射**取值相关功能。  
  + TextUtil  
  字符文件的读写功能。  
+ Xml  
XML相关功能支持： 序列化与反序列化  
+ Callback  
通用回调上下文  
+ ICloneable  
通用克隆接口  

### GameDriver/Runtime/Actions
命名空间为 **JLGames.GameDriver.Actions**  
+ Animatorx  
针对Unity动画系统的功能支持。包含动画查找、动画播放、事件管理等功能。  
+ AssetIndex  
Editor功能，提供对项目中资产生成 “名称 -> 路径” 索引的功能。  
+ Audio  
音频管理器，提供对项目中的音频进行统一管理的功能，详细请看[5.音频管理模块(AudioManager)](Manual_5.Audio_cn.html)。  
+ Component  
一些有用的组件。  
+ Component2D  
一些有用的2D组件。  
+ DateTimex  
时间相关功能，包含依赖Unity引擎的计时器、周期循环时间片功能等。  
+ ExcelExporter  
对第三方导表工具[ExcelExporter](https://github.com/xuzhuoxi/ExcelExporter)导出数据的功能支持。  
+ Extensions
Unity中常用数据结构的扩展功能。  
+ Graphicsx  
图像相关功能。包含颜色转换函数、图像的像素数据结构、纹理函数等。  
+ i18n  
国际化功能。 详细请看[3.国际化(i18n)](Manual_3.i18n_cn.html)。 
+ Jsonx  
Json处理的相关功能。  
+ Layer  
Unity显示结构分层设计功能。  
+ Loaderx  
资源加载管理模块。详细请看[2.加载管理模块(Loader))](Manual_2.Loader_cn.html)。
+ Localx  
依赖于 PlayerPrefs 的本地存储功能。
+ Pool  
对象池功能，对 GameDriver/Runtime/CSharp/Pool 中的对象池功能进行扩展，增加了与Unity相关的部分。  
+ Service  
服务框架Unity支持。详细可查看[7.服务框架(Service)](Manual_7.Service_cn.html)  
+ TheadEvent  
事件相关功能。对 GameDriver/Runtime/CSharp/Event 增加了Unity多线程支持。  
+ UIElements  
Editor功能。是对Untiy中UIElements功能的扩展。  
+ Utils  
  依赖 Untiy 的常用函数功能。  
  + CameraUtil  
  **相机**相关功能。  
  + CaptureUtil  
  **截图**相关功能。  
  + ComponentUtil  
  **组件**相关功能。  
  + DebugUtil  
  **调试打印**相关功能。  
  + GeometryUtil  
  **几何计算**相关功能。  
  + IdentifyUtil  
  **机器Id**相关功能。  
  + ImageUtil  
  **图像**相关功能。  
  + MathfUtil  
  **数学计算**相关功能
  + PositionUtil  
  Unity物件**位置计算**相关功能。  
  + TilemapUtil  
  **UnityEngine.Tilemaps** 组件下的常用公共行为。  
  + TransformUtil  
  **UnityEngine.Transform** 组件相关的扩展功能。  
  + UnityPathUtil  
  与Untiy相关的路径处理功能。  
+ Wait  
Unity协程相关功能。  

### GameDriver/Runtime/Games
命名空间为 **JLGames.GameDriver.Games**  
+ LocalAccount  
本地账号存储功能。  
+ NetManager  
网络连接管理、虚拟服务器。详细请看[4.网络管理扩展模块(NetManager)](Manual_4.Net_cn.html)。  
+ PanelManager  
面板管理模块。详细请看[6.面板管理模块(PanelManager)](Manual_6.Panel_cn.html)
+ RpgMaterial  
游戏数据管理系统。 详细请看[8.Rpg材料数据系统(RpgMaterial)](Manual_8.RpgMaterial_cn.html)。
+ Service  
服务框架下的常用服务实例。详细请看[7.服务框架(Service)](Manual_7.Service_cn.html)。
+ Tiledx  
针对第三方软件[Tiled](https://www.mapeditor.org/)的数据解释功能。  

# 常用功能模块
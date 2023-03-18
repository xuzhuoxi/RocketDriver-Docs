# GameDriver Pro 更新日志



## 版本 v1.1.0(2023.03.18) 

### 新功能  
+ **Runtime**: 增加 Lua解释器：LuaInterpreter。  
+ **Runtime**:  支持Lua代码调用C#函数。  
+ **Runtime**:  支持C#执行Lua代码。  
+ **Editor**:  ExportSettingsEditor 增加对AssetPaths进行排序的功能。  

### 更新  
+ **RPG材料数据系统**：调整设计，把quality(品质)从 价值分类 转换到 显示分类。  

### 修复问题
+ **RPG材料数据系统**：解决示例RpgMaterialDemo的显示异常，调整设计分辨率为 1024x768。  



------



## 版本 v1.0.4(2023.01.31)  

### 新功能  
+ **RPG材料数据系统**： 增加默认的数据更新逻辑。  
  + 数据更新功能逻辑封装在MaterialServiceProxy实现中。  
  + MaterialService通过MaterialServiceProxy实现数据更新。  
+ **RPG材料数据系统**： 增加常用事件支持。  
  + MaterialServiceProxy在数据更新时，实现事件的抛出。  
+ **RPG材料数据系统**： 增加数据变更触发器功能。  
  + MaterialServiceProxy实现了触发器的注册逻辑。  
  + MaterialServiceProxy在数据更新时，实现触发器的调用。  
+ **RPG材料数据系统**： 增加加相应示例 “Samples/RpgMaterial”。  

### 更新  
+ **RPG材料数据系统**：新增IMaterialSetMod接口，MaterialSet实现了该接口。  
+ **RPG材料数据系统**：定义唯一Id的生成功能接口IUniqueIdGenerator，和相应实现UniqueIdGenerator。  
+ **RPG材料数据系统**：新增可复用代理MaterialServiceProxy，实现用户数据更新时抛出事件与执行触发器。  
+ **RPG材料数据系统**：修改IMaterialServicel，默认继承IEventDispatcher.  
+ **RPG材料数据系统**：修改MaterialService实现，支持数据更新、事件管理和数据触发器。  

### 修复问题
+ Games.RpgMaterial: 修复IMaterialSet、MaterialSet命名空间错误。  



------



## 版本 v1.0.3(2023.01.05)

初始版本。

### 新功能  

+ **事件模块**  
  + 支持自定义扩展。  
  + 支持统一管理。  
  + 支持Unity多线程。  

+ **资源加载器**  
  + 支持Editor、Resources、Assetbundle三种模式切换。  
  + 支持配置管理。  
  + 提供关键时机下的事件调度。  

+ **国际化**  
  + 支持语言扩展。  
  + 支持多文件数据集。  
  + 支持自定义数据加载器。  
  + 提供关键时机下的事件调度。  

+ **网络管理**  
  + 支持链接管理。  
  + 提供兼容TCP、UDP、 HTTP(HTTPS)、WebSocket(WebSockets)等协议的Socket API。  
  + 提供一套用于单机游戏的前后端逻辑分离的扩展服务框架。  
  + 提供关键时机下的事件调度。  

+ **音频管理**  
  + 支持系统级与用户级的配置管理。  
  + 支持自定义音频加载器。  
  + 支持播放数量的配置限制。  
  + 提供关键时机下的事件调度。  

+ **面板管理**  
  + 支持显示层管理。  
  + 支持面板信息的注入管理。  
  + 支持面板自定义背景、动画。  
  + 支持面板功能自定义扩展。  
  + 提供关键时机下的事件调度。  

+ 服务框架  
  + 支持把业务逻辑分割为服务，并加以管理。  
  + 支持服务的数据注入，初始化、数据初始化、数据保存、数据加载、重置等扩展。  
  + 支持服务的统一管理和调试。  
  + 提供关键时机下的事件调度。  

+ **RPG材料数据系统**  
  + 支持对游戏配置数据进行 **KTD(Key-Type-Define)** 格式进行统一管理。  
  + 支持对玩家数据进行  **KTV(Key-Type-Value)** 格式进行管理(内存、本地文件、服务器等)。  
  + 支持同一配置定义下对应多条玩家数据的机制。  
  + 提供关键时机下的事件调度。  

+ **其它功能**  
  + A\*算法  
  + 解压缩功能  
  + 时间相关功能  
  + 图像处理  
  + 数据工具  
  + 对象池  
  + 动画事件功能  
  + Excel导表解释  
  + 本地数据保存  

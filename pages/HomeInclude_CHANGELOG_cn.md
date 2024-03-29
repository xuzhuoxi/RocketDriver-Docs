# RocketDriver Pro 更新日志

## 版本 v2.1.1111(2023.11.11)

### 新功能  
+ CodingMap: 基于Dictionary<string,object>的Key-Value结构，包含字节序列化与反序列化功能。  
+ CodingList: 基于List的Key-Value结构，包含字节序列化与反序列化功能。  
+ Editor: 增加一个查找Prefab是否包含Layer的工具。 
+ Editor: 增加 LoaderSettings、AudioSettings、I18NSettings、PreloadSettings 的右键菜单生成。
+ Animatorx: 增加两个随机动画处理器。

### 更新&修改  
+ TransformUtil: 修改部分函数命名。
+ MetaObjectPool: 增加查找函数、增加删除指定元素的函数。
+ MetaGameObjectPool: 重写RemoveFirst和RemoveLast函数。

### 修复问题  
+ VectorInt.Mul: 修复逻辑错误。
+ DataBuffer: 修复读取时的错误。优化读取数组相关函数。更新写入数组的逻辑。
+ DataTimex:  修复MonoTimer累计时间使用Time.deltaTime的问题，更改为Time.FixedDeltaTime.




------




## 版本 v2.0.0810(2023.08.10)

**注意**：本版本对的命名空间进行大量修改。  

### 新功能  
+ Lua: 增加Monoe脚本的AOT替换支持。  
+ 新增加队列串行处理功能：CSharp.Serial。  

### 更新&修改  
+ 更新名称： 项目改名为 **RocketDriver Pro**， **避免商标纠纷**。  
+ CSharp.Buff: 规范化各个Reader、Writer、Copier接口与实现。  
+ CSharp.Net: 优化Socket关于接收消息的功能，由多线程写法改为Socket.BeginReceive。  
+ CSharp.Net: 优化ScokClinet关于连接与断开连接的功能。  
+ CSharp.Net:  优化消息读写接口的功能，并重命名为 IMessageBuffPacker => IMessageWriter、 IMessageBuffUnpacker => IMessageReader。  
+ CSharp.Net: 规范化IMessageReader、IMessageWriter接口。  
+ Actions.ThreadEvent: MonoEventProxy扩展功能，增加指定主线程执行逻辑的功能。  
+ Games/RpgMaterial: 优化结构：全部用户数据都包含UId，统一逻辑。  
+ Games/RpgMaterial: 数据变更相关数组结构同样加入UId字段。  
+ Games/RpgMaterial: 当相同类型与MId的数据可叠加时，默认UId为0。  

### 修复问题  
+ CSharp.Buffer: ByteBuffer写入数据时缓存区不足带来的报错。  
+ CSharp.Buffer: 修复Bug，函数CopyBytes(int offset =0) 计算剩余长度错误。  
+ CSharp.Net: SockClient在接收消息的过程中断开连接带来的报错。  
+ CSharp.Net: 修复SockReceiver每次只解释一条数据的问题。  
+ CSharp.Net: 修复SockClient中ISockReceiver与ISockSender为空时的调用报错。  




------



## 版本 v1.2.0515(2023.05.15)

### 新功能  
+ **Loaderx**: 在ILoader接口中增加取得LoaderSettings实现的入口。  

### 修复问题  
+ **Loaderx**: 修复Settings中自定义Editor代码缺少宏定义，平台编译时的报错。  



------



## 版本 v1.2.0(2023.04.21)

### 新功能  
+ **RpgMaterial**: 增加配置对时间有效范围的验证功能。  
+ **RpgMaterial**: 增加配置对时间有效时长的验证功能。  
+ **RpgMaterial**: 增加用户数据记录初次获得时间戳的功能。  

### 更新  
+ JLGames.RocketDriver.Games.RpgMaterial.Common 重命名：  
  + MaterialData =>MetaData  
  + MaterialDataDisplay => MetaDisplay  
  + MaterialDataOper => MetaOper  
  + MaterialDataWorth => MetaWorth 
  + IUserMaterialData => IUserData  
  + IUserMaterialData1 => IUserData1  
  + UserMaterialData => UserData  
  + UserMaterialData1 => UserData1  
+ JLGames.RocketDriver.Games.RpgMaterial.Common 新增类：  
  + MetaValidDuration： 用于处理时长验证功能。  
  + MetaValidStamp： 用于处理有效时间范围的验证功能。  
  + IUserValidData： 用于记录**无**唯一Id、有获得时间戳记录的用户数据接口。  
  + IUserValidData1： 用于记录**有**唯一Id、有获得时间戳记录的用户数据接口。  
  + UserValidData： 用于记录**无**唯一Id、有获得时间戳记录的用户数据。  
  + UserValidData1： 用于记录**有**唯一Id、有获得时间戳记录的用户数据。  
+ JLGames.RocketDriver.Games.RpgMaterial.Material 增加加接口与实现：  
  + IMaterialValid： 配置结构的时间相关验证的接口定义。  
  + MaterialValidDuration： 抽象类，实现了对配置结构的时长验证支持。  
  + MaterialValidStamp： 抽象类，实现了对配置结构的固定时间验证支持。  
+ JLGames.RocketDriver.Games.RpgMaterial.User 增加加接口与实现：  
  + IUserMaterialValid:  用户数据结构时间相关验证的接口定义。  
  + IUserMaterialValid1： 用户数据结构时间相关验证的接口定义。  
  + IUserMaterialValidMod： 用户数据结构时间相关验证的接口定义（修改）。  
  + IUserMaterialValidMod1： 用户数据结构时间相关验证的接口定义（修改）。  
  + UserMaterialValid： 抽象类，用户数据结构参考基类  
  + UserMaterialValid1： 抽象类，用户数据结构参考基类  
+ JLGames.RocketDriver.Games.RpgMaterial.Service 增加加接口与实现：  
  + IMaterialServiceValid: 时间相关验证的服务接口。  
+ **RpgMaterial**: 调整部分源代码的目录结构。   
+ **RpgMaterial**: 新增获取当前时间戳的代理函数设置功能ValidUtil。   
+ **DateTimeUtil**： 新增本地时区的格式化字符串输入函数FormatDateTimeLocal。  

### 修复问题  
+ DateTimeUtil.FormatDateTime 补充强制UTC设置。  



------



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

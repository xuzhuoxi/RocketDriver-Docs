# 常见问题

#### 1.使用Event模块时、事件捕捉不到？  
1. 确认事件的调度和捕捉，必须是同一个对象。  
2. 确认事件是否真的被调度了。  

#### 2.使用Loader模块时，资源加载不成功或报错？  
1. 确认配置文件是否生成，并且位于 Resources 目录下。  
2. 确认 LoaderManager 是否进行初始化了，并传入名称与配置名称是否一致。  
3. 确认配置文件 (LoaderSettings.asset) 中选择的 **运行模式** 和 **下载模式** 是否正确。  
4. 确认配置中 "ProjectBasePath" 中的路径是否与项目一致。  
5. 确认 LoaderManager 是否对版本进行初始化化了。  
6. 确认路径、文件名是否正确。  
7. 确认是否在协程中开启了新的协程。Unity 对协程嵌套层次有限制。  

#### 3.使用I18n模块时，国际化文本显示不成功？  
1. 确认语言是否已经注册。  
2. 确认文件集是否已经注册。  
3. 确认默认语言与默认文件集是否正确。  
4. 确认是否进行了数据的加载。  
5. 确认是否使用了自定义加载器，并查看加载器逻辑。  

#### 4.使用Audio模块时，播放不成功？  
1. 确认配置文件是否生成，并且位于 Resources 目录下。  
2. 确认 AudioManager.prefab 是否放入到场景中。  
3. 确认注册音频信息时，bundleName, path是否正确。  
4. 确认播放调用时信息传入是否正确。  
5. 确认是否使用了自定义加载器，并查看加载器逻辑。  

#### 5.使用Panel模块时，打开面板不成功？  
1. 确认相关信息是否正确地注册到 PanelRegiester 中。  
2. 确认信息关联中键值是否正确。  

#### 6.使用Service模块时，找不到自己的服务？  
1. 确认服务实例是否为IService的实现类。  
2. 确认服务实例是否已经注册。  
3. 确认服务名称是否重名。   

#### 7.使用RpgMaterial模块时，怎样从Excel表格中生成数据各定义结构  
1. RpgMaterial中默认支持的Excel导表工具是 ExcelExporter， 支持把Excel数值表和常量表导出为多种数据文件和多种编程语言的结构定义。并支持自定义扩展。  
2. ExcelExporter是一个开源项目，位于  
[https://github.com/xuzhuoxi/ExcelExporter](https://github.com/xuzhuoxi/ExcelExporter)。  
3. 要实现导出后的同步处理，建议使用 FileSync. FileSync同样是一个开源项目，位于  
[https://github.com/xuzhuoxi/FileSync](https://github.com/xuzhuoxi/FileSync)。  

#### 8.执行Lua脚本时，调用C#函数无效怎么办
1. 检查函数是否已经注册。
2. 检查函数中参数类型和返回值类型是否为 bool、string、double，目前只支持这三种类型的参数。 返回值可以是void。 
3. 检查Lua脚本中调用C#函数是使用的名称是否与注册的一致，包括参数类型与数量。
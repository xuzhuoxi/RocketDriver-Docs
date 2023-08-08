## 3. 国际化(i18n) - 轻量级国际化解决方案

+ **JLGames.RocketDriver.Actions.i18n** 提供了国际化模块全部的功能支持。
+ 建议使用 [BabelEdit](https://www.codeandweb.com/babeledit) 创作管理数据集。
+ 使用国际化(i18n)分为三个步骤：
  1. 准备数据。
  2. 初始化（**通过注册信息然后初始化** 或 **通过配置资产进行初始化**）。
  3. 使用。

### 3.1 准备
理清楚项目的国际化需求，并准备好数据文件。  

#### 3.1.1 理清楚项目需要支持的国际化语言种类
这里以 **英文[英文]** 、**中文[简体]**、**中文[繁体]** 举例。  

#### 3.1.2 准备国际化数据文件
支持多个文件集，这里以两个文件集 **unity**、**rider** 举例。  
![image](assets/img/i18n_1.png)  
数据格式以 Key-Value 形式：  
![image](assets/img/i18n_11.png)  
当前测试数据集使用 Jetbrains 的 [BabelEdit](https://www.codeandweb.com/babeledit) 创作，这是一个不错的工具。  

### 3.2 通过注册国际化信息进行初始化

#### 3.2.1 向注册表注册语言。
调用 I18NRegister 实例中的 RegisterLang 函数：  
![image](assets/img/i18n_6.png)  
+ langName 与 langSuffix 建议一样。
+ default=true 时设置当前语言为默认语言。
  
#### 3.2.2 向注册表注册文件集加载信息
调用 I18NRegister 实例中的 RegisterFile 函数：  
![image](assets/img/i18n_7.png)  
+ fileKey 用于标识当前设置的文件集。
+ default=truej时设置当前文件集为默认文件集。

#### 3.2.3 根据注册表，加载数据到管理器中
调用 II18NManager 实例中的 LoadData 函数：  
`I18NManagerShared.Manager.LoadData();`  
![image](assets/img/i18n_8.png)  

**注意**：如果在过去已经执行为加载数据，那您应该先清除旧数据：  
`I18NManagerShared.Manager.ClearData();`  
![image](assets/img/i18n_9.png)  

### 3.3 通过配置资产进行初始化

#### 3.3.1 生成配置资产并配置信息
1. 选择配置资产的生成目录，点击菜单"Tools -> RocketDriver -> Project -> Gen I18NSettings".  
2. 生成的资产文件名为 "I18NSettings.asset".  
3. 设置文件集的扩展名称：Asset Extension。 这里建议 "json"。  
4. 把文件集加入到Assets配置列表中。或设置其中一个为默认(**只有最后一个默认生效**)。  
![image](assets/img/i18n_13.png)  

#### 3.3.3 通过配置资产初始化数据
调用 II18NManager 实例中的 LoadDataFromSettings 函数：  
`I18NManagerShared.Manager.LoadDataFromSettings(settings);`  
![image](assets/img/i18n_14.png)  

### 3.4 使用

#### 3.4.1 使用 I18NTMPText 组件，为TMP_Text增加国际化支持。
为TMP_Text节点增加 I18NTMPText 组件   
![image](assets/img/i18n_3.png)  
+ File Key 为注册文件集时的fileKey参数。
+ Auto Refresh 选中时，管理器重新加载数据后会自刷新。
  
#### 3.4.2 使用 I18NText 组件，为Text增加国际化支持。
为Text节点增加 I18NText 组件   
![image](assets/img/i18n_2.png)  
+ File Key 为注册文件集时的fileKey参数。
+ Auto Refresh 选中时，管理器重新加载数据后会自刷新。

#### 3.4.3 在代码中读取国际化数据。
`I18NManagerShared.Manager.GetValue(id, fileKey, lang);`  
![image](assets/img/i18n_10.png)  

#### 3.4.4 在代码中把文本内容进行国际化。
在文件内容中支持脚本格式： `{{id}}`  
`I18NManagerShared.Manager.GetContent(content, fileKey, lang);`  
![image](assets/img/i18n_12.png)  

### 3.5 示例
JLGames/RocketDriver/Samples/i18n  
![image](assets/img/i18n_4.png)  
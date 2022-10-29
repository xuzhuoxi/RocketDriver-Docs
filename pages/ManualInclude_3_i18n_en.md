## 3. Internationalization (i18n) - Lightweight Internationalization Solution

+ **JLGames.GameDriver.Actions.i18n** provides full functional support for the internationalization module.
+ [BabelEdit](https://www.codeandweb.com/babeledit) is recommended for authoring management datasets.
+ Use internationalization (i18n) in three steps:
   1. Prepare the data.
   2. Initialize (**Initialize by registering information** or **Initialize by configuring assets**).
   3. Use.

### 3.1 Preparation
Understand the internationalization requirements of the project and prepare data files.   

#### 3.1.1 Clarify the types of international languages ​​that the project needs to support
Here are **English[English]**, **Chinese[Simplified]**, **Chinese[Traditional]** as examples.  

#### 3.1.2 Prepare internationalization data files
Multiple file sets are supported, here are two file sets **unity**, **rider** for example.  
![image](assets/img/i18n_1.png)  
The data format is in the form of Key-Value:  
![image](assets/img/i18n_11.png)  
The current test dataset is authored using Jetbrains' [BabelEdit]  (https://www.codeandweb.com/babeledit), which is a nice tool.  

### 3.2 Initialize by registering internationalization informations

#### 3.2.1 Register languages with the registry.
Call the RegisterLang function in the I18NRegister instance:  
![image](assets/img/i18n_6.png)  
+ langName as langSuffix suggests.
+ default=true sets the current language as the default language.
  
#### 3.2.1 Loading information to the registry registration file set
Call the RegisterFile function in the I18NRegister instance:  
![image](assets/img/i18n_7.png)  
+ fileKey is used to identify the currently set fileset.
+ default=truej Set the current fileset as the default fileset.

#### 3.2.3 According to the registry, load data into the manager
Call the LoadData function in the II18NManager instance:  
`I18NManagerShared.Manager.LoadData();`  
![image](assets/img/i18n_8.png)  

**NOTE**: If you have performed load data in the past, you should clear the old data first:  
`I18NManagerShared.Manager.ClearData();`  
![image](assets/img/i18n_9.png)  

### 3.3 Initialize by configuring asset

#### 3.3.1 Generate configuration assets and configure information
1. Select the generation directory of the configuration assets, click the menu "Tools -> GameDriver -> Project -> Gen I18NSettings".  
2. The generated asset file is named "I18NSettings.asset".  
3. Set the extension name of the fileset: Asset Extension. "json" is suggested here.  
4. Add the fileset to the Assets configuration list. Or set one of them as default (**only the last default takes effect**).  
![image](assets/img/i18n_13.png)  

#### 3.3.3 Initializing data by configuring assets
Call the LoadDataFromSettings function in the II18NManager instance:  
`I18NManagerShared.Manager.LoadDataFromSettings(settings);`  
![image](assets/img/i18n_14.png)  

### 3.4 Use

#### 3.4.1 Use the I18NTMPText component to add internationalization support to TMP_Text.
Add I18NTMPText component to TMP_Text node  
![image](assets/img/i18n_3.png)  
+ File Key is the fileKey parameter when registering a file set.
+ Auto Refresh When checked, the manager will refresh itself after reloading the data.
  
#### 3.4.2 Use the I18NText component to add internationalization support to Text.
Add I18NText component to Text node  
![image](assets/img/i18n_2.png)  
+ File Key is the fileKey parameter when registering a file set.
+ Auto Refresh When checked, the manager will refresh itself after reloading the data.

#### 3.4.3 Reading internationalized data in code.
`I18NManagerShared.Manager.GetValue(id, fileKey, lang);`
![image](assets/img/i18n_10.png)  

#### 3.4.4 Internationalize the text content in the code.
Support script format in the file content: `{{id}}`   
`I18NManagerShared.Manager.GetContent(content, fileKey, lang);`  
![image](assets/img/i18n_12.png)  

### 3.5 Example
GameDriver/Samples/i18n  
![image](assets/img/i18n_4.png)  
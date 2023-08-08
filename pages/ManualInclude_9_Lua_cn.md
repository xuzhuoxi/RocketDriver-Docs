## 9. Lua脚本解释器
+ 引入轻量级的开源Lua解释器：LuaInterpreter。  
+ 进行了功能扩展和优化，使之在Unity中能更好地工作。  

### 9.1 库说明

#### 9.1.1信息说明
+ 库名称: **Lua Interpreter**  
+ 作者: **Liu Junfeng**  
+ URL: http://www.codeproject.com/Articles/228212/Lua-Interpreter  
+ License: **MIT** (http://opensource.org/licenses/mit-license.php)  

#### 9.1.2修改说明
1. 去除了WinFrom相关代码逻辑。  
2. 对LuaTable类进行的函数扩展。  
3. 增加了多个针对LuaValue相关的函数处理。  
4. 增加Unity使用包装类Lua，这也是常用功能入口。  

### 9.2 使用

#### 9.2.1 在C#中执行Lua脚本
1. 调用 `Lua.RunLuaRaw` 函数，或直接执行Lua脚本。如有返回值，则获得返回值。  
![image](assets/img/Lua_6.jpg)  
2. 调用 `Lua.RunLua` 函数，同样可以执行Lua脚本。并针对返回值返回了包装类LuaResult。  
![image](assets/img/Lua_5.jpg)  
3. 调用 `Lua.IsTrue` 函数，可直接判断Lua的逻辑表达式，并获得结果布尔值。  
![image](assets/img/Lua_4.jpg)  

#### 9.2.2 在Lua中调用C#函数
1. 首先需要把C#函数注册到Lua解释器环境中，我们可以用 `Lua.RegisterFunction` 函数执行注册逻辑。  
![image](assets/img/Lua_2.jpg)   
2. 在Lua脚本中，使用注册时的funcName则可以调用被注册的函数。  
3. 重复使用同一个funcName进行注册，则会进行覆盖。  
4. 使用 `Lua.UnregisterFunction` 函数则可能 解除注册行为。  
![image](assets/img/Lua_3.jpg)   

#### 9.2.3 重置Lua解释器
1. 使用 `Lua.Restart` 函数，可重置Lua解释器，这将清空全部上下文。  
![image](assets/img/Lua_7.jpg)  

### 9.3 示例
JLGames/GameDriver/Samples/LuaDemo   
![image](assets/img/Lua_1.png)  
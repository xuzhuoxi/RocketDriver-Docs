# Getting Start

### Overview
This User Manaul was designed to provide GaemDriver Pro users with a basic overview of the
features and functionality of the tool.  

### Install
1. After downloading GameRiver Pro from Unity's Asset Store, go to: "Assets->Import Package->Custom Package...". 
2. In the Import Assets window, find and select the RocketDriver Pro UnityPackage file. 
3. Once Unity appears in the Import Packages window, verify that Import is selected for all projects, then click the Import button at the bottom right of the window. 
4. All RocketDriver Pro files will be added to Assets/JLGames/RocketDriver.

You can also select the desired section to import.  

### support
If you want to quickly understand the important features in RocketDriver Pro, you can directly refer to the examples in JLGames/RocketDriver/Samples.  

If you want to learn more about the design ideas and details of each functional module in RocketDriver Pro, you can find more information and FAQs in [Online Help](https://www.xuzhuoxi.com/RocketDriver-Docs/) .  

If you can't find the information you're looking for, please [file an issue](https://github.com/xuzhuoxi/RocketDriver-Docs/issues/new) (or submit a pull request) to describe your experience.  

Or contact the author: xuzhuoxi@gmail.com or mailxuzhuoxi@163.com  

# Features
Source code storage locations in RocketDriver Pro are regular.  
+ The source code in **JLGames/RocketDriver/Runtime/CSharp** only depends on the C# standard library, ** does not depend on the Unity standard library. It is an extension to C#.

+ The source code in **JLGames/RocketDriver/Runtime/Actions** depends on CSharp and the Unity standard library. It is a functional extension to the Unity engine.

+ The source code in **JLGames/RocketDriver/Runtime/Games** depends on CSharp and Actions. It is a general implementation of system functions commonly used in the game development process.

## Functional Overview

### JLGames/RocketDriver/Runtime/CSharp
The namespace is **JLGames.RocketDriver.CSharp**  
+ Algs  
  Transparent algorithm related functions  
  + AStar  
  A\* general algorithm  
+ Archive  
File archiving related functions, now including zip decompression function  
+ Buffer  
The byte data cache function supports reading and writing of big and small endian settings and basic data types.  
+ DateTimex  
Time related functions. Contains calculation conversions between time units, string formatting of times, timers that support pause and resume, and more.  
+ Event  
Event related functions. Contains event monitoring, removal and scheduling functions. For details, see [1.Event System(Event)](Manual_1.Event_en.html)  
+ Extensions  
Extensions for basic data types in CSharp.  
+ Imagex  
Image related functions. Now includes RGBA data objects, filter processing functions, and more.  
+ Mathx  
Mathematical calculation related functions.  
+ Net  
Socket API definition, message encapsulation and unpacking functions, etc.  
+ Pool  
Object pool related functions. Contains Key-Value object pool, metadata object pool, reuse object pool, etc.  
+ Service  
Service framework basic support. For details, see [7. Service Framework(Service)](Manual_7.Service_en.html)  
+ TinyJson  
Simple Json reading and writing library. Open source from Github: [https://github.com/zanders3/json](https://github.com/zanders3/json) .  
+ Utils  
  Common tool functions based on CSharp  
  + Encrypt  
  **Encryption and decryption** related functions, now including Des, Rijandel, RSA  
  + ArrayUtil  
  **Array** related functions, such as array cloning, merging, type conversion, array matrix rotation and other functions  
  + BitUtil  
  The **bit operation** function of numeric values.  
  + ConfusedUtil  
  **Data Obfuscation** related functions.  
  +DirectionUtil  
  **Directory** related functions in the file system.  
  + FileUtil  
  **File** related functions in the file system.  
  + PathUtil  
  **Path** related functions in the file system.  
  +PrintUtil  
  **Print** support for object information.  
  + ReflexUtil  
  **Reflection** value-related functions.  
  + TextUtil  
  Character file read and write functions.  
+ Xml  
XML related function support: serialization and deserialization  
+ Callback  
Generic Callback Context  
+ ICloneable  
Generic clone interface  

### JLGames/RocketDriver/Runtime/Actions  
The namespace is **JLGames.RocketDriver.Actions**  
+ Animatorx  
Feature support for Unity's animation system. Contains animation search, animation playback, event management and other functions.  
+ AssetIndex  
The Editor function provides the ability to generate a "name -> path" index for assets in the project.  
+ Audio  
Audio Manager, which provides the function of unified management of audio in the project. For details, please see [5. Audio Manager (AudioManager)](Manual_5.Audio_en.html).  
+ Component  
Some useful components.  
+ Component2D  
Some useful 2D components.  
+ DateTimex  
Time-related functions, including timers that rely on the Unity engine, cycle time slice functions, etc.  
+ ExcelExporter  
Function support for exporting data from the third-party table export tool [ExcelExporter](https://github.com/xuzhuoxi/ExcelExporter).  
+ Extensions  
Extensions to commonly used data structures in Unity.  
+ Graphicsx  
Image related functions. Contains color conversion functions, image pixel data structures, texture functions, etc.  
+ i18n  
Internationalization function. For details, see [3. Internationalization System(i18n)](Manual_3.i18n_en.html).  
+Jsonx  
Related functions for Json processing.  
+ Layer  
Unity displays the structural layered design capabilities.  
+ Loaderx  
Resource loading management module. For details, see [2. Loader System (Loader))](Manual_2.Loader_en.html).  
+ Localx  
Depends on the local storage capabilities of PlayerPrefs.  
+ Pool  
The object pool function extends the object pool function in JLGames/RocketDriver/Runtime/CSharp/Pool, and adds parts related to Unity.  
+ Service  
Service framework Unity support. For details, see [7. Service Framework(Service)](Manual_7.Service_en.html)  
+ TheadEvent  
Event related functions. Added Unity multithreading support to JLGames/RocketDriver/Runtime/CSharp/Event.  
+ UIElements  
Editor function. It is an extension to the UIElements functionality in Unity.  
+ Utils  
  Rely on common functions of Unity.   
  + CameraUtil  
  **Camera** related functions.  
  + CaptureUtil  
  **Screenshot** related functions.  
  + ComponentUtil  
  **Component** related functions.  
  +DebugUtil  
  **Debug printing** related functions.  
  + GeometryUtil  
  **Geometric calculation** related functions.  
  + IdentifyUtil  
  **Machine Id** related functions.  
  + ImageUtil  
  **Image** related functions.  
  + MathfUtil  
  **Mathematical calculation** related functions  
  + PositionUtil  
  Unity object **position calculation** related functions.  
  + TilemapUtil  
  Common public behavior under the **UnityEngine.Tilemaps** component.  
  + TransformUtil  
  **UnityEngine.Transform** component related extension functions.  
  + UnityPathUtil  
  Untiy-related path handling functions.
+ Wait  
Unity coroutine related functions.  

### JLGames/RocketDriver/Runtime/Games  
The namespace is **JLGames.RocketDriver.Games**  
+ LocalAccount  
Local account storage function.  
+ NetManager  
Network connection management, virtual servers. For details, see [4. Network Manager (NetManager)](Manual_4.Net_en.html).  
+ PanelManager  
Panel management module. For details, see [6. Panel Manager (PanelManager)](Manual_6.Panel_en.html)
+RpgMaterial  
Game data management system. Please see [8.RPG Material Data System(RpgMaterial)](Manual_8.RpgMaterial_en.html) for details.  
+ Service  
Common service instances under the service framework. For details, see [7. Service Framework(Service)](Manual_7.Service_en.html).  
+ Tiledx  
Data interpretation capabilities for third-party software [Tiled](https://www.mapeditor.org/).  

# Common function modules
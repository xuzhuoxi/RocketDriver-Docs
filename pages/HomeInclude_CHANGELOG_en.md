# GameDriver Pro Changelog
## Version v1.2.0(2023.04.21)

### New Features  
+ **RpgMaterial**: Add configuration validation function for valid range of time.  
+ **RpgMaterial**: Add the validation function of configuring the effective duration of time.  
+ **RpgMaterial**: Add the function of user data record getting timestamp for the first time.  

### Updates  
+ JLGames.GameDriver.Games.RpgMaterial.Common renamed:  
   + MaterialData => MetaData  
   + MaterialDataDisplay => MetaDisplay  
   + MaterialDataOper => MetaOper  
   + MaterialDataWorth => MetaWorth  
   + IUserMaterialData => IUserData  
   + IUserMaterialData1 => IUserData1  
   + UserMaterialData => UserData  
   + UserMaterialData1 => UserData1  
+ JLGames.GameDriver.Games.RpgMaterial.Common new class:  
   + MetaValidDuration: Used to handle the duration validation function.  
   + MetaValidStamp: Validation function for handling valid time ranges.  
   + IUserValidData: User data interface used to record **without** unique Id and with timestamp records.  
   + IUserValidData1: It is used to record the user data interface with **unique** ID and timestamp record.  
   + UserValidData: Used to record user data that has **no** unique Id and has obtained timestamp records.  
   + UserValidData1: Used to record user data with **unique** ID and timestamp records.  
+ JLGames.GameDriver.Games.RpgMaterial.Material added interface and implementation:  
   + IMaterialValid: Interface definition for time-dependent validation of configuration structures.  
   + MaterialValidDuration: An abstract class that implements duration validation support for configuration structures.  
   + MaterialValidStamp: An abstract class that implements fixed-time validation support for configuration structures.  
+ JLGames.GameDriver.Games.RpgMaterial.User added interface and implementation:  
   + IUserMaterialValid: Interface definition for time-related validation of user data structures.  
   + IUserMaterialValid1: Interface definition for time-dependent validation of user data structures.  
   + IUserMaterialValidMod: Interface definition (modification) for time-dependent validation of user data structures.  
   + IUserMaterialValidMod1: Interface definition (modification) for time-dependent validation of user data structures.  
   + UserMaterialValid: abstract class, user data structure reference base class  
   + UserMaterialValid1: abstract class, user data structure reference base class  
+ Add interface and implementation of JLGames.GameDriver.Games.RpgMaterial.Service:  
   + IMaterialServiceValid: Service interface for time-related validation.  
+ **RpgMaterial**: Adjust the directory structure of some source codes.  
+ **RpgMaterial**: Added the proxy function setting function ValidUtil to obtain the current timestamp.  
+ **DateTimeUtil**: Added format string input function FormatDateTimeLocal for local time zone.  

### Fixes  
+ DateTimeUtil.FormatDateTime added to enforce UTC settings.  



------



## Version v1.1.0(2023.03.18) 

### New Features  
+ **Runtime**: Add Lua interpreter: LuaInterpreter.  
+ **Runtime**: Support Lua code to call C# function.  
+ **Runtime**: Support C# to execute Lua code.  
+ **Editor**: ExportSettingsEditor adds the function of sorting AssetPaths.  

### Updates  
+ **RPG Material Data System**: Adjust the design and convert the quality (quality) from value classification to display classification.  

### Fixes  
+ **RPG Material Data System**: Solve the abnormal display of the example RpgMaterialDemo, adjust the design resolution to 1024x768.  



------



## Version v1.0.4(2023.01.31)  

### New Features  
+ **RPG Material Data System**: Add default data update logic.  
  + The data update function logic is encapsulated in the MaterialServiceProxy implementation.  
  + MaterialService implements data update through MaterialServiceProxy.  
+ **RPG Material Data System**: Add support for common events.  
  + MaterialServiceProxy implements event throwing when data is updated.  
+ **RPG Material Data System**: Add data change trigger function.  
  + MaterialServiceProxy implements the trigger registration logic.  
  + MaterialServiceProxy implements the trigger call when the data is updated.  
+ **RPG Material Data System**: Add the corresponding sample “Samples/RpgMaterial”.  

### Updates  
+ **RPG Material Data System**: Added IMaterialSetMod interface, MaterialSet implements this interface.  
+ **RPG Material Data System**: Define the unique Id generation function interface IUniqueIdGenerator, and implement UniqueIdGenerator accordingly.  
+ **RPG Material Data System**: Added a reusable proxy MaterialServiceProxy to implement throwing events and executing triggers when user data is updated.  
+ **RPG Material Data System**: Modify IMaterialServicel, inherit IEventDispatcher by default.  
+ **RPG Material Data System**: Modify the MaterialService implementation to support data update, event management and data triggers.  

### Fixes  
+ Games.RpgMaterial: Fix IMaterialSet, MaterialSet namespace errors.  



------



## Version v1.0.3 (2023.01.05)
initial version.  

### New Features  
+ **Event Module**  
  + Support for custom extensions.  
  + Support unified management.  
  + Support Unity multithreading.  

+ **Asset Loader**  
  + Support Editor, Resources, Assetbundle mode switching.  
  + Support configuration management.  
  + Provide event dispatched under critical timing.  

+ **Internationalization**  
  + Support for language extensions.  
  + Support for multi-file datasets.  
  + Support for custom data loaders.  
  + Provide event dispatched under critical timing.  

+ **Network management**  
  + Support link management.  
  + Provide Socket API compatible with protocols such as TCP, UDP, HTTP(HTTPS), WebSocket(WebSockets).  
  + Provides a set of extended service framework for the separation of front-end and back-end logic for stand-alone games.   
  + Provide event dispatched under critical timing.  

+ **Audio management**  
  + Support system-level and user-level configuration management.  
  + Support custom audio loader.  
  + Supports configuration limit for the number of playbacks.  
  + Provide event dispatched under critical timing.  

+ **Panel management**  
  + Support display layer management.  
  + Support the injection management of panel information,  
  + Support panel custom background, animation.  
  + Support panel function custom extension.  
  + Provide event dispatched under critical timing.  

+ **Service Framework**  
  + Supports dividing business logic into services and managing them.  
  + Support service data injection, initialization, data initialization, data saving, data loading, reset and other extensions.  
  + Unified management and debugging of support services.  
  + Provide event dispatched under critical timing.  

+ **RPG Material Data System**  
  + Support unified management of game configuration data in **KTD(Key-Type-Define)** format.  
  + Support player data management in **KTV(Key-Type-Value)** format (memory, local files, servers, etc.).  
  + Supports the mechanism that corresponds to multiple player data under the same configuration definition.  
  + Provide event dispatched under critical timing.  

+ **Other features**  
  + A\* algorithm  
  + unzip function  
  + time related functions  
  + image processing  
  + data tools  
  + object pool  
  + animation event function  
  + Excel guide table explanation  
  + local data saving  
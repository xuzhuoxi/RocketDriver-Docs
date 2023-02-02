# GameDriver Pro Changelog

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
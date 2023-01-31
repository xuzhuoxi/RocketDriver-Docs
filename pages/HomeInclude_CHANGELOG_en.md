# GameDriver Pro Changelog

## Version v1.0.4(2023.01.31)

### Features

+ Games.RpgMaterial: Add default data update logic.
   + The data update function logic is encapsulated in the MaterialServiceProxy implementation.
   + MaterialService implements data update through MaterialServiceProxy.
+ Games.RpgMaterial: Add support for common events.
   + MaterialServiceProxy implements event throwing when data is updated.
+ Games.RpgMaterial: Add data change trigger function.
   + MaterialServiceProxy implements the trigger registration logic.
   + MaterialServiceProxy implements the trigger call when the data is updated.
+ Games.RpgMaterial: Add the corresponding sample “Samples/RpgMaterial”.

### Updates

+ Games.RpgMaterial: Added IMaterialSetMod interface, MaterialSet implements this interface.
+ Games.RpgMaterial: Define the unique Id generation function interface IUniqueIdGenerator, and implement UniqueIdGenerator accordingly.
+ Games.RpgMaterial: Added a reusable proxy MaterialServiceProxy to implement throwing events and executing triggers when user data is updated.
+ Games.RpgMaterial: Modify IMaterialServicel, inherit IEventDispatcher by default.
+ Games.RpgMaterial: Modify the MaterialService implementation to support data update, event management and data triggers.

### Fixes

+ Games.RpgMaterial: Fix IMaterialSet, MaterialSet namespace errors.  

## Version v1.0.3 (2023.01.05)

initial version.  

+ New feature: Event Module.
  + Support for custom extensions.
  + Support unified management.
  + Support Unity multithreading.

+ New feature: Resource Loader.
  + Support Editor, Resources, Assetbundle mode switching.
  + Support configuration management.
  + Provide event dispatched under critical timing.

+ New feature: Internationalization.
  + Support for language extensions.
  + Support for multi-file datasets.
  + Support for custom data loaders.
  + Provide event dispatched under critical timing.

+ New feature: Network management.
  + Support link management.
  + Provide Socket API compatible with protocols such as TCP, UDP, HTTP(HTTPS), WebSocket(WebSockets).
  + Provides a set of extended service framework for the separation of front-end and back-end logic for stand-alone games.
  + Provide event dispatched under critical timing.

+ New feature: Audio management.
  + Support system-level and user-level configuration management.
  + Support custom audio loader.
  + Supports configuration limit for the number of playbacks.
  + Provide event dispatched under critical timing.

+ New feature: Panel management.
  + Support display layer management.
  + Support the injection management of panel information,
  + Support panel custom background, animation.
  + Support panel function custom extension.
  + Provide event dispatched under critical timing.

+ New feature: Service Framework
  + Supports dividing business logic into services and managing them.
  + Support service data injection, initialization, data initialization, data saving, data loading, reset and other extensions.
  + Unified management and debugging of support services.
  + Provide event dispatched under critical timing.

+ New Feature: RPG Material Data System
  + Support unified management of game configuration data in **KTD(Key-Type-Define)** format.
  + Support player data management in **KTV(Key-Type-Value)** format (memory, local files, servers, etc.).
  + Supports the mechanism that corresponds to multiple player data under the same configuration definition.
  + Provide event dispatched under critical timing.

+ new features: other features
  + A\* algorithm
  + unzip function
  + time related functions
  + image processing
  + data tools
  + object pool
  + animation event function
  + Excel guide table explanation
  + local data saving
  + wait
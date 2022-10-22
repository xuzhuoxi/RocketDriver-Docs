---
layout: default
page_id: 'home.faqs'
group_id: home
lang: en
title: 'FAQS | GameDriver Pro'
---
# FAQs

#### 1. When using the Event module, the event cannot be captured?
  1. Check that the dispatch and capture of confirmation events must be the same object. 
  2. Check that the event was actually dispatched.

#### 2. When using the Loader module, does the resource loading fail or report an error?
  1. Check whether the configuration file is generated and located in the Resources directory.
  2. Check whether LoaderManager is initialized, and whether the incoming name is the same as the configuration name.
  3. Check that the **Operation Mode** and **Download Mode** selected in the configuration file (LoaderSettings.asset) are correct.
  4. Check that the path in "ProjectBasePath" in the configuration is consistent with the project.
  5. Check whether LoaderManager has initialized the version.
  6. Check whether the path and file name are correct.
  7. Check whether a new coroutine is started in the coroutine. Unity has restrictions on the nesting level of coroutines.

#### 3. When using the I18n module, the internationalized text is not displayed successfully?
  1. Check if the language is registered.
  2. Check that the fileset is registered.
  3. Check that the default language and default fileset are correct.
  4. Check whether the data has been loaded.
  5. Check that a custom loader is used and review the loader logic.

#### 4. When using the Audio module, the playback is unsuccessful?
  1. Check whether the configuration file is generated and located in the Resources directory.
  2. Check whether AudioManager.prefab is placed in the scene.
  3. Check whether the bundleName and path are correct when registering audio information.
  4. Check whether the information is passed in correctly when the playback is called.
  5. Check that a custom loader is used and review the loader logic.

#### 5. When using the Panel module, the panel fails to open?
  1. Check whether the relevant information is correctly registered in the PanelRegister.
  2. Check whether the key value in the information association is correct.

#### 6. Can't find your own service when using the Service module?
  1. Check whether the service instance is the implementation class of IService.
  2. Check whether the service instance has been registered.
  3. Check whether the service names are the same.

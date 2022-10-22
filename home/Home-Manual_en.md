---
layout: default
page_id: 'home.manual'
group_id: home
lang: en
---
# Getting Start

### Overview
This User Manaul was designed to provide GaemDriver Pro users with a basic overview of the
features and functionality of the tool.  

### Install
1. After downloading GameRiver Pro from Unity's Asset Store, go to: "Assets->Import Package->Custom Package...". 
2. In the Import Assets window, find and select the GameDriver Pro UnityPackage file. 
3. Once Unity appears in the Import Packages window, verify that Import is selected for all projects, then click the Import button at the bottom right of the window. 
4. All GameDriver Pro files will be added to Assets/GameDriver.

You can also select the desired section to import.  

### support
If you want to quickly understand the important features in GameDriver Pro, you can directly refer to the examples in GameDriver/Samples.  

If you want to learn more about the design ideas and details of each functional module in GameDriver Pro, you can find more information and FAQs in [Online Help](https://www.xuzhuoxi.com/GameDriver-Docs/) .  

If you can't find the information you're looking for, please [file an issue](https://github.com/xuzhuoxi/GameDriver-Docs/issues/new) (or submit a pull request) to describe your experience.  

Or contact the author: xuzhuoxi@gmail.com or mailxuzhuoxi@163.com  

# Features
Source code storage locations in GameDriver Pro are regular.  
+ The source code in **GameDriver/Runtime/CSharp** only depends on the C# standard library, ** does not depend on the Unity standard library. It is an extension to C#.
+ The source code in **GameDriver/Runtime/Actions** depends on CSharp and the Unity standard library. It is a functional extension to the Unity engine.
+ The source code in **GameDriver/Runtime/Games** depends on CSharp and Actions. It is a general implementation of system functions commonly used in the game development process.


**Table of contents**:  

{% assign pages = site.data.manual.pages | where: "lang", page.lang %}
{% for p in pages %}
  <h4><a href="{{ site.home.url }}/{{ p.pattern }}">{{ p.text }}</a><h4>
{% endfor %}
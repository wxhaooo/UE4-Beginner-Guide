# 1. UE4 新手入门指南
<!-- TOC -->

- [1. UE4 新手入门指南](#1-ue4-新手入门指南)
  - [1.1. 阅读指南](#11-阅读指南)
    - [1.1.1. Quick Start](#111-quick-start)
    - [1.1.2. Slow Start](#112-slow-start)
    - [1.1.3. Go Deep](#113-go-deep)
  - [1.2. Foundamentation](#12-foundamentation)
    - [1.2.1. Blueprint Visual Scripting](#121-blueprint-visual-scripting)
    - [1.2.2. Coding Standard](#122-coding-standard)
    - [1.2.3. Project Name Standard](#123-project-name-standard)
  - [1.3. Gameplay](#13-gameplay)
    - [1.3.1. Animation System](#131-animation-system)
      - [1.3.1.1. Overview of Animation System](#1311-overview-of-animation-system)
      - [1.3.1.2. Animation With C++](#1312-animation-with-c)
      - [1.3.1.3. Animation Misc](#1313-animation-misc)
    - [1.3.2. HUD](#132-hud)
    - [1.3.3. AI](#133-ai)
  - [1.4. Engine Mechanism](#14-engine-mechanism)
    - [1.4.1. Extensions to C++](#141-extensions-to-c)
      - [1.4.1.1. Delegate](#1411-delegate)
        - [1.4.1.1.1. Use Delegate](#14111-use-delegate)
        - [1.4.1.1.2. Why use Delegate?](#14112-why-use-delegate)
        - [1.4.1.1.3. Delegate Details](#14113-delegate-details)
      - [1.4.1.2. Reflection](#1412-reflection)
      - [1.4.1.3. Modules](#1413-modules)
      - [1.4.1.4. Coroutine](#1414-coroutine)
      - [1.4.1.5. MultiThreads](#1415-multithreads)
      - [1.4.1.6. Serialization](#1416-serialization)
    - [1.4.2. Engine Architecture](#142-engine-architecture)
  - [1.5. Rendering](#15-rendering)
  - [1.6. Project & Courses](#16-project--courses)
    - [1.6.1. Complete Project](#161-complete-project)
    - [1.6.2. Gameplay](#162-gameplay)
    - [1.6.3. Character,Camera,Control (3C)](#163-charactercameracontrol-3c)
    - [1.6.4. User Interface (UI)](#164-user-interface-ui)
    - [1.6.5. Resources](#165-resources)
  - [1.7. Wonderful Reference](#17-wonderful-reference)

<!-- /TOC -->

## 1.1. 阅读指南

### 1.1.1. Quick Start

__这一节适用于需要快速上手UE4并投入到开发中，适用于时间比较紧迫，有一定引擎使用经验和编程经验的同学。__

__建议的路径是首先确认开发手段，是蓝图、C++还是Lua，熟悉后即可以参看项目相关部分__。

如果是蓝图，跳转到[Blueprint Visual Scripting](#blueprint-visual-scripting)熟悉官方文档。

如果是C++，跳转到[Coding Standard](#coding-standard)首先熟悉UE4中使用的代码规范，然后可以一边看项目相关代码，一边参考[Programming with C++ | Unreal Engine Documentation](https://docs.unrealengine.com/4.27/en-US/ProgrammingAndScripting/ProgrammingWithCPP/)官方文档上手工作。

如果是Lua，路径暂缺，需要相关同学补充。

### 1.1.2. Slow Start

__这一节适合有一定编程基础，但是游戏开发方面基础为0的同学。__

__建议的路径是如果是后续开发仅使用蓝图的同学，走蓝图路线即可。如果是后续使用C++较多的同学，直接走C++路线即可。__

__在对C++和蓝图均熟悉以后，建议在进入Lua路线。__

 **蓝图路线** ：首先跳转到[Blueprint Visual Scripting](#blueprint-visual-scripting)熟悉官方文档。其次建议学习蓝图项目 [虚幻引擎4游戏开发：使用蓝图制作大逃杀游戏](https://www.udemy.com/course/ue4blueprintbattleroyalecn/learn/lecture/22825523#overview)。这个课程是一个纯蓝图课程，用蓝图完整实现了一个大逃杀like游戏。通过这个项目基本可以熟悉蓝图的使用。
 
 **C++路线**：跳转到[Coding Standard](#coding-standard)首先熟悉UE4中使用的代码规范。接着建议学习C++项目[Unreal Engine 4 Mastery：Create Multiplayer Games with C++](https://www.bilibili.com/video/BV1pb41177pn)。这个课程绝大多数主体用C++进行开发，少量使用蓝图辅助开发。通过这个课程，基本可以掌握UE4 C++开发的基本知识。同时建议看不懂的地方多参考[Programming with C++ | Unreal Engine Documentation](https://docs.unrealengine.com/4.27/en-US/ProgrammingAndScripting/ProgrammingWithCPP/)。
 
 **Lua落线**：C++和蓝图都熟悉了，只要了解了Lua语法，上手就是顺其自然而然的事情了~。
 
 ### 1.1.3. Go Deep
 
__在完成上面的简单入门/快速入门后，就可以上手项目在项目中学习了，文章中整理了少量特化领域的知识和问题以供参考，也希望负责对应部分的同学可以把自己的经验有时间的时候补充到对应部分:)__
 
除此之外，UE的C++的有很多值得研究的底层公共课题： 比如**delegate的原理、反射实现机制、模块化、多线程、蓝图虚拟机**等等。 如果有同学对这方面感兴趣可以在参考本文档中对应部分。目前这部分还不完善，希望后面有时间的同学可以一起渐渐完善这部分:)。

## 1.2. Foundamentation

### 1.2.1. Blueprint Visual Scripting

* [Blueprint Visual Scripting](https://docs.unrealengine.com/en-US/ProgrammingAndScripting/Blueprints/index.html)

> The official document contains the concept and usage of blueprints, If you want to understand the blueprint, this document is the best choice for beginner.

### 1.2.2. Coding Standard

* [Coding Standard](https://docs.unrealengine.com/en-US/ProductionPipelines/DevelopmentSetup/CodingStandard/index.html)

> Standards and conventions used by Epic Games in the Unreal Engine 4 codebase.

### 1.2.3. Project Name Standard

* [UE4 Style Guide](https://github.com/Allar/ue4-style-guide)

> UE4 C++ and engineering resource naming specification

__`Be sure to read these two documents before writing C++ code in UE4, this will make your code look more professional and more suitable for multi-person cooperation project`__

## 1.3. Gameplay

### 1.3.1. Animation System

#### 1.3.1.1. Overview of Animation System

* [Animation System Overview](https://docs.unrealengine.com/en-US/AnimatingObjects/SkeletalMeshAnimation/Overview/index.html)
> Official documents containing the basic concepts of the animation system and all of subsystem about animation.

* [A deep look into animation framework in ue4](https://arrowinmyknee.com/2019/09/11/a-deep-look-into-animation-framework-in-ue4/)
> A overview of detailed implementation of animation system with c++ in UE4.

* [Link1: Mapping Out The UE4 Animation Architecture Flow
](https://gist.github.com/ikrima/a900a50c1d4b7293d44b)

* [Link2: Mapping Out The UE4 Animation Architecture Flow](https://bebylon.dev/ue4guide/gameplay-programming/animation-subsystem/animation-subsystem/)

> A framework for animation subsystem in ue4

* [UAnimNotify & UAnimNotifyState](http://jollymonsterstudio.com/2018/12/10/unreal-engine-c-fundamentals-uanimnotify-uanimnotifystate/)

#### 1.3.1.2. Animation With C++

* [How can I play animations strictly from C++?](https://answers.unrealengine.com/questions/292345/how-can-i-play-animations-strictly-from-c.html)
> Unreal has two programming methods: Blueprint and C++. It is very important to choose the correct method to meet the needs. It is especially important in animation systems. This question discusses which parts of the animation are more appropriate to use C++ and which are more appropriate to use visual blueprints.

#### 1.3.1.3. Animation Misc

> Unreal中的IK节点

* [IK节点详解](https://zhuanlan.zhihu.com/p/41425611)
> 包含了Unreal常用的two bone IK & FABRIK & Hand IK Retargeting的详解和原理

* [动画融合](https://blog.uwa4d.com/archives/Study_Unreal4_Animation_2.html)
> 包含了UE中常用的各种动画融合节点的使用方法，最重要的是有动画蒙太奇（animation montage）的介绍和使用，__最重要的是介绍了Layered Animation与Animation Composite并且区分了两者的不同__。


### 1.3.2. HUD

### 1.3.3. AI

wait to add.

## 1.4. Engine Mechanism

### 1.4.1. Extensions to C++

#### 1.4.1.1. Delegate

##### 1.4.1.1.1. Use Delegate

* [Delegates in UE4, Raw C++, and BP Exposed](https://unreal.gg-labs.com/wiki-archives/macros-and-data-types/delegates-in-ue4-raw-c++-and-bp-exposed)
> [The official documents about delegates](https://docs.unrealengine.com/en-US/ProgrammingAndScripting/ProgrammingWithCPP/UnrealArchitecture/Delegates/index.html) are vague and difficult to understand. This article explains the use of delegates very well.

##### 1.4.1.1.2. Why use Delegate?

> __`C++ don't have event system out of the box, at most you got normal function calls which you know that will be called on specific occasion. The weakness of this set up is fact that you can't detect events in code outside of the object it self, or else called of event sends it also somewhere else, external object can't get call then other object is destroyed for example. Thats why delegates was made which work like variable and other object (or even object less static function) can register it to the event to receive the call when it occurs.` [Ref: Seeking a purpose of Delegates!](https://answers.unrealengine.com/questions/783913/view.html)__

> C++本身不具有事件响应功能。只能在发生事件时主动调用需要侦听该事件的对象的相应函数。这要求事件发出者（被观察者）拥有观察者的信息以便调用响应事件。但事件发出者拥有观察者逻辑上不合理。所以使用观察者模式来分离。delegate就是观察者模式的一种实现。由被观察者约定观察者响应事件的接口，需要侦听该事件的观察者通过delegate在自己的类中侦听时间。当事件发生时，被观察者广播该事件给所有侦听者。（用法见[Use Delegate](#use-delegate)，原理见下面几个推荐。）

* [什么是“观察者模式”？](https://zhuanlan.zhihu.com/p/158537313)
> Delegate是观察者模式的一个实现，了解delegate，也有必要看看观察者模式。 

##### 1.4.1.1.3. Delegate Details

* [游戏引擎原理与实践：卷一 基础框架，4.4节]()
> 这本书的4.4节通过作者自己的引擎讲解了一个类UE4 Delegate的实现，如果直接看UE的源码看不懂可以参考这本书的4.4节。

* [UE4-深入委托Delegate实现原理](https://zhuanlan.zhihu.com/p/261717182)
> 对UE4中Delegate的实现进行了一个总结，建议看完上面的简单实现再对照UE的源码来看一看UE4中的实现。

#### 1.4.1.2. Reflection

* [我所理解的 C++ 反射机制](https://blog.csdn.net/K346K346/article/details/51698184)
> 这篇文章提及的反射机制比较通俗易懂，适合来理解反射

* [UE4的对象系统](https://zhuanlan.zhihu.com/p/24319968)
> 这是一个系列文章，共有十三个小章节。作者详细的剖析了UE4的反射系统，初读起来可能比较困难，可以反复多看几遍。

#### 1.4.1.3. Modules

#### 1.4.1.4. Coroutine

#### 1.4.1.5. MultiThreads

* [《Exploring in UE4》多线程机制详解[原理分析]](https://zhuanlan.zhihu.com/p/38881269)

#### 1.4.1.6. Serialization

* [Ue4_序列化浅析](https://blog.csdn.net/mohuak/article/details/83027211)

### 1.4.2. Engine Architecture

## 1.5. Rendering

Wait to add.

## 1.6. Project & Courses

### 1.6.1. Complete Project

* [Unreal Engine 4 Mastery：Create Multiplayer Games with C++](https://www.bilibili.com/video/BV1pb41177pn)

> The course make a third-person shooter game with c++ in Unreal. If you are familar with c++, you could learn a lot of gameplay details of TPS.

* [虚幻引擎4游戏开发：使用蓝图制作大逃杀游戏](https://www.udemy.com/course/ue4blueprintbattleroyalecn/learn/lecture/22825523#overview)

> The course make a PUBG-like third-person shooter game with detailed guide using blueprint. __Before you entroll the course, it is encouraged to have some knowledage about blueprint. (To see [Blueprint Visual Scripting](#blueprint-visual-scripting) section)__

* [Ascent Combat Framework (ACF) - C++ Action RPG Creator](https://www.unrealengine.com/marketplace/zh-CN/product/ascent-combat-framework-c-action-rpg-creator)
> Ascent Combat Framework (ACF) is a multi-modules C++ Plugin for Unreal Engine 4 that provides an extendable and easy to use framework to build your __Action RPG games__ in a very short amount of time. It features everything you need to design and create a state-of-the-art fluid Ranged and/or Melee Combat System and supports networking.
It is excellent work to help beginner to learn AAA game devoplement.

### 1.6.2. Gameplay

* [Weapon System (blueprint)](https://www.unrealengine.com/marketplace/zh-CN/product/weapon-system)
> The Weapon System includes various firing modes, predictive recoil and bullet spread. It supports weapons sounds, sfx, and other advanced features. The Weapon System is fully replicated.


### 1.6.3. Character,Camera,Control (3C)

* [Advanced Third Person Camera (C++)
](https://www.unrealengine.com/marketplace/zh-CN/product/advanced-third-person-camera)

> Advanced 3rd Person camera is a very flexible, powerful and scalable system that allows you to conveniently create and manage various camera modes with unique behavior and many parameters for configuring or creating custom scripts with logic for each camera mode. Also, the plugin has the functionality of automatic switching the camera modes by using special triggers on certain locations.

* [TPS - FPS Character System (blueprint)](https://www.unrealengine.com/marketplace/zh-CN/product/tps-fps-character-system)
> Powerful weapon system, various character movements abilities with cover system and __third / first person player camera__.

* [Advanced Locomotion System V4 (blueprint)](https://www.unrealengine.com/marketplace/zh-CN/product/advanced-locomotion-system-v1)

An advanced bipedal locomotion and layering system focusing on high quality character animation with responsive movement. Built to be flexible, extendable, and to provide a solid starting point for new projects. Currently Singleplayer only. __If you want to learn animation systems, it is highly recommended to study this project carefully__

* [FPS Animation (blueprint)](https://unrealengine.com/marketplace/zh-CN/product/first-person-shooter-animation-blueprint#:~:text=This%20is%20a%20fully%20featured%20First%20Person%20Shooter,can%20be%20easily%20added%20to%20your%20existing%20character.)
> A full First Person Shooter animation blueprint and character controller.

### 1.6.4. User Interface (UI)

* [Competitive Shooter HUD (blueprint)](https://www.unrealengine.com/marketplace/zh-CN/product/competitive-shooter-hud)

> Competitive Shooter HUD is a gameplay HUD UI pack and consists of a wide range of effective HUD features typical for first person shooters. In addition to a number of effects such as achievements, medals, damage feedback, damage indicator, etc., it also offers the shooter typical health and armor bars, weapon bars, action bars and team kill counter, timer, a sophisticated crosshair system, intermediate points count and much more.

### 1.6.5. Resources

wait to add.

## 1.7. Wonderful Reference

* [UE4 Guidebook](https://unreal.gg-labs.com/wiki-archives/macros-and-data-types/delegates-in-ue4-raw-c++-and-bp-exposed)

> This guide aims to be a new community resource for Unreal Engine 4.

* [Unreal Engine Community Wiki](https://www.ue4community.wiki/)

> Community-driven resource working together to create educational content around the Unreal game engine

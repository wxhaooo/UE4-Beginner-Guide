# UE4 新手入门指南
<!-- TOC -->

- [UE4 新手入门指南](#ue4-新手入门指南)
  - [阅读指南](#阅读指南)
    - [Quick Start](#quick-start)
    - [Slow Start](#slow-start)
    - [Go Deep](#go-deep)
  - [Foundamentation](#foundamentation)
    - [Blueprint Visual Scripting](#blueprint-visual-scripting)
    - [Coding Standard](#coding-standard)
    - [Project Name Standard](#project-name-standard)
  - [Modules](#modules)
    - [Animation System](#animation-system)
      - [Overview of Animation System](#overview-of-animation-system)
      - [Animation With C++](#animation-with-c)
      - [Animation Misc](#animation-misc)
      - [Dive in Animation System](#dive-in-animation-system)
    - [Water](#water)
    - [Rendering](#rendering)
      - [Pipeline](#pipeline)
      - [RDG](#rdg)
    - [Gameplay](#gameplay)
  - [Engine Mechanism](#engine-mechanism)
    - [Extensions to C++](#extensions-to-c)
      - [Delegate](#delegate)
        - [Use Delegate](#use-delegate)
        - [Why use Delegate?](#why-use-delegate)
        - [Delegate Details](#delegate-details)
      - [Reflection](#reflection)
      - [Modules](#modules-1)
      - [Coroutine](#coroutine)
      - [MultiThreads](#multithreads)
      - [Serialization](#serialization)
  - [Project \& Courses](#project--courses)
    - [Complete Project](#complete-project)
    - [Gameplay](#gameplay-1)
    - [Character,Camera,Control (3C)](#charactercameracontrol-3c)
    - [User Interface (UI)](#user-interface-ui)
    - [Resources](#resources)
  - [Wonderful Reference](#wonderful-reference)

<!-- /TOC -->

## 阅读指南

### Quick Start

__这一节适用于需要快速上手UE4并投入到开发中，适用于时间比较紧迫，有一定引擎使用经验和编程经验的同学。__

__建议的路径是首先确认开发手段，是蓝图、C++还是Lua，熟悉后即可以参看项目相关部分__。

如果是蓝图，跳转到[Blueprint Visual Scripting](#blueprint-visual-scripting)熟悉官方文档。

如果是C++，跳转到[Coding Standard](#coding-standard)首先熟悉UE4中使用的代码规范，然后可以一边看项目相关代码，一边参考[Programming with C++ | Unreal Engine Documentation](https://docs.unrealengine.com/4.27/en-US/ProgrammingAndScripting/ProgrammingWithCPP/)官方文档上手工作。

如果是Lua，路径暂缺，需要相关同学补充。

### Slow Start

__这一节适合有一定编程基础，但是游戏开发方面基础为0的同学。__

__建议的路径是如果是后续开发仅使用蓝图的同学，走蓝图路线即可。如果是后续使用C++较多的同学，直接走C++路线即可。__

__在对C++和蓝图均熟悉以后，建议在进入Lua路线。__

 **蓝图路线** ：首先跳转到[Blueprint Visual Scripting](#blueprint-visual-scripting)熟悉官方文档。其次建议学习蓝图项目 [虚幻引擎4游戏开发：使用蓝图制作大逃杀游戏](https://www.udemy.com/course/ue4blueprintbattleroyalecn/learn/lecture/22825523#overview)。这个课程是一个纯蓝图课程，用蓝图完整实现了一个大逃杀like游戏。通过这个项目基本可以熟悉蓝图的使用。
 
 **C++路线**：跳转到[Coding Standard](#coding-standard)首先熟悉UE4中使用的代码规范。接着建议学习C++项目[Unreal Engine 4 Mastery：Create Multiplayer Games with C++](https://www.bilibili.com/video/BV1pb41177pn)。这个课程绝大多数主体用C++进行开发，少量使用蓝图辅助开发。通过这个课程，基本可以掌握UE4 C++开发的基本知识。同时建议看不懂的地方多参考[Programming with C++ | Unreal Engine Documentation](https://docs.unrealengine.com/4.27/en-US/ProgrammingAndScripting/ProgrammingWithCPP/)。
 
 **Lua路线**：C++和蓝图都熟悉了，只要了解了Lua语法，上手就是顺其自然而然的事情了~。
 
### Go Deep
 
__在完成上面的简单入门/快速入门后，就可以上手项目在项目中学习了，文章中整理了少量特化领域的知识和问题以供参考，也希望负责对应部分的同学可以把自己的经验有时间的时候补充到对应部分:)__
 
除此之外，UE的C++的有很多值得研究的底层公共课题： 比如**delegate的原理、反射实现机制、模块化、多线程、蓝图虚拟机**等等。 如果有同学对这方面感兴趣可以在参考本文档中对应部分。目前这部分还不完善，希望后面有时间的同学可以一起渐渐完善这部分:)。

## Foundamentation

### Blueprint Visual Scripting

* [Blueprint Visual Scripting](https://docs.unrealengine.com/en-US/ProgrammingAndScripting/Blueprints/index.html)

> The official document contains the concept and usage of blueprints, If you want to understand the blueprint, this document is the best choice for beginner.

### Coding Standard

* [Coding Standard](https://docs.unrealengine.com/en-US/ProductionPipelines/DevelopmentSetup/CodingStandard/index.html)

> Standards and conventions used by Epic Games in the Unreal Engine 4 codebase.

### Project Name Standard

* [UE4 Style Guide](https://github.com/Allar/ue4-style-guide)

> UE4 C++ and engineering resource naming specification

__`Be sure to read these two documents before writing C++ code in UE4, this will make your code look more professional and more suitable for multi-person cooperation project`__

## Modules

### Animation System

#### Overview of Animation System

* [Animation System Overview](https://docs.unrealengine.com/en-US/AnimatingObjects/SkeletalMeshAnimation/Overview/index.html)
> Official documents containing the basic concepts of the animation system and all of subsystem about animation.

* [A deep look into animation framework in ue4](https://arrowinmyknee.com/2019/09/11/a-deep-look-into-animation-framework-in-ue4/)
> A overview of detailed implementation of animation system with c++ in UE4.

* [Link1: Mapping Out The UE4 Animation Architecture Flow
](https://gist.github.com/ikrima/a900a50c1d4b7293d44b)

* [Link2: Mapping Out The UE4 Animation Architecture Flow](https://bebylon.dev/ue4guide/gameplay-programming/animation-subsystem/animation-subsystem/)

> A framework for animation subsystem in ue4

* [UAnimNotify & UAnimNotifyState](http://jollymonsterstudio.com/2018/12/10/unreal-engine-c-fundamentals-uanimnotify-uanimnotifystate/)

#### Animation With C++

* [How can I play animations strictly from C++?](https://answers.unrealengine.com/questions/292345/how-can-i-play-animations-strictly-from-c.html)
> Unreal has two programming methods: Blueprint and C++. It is very important to choose the correct method to meet the needs. It is especially important in animation systems. This question discusses which parts of the animation are more appropriate to use C++ and which are more appropriate to use visual blueprints.

#### Animation Misc

> Unreal中的IK节点

* [IK节点详解](https://zhuanlan.zhihu.com/p/41425611)
> 包含了Unreal常用的two bone IK & FABRIK & Hand IK Retargeting的详解和原理

* [动画融合](https://blog.uwa4d.com/archives/Study_Unreal4_Animation_2.html)
> 包含了UE中常用的各种动画融合节点的使用方法，最重要的是有动画蒙太奇（animation montage）的介绍和使用，__最重要的是介绍了Layered Animation与Animation Composite并且区分了两者的不同__。

#### Dive in Animation System

* [Skinned Mesh原理解析和一个最简单的实现示例](https://happyfire.blog.csdn.net/article/details/3105872)
> 实现了一个简易的Skinned Mesh，可以用于了解骨骼动画原理

* [图解动画系统源码](https://zhuanlan.zhihu.com/p/446851284)
> 详细梳理了UE中动画系统是如何运行的

* [UE4动画系统更新源码分析](https://zhuanlan.zhihu.com/p/405437842)
> 详解了UE4动画系统的更新部分是如何运作的

### Water

> [Water System Depp Dive](https://www.bilibili.com/video/BV1zb4y1k7jR/?spm_id_from=333.1007.top_right_bar_window_history.content.click&vd_source=d9c3a93d5a5e702ce7969bbab5c01c0f)

**这个视频主要介绍了如何使用水系统制作一个场景以及对默认的水材质做了一个简单的介绍。**

### Rendering

#### Pipeline

[实时渲染深入探究](https://www.bilibili.com/video/BV1h54y1J7SR/?spm_id_from=333.1007.top_right_bar_window_custom_collection.content.click&vd_source=d9c3a93d5a5e702ce7969bbab5c01c0f)
> 官方对渲染体系的一个系统介绍，虽然标题是深入探究，但非常适合有不算太多渲染经验的同学入门UE渲染体系。

[剖析虚幻渲染体系](https://www.cnblogs.com/timlly/p/13512787.html#%E5%86%85%E5%AE%B9%E7%BA%B2%E7%9B%AE)
> 这位博主详细剖析了UE渲染部分的方方面面，非常适合对着源码来看。每篇文章都比较长，但是干货很多，耐心看完一定会很有收获:)

[Unreal Engine 4 Rendering](https://medium.com/@lordned/unreal-engine-4-rendering-overview-part-1-c47f2da65346)
> 一个剖析UE渲染管线的系列文章，包含shader和顶点工厂（Vertex Factories），Drawing Policies，Shader架构以及增加shading model的教程。**这个系列相对比较旧，Draw Policies在UE4.22后已经被废弃，参考的时候注意一下。**

[UE4网格渲染管线重构](https://www.bilibili.com/video/BV1gJ411J7j1/?spm_id_from=333.1007.top_right_bar_window_custom_collection.content.click&vd_source=d9c3a93d5a5e702ce7969bbab5c01c0f)
> UE渲染管线重构的官方介绍，适合深入学习渲染管线的时候参照。


#### RDG

[Rendering Dependency Graph解析](https://www.bilibili.com/video/BV18K411Z7Jg/?spm_id_from=333.1007.top_right_bar_window_custom_collection.content.click&vd_source=d9c3a93d5a5e702ce7969bbab5c01c0f)
> 官方对RDG流程的分析，适合对RDG有一定使用经验后去进一步的学习RDG的实现。

### Gameplay

[游戏中QTE和断肢是如何实现的？](https://www.bilibili.com/video/BV1jm4y1k7KK/?spm_id_from=333.999.0.0&vd_source=d9c3a93d5a5e702ce7969bbab5c01c0f)
> 对游戏中QTE实现的简单介绍，可以学到制作思路，细节还需要琢磨下。

## Engine Mechanism

### Extensions to C++

#### Delegate

##### Use Delegate

* [Delegates in UE4, Raw C++, and BP Exposed](https://unreal.gg-labs.com/wiki-archives/macros-and-data-types/delegates-in-ue4-raw-c++-and-bp-exposed)
> [The official documents about delegates](https://docs.unrealengine.com/en-US/ProgrammingAndScripting/ProgrammingWithCPP/UnrealArchitecture/Delegates/index.html) are vague and difficult to understand. This article explains the use of delegates very well.

##### Why use Delegate?

> __`C++ don't have event system out of the box, at most you got normal function calls which you know that will be called on specific occasion. The weakness of this set up is fact that you can't detect events in code outside of the object it self, or else called of event sends it also somewhere else, external object can't get call then other object is destroyed for example. Thats why delegates was made which work like variable and other object (or even object less static function) can register it to the event to receive the call when it occurs.` [Ref: Seeking a purpose of Delegates!](https://answers.unrealengine.com/questions/783913/view.html)__

> C++本身不具有事件响应功能。只能在发生事件时主动调用需要侦听该事件的对象的相应函数。这要求事件发出者（被观察者）拥有观察者的信息以便调用响应事件。但事件发出者拥有观察者逻辑上不合理。所以使用观察者模式来分离。delegate就是观察者模式的一种实现。由被观察者约定观察者响应事件的接口，需要侦听该事件的观察者通过delegate在自己的类中侦听时间。当事件发生时，被观察者广播该事件给所有侦听者。（用法见[Use Delegate](#use-delegate)，原理见下面几个推荐。）

* [什么是“观察者模式”？](https://zhuanlan.zhihu.com/p/158537313)
> Delegate是观察者模式的一个实现，了解delegate，也有必要看看观察者模式。 

##### Delegate Details

* [游戏引擎原理与实践：卷一 基础框架，4.4节]()
> 这本书的4.4节通过作者自己的引擎讲解了一个类UE4 Delegate的实现，如果直接看UE的源码看不懂可以参考这本书的4.4节。

* [UE4-深入委托Delegate实现原理](https://zhuanlan.zhihu.com/p/261717182)
> 对UE4中Delegate的实现进行了一个总结，建议看完上面的简单实现再对照UE的源码来看一看UE4中的实现。

#### Reflection

* [我所理解的 C++ 反射机制](https://blog.csdn.net/K346K346/article/details/51698184)
> 这篇文章提及的反射机制比较通俗易懂，适合来理解反射

* [UE4的对象系统](https://zhuanlan.zhihu.com/p/24319968)
> 这是一个系列文章，共有十三个小章节。作者详细的剖析了UE4的反射系统，初读起来可能比较困难，可以反复多看几遍。

#### Modules

#### Coroutine

#### MultiThreads

* [《Exploring in UE4》多线程机制详解[原理分析]](https://zhuanlan.zhihu.com/p/38881269)

#### Serialization

* [Ue4_序列化浅析](https://blog.csdn.net/mohuak/article/details/83027211)

## Project & Courses

### Complete Project

* [Unreal Engine 4 Mastery：Create Multiplayer Games with C++](https://www.bilibili.com/video/BV1pb41177pn)

> The course make a third-person shooter game with c++ in Unreal. If you are familar with c++, you could learn a lot of gameplay details of TPS.

* [虚幻引擎4游戏开发：使用蓝图制作大逃杀游戏](https://www.udemy.com/course/ue4blueprintbattleroyalecn/learn/lecture/22825523#overview)

> The course make a PUBG-like third-person shooter game with detailed guide using blueprint. __Before you entroll the course, it is encouraged to have some knowledage about blueprint. (To see [Blueprint Visual Scripting](#blueprint-visual-scripting) section)__

* [Ascent Combat Framework (ACF) - C++ Action RPG Creator](https://www.unrealengine.com/marketplace/zh-CN/product/ascent-combat-framework-c-action-rpg-creator)
> Ascent Combat Framework (ACF) is a multi-modules C++ Plugin for Unreal Engine 4 that provides an extendable and easy to use framework to build your __Action RPG games__ in a very short amount of time. It features everything you need to design and create a state-of-the-art fluid Ranged and/or Melee Combat System and supports networking.
It is excellent work to help beginner to learn AAA game devoplement.

### Gameplay

* [Weapon System (blueprint)](https://www.unrealengine.com/marketplace/zh-CN/product/weapon-system)
> The Weapon System includes various firing modes, predictive recoil and bullet spread. It supports weapons sounds, sfx, and other advanced features. The Weapon System is fully replicated.


### Character,Camera,Control (3C)

* [Advanced Third Person Camera (C++)
](https://www.unrealengine.com/marketplace/zh-CN/product/advanced-third-person-camera)

> Advanced 3rd Person camera is a very flexible, powerful and scalable system that allows you to conveniently create and manage various camera modes with unique behavior and many parameters for configuring or creating custom scripts with logic for each camera mode. Also, the plugin has the functionality of automatic switching the camera modes by using special triggers on certain locations.

* [TPS - FPS Character System (blueprint)](https://www.unrealengine.com/marketplace/zh-CN/product/tps-fps-character-system)
> Powerful weapon system, various character movements abilities with cover system and __third / first person player camera__.

* [Advanced Locomotion System V4 (blueprint)](https://www.unrealengine.com/marketplace/zh-CN/product/advanced-locomotion-system-v1)

An advanced bipedal locomotion and layering system focusing on high quality character animation with responsive movement. Built to be flexible, extendable, and to provide a solid starting point for new projects. Currently Singleplayer only. __If you want to learn animation systems, it is highly recommended to study this project carefully__

* [FPS Animation (blueprint)](https://unrealengine.com/marketplace/zh-CN/product/first-person-shooter-animation-blueprint#:~:text=This%20is%20a%20fully%20featured%20First%20Person%20Shooter,can%20be%20easily%20added%20to%20your%20existing%20character.)
> A full First Person Shooter animation blueprint and character controller.

### User Interface (UI)

* [Competitive Shooter HUD (blueprint)](https://www.unrealengine.com/marketplace/zh-CN/product/competitive-shooter-hud)

> Competitive Shooter HUD is a gameplay HUD UI pack and consists of a wide range of effective HUD features typical for first person shooters. In addition to a number of effects such as achievements, medals, damage feedback, damage indicator, etc., it also offers the shooter typical health and armor bars, weapon bars, action bars and team kill counter, timer, a sophisticated crosshair system, intermediate points count and much more.

### Resources

wait to add.

## Wonderful Reference

* [UE4 Guidebook](https://unreal.gg-labs.com/wiki-archives/macros-and-data-types/delegates-in-ue4-raw-c++-and-bp-exposed)

> This guide aims to be a new community resource for Unreal Engine 4.

* [Unreal Engine Community Wiki](https://www.ue4community.wiki/)

> Community-driven resource working together to create educational content around the Unreal game engine

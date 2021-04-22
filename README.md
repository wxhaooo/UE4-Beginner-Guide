# UE4 Beginner Guide
<!-- TOC -->

- [UE4 Beginner Guide](#ue4-beginner-guide)
  - [Foundamentation](#foundamentation)
    - [Blueprint Visual Scripting](#blueprint-visual-scripting)
    - [Coding Standard](#coding-standard)
    - [Project Name Standard](#project-name-standard)
  - [Gameplay](#gameplay)
    - [Animation System](#animation-system)
      - [Overview of Animation System](#overview-of-animation-system)
      - [Animation With C++](#animation-with-c)
      - [Animation Misc](#animation-misc)
    - [HUD](#hud)
    - [AI](#ai)
  - [Engine Mechanism](#engine-mechanism)
    - [MultiThreads](#multithreads)
    - [Delegate](#delegate)
    - [Serialization](#serialization)
    - [Reflection](#reflection)
  - [Rendering](#rendering)
  - [Project & Courses](#project--courses)
    - [Complete Project](#complete-project)
    - [Gameplay](#gameplay-1)
    - [Character,Camera,Control (3C)](#charactercameracontrol-3c)
    - [User Interface (UI)](#user-interface-ui)
    - [Resources](#resources)
  - [Wonderful Reference](#wonderful-reference)

<!-- /TOC -->

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

## Gameplay

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


### HUD

### AI

wait to add.

## Engine Mechanism

### MultiThreads

* [《Exploring in UE4》多线程机制详解[原理分析]](https://zhuanlan.zhihu.com/p/38881269)

### Delegate

* [Delegates in UE4, Raw C++, and BP Exposed](https://unreal.gg-labs.com/wiki-archives/macros-and-data-types/delegates-in-ue4-raw-c++-and-bp-exposed)
  
> [The official documents about delegates](https://docs.unrealengine.com/en-US/ProgrammingAndScripting/ProgrammingWithCPP/UnrealArchitecture/Delegates/index.html) are vague and difficult to understand. This article explains the use of delegates very well.

__`C++ don't have event system out of the box, at most you got normal function calls which you know that will be called on specific occasion. The weakness of this set up is fact that you can't detect events in code outside of the object it self, or else called of event sends it also somewhere else, external object can't get call then other object is destroyed for example. Thats why delegates was made which work like variable and other object (or even object less static function) can register it to the event to receive the call when it occurs.` [Ref: Seeking a purpose of Delegates!](https://answers.unrealengine.com/questions/783913/view.html)__

* [什么是“观察者模式”？](https://zhuanlan.zhihu.com/p/158537313)
> Delegate是观察者模式的一个实现，了解delegate，也有必要看看观察者模式。 

### Serialization

* [Ue4_序列化浅析](https://blog.csdn.net/mohuak/article/details/83027211)

### Reflection

* [我所理解的 C++ 反射机制](https://blog.csdn.net/K346K346/article/details/51698184)
> 这篇文章提及的反射机制比较通俗易懂，适合来理解反射


## Rendering

Wait to add.

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
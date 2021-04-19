# UE4 Beginner Resource Guide
<!-- TOC -->

- [UE4 Beginner Resource Guide](#ue4-beginner-resource-guide)
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
  - [Rendering](#rendering)
  - [Project & Courses](#project--courses)
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

## Engine Mechanism

### MultiThreads

[《Exploring in UE4》多线程机制详解[原理分析]](https://zhuanlan.zhihu.com/p/38881269)

### Delegate

* [Delegates in UE4, Raw C++, and BP Exposed](https://unreal.gg-labs.com/wiki-archives/macros-and-data-types/delegates-in-ue4-raw-c++-and-bp-exposed)
  
> [The official documents about delegates](https://docs.unrealengine.com/en-US/ProgrammingAndScripting/ProgrammingWithCPP/UnrealArchitecture/Delegates/index.html) are vague and difficult to understand. This article explains the use of delegates very well.


## Rendering

## Project & Courses

[虚幻引擎4游戏开发：使用蓝图制作大逃杀游戏](https://www.udemy.com/course/ue4blueprintbattleroyalecn/learn/lecture/22825523#overview)

> The course make a PUBG-like third-person shooter game with detailed guide using blueprint. __Before you entroll the course, it is encouraged to have some knowledage about blueprint. (To see `Blueprint Visual Scripting` section)__ 

## Wonderful Reference

* [UE4 Guidebook](https://unreal.gg-labs.com/wiki-archives/macros-and-data-types/delegates-in-ue4-raw-c++-and-bp-exposed)

> This guide aims to be a new community resource for Unreal Engine 4.

* [Unreal Engine Community Wiki](https://www.ue4community.wiki/)

> Community-driven resource working together to create educational content around the Unreal game engine
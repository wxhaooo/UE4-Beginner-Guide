[TOC]

# Water System Deep Dive笔记

[Water System Depp Dive视频链接地址](https://www.bilibili.com/video/BV1zb4y1k7jR/?spm_id_from=333.1007.top_right_bar_window_history.content.click&vd_source=d9c3a93d5a5e702ce7969bbab5c01c0f)

**这个视频主要介绍了如何使用水系统制作一个场景以及对默认的水材质做了一个简单的介绍。**


## 漂浮系统

可以结合Niagra来制作漂浮在海浪上的物体。

## 水系统的使用步骤

1. 制作自己需要的水材质，官方默认的水材质会更卡通一些

## 水系统的限制

* 地形最大为4K，暂时不适合开放大世界，适合用于某个Level中
> LandscapeWaterBrushManager
* 近岸海水如何制作？Lake、Oecan和river的交界处怎么融合？白水怎么制作？
* 水系统依赖于LandscapeWaterBrushManager，或者首先创建地形，然后创建水也会自动创建LandscapeWaterBrushManager
* 水里的船怎么可以和水交互但是不穿模？
* 怎么做渐进的水渲染效果？（可以随着深度渐进的看见水底）
* 天气和昼夜转换怎么做？
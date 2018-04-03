---
title: Flex 布局（一）
date: 2018-03-09 10:06:13
categories:
- Web
- Flex
tags:
- Web
- 前端
- CSS布局
- Flex
---
# 认识 Flex

## 背景

目前主要的前端布局方案主要有三种：

- 传统布局方案（通过浮动、定位等方式实现）
- Flex 布局方案
- Grid 布局方案

传统的布局方案，需要熟练掌握元素的分类及布局特性、浮动原理和定位原理等基础知识，学习成本较大，实现的复杂度也比较高。
Flex 布局方案，真是为了解决传统布局方案的不变，而提出的一种新型布局方案，只需要简单通过对父元素和子元素相关规则配置就能实现效果。
Flex 布局的主要思想是使父元素能够调节子元素的高度、宽度和排布的顺序，从而能够最好地适应可用布局空间（能够适应不同的设备和不同大小的屏幕）。设定为flex布局的元素能够放大子元素使之尽可能填充可用空间，也可以收缩子元素使之不溢出。与传统布局中块状元素按照垂直方向摆放，行内元素按照水平方向摆放相比，Flex 布局是无方向的,传统布局在应对大型复杂的布局时缺乏灵活性，特别是在改变方向、改变大小、伸展、收缩等等方面。
Flex 布局适合小规模的布局方案，而 Grid 布局方案适合大规模的布局方案。
Flex 布局的兼容性：
![支持的浏览器](flex-layout/bg2015071003.jpg "支持的浏览器")
总的来说，Flex 布局方案是未来的首选布局方案。

## 基本概念

采用 Flex 布局的元素，称为 Flex 容器（flex container），简称为“容器”。它的所有子元素自动成为容器成员，称为 Flex 项目（flex item），简称"项目"。
![flex 布局](flex-layout/flex-bg-2018032801.png "flex 布局")
容器中存在两条轴：`主轴`(main axis) 和 `交叉轴`(cross axis)。`主轴` 开始的位置为 `main start`，结束的位置为 `main end`；交叉轴开始的位置为 `cross start` ，结束的位置为 `cross end`。
项目默认沿主轴排列。单个项目占据的主轴空间叫做 `main size`，占据的交叉轴空间叫做 `cross size`。
相关概念：

- **main axis**：Flex 容器的主轴。主要用来配置 Flex 项目。注意，它不一定是水平的，主要取决于 `flex-direction` 属性。
- **main start | main end**：Flex 项目的配置从容器的主轴起点边开始，往主轴终点边结束。
- **main size**：Flex项目的在主轴方向的宽度或高度就是项目的主轴长度，Flex项目的主轴长度属性是width或height属性，由哪一个对着主轴方向决定
- **cross axis**
- **cross start | cross end**
- **cross size**
---
title: "Css重点知识"
date: 2019-09-12T15:09:24+08:00
draft: false
---

# css简介

css就是层叠样式表(英文全称：Cascading Style Sheets)。它可以静态的修饰网页，css不仅可以将样式层叠起来，还可以配合各种脚本语言动态地对网页各元素进行格式化。css的创造在web历史上非常重要。

## css的历史


1990年，李爵士发明了Web。1994年，Web真正走出实验室。从HTML被发明开始，样式就以各种形式存在。不同的浏览器结合它们各自的样式语言为用户提供页面效果的控制。最初的HTML只包含很少的显示属性。随着HTML的成长，为了满足页面设计者的要求，HTML添加了很多显示功能。但是随着这些功能的增加，HTML变的越来越杂乱，而且HTML页面也越来越臃肿。于是CSS便诞生了。他是由李爵士的同时赖先生（Hakon Wium Lie）提出的。1996年发表了css1，到目前为止已经发展到了css3。之后的版本的是分模块升级的。

## css丰富的样式

CSS现在的功能非常强大，甚至可以制作动画，一个网页有很多元素，要有HTML、CSS等，然后经过浏览器渲染，才能展现出来我都可以认可的网页，所以CSS有着丰富的样式，这样才能满足我们用户的视觉需求。

## 浏览器渲染原理


1. 根据HTML构建HTML树
2. 根据css构建css树
3. 将两棵树合并成一颗渲染树
4. layout布局（文档流，盒摸型，计算大小）
5. paint绘制（把边框颜色，背景，阴影画出来）
6. Composite合成（根据层叠关系展示画面）

## css动画（例子:制作一颗小红心)

有两种方法:

1. 用transform,hover制作一颗小红心

[transform示例](http://jsbin.com/jazabopaja/edit?output)

2. 用animation制作一颗小红心

[animation示例](http://js.jirengu.com/yosagirizi/1/edit?output)

### 更新样式，一般用js更新样式

有三种更新方式：

* 第一种（全走）

div.remove()，过程4，5，6都要走一遍

* 第二种，跳过layout

改变背景颜色

* 第三种，只需要composite

改变transform，只需改变composite
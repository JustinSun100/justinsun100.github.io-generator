---
title: "HTML重点标签"
date: 2019-08-31T22:15:32+08:00
draft: false
---

# HTML 常用标签

## 几个很常用的标签

这里有几个常见的标签给大家介绍一下：

**a/img/iframe/table**

---

## a 标签

```html
<a href="http//:google.com" target="_blank"></a>
```

### a 标签的作用是：

1. 跳转到一个外部页面；
2. 跳转到内部锚点（锚点就是跳转到具有 id 属性的标签位置，在 id 前加#即可）；
3. 跳转到邮箱或电话；

### a 标签的属性：

1. href:超链接，链接到一个网页。
2. target：意思是在那个在哪一个窗口打开超链接，有 4 个值；

- \_blank：在新的页面打开
- \_self：在当前页面打开
- \_top：在顶层页面打开
- \_parent：在父级页面打开

3. download:不是打开网页，而是下载网页
4. rel=noopener:阻止将引用着信息传递给新选项卡，可以防止网站进行跨站点的恶意攻击，提高安全性

_注意：如果想要点击 a 标签，网页什么也不做只是刷新一次，只有将 href 属性设置为 js 伪协议_

## iframe 标签：

iframe 标签是一个内联框架元素，他能将另一个 HTML 页面嵌入到当前页面中

![iframe例图](/images/4-1.PNG)

这就是在网页中嵌套了一个 iframe，红色区域就是一个 iframe 窗口

## table 标签

结构：

```html
<table>
  <thead></thead>
  <tbody></tbody>
  <tfoot></tfoot>
</table>
```

三个标签与顺序无关，总是 thead 的内容在上，tfoot 内容在下。

相关的样式：

- table-layout:行宽
- border-spacing：边框之间的距离
- border-collapse：边框合并

_table 的默认样式是有边框距离的，所以很丑_

## img 标签

### 作用：

发出一个 get 请求，展示一张图片

**图片不能同时设置宽和高！！！（会使图片变形）**

### 如何让图片变成响应式的，加上一句话即可：

```html
<style>
  img {
    max-width: 100%;
  }
</style>
<img src="图片地址" alt="图片打不开的描述" />
```

这几个标签是 HTML 中很常见的标签用到的情况非常多，有很多容易忽略的地方，大家一起努力！下次我们来学习 css 常见的问题。

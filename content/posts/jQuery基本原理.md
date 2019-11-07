---
title: "JQuery基本原理"
date: 2019-11-07T13:27:06+08:00
draft: false
---

# jQuery

jQuery 毫无疑问是 JS 历史上最经典的 js 库，直至今日，很多网站依然在使用 jQuery 它的许多思想值得我们开发者学习，但是想要掌握它也并不容易，经典的思想有哪些呢？

## 一、jQuery 如何获取元素

要知道 jQuery 是一个封装起来的库，简写就是\$()，获取想要操作的元素，通过选择表达式

例如：

```js
$("#test"); //获取id为test的元素
$("div.demo"); //获取类名为class的div元素
$("tr:odd"); //选择表格的奇数行（jQuery特有的选择式）
$("div:gt(2)"); // 选择所有的div元素，除了前三个（jQuery特有的选择式）
```

## 二、jQuery 的链式操作是怎么样的

jQuery 设计思想之一，就是最终选中网页元素以后，以链条的形式写出来并操作，原因是：

1.  jQuery 是一个特殊的函数
2.  jQuery 的返回值是一个对象

```js
$("div")
  .find("p")
  .eq(2)
  .html("Hello"); //由于返回值是一个对象所以就可以在对象上继续操作
```

## 三、jQuery 如何创建元素

创建元素非常的简单只需要将元素直接传如 jQuery 的构造函数中就可以例如：

```js
$("<div>创建一个新的div</div>"); //创建一个新的div
$("ul.first").append.$("<li>new li</li>"); //创建一个新的li插入class为first的ul中
```

## 四、如何移动元素

想把一个元素移动到另一个元素前面有两种方法。

第一种方法是 insertAfter()，把 div 元素移动 p 元素后面。

```js
$("div").insertAfter($("p"));
```

第二种方法是 after()，把 p 元素加到 div 元素前面。

```js
$("p").after($("div"));
```

这两种方法是有区别的,第一种方法返回的是 div 元素，第二种方法返回的是 p 元素

<mark>这种移动又有四种：<mark>

```
.insertAfter()和.after()：在现存元素的外部，从后面插入元素

.insertBefore()和.before()：在现存元素的外部，从前面插入元素

.appendTo()和.append()：在现存元素的内部，从后面插入元素

.prependTo()和.prepend()：在现存元素的内部，从前面插入元素
```

## 五、如何修改元素的属性

jQuery 中修改一个元素的属性用到了**适配器**

适配器就是根据参数数量的变化而执行不同的操作

```js
$("div.x").attr("color", "red"); //修改class为x的div元素的color属性为红色
$("div.x").attr("color"); //获取class为x的div元素的color属性
```

---
title: "JavaScript的诞生"
date: 2019-09-14T21:30:41+08:00
draft: false
---

# JavaScript的历史

## 浏览器的诞生与JavaScript的密切联系

* 1993年，伊利诺伊大学厄巴纳-尚佩恩分校的国家超级计算机应用中心（NCSA）发表了NCSA Mosaic，这是最早流行的图形接口网页浏览器。
* 
![Netscape](/images/NetScape.PNG)
* 1994年，一家名为Mosaic Communications的公司在加州芒廷维尤成立了，并雇用了许多原来的NCSA Mosaic开发者用来开发Mosaic Netscape，该公司的目标是取代NCSA Mosaic成为世界第一的网页浏览器。第一个版本的网页浏览器Mosaic Netscape 0.9于1994年底发布。为避免NCSA的商标所有权问题，该浏览器于同年更名为Netscape Navigator（网景）。
* 网景预见到网络需要变得更动态。公司的创始人马克·安德森认为HTML需要一种胶水语言，让网页设计师和兼职程序员可以很容易地使用它来组装图片和插件之类的组件，且代码可以直接编写在网页标记中。
* 1995年，网景招募了布兰登·艾克，网景决定发明一种与Java搭配使用的辅助脚本语言并且语法上有些类似，这个决策导致排除了采用现有的语言，例如Perl、Python、Tcl或Scheme。为了在其他竞争提案中捍卫JavaScript这个想法，公司需要有一个可以运作的原型。艾克在1995年5月仅花了十天时间就把原型设计出来了（这就是JavaScript的第一版）。
* 最初命名为Mocha，1995年9月在Netscape Navigator 2.0的Beta版中改名为LiveScript，同年12月，Netscape Navigator 2.0 Beta 3中部署时被重命名为JavaScript。

**！所以JavaScript和Java是没有关系的**

## Brendan Eich（布兰登·艾克）

![js之父](/images/js之父.PNG)

* 布兰登·艾克出生于1961年，是JavaScript主要创造者与架构师，曾任Mozilla公司的首席技术官，并曾短暂担任首席执行官。
* 1995年4月，网景公司录用了34岁的系统程序员Brendan Eich，Brendan Eich的主要方向和兴趣是函数式编程，网景公司招聘他的目的，是研究将Scheme语言作为网页脚本语言的可能性。Brendan Eich本人也是这样想的，以为进入新公司后，会主要与Scheme语言打交道。
* 仅仅一个月之后，1995年5月，网景公司做出决策，未来的网页脚本语言必须"看上去与Java足够相似"，但是比Java简单，使得非专业的网页作者也能很快上手。这个决策实际上将Perl、Python、Tcl、Scheme等非面向对象编程的语言都排除在外了。
* 不久后，Brendan Eich被指定为这种"简化版Java语言"的设计师。但是，他对Java一点兴趣也没有。为了应付公司安排的任务，他只用10天时间就把Javascript设计出来了。
* 由于设计时间太短，语言的一些细节考虑得不够严谨，导致后来很长一段时间，Javascript写出来的程序混乱不堪。

### 他的设计思路是这样的：

（1）借鉴C语言的基本语法；

（2）借鉴Java语言的数据类型和内存管理；

（3）借鉴Scheme语言，将函数提升到"第一等公民"（first class）的地位；

（4）借鉴Self语言，使用基于原型（prototype）的继承机制。

## 它的优秀之处并非原创，它的原创之处并不优秀

这句话源自十八世纪英国文学家约翰逊博士，拿来形容JavaScript真是恰如其分，js有很多的问题，比许多编程语言的问题都要多很多。造成这种问题的原因就这么几点：

1. 设计时间太短，因为JavaScript是有布兰登10天设计出来的，很多细节做的不全面也是在所难免的了
2. 没有先例，JavaScript是一门借鉴了函数式语言和面向对象语言的新语言，所以很多问题是没有参考的，只能靠程序员们慢慢发掘。
3. 标准制定太早，由于历史原因JavaScript在设计出来一年的时候就进行了标准化制定，这就是的很多问题在没有得到及时更改的情况下就已经写进了标准。

# Javascript的10个设计缺陷

1.不适合开发大型程序

2.非常小的标准库

3.null和undefined

两者区别很模糊，null一般表示数值的空，undefined表示对象的空

4.全局变量难以控制

5.自动插入行尾分号

JavaScript的定义是会在行尾自动插入分号，这样其实是不利于代码的编写

6.加号运算符

加号有两种用法，一直是将数值相加，另一种是作为连接符使用，这样其实使运算的复杂性提高

7.NaN

NaN是作为一个数值，表示该数值超出了解释器的理解，其又是一个不确定的数值，所以大大增加了解释器的负担

8.数组和对象的区分

9.== 和 ===

两者都表示等于，前者会自动转换类型，这样就会变声一些奇怪的结果，所以推荐一直使用“===”

10.基本类型的包装对象
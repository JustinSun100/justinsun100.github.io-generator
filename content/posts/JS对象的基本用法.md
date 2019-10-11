---
title: "JS对象的基本用法"
date: 2019-10-04T21:49:40+08:00
draft: false
---
    

# 对象：

* 无序的数据集合
* 键值对的集合

## 1.声明对象的两种语法

```js
let obj={'name':frank,'age':18}
```

我们通常用这种方法定义对象

```js
let obj=new Object{'name':frank,'age':18}
```

这是定义对象的标准语句，说明语句是通过Object构造函数定义的


注意键值一定是字符串（并且会自己将其变为字符串），但是如果键值用方括号[]括起来，那么键值就是变量的值

```js
let p1='name';
let obj={p1:frank};                  //键值是'p1'
let obj={[p1]:frank};                //键值是'name'
```

## 2.如何删除对象的属性

```
var obj={'name':'frank','age':18}
```

删除对象的属性，看一下下面两种方法

```
obj.name=undefined      //将name属性设为undefined，name属性存在，删除属性值
delete obj.name         //将name属性删除，删除属性名
```

## 3.如何查看对象的属性

### 查看自身所有属性

```
Object keys(obj);        //打出所有的键值
Object values(obj);      //打出所有的属性值
Object entries(obj);     //以数组形式打出所有的键值对 
```

### 查看自身+共有属性

```
console.dir(obj);
obj.__proto__           //不推荐
```

### 判断一个属性是自身还是共有属性

```
obj.hasOwnProperty('toString')          //false
```

### 查看属性的值：

```
1. obj['name'];     //新人推荐使用
2. obj.name；       //熟练后使用
```

obj[name]是错误的写法，因为[name]是变量。

## 4.如何修改或添加对象的属性

### 直接赋值

```
let obj={name:'frank'}
obj.name='frank'
```

### 批量赋值

```
Object.assign(obj,{age:18'gender:'男'})
```

### 无法通过自身修改或增加共有属性：

```
obj.toString='xxx';         //无法修改原型的toSting
```

*读的时候走原型，写的时候不走原型*

修改原型直接```obj.__proto__.toString='xxx'```,但是实际开发中最好永远不要这么干

用另一种方法：```window.Object.prototype='xxx'```

### 修改原型
```
let obj=Object.create(common);      //表示obj的原型就是common，先创建再修改其属性
```

## 5.'name' in obj和obj.hasOwnProperty('name')的区别

* (1)```'name' in obj```是不会区分某个属性是自身的还是共有的


* (2)```obj.hasOwnProperty('name')```是判断一个对象是否属于自身属性
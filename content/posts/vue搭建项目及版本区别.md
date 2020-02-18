---
title: "Vue搭建项目及版本区别"
date: 2020-02-18T10:40:13+08:00
draft: false
---

# 如何搭建一个 Vue 项目

### 使用 @vue/cli 搭建项目

- 安装@vue/cli

```
yarn global add @vue/cli
```

- 通过<mark>vue --version</mark>命令来验证有没有安装成功

* 创建项目

```
vue create 项目名
yarn serve  //预览服务
```

在创建项目时有一些选项根据自己的需求选择，也可以在[codesandbox](https://codesandbox.io/) 中创建项目,然后将项目下载下来。

### 使用 codesandebox 搭建项目：

1. 进入网址[codesandbox](https://codesandbox.io/) ，这里要注意不能登录，因为登录之后就只能创建 50 个项目，不登陆可以一直创建
2. 点击创建一个 vue 项目
   ![](/images/vue.PNG)
3. 导出项目，这里导出的时压缩文件，解压后就是我们的项目了
   ![](/images/vue-1.PNG)

好了我们已经成功创建好项目了，下面介绍一下版本的区别

# 版本区别

## 完整版 Vue.js

1. 可以直接在 html 和 template 标签中得到视图内容
2. 对于初学者而言更清晰易懂

## 非完整版 Vue.runtime.js

1. 不能直接从 html 或 template 得到视图要用 js 构建视图
2. 代码体积小，大概为完整版的 70%，节省了空间
3. 通过 render 函数将数据渲染到视图中

**注意**：

- template 就是模板可以在完整版将你想要显示的视图写在模板中，然后将数据 替换
- render 在非完整版中将数据渲染到视图中，在非完整版中不能用 template
- 实际上我们可以通过 webpack 实现 html 与 js 之间的转换你，这样我们只需要写 html 就你能实现非完整版的功能

# 单文本组件

Vue 的作者为了让使用者可以更简单的使用 Vue 提供了单文本组件这个功能

组件由三部分组成：

![](/images/vue-2.PNG)

- template 中写视图
- script 中写视图外的东西，例如数据（组件中 data 必须使用函数）
- style 中写 css

然后将组件通过 import 导入，这样我们就可以在 html 上写视图，在 js 文件上通过 render 渲染就可以了

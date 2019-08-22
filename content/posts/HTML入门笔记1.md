---
title: "HTML入门笔记1"
date: 2019-08-22T14:48:02+08:00
draft: false
---

# HTML 入门

## HTML 是谁发明的？

蒂莫西·约翰·伯纳斯-李爵士，英国计算机科学家。他是万维网的发明者，1990 年 12 月 25 日，他成功利用互联网实现了超文本传输协议客户端与服务器的第一次通讯

## HTML 起手应该写什么

一个完整的起手式：

![一个完整的起手式](/images/html起手式.PNG)

```
<!DOCTYPE html>
<html lang="en">
```

开头写的东西，DOCTYPE 就是文档类型的意思，这里的文档类型就是 html。lang 是语言，这里是英文， 如果想改成汉字就将“en”改为“zh-CN”。

    <meta charset="UTF-8" />

文件字符编码为“UTF-8”

    <meta name="viewport" content="width=device-width, initial-scale=1.0" />

禁用缩放，兼容手机。

    <meta http-equiv="X-UA-Compatible" content="ie=edge" />

告诉 IE 使用最新内核。

    <title>Document</title>

title 中为文档的标题。

## 常用的表章节的标签

### h1——h6/section/article/main/aside/p

h1——h6 是标题标签。h1 最大，h6 最小，他们是自动加黑加粗的。

section 是章节标签，main 标签里面放主要内容，aside 标签里面放旁支内容，article 使文章标签，这些标签都是章节标签。

## HTML 的全局属性

### class/contenteditable/hidden/id/style/tabindex/title

1. class 创建一个类名
2. contenteditable 可以让一个标签被编辑
3. hidden 隐藏
4. id 创建一个 id，不要轻易用它（浏览器无法识别 id 的唯一性）
5. style 样式
6. tabindex 按下 tab 时跳转的位置（可交互的内容），赋值为顺序，为 0 时最后访问，为-1 时不访问。
7. title 标题

## 常用的内容标签

### a/strong/em/code/pre

1. a 链接
2. strong 重要
3. em 强调
4. code 代码（里面的内容是等宽的）
5. pre 可以保留你的输入，浏览器将连续空白视为一个空格，用 pre 可以避免这种情况。

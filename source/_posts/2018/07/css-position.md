---
title: 学习CSS布局 之 position定位
tags:
  - 前端
  - css
date: 2018-07-05 15:32:55
---


为了制作更多复杂的布局，我们必须要学习下 __position__ 属性。它有以下这些值：__static__、__relative__、__fixed__、__absolute__，具体可以查看[W3C手册](http://www.w3school.com.cn/cssref/pr_class_position.asp)。

接下来让我来一一介绍这些属性值

static
==

static 是默认值。任意 __position: static;__ 的元素不会被特殊的定位。一个 static 元素表示它不会被"positioned"，一个 position 属性被设置为其他值的元素表示它会被"positioned"。
```html
<style>
    .static {
        position: static;
    }
</style>
<div class='static'>
    文本内容****文本内容****文本内容****文本内容****
</div>
```
页面效果：[查看](/demo/css-position/static.html) 或 <a href="/demo/css-position/static.html" download="css-position-static.html">下载</a> 

relative
==
relative 表现的和 static 一样，除非你添加了一些额外的属性。

在一个相对定位（position属性的值为relative）的元素上设置 top 、 right 、 bottom 和 left 属性会使其偏离其正常位置。其他的元素的位置则不会受该元素的影响发生位置改变来弥补它偏离后剩下的空隙。

```html
<style>
.relative1 {
  position: relative;
}
.relative2 {
  position: relative;
  top: -20px;
  left: 20px;
  background-color: white;
  width: 500px;
}
</style>
<div class="relative1">
    区块1
</div>
<div class="relative2">
    区块2
</div>
```
页面效果：[查看](/demo/css-position/relative.html) 或 <a href="/demo/css-position/relative.html" download="css-position-relative.html">下载</a> 
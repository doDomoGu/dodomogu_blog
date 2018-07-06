---
title: 学习CSS布局 之 position定位
tags:
  - 前端
  - css
date: 2018-07-05 15:32:55
---


为了制作更多复杂的布局，我们必须要学习下 __position__ 属性。它有以下这些值：__static__、__relative__、__fixed__、__absolute__，具体可以查看[__W3C手册__](http://www.w3school.com.cn/cssref/pr_class_position.asp)。

接下来让我来一一介绍这些属性值

<!--more-->
static
==

static 是默认值。任意 __position: static;__ 的元素不会被特殊的定位。一个 static 元素表示它不会被"positioned"，一个 position 属性被设置为其他值的元素表示它会被"positioned"。
```css
.static {
    position: static;
}
```
页面效果：[查看](/demo/css-position/static.html) 或 <a href="/demo/css-position/static.html" download="css-position-static.html">下载</a> 

relative
==

relative 表现的和 static 一样，除非你添加了一些额外的属性。

在一个相对定位（position属性的值为relative）的元素上设置 top 、 right 、 bottom 和 left 属性会使其偏离其正常位置。其他的元素的位置则不会受该元素的影响发生位置改变来弥补它偏离后剩下的空隙。

```css
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
```
页面效果：[查看](/demo/css-position/relative.html) 或 <a href="/demo/css-position/relative.html" download="css-position-relative.html">下载</a> 

fixed
==

一个固定定位（__position__ 属性的值为 __fixed__）元素会相对于视窗来定位，这意味着即便页面滚动，它还是会停留在相同的位置。和 __relative__ 一样， top 、 right 、 bottom 和 left 属性都可以用来调整它的相对位置。

一个固定定位元素 __不会保留__ 它原本在页面应有的空隙（脱离文档流）。

```css
.fixed {
  position: fixed;
  bottom: 0;
  left: 0;
  width: 200px;
  background-color: white;
}
```

页面效果：[查看](/demo/css-position/fixed.html) 或 <a href="/demo/css-position/fixed.html" download="css-position-fixed.html">下载</a> 

absolute
==

absolute 是最棘手的position值。 absolute 与 fixed 的表现类似，但是它不是相对于视窗而是相对于最近的“positioned”祖先元素。如果绝对定位（position属性的值为absolute）的元素没有“positioned”祖先元素，那么它是相对于文档的 body 元素，并且它会随着页面滚动而移动。记住一个“positioned”元素是指 position 值不是 static 的元素。

```css
.relative {
    position: relative;
    width: 600px;
    height: 400px;
    border: 1px solid #333;
    background:#cceeff;
}

.absolute {
    position: absolute;
    top: 120px;
    right: 0;
    width: 200px;
    height: 100px;
    background-color: #f1a7a7;
    border: 1px solid #333;
}
```

页面效果：[查看](/demo/css-position/absolute.html) 或 <a href="/demo/css-position/absolute.html" download="css-position-absolute.html">下载</a> 
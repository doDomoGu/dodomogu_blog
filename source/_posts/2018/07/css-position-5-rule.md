---
title: CSS布局之 position(定位)各属性值的五条叠加法则
date: 2018-07-09 11:17:03
tags:
    - css
---
很多在学习css布局的时候，对为什么这个div在上层，那个div在下层、无论如何设置z-index都无法居上的问题很烦心，使得不敢随意使用层的叠加。但层的叠加效果，在交互设计中却频频出现，所以我们必须驾驭它，弄懂他，要明白和掌握其规律。

首先明确几点在文中所需要用到的概念:

静态定位：position:static（为position属性的默认值），也被称为不是'positioned'的状态。
动态定位：position:除了static的其他状态，relative或absolute或fixed，也被统称为是'positioned'的状态。
祖元素：任意包含该元素的元素。
父元素：直接包含该元素的祖元素。
同辈元素：拥有共同的父元素的元素。

注：这些概念为作者自定义，仅用于本文。

接下来看看这五条法则:

法则一：同辈元素定位方式相同，且无z-index设置时，html靠后者居上。
---
```css
.div1 {
    position: static;
    border: 1px solid #333;
    width:200px;
    height:100px;
    background: #eeffee;
}
.div2 {
    position: static;
    border: 1px solid #333;
    margin-top: -40px;
    margin-left: 40px;
    width:200px;
    height:100px;
    background: #ffeeff;
}
.div3 {
    position: relative;
    border: 1px solid #333;
    width:200px;
    height:100px;
    background: #eeffee;
}
.div4 {
    position: absolute;
    border: 1px solid #333;
    width:200px;
    height:100px;
    margin-top:-40px;
    margin-left:40px;
    background: #ffeeff;
}
.div5 {
    position: absolute;
    border: 1px solid #333;
    width:200px;
    height:100px;
    background: #eeffee;
}
.div6 {
    position: relative;
    border: 1px solid #333;
    width:200px;
    height:100px;
    margin-top:60px;
    margin-left:40px;
    background: #ffeeff;
}
```
页面效果：[查看](/demo/css-position-5-rule/1.html) 或 <a href="/demo/css-position-5-rule/1.html" download="css-position-5-rule-1.html">下载</a> 


法则二：同辈元素同为动态定位时，且有z-index设置时，z-index值大者居上。
---
```css
.div1 {
    position: relative;
    border: 1px solid #333;
    width:200px;
    height:100px;
    background: #eeffee;
    z-index: 100;
}
.div2 {
    position: absolute;
    border: 1px solid #333;
    width:200px;
    height:100px;
    margin-top:-40px;
    margin-left:40px;
    background: #ffeeff;
}
.div3 {
    position: absolute;
    border: 1px solid #333;
    width:200px;
    height:100px;
    background: #eeffee;
    z-index: 100;
}
.div4 {
    position: relative;
    border: 1px solid #333;
    width:200px;
    height:100px;
    margin-top:60px;
    margin-left:40px;
    background: #ffeeff;
}
```

页面效果：[查看](/demo/css-position-5-rule/2.html) 或 <a href="/demo/css-position-5-rule/2.html" download="css-position-5-rule-2.html">下载</a> 

法则三：同辈元素定位方式不同时，动态定位居上。
---
```css
.div1 {
    position: relative;
    border: 1px solid #333;
    width:200px;
    height:100px;
    background: #eeffee;
}
.div2 {
    position: static;
    border: 1px solid #333;
    margin-top: -40px;
    margin-left: 40px;
    width:200px;
    height:100px;
    background: #ffeeff;
}
.div3 {
    position: static;
    border: 1px solid #333;
    width:200px;
    height:100px;
    background: #eeffee;
    z-index: 100;
}
.div4 {
    position: absolute;
    border: 1px solid #333;
    width:200px;
    height:100px;
    margin-top:-40px;
    margin-left:40px;
    background: #ffeeff;
}
```
页面效果：[查看](/demo/css-position-5-rule/3.html) 或 <a href="/demo/css-position-5-rule/3.html" download="css-position-5-rule-3.html">下载</a> 

法则四：非同辈元素，任意一者及其祖元素不具备动态布局时，html靠后者居上。
---
```css
.div1 {
    position: static;
    border: 1px solid #333;
    width: 200px;
    height: 100px;
    margin-left:20px;
    background: #eeffee;
}
.div1-parent {
    position: static;
    border: 1px solid #333;
    width: 240px;
    height: 150px;
    background:#eeeeff;
}
.div2 {
    position: static;
    border: 1px solid #333;
    width:200px;
    height:100px;
    margin-left:20px;
    background: #eeffee;
}
.div2-parent {
    position: static;
    border: 1px solid #333;
    width: 240px;
    height: 150px;
    margin-top:-80px;
    margin-left:80px;
    background:#eeeeff;
}




.div3 {
    position: static;
    border: 1px solid #333;
    width: 200px;
    height: 100px;
    margin-left:20px;
    background: #eeffee;
}
.div3-parent {
    position: static;
    border: 1px solid #333;
    width: 240px;
    height: 150px;
    margin-left:20px;
    background:#eeeeff;
}
.div3-grand {
    position: static;
    border: 1px solid #333;
    width: 280px;
    height: 190px;
    background:#ffeeff;
}
.div4 {
    position: static;
    border: 1px solid #333;
    width:200px;
    height:100px;
    margin-left:20px;
    background: #eeffee;
}
.div4-parent {
    position: static;
    border: 1px solid #333;
    width: 240px;
    height: 150px;
    margin-left:20px;
    background:#eeeeff;
}
.div4-grand {
    position: static;
    border: 1px solid #333;
    width: 280px;
    height: 190px;
    margin-top:-80px;
    margin-left:80px;
    background:#ffeeff;
}
```

页面效果：[查看](/demo/css-position-5-rule/4.html) 或 <a href="/demo/css-position-5-rule/4.html" download="css-position-5-rule-4.html">下载</a> 


法则五：【重要】非同辈元素，任意一者或其祖元素拥有动态定位时，同时各自向上寻找动态定位的祖元素，并分别从中拿出具备最高级别的祖元素（或其本身）进行比较。
---

情况1：子元素的z-index无论多大，父元素大者居上。



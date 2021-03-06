---
title: 【译】前端入门学习HTML&CSS （二）了解HTML
date: 2018-07-13 17:45:31
tags:
    - 教程
    - 前端
    - 文档翻译
categories:
    - 前端入门学习HTML&CSS
---

原地址链接：[https://learn.shayhowe.com/html-css/getting-to-know-html/](https://learn.shayhowe.com/html-css/getting-to-know-html/)


第二课

了解HTML
===
随着我们对HTML和CSS的完整介绍，现在是深入挖掘HTML并考察组成这一语言的不同组件的时候了。

为了开始构建网站，我们需要了解一下不同类型的内容最好对应的用哪些HTML元素去呈现。同样重要的是理解元素如何在网页上显示，以及不同的元素的语义。

想在工作中使用合适的元素还有相当长的路要走，我们想要在这个过程中做出明智的决定。

语义概述
===

那么语义究竟是什么呢？HTML中的语义是通过使用适当的元素在页面上赋予内容的意义和结构的实践。语义代码描述内容在页面上的价值，而不考虑内容的样式或外观。使用语义元素有很多好处，包括使计算机、屏幕阅读器、搜索引擎和其他设备能够充分地阅读和理解网页上的内容。此外，语义化的HTML更易于管理和使用，因为它清楚地展示了每一个内容是关于什么的。

随着新元素的引入，我们将讨论这些元素的实际意义以及它们最能代表的内容类型。在我们这样做之前，让我们看看两个元素——&lt;div>和&lt;span>，它们实际上没有任何语义价值。它们仅用于表示不同的样式。

区分DIV和SPAN
===

区块，或&lt;div>和&lt;span>是HTML元素，它们仅作为带样式的容器。作为通用容器，它们不具有任何重要的含义或语义。段落是语义，即被理解为段落包裹在&lt;p>元素中的内容。&lt;div>和&lt;span>不持有任何这样的含义，只是容器。

>块与内联元素
>---
>大多数元素不是块（block-level）就是内联（inline-level）层级的元素。它们有什么区别呢？
>块级元素开始新的一行，且堆叠在另一行上，并占据任何可用的宽度。块级元素可以嵌套在一起，并且可以包裹内联级别元素。我们通常会看到块级元素用于更大的内容片段，如段落。
>内联元素不会在新的一行上开始。它们处在正常的文档流中，一个接一个地排列着，并且只保留其内容的宽度。内联级别元素可以嵌套在另一个元素中，但是它们不能包裹块级元素。我们通常会看到内联水平元素，有少量的内容，比如几个单词。

然而，在构建网站时，&lt;div>和&lt;span>都是非常有价值的，因为它们使我们有能力将有针对性的样式应用到所包含的内容中。

&lt;div> 是块级别的元素，通常用于标识一大组内容，有助于构建web页面的布局和设计。相对的，&lt;span>是内联级元素，通常用于标识块级元素中较小的文本分组。

我们通常会看到&lt;div>和&lt;span>，它们具有用于样式化的class或id属性。选择CLASS或ID属性值或名称需要小心。我们希望选择一个引用元素内容的值，而不一定是元素的外观。
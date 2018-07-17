---
title: 【译】前端入门学习HTML&CSS （一）
date: 2018-07-13 17:43:53
tags:
    - 前端
categories:
    - 前端入门学习HTML&CSS
---
原地址链接：[https://learn.shayhowe.com/html-css/building-your-first-web-page/](https://learn.shayhowe.com/html-css/building-your-first-web-page/)

第一课

创建你自己的第一个网站
===

你可以想象一下在互联网发明之前。没有网站的存在，你的主要信息来源是书籍、报纸等。这需要你花费大量的精力和阅读量来找寻你想要知道的确切信息。   

如今，你可以打开一个网页浏览器，跳转到你所要选择的搜索引擎，输入你想要搜索的内容。任何你想要的信息就呈现在你的眼前。而且你所想要的搜索结果有可能就在某个人在某处建立的网站上。

在这本书中，我将向您展示如何使用这两种最重要的编程语言——HTML和CSS，来构建你自己的网站。

在我们开始学习如何使用HTML和CSS构建网站之前，了解两种语言之间的差异、每种语言的语法以及一些常见的术语是很重要的。

HTML & CSS 是什么？
===

HTML，超文本标记语言，通过定义内容，例如标题、段落或图像，赋予内容结构和意义。CSS（或被称作为级联样式表）是一种陈述性语言，用来调整内容的外观，例如文字的字体和颜色。

应该保持这两种语言HTML和CSS是彼此独立的。CSS不应该写在HTML文档内部，反之亦然。通常，HTML总是表示内容，CSS则总是表示内容的外观。

通过了解HTML和CSS之间的差异，让我们更深入地研究HTML。

了解常用的HTML术语
===

在刚开始使用HTML时，您可能会遇到一些经常用到的陌生的术语。随着时间的推移，你会越来越熟悉它们，但是你应该一开始就要了解三个常见的HTML术语：元素（Elements）、标签（Tags）和属性（Attributes）。

元素（Elements）
---

元素是定义页面内对象的结构和内容的指示符。一些经常用到的元素包括多级标题（被标识为从&lt;H1>至&lt;H6>元素）和段落（被标识为&lt;p>元素），还有一系列的元素，包括有&lt;a>，&lt;div>，&lt;span>，&lt;strong>，和&lt;em>，及更多。

元素通过使用小于号和大于号（&lt;>）将元素名称包围起来。因此，一个元素看起来如下所示：
```html
<a>
```

标签（Tags）
---

这个在元素周围使用小于号和大于号包围起来的方法创造了被称作为标签的东西。标签最常见的是成对的开始和结束标签。

开始标签表示元素的开始。它包含一个小于符号，后面跟着一个元素的名称，然后用一个大于符号结尾，例如，&lt;div>。

结束标签表示元素的结束。它包括一个小于符号，后面是一个正斜杠和元素的名称，然后用一个大于符号结尾，例如&lt;/div>。

位于开始和结束标签之间的内容是该元素的内容。例如，一个锚链接包含一个开始标签&lt;a>和一个结束标签&lt;/a>。这两个标签之间的内容将是锚链接的内容。

所以，锚标签看起来有点像：

```html
<a>...</a>
```

属性（Attributes）
---
属性是用来提供关于元素的附加信息的特性。最常见的属性包括标识元素的 __id__ 属性；对元素进行分类的 __class__ 属性；指定可嵌入内容源的 __src__ 属性；以及提供链接资源的超链接引用的 __href__ 属性。

属性在开始标签中的元素名称之后定义。通常属性包括属性名称和属性值。这些属性的格式包括属性名称，后面紧跟着等号，然后是用引号括起来的属性值。例如，一个包含 __href__ 属性的&lt;a>元素看起来就像：
```html
<a href="http://shayhowe.com/">Shay Howe</a>
```

常用HTML术语演示
===

<iframe height='265' scrolling='no' title='qyZYrV' src='//codepen.io/doDomoGu/embed/qyZYrV/?height=265&amsp;theme-id=light&amsp;default-tab=html,result&amsp;embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>See the Pen <a href='https://codepen.io/doDomoGu/pen/qyZYrV/'>qyZYrV</a> by Gu (<a href='https://codepen.io/doDomoGu'>@doDomoGu</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

以上代码会将文本 __Shay Howe__ 显示在网页上，且用户点击 __Shay Howe__ 文本后，会跳转到页面 http://shayhowe.com/ 。锚元素以开始标签&lt;a>和结束标签&lt;/a>围绕文本，并且在开始标签中用 __href=&quot;http://shayhowe.com/&quot;__ 声明超链接引用的属性和值。
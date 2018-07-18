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

<iframe height='265' scrolling='no' title='qyZYrV' src='//codepen.io/doDomoGu/embed/qyZYrV/?height=265&amp;theme-id=light&amp;default-tab=html,result&amp;embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>See the Pen <a href='https://codepen.io/doDomoGu/pen/qyZYrV/'>qyZYrV</a> by Gu (<a href='https://codepen.io/doDomoGu'>@doDomoGu</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

以上代码会将文本 __Shay Howe__ 显示在网页上，且用户点击 __Shay Howe__ 文本后，会跳转到页面 http://shayhowe.com/ 。锚元素以开始标签&lt;a>和结束标签&lt;/a>围绕文本，并且在开始标签中用 href=&quot;http://shayhowe.com/&quot; 声明超链接引用的属性和值。

{% qnimg learn-to-html-and-css/lesson-1/html-syntax-outline.png title:图表1：HTML语法草图包含元素、属性和标签 alt:html-syntax-autline %}

现在，你应该知道HTML元素、标签和属性都是些什么了，让我们来看看把它们放进我们的第一个网页里。如果有新的东西，不用担心，我们来一一解读它。

建立HTML文档结构
===

HTML文档是用.html文件扩展名保存的纯文本文档，而不是.txt文件扩展名。要开始编写HTML，首先需要使用一个简单的文本编辑器。遗憾的是，这并不包括微软的Word或Pages，因为它们是富文本编辑器。两个比较流行的用于编写HTML和CSS的纯文本编辑器是 __Dreamweaver__ 和 __Sublime Text__。免费的备选方案还包括Windows的 __Notepad++__ 和Mac的 __TextWrangler__。

所有HTML文档都有一个必需的结构，包括以下声明和元素：&lt;!DOCTYPE html>，&lt;html>，&lt;head>和&lt;body>。

文档类型声明或&lt;!DOCTYPE html>,告知Web浏览器正在使用的HTML版本，并放置在HTML文档的最开始。因为我们将使用最新版本的HTML，我们的文档类型声明直接是&lt;!DOCTYPE html>。在文档类型声明之后，&lt;html>元素表示文档的开始。

在&lt;html>元素内，&lt;head>元素标识文档的头部，包括任何元数据（伴随着整个网页的信息）。在网页上不显示“标题”元素中的内容。相反，它可以包括文档标题（在浏览器窗口中的标题栏上显示）、链接任何外部文件或任何其他有用的元数据。

网页中的所有可见内容放在&lt;body>元素内。一个典型的HTML文档结构是这样的：
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <title>Hello World</title>
  </head>
  <body>
    <h1>Hello World</h1>
    <p>This is a web page.</p>
  </body>
</html>
````
<iframe height='265' scrolling='no' title='rrebGW' src='//codepen.io/doDomoGu/embed/rrebGW/?height=265&amp;theme-id=light&amp;default-tab=html,result&amp;embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>See the Pen <a href='https://codepen.io/doDomoGu/pen/rrebGW/'>rrebGW</a> by Gu (<a href='https://codepen.io/doDomoGu'>@doDomoGu</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

上面的代码显示了从文档类型声明开始的文档，&lt;!DOCTYPE HTML>，后面紧跟着&lt;html>元素。在&lt;html>元素中，出现了&lt;head>和&lt;body>元素。元素&lt;head>元素包括通过&lt;meta charset="utf-8">标签来声明网页的字符编码和通过&lt;title>元素来表示页面标题。&lt;body>元素包括通过&lt;h1>元素表示的主题和通过&lt;p>元素表示的段落。因为主题和段落都嵌套在&lt;body>元素中，所以它们在网页上是可见的。

当元素放置在另一个元素的内部时，通常被也称为嵌套，用缩进该元素的写法来保持文档结构的组织性和可读性是一个好主意。在上面的代码中，&lt;head>和&lt;body>元素都嵌套在&lt;html>元素中，且被缩进了。在新的元素被添加到&lt;head>和&lt;body>元素中时，元素的缩进模式持续地被应用。

自闭合元素
---

在前一个例子中，&lt;meta>元素只有一个标签，没有包含结束标签。不要害怕，这是有意为之的。并非所有元素都由开始和结束标签组成。某些元素只从单个标签中的属性获得它们的内容或行为。&lt;meta>是其中的一个。前面的&lt;meta>元素的内容指定了网页使用的字符集属性和值。其他常见的自闭合标签包括：

|自闭合标签|||
|--|--|--|
|&lt;br>|&lt;embed>|&lt;hr>|
|&lt;img>|&lt;input>|&lt;link>|
|&lt;meta>|&lt;param>|&lt;source>|
|&lt;wbr>|  |  |



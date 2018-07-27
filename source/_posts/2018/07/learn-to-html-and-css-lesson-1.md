---
title: 【译】前端入门学习HTML&CSS （一）创建你自己的第一个网站
date: 2018-07-13 17:43:53
tags:
    - 前端
    - 技术文档
    - 翻译
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

<!--more-->
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


这里概述的由&lt;!DOCTYPE html>文档类型和&lt;html>、&lt;head>和&lt;body>元素组成的结构是很常见的。我们希望保持这种方便的文档结构，因为在创建新的HTML文档时，我们要经常用到。

>
> 代码校验
> ---
>
>无论我们在编写代码时多么小心，我们都不可避免地会犯错误。值得庆幸的是，在编写HTML和CSS时，我们有校验器来检查我们的工作。W3C已经建立了用来扫描HTML和CSS代码错误的校验器。校验我们的代码不仅有助于它正确地跨浏览器运行，而且有助于教我们编写代码的最佳实践。

实践
===

作为网页设计师和前端开发人员，我们有幸参加了许多致力于发展我们技术的大会。我们将要组建我们自己的大会——风格大会，并通过之后的课程为它建立一个网站。让我们开始吧！   
1. 让我们打开文本编辑器，创建一个名为 __index.html__ 的新文件，并将其保存到一个我们不会忘记的位置。我将在我的桌面上创建一个名为"风格-大会"的文件夹，并那个新文件保存到这里面。   
2. 让我们在index.html中，添加文档结构，包括&lt;!DOCTYPE html>文档类型和&lt;html>、&lt;head>和&lt;body>这些元素。

```html
<!DOCTYPE html>
<html lang="en">
  <head>
  </head>
  <body>
  </body>
</html>
```

3. 让我们在&lt;head>元素中，添加&lt;meta>和&lt;title>元素。&lt;meta>元素应该包含适当的字符集属性和值，而&lt;title>元素应该包含页面的标题，既"风格大会"。
```html
<head>
  <meta charset="utf-8">
  <title>Styles Conference</title>
</head>
```

4. 在&lt;body>元素中，让我们添加&lt;h1>和&lt;p>元素。&lt;h1>元素应该包括我们所希望的标题——让我们再次使用"风格-大会"，&lt;p>元素应该包括一个简单的段落来介绍我们的大会。
```html
<body>
  <h1>Styles Conference</h1>
  <p>Every year the brightest web designers and front-end developers descend on Chicago to discuss the latest technologies. Join us this August!</p>
</body>
```

5. 现在是时候看看我们是如何做到的！让我们找到我们的文件 __index.html__(我的文件在我得桌面上的"风格-大会"文件夹里)。双击该文件或将其拖到Web浏览器中，来打开它供我们查看。

{% qnimg learn-to-html-and-css/lesson-1/practice-1.png "title:图表2：建设我们的&quot;风格-大会&quot;网站的第一步" "alt:Our first steps into building our Styles Conference website" %}

让我们转换一下，先把HTML放一下，来看看CSS。记住！HTML定义网页的内容和结构，而CSS定义网页的视觉风格和表现。

了解常用的CSS术语
===

除了HTML术语外，还有一些需要你去熟悉的常见的CSS术语。这些术语包括选择器（__Selectors__）、属性（__Properties__）和值（__Values__）。与HTML术语一样，CSS术语也越来越运用自如。

选择器（Selectors）
---

当元素被添加到网页时，可以使用CSS修改它们的样式。选择器精确地指向HTML中的单个或多个元素，并将样式（例如颜色、大小和位置）应用到它们身上。选择器可以包括不同的限定符组合来选择特定的元素，这取决于我们希望用到的哪种程度。例如，我们可能想要选择一个页面上的每一个段落，或者我们希望只选择页面上的一个特定的段落。   
选择器通常针对属性值，例如ID(id)或类(class)的值，或者针对元素的类型，如&lt;h1>或&lt;p>。   
在CSS中，选择器后面跟着大括号{}，其中包含要应用于所选元素的样式。这里的选择器是针对所有&lt;p>元素的。

```css
p { ... }
```

属性（Properties）
---
一旦选定元素，一个属性决定的样式将应用于该元素。属性名称在一个选择器后面，且在大括号（{}）内，并且后面紧跟这冒号，：。我们有很多属性可以使用，例如背景、颜色、字体大小、高度和宽度，并且经常添加新属性。在下面的代码中，我们定义要应用到所有&lt;p>元素的颜色和字体大小的属性。

```css
p {
  color: ...;
  font-size: ...;
}
```

值（Values）
---
到目前为止，我们已经可以用一个选择器来选择一个元素，并可以通过一个属性来决定我们要修改的哪种样式。现在我们可以用一个值来确定那个属性的行为。值（Values）可以被标识为冒号和分号之间的文本。我们选择所有&lt;p>元素，并将颜色属性的值设置为橙色，字体大小属性的值为16像素。
```css
p {
  color: orange;
  font-size: 16px;
}
```

回顾一下，在CSS中，我们的规则集从选择器开始，紧跟其后的是大括号。在这些括号内是由成对的属性和值组成的声明。每个声明从一个属性开始，后面跟着冒号，然后是属性值，最后是分号。   
缩进括号内成对的属性和值是一种常见的做法。与HTML一样，这些缩进有助于保持代码的组织性和清晰性。


{% qnimg learn-to-html-and-css/lesson-1/css-syntax-outline.png "title:图表3：CSS语法草图包括选择器、属性和值" "alt:CSS syntax outline including a selector, properties, and values" %}

熟识一些CSS的常用术语和语法是一个很好的开始，但是在我们要到达更深层次之前还有许多东西要学。具体来说，我们需要仔细研究选择器是如何在CSS中工作的。

类型选择符（Type Selectors）
---
类型选择器以元素类型为目标元素。例如，如果我们希望针对所有的分隔元素（&lt;div>），我们将使用div的类型选择器。下面的代码显示了分隔元素的类型选择器以及它所选择的相应HTML。   
CSS
```css
div { ... }
```
              
HTML              
```html
<div>...</div>          
<div>...</div>
```
类选择符（Class Selectors）
---
类选择器允许我们根据元素的类属性值选择元素。类选择器比类型选择器更具体一些，因为它们选择一组特定的元素，而不是一种类型的所有元素。   
类选择器允许我们通过在多个元素上使用相同的类属性值，同时对不同的元素应用相同的样式。  
在CSS中，类由一个先导符号（.）来标记，接着是类属性值。这里，类选择器将选择包含类属性值为 __awesome__ 的任何元素，包括分隔元素（&lt;div>）和段落元素（&lt;p>）。   
CSS
```css
.awesome { ... }
```
              
HTML
```html
<div class="awesome">...</div>
<p class="awesome">...</p>
```

ID选择符（ID Selectors）

ID选择器甚至比类选择器更精确，因为它们一次只针对一个唯一元素。正如类选择器使用元素的类属性值作为选择器一样，ID选择器使用元素的ID属性值作为选择器。   
不管它们出现在哪一种元素上，ID属性值只能在每个页面使用一次。它们应该被使用在含有重要意义的元素。   
在CSS中，ID选择器用一个先导符号（#）来表示，后面是ID属性值。ID选择器只选择了包含ID属性值是 __shayhowe__ 的元素。   
CSS
```css
#shayhowe { ... }
```
              
HTML
```html
<div id="shayhowe">...</div>
```   

附加选择器（Additional Selectors）
---
选择器是非常强大的，这里概述的选择器是我们会遇到的最常见的选择器。这些选择器也仅仅是开始。存在许多更高级的选择器并随时可以使用。当你对这些选择器感到得心应手的时候，不妨去看一些更高级的选择器。   
好的，一切都开始了。我们将元素添加到HTML页面中，然后我们可以使用CSS选择这些元素并将样式应用到它们身上。现在让我们把HTML和CSS之间的点连接起来，让这两种语言一起工作。
              
引入CSS
===
为了让我们的CSS能在HTML中使用，我们需要在HTML中引入CSS文件。引入CSS的最佳实践是将所有样式包含在一个外部样式表中，然后在HTML文档的&lt;head>元素中引用。使用一个单一的外部样式表可以让我们在整个网站上使用相同的样式，并迅速地在整个站点进行更改。             

>
>引入CSS的其他方法
>---
>引入CSS的其他方法包括使用内部样式和内联样式。你可能会在其他地方看到这些方法，但这些通常把不被推荐，因为它们使更新网站变得繁琐和不便。
>

为了创建我们的外部CSS样式表，我们希望再次使用我们的文本编辑器来创建一个带有.css文件扩展名的新的纯文本文件。我们的CSS文件应该保存在和HTML文件相同的文件夹中，或者保存在HTML文件所在的子文件夹中。      
在HTML文档的&lt;head>元素中，&lt;link>元素用于定义HTML文件与CSS文件之间的关系。因为我们链接的是CSS，所以我们使用值为 __stylesheet__ 的属性 __rel__ 来特指它们之间的关系。此外，__href__（或叫做超链接引用）属性用于标明CSS文件的位置或路径。    
思考一下下面这个例子，在HTML文档&lt;head>元素中引用以个外部样式表。
```html
<head>
  <link rel="stylesheet" href="main.css">
</head>
```

为了使CSS正确地渲染，属性 __href__ 的值所指路径必须直接与CSS文件的保存位置相关联。在前面的示例中，文件 __man.css__ 保存在与HTML文件相同的位置，也称为根目录。   
如果我们的CSS文件在一个子目录或子文件夹内，则属性 ___href__ 的值需要与此路径相关。例如，如果我们的文件 __main.css__ 存储在名为 __stylesheet__ 的子目录中，__href__ 的属性值将是 __stylesheet/main.css__ ，使用正斜杠表示移动到子目录中。   
此刻，我们的页面正有条不紊地变得生动起来。我们还没有深入研究CSS，但是您可能已经注意到，一些元素有我们在CSS中没有声明过的默认样式。这是浏览器为这些元素强加的CSS样式。幸运的是，我们可以很容易地使用CSS重置来覆盖这些样式，接下来我们就来学习这种方法。

使用CSS重置
===

每个Web浏览器对于不同的元素都有自己的默认样式。谷歌浏览器如何呈现标题、段落、列表等等可能不同于Internet Explorer的做法。CSS重置已被广泛用于确保跨浏览器的兼容性。   

CSS重置给每一个通用的HTML元素设置预定义样式，并为所有浏览器提供统一的样式。这些重置通常涉及删除任何大小、边距、填充或附加的样式，并调低这些值。因为CSS是由上至下的，所以我们的重置代码需要在我们的样式表的最顶层。这样做确保了这些样式首先被读取且所有不同的Web浏览器都是从一个共同的基础上开始工作。

有许多不同的重置可供使用，所有这些重置都有自己的特长。最流行的重置之一是 [Eric Meyer’s reset](https://meyerweb.com/eric/tools/css/reset/)，它已经对包含新HTML5元素的样式进行了适配。

如果你觉得这有点冒险，也可以使用由Nicolas Gallagher创建的 [Normalize.css](http://necolas.github.io/normalize.css/)。__Normalize.css__ 关注的不是将所有常见元素的样式全部重置，而是针对这些元素设置普通的样式。这需要对CSS有更深刻的理解，同时也要意识到你想要什么样的风格。

> 跨浏览器兼容性和测试
> ---
> 如前所述，不同的浏览器以不同的方式呈现元素。重要的是认识到跨浏览器兼容性和测试的价值。网站不需要在每一个浏览器中都完全相同，但它们应该很相近。你希望支持哪些浏览器，以及在多大程度上，你需要根据哪种方式对于你的网站是最好的来做出决定。

在编写CSS时会遇到一些麻烦。好消息是任何事情都是可能的，只要有一点耐心，我们就能把它解决掉。

实践
===

回顾一下我们上次在"大会"网站上遗留的一些问题，让我们看看是否可以添加一些CSS。

1. 在我们的"风格大会"文件夹中，让我们创建一个名为"__assets__"的新文件夹，我们将在该文件夹中存储我们网站的所有资源，如样式表、图片、视频等。对于我们的样式表，让我们先在"__assets__"文件夹中添加另一个名为"__stylesheets__"的文件夹。

2. 让我们用我们的文本编辑器创建一个名为 __main.css__的新文件，并将它保存在我们刚刚创建的"__stylesheets__"文件夹中。

3. 在Web浏览器中查看我们的 __index.html__ 文件，我们可以看到&lt;h1>和&lt;p>元素都有默认的CSS样式。具体来说，它们每个都有一个特有的字体大小和间距。使用Eric Meyer的重置，我们可以弱化这些样式，让它们每一个变成同一种基础的风格。要做到这一点，让我们回到Eric的网站，复制他的重置代码，并粘贴到我们的 __main.css__ 文件的顶部。
```css
/* http://meyerweb.com/eric/tools/css/reset/ 2. v2.0 | 20110126
  License: none (public domain)
*/

html, body, div, span, applet, object, iframe,
h1, h2, h3, h4, h5, h6, p, blockquote, pre,
a, abbr, acronym, address, big, cite, code,
del, dfn, em, img, ins, kbd, q, s, samp,
small, strike, strong, sub, sup, tt, var,
b, u, i, center,
dl, dt, dd, ol, ul, li,
fieldset, form, label, legend,
table, caption, tbody, tfoot, thead, tr, th, td,
article, aside, canvas, details, embed,
figure, figcaption, footer, header, hgroup,
menu, nav, output, ruby, section, summary,
time, mark, audio, video {
  margin: 0;
  padding: 0;
  border: 0;
  font-size: 100%;
  font: inherit;
  vertical-align: baseline;
}
/* HTML5 display-role reset for older browsers */
article, aside, details, figcaption, figure,
footer, header, hgroup, menu, nav, section {
  display: block;
}
body {
  line-height: 1;
}
ol, ul {
  list-style: none;
}
blockquote, q {
  quotes: none;
}
blockquote:before, blockquote:after,
q:before, q:after {
  content: '';
  content: none;
}
table {
  border-collapse: collapse;
  border-spacing: 0;
}
```

4. 随着我们的 __main.css__ 文件开始成形，让我们把它和我们的 __index.html__ 文件连接起来。在文本编辑器中打开 __index.html__ 文件，在 __&lt;head>__ 元素中添加 __&lt;link>__ 元素，跟在 __&lt;title>__ 元素之后。

5. 因为我们将使用&lt;link>元素来引用样式表，让我们添加关系属性（__rel__），并设置其值为 __stylesheet__。

6. 还要包含一个超链接引用，使用 __href__ 属性，指向我们的 __main.css__ 文件。请记住，我们的 __main.css__ 文件保存在 "assets" 文件夹下的子文件夹 "stylesheets" 中。因此，__href__ 属性值是 __main.css__ 文件的路径，应该是 __assets/stylesheets/main.css__。

```html
<head>
  <meta charset="utf-8">
  <title>Styles Conference</title>
  <link rel="stylesheet" href="assets/stylesheets/main.css">
</head>
```

是时候验收下我们的工作了，看看我们的HTML和CSS是否进展顺利。现在，在Web浏览器中打开我们的 __index.html__ 文件（或者如果已经打开则刷新页面）应该会显示出与以前略有不同的结果。    

{% qnimg learn-to-html-and-css/lesson-1/practice-2.png "title:图表4：在我们的&quot;风格-大会&quot;网站中使用CSS重置" "alt:Our Styles Conference website with a CSS reset" %}

总结
===

目前一切都好！我们在这一课中取得了很大的进步。

试想一下，你现在掌握了HTML和CSS的基础知识。随着我们的继续，你会花更多的时间来写HTML和CSS，你也会对这两种语言越来越得心应手。

回顾一下，我们已经覆盖了以下这些知识点：

* HTML与CSS的区别

* 了解HTML的元素、标签和属性

* 创建第一个网页的结构

* 了解CSS的选择器、属性和值

* 使用CSS选择器

* 在HTML中引用CSS

* CSS重置的价值

现在让我们更仔细学习HTML并了解一些语义。

参考资料
===

* [Common HTML terms](http://www.scriptingmaster.com/html/HTML-terms-glossary.asp) via Scripting Master

* [CSS Terms & Definitions](http://www.impressivewebs.com/css-terms-definitions/) via Impressive Webs 

* [CSS Tools: Reset CSS](http://meyerweb.com/eric/tools/css/reset/) via Eric Meyer 

* [Normalize.css](http://necolas.github.io/normalize.css/) via Nicolas Gallagher    

* [An Intro to HTML & CSS](http://www.shayhowe.com/web-design/intro-to-html-css/) via Shay Howe
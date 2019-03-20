---
title: Web development advanced technology stack (frontend)
date: 2019-03-20 21:01:52
tags:
  - 前端
  - 学习资料
---
# WEB开发前沿技术栈 （前端篇）

## HTML

HTML 5于2014年正式发布，是下一代的 HTML。   
HTML 5 仍处于完善之中。然而，大部分现代浏览器已经具备了某些 HTML5 支持。

### 新特性   
  1. 语义标签
	2. 增强型表单
	3. 视频和音频
	4. Canvas绘图
	5. SVG绘图
  6. 地理定位
  7. 拖放API
  8. Web Worker
  9. Web Storage
  10. WebSocket

### 未来趋势
  1. 移动优先
  2. 游戏开发
  3. 响应式设计
  4. 设备访问
  5. 离线缓存


## JavaScript

### ECMAScript 6.0

ECMAScript 6.0（以下简称 ES6）是 JavaScript 语言的下一代标准，已经在 2015 年 6 月正式发布了。它的目标，是使得 JavaScript 语言可以用来编写复杂的大型应用程序，成为企业级开发语言。

ES6入门： http://es6.ruanyifeng.com/

主要新特性：   
  * let 和 const 命令
  * 变量的解构赋值
  * 字符串的扩展
  * 正则的扩展
  * 数值的扩展
  * 函数的扩展
  * 数组的扩展
  * 对象的扩展
  * 对象的新增方法
  * Symbol
  * Set 和 Map 数据结构
  * Promise 对象
  * Iterator 和 for...of 循环
  * Generator 函数的语法
  * Generator 函数的异步应用
  * async 函数
  * Class 的基本语法
  * Class 的继承
  * Module 的语法
  * Module 的加载实现

### TypeScript
		
		TypeScript是一种由微软开发的自由和开源的编程语言。它是JavaScript的一个超集，增强了JavaScript的特性。

		TypeScript中文网：https://www.tslang.cn/docs/home.html

		主要特性有：

			类型批注（Type annotations）

			编译时类型检查 （Compile time type checking）

			接口（Interfaces）

			类（Classes）

			模块（Modules）

			箭头函数表达式（lambda表达式）


CSS
	预处理器

		什么是 CSS 预处理器呢？

			CSS 预处理器定义了一种新的语言，其基本思想是，用一种专门的编程语言，为 CSS 增加了一些编程的特性，将 CSS 作为目标生成文件，然后开发者就只要使用这种语言进行CSS的编码工作。

       	目前流行的主要有两种预处理器：Less 和 Sass

       	Less和Sass的相同之处：

			1.变量：可以单独定义一系列通用的样式，在需要的时候进行调用。

			2.混合（Mixins）：class中的class（讲一个class引入到另一个class，实现class与class之间的继承），还可以带参数的混合，就像函数一样。

			3.嵌套：class中嵌套class，从而减少代码的重复。

			4.运算：提供了加减乘除四则运算，可以做属性值可颜色的运算。

		Less和Sass之间的区别：

			1.实现方式：Less是基于JavaScript，是在客户端进行处理的；Sass是基于Ruby，是在服务器端进行处理的。所以相比较之下前者解析会比后者慢一点

			2.定义变量：Less定义变量时使用前缀：@；Sass定义变量时使用前缀：$。

			3.混合（Mixins）：Less中使用混合时，只需在classB中根据classA的命名来是用；Sass中首先在定义混合时需要使用@mixin命令，其次在调用时需要使用@include命令来引入之前定义的混合。

			4.解析方式：Less可以向上/向下解析；Sass只能向上解析。

			5.变量的作用域：Less中的变量有全局和局部之分；Sass可以变量可以理解为都是全局的，但可以通过在变量后面跟！default，在引入Sass文件之前改变变量的属性值来解决这一问题。

			6.比起Less，Sass中增加了条件语句（if、if...else）和循环语句（for循环、while循环和each循环）还有自定义函数：



前后端分离

主流前端架构模式 MVC / MVVM 

	MVC架构模式
		M - Model  数据：数据实体,用来保存页面要展示的数据.
		V - View   视图：负责显示数据的,一般其实就是指的html页面.
		C - Controller 控制器： 控制整个业务逻辑,负责处理数据,比如数据的获取,以及数据的过滤，进而影响数据在视图上的展示.

	MVVM架构模式
		M - Model 数据：它是与应用程序的业务逻辑相关的数据的封装载体
		V - View 视图：它专注于界面的显示和渲染
		VM - ViewModel 视图-数据：它是View和Model的粘合体，负责View和Model的交互和协作

	MVVM的优点
		- 低耦合(组件化)：View可以独立于Model变化和修改，同一个ViewModel可以被多个View复用；并且可以做到View和Model的变化互不影响；
		- 可重用性(组件化)：可以把一些视图的逻辑放在ViewModel，让多个View复用；
		- 独立开发：开发人员可以专注与业务逻辑和数据的开发ViewMode，设计人员可以专注于UI(View)的设计；
		- 可测试性：清晰的View分层，使得针对表现层业务逻辑的测试更容易，更简单。

	MVVM主流框架
		- React.js  (https://react.docschina.org/)
		- Vue.js  (https://cn.vuejs.org/)
		- Angular.js (https://www.angular.cn/)


	
UI组件库
	
	响应式 （桌面端/移动端）

		Bootstrap (JQuery)

		Amaze UI Web (JQuery)

	桌面端 (企业级中后台产品)

		Element-UI (基于Vue.js)

		Ant Design （基于React) / Ant Design Pro (基于AntDesign的开箱即用框架)

		iview (基于Vue.js)


	移动端

		Mint-ui （饿了么，基于Vue.js)

		Ant Design Mobile 

		Vux （基于Vue.js）

		WeUI (微信/小程序)

构建工具

	webpack

	parcel

	gulp

	grunt




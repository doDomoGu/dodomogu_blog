---
title: 别人的包里bug，用起来不方便？发布自己的npm包
tags:
  - npm
  - Node.js
date: 2018-02-24 17:58:44
---
我们基于nodejs平台上面的npm上，可以随意下载很多npm安装包。  
别人的包里bug，用起来不方便？  
那我们如何创建自己的npm包呢？很简单，废话少说，开始做~

开始做之前nodejs默认是要安装的，怎么安装自行百度其他教程。

首先在npm网站上注册一个账号，这个账号之后会用到。

npm网站地址：https://www.npmjs.com/

npm网站注册地址：https://www.npmjs.com/signup

注册完毕，回到命令行工具:

``` 
//输入以下命令，会提示输入用户名、密码、邮箱，这些都是注册时填写过的。
npm login
```
![npm_login](publish_your_own_npm_package/WX20180228-103234@2x.png-w1100 "npm login")

创建一个自己的目录，进入目录，并进行npm初始化操作，建立配置文件：

```
//输入以下命令，会提示配置包的相关信息，名称版本等等，都是包的基本配置信息
npm init
```

<font color="red">**一般开源的包都会存放在github上，你可以fork下来项目源码，自己认为有bug的地方，建立自己的分支做修正。然后可以将这个修正后的代码做为一个新的包发布到npm上。**  </font>

下面是发布操作：

```
//退出当前文件夹，开始命令行发布包，命令如下：
npm publish your_dir    //your_dir 是你的包所在目录的名称
```
如果发布成功，就可以立刻进行安装下载了
```
npm install your_dir
```
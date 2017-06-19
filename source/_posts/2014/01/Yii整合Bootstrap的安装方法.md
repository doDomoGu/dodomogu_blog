---
title: Yii整合Bootstrap的安装方法
tags:
  - Yii
date: 2014-01-02 16:39:36
---

<b>转发至我的网站页面 <a title="http://www.dodomogu.com/bootstrap/guide" href="http://www.dodomogu.com/bootstrap/guide" target="_blank">http://www.dodomogu.com/bootstrap/guide</a></b>

### 这里使用 Yii-bootstrap 这个扩展，支持的是Bootstrap 2。


bootstrap已经推出了3.0的新版，看起来2.3.x版本也不会再更新了。那么bootstrap 2.3版与3.0版的区别在哪里呢？ Bootstrap 3.0增加了一些新的特性，对于一些类也进行了调整。不过两个版本在使用的方法上是没什么大的区别的。所以bootstrap 2 对于基本使用来讲是完全够用的。   

### 1.解压到 protected/extensions/bootstrap (如果你没更改过你的默认扩展位置)    

    protected/  
        └── extensions        
            └── bootstrap       
                ├── actions
                ├── assets
                │   ├── css
                │   ├── img
                │   └── js
                ├── components
                │   └── Bootstrap.php
                └── widgets
                    └── input   

*在此罗列出主要目录文件   


### 2.修改 protected/config/main.php 配置文件   
首先在配置文件开头声明一个路径别名bootstrap，再在components组件中增加 'bootstrap'   

    Yii::setPathOfAlias('bootstrap', dirname(__FILE__).'/../extensions/bootstrap');
    return array(
        ...
        'components' => array(
            ...
            'bootstrap' => array(
                'class' => 'ext.bootstrap.components.Bootstrap',
            ),
            ...
        ),
        ...
    )   

### 3.修改模板文件   
调整&lt;head&gt;&lt;/head&gt;之间对于css和js文件的加载，将原本yii自带的css内容全都去除，使用html5的开头，增加一行“Yii::app()-&gt;bootstrap-&gt;init();”，用来统一加载bootstrap的样式表和脚本。   


	<!DOCTYPE html>
		<html lang="en">
    		<head>
            <?php Yii::app()->bootstrap->register();?>
            <meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
            <title>doDomo_Gu's Home - Guide Bootstrap</title>
            </head>
        
#####至此已经可以在Yii中开始使用bootstrap的功能了

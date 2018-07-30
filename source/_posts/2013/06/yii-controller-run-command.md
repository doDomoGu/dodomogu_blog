---
title: Yii 在controller中调用command
tags:
  - Yii
date: 2013-06-26 17:52:23
---
这里是Yii 1.X版本

这里用到exec()这个函数,其实是一个php问题.

例 command:   /data/html/XXX/protected/yiic   test
则在TestController里面
function actionTestCommand(){
exec('/data/html/XXX/protected/yiic test');    //使用   www.xxx.com/test/testCommand 就能访问并运行这个 command了
}

注意 exec函数    在windows下,由于文件路径使用的是斜杠"\",在使用双引号时会转义

错误的例子:exec("D:\xampp\htdocs\xxx\protected\yiic aaa")
正确的应该是 exec("D:\\\\xampp\\\\htdocs\\\\xxx\\\\protected\\\\yiic aaa")
或者使用单引号  exec('D:\xampp\htdocs\xxx\protected\yiic aaa')
<p style="text-align: right;">----- doDomo Gu</p>
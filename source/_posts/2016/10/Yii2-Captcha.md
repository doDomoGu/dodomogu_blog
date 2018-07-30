---
title: Yii2 Captcha验证码，在activeForm开启enableAjaxValidation时验证错误的解决办法
tags:
  - Yii
date: 2016-10-23 03:07:18
---

注册表单需要加入Captcha图片验证码。

当activeForm 开启Ajax验证时,验证码会显示验证不正确，是因为在Ajax验证时，
<code>enableAjaxValidation =&gt; true</code>
执行yii\captcha\CaptchaAction的validate方法时会重新生成验证码 （如下图，调用getVerifyCode方法时带上参数true重新生成验证码）

<img class="alignnone size-full wp-image-57" src="" alt="QQ截图20161023025052" width="900" height="314" />

<img class="alignnone size-full wp-image-58" src="" alt="QQ截图20161023025113" width="836" height="380" />

所以解决办法是新建一个继承类，继承CaptchaAction,并重写validate方法 (如下图)

<img class="alignnone size-full wp-image-60" src="" alt="QQ截图20161023025529" width="1065" height="533" />

接下来在生成这个验证码的action上，修改类名

<img class="alignnone size-full wp-image-61" src="" alt="QQ截图20161023025640" width="827" height="501" />

至此，解决了这个问题。

<hr />

&nbsp;

另外大家是不是发现刷新页面，验证码不会刷新。我们查看CaptchaAction的run方法，其中生成验证码的地方没有带上参数true所以不会强制刷新 （如下图）

<img class="alignnone size-full wp-image-62" src="" alt="QQ截图20161023030125" width="976" height="481" />

所以大家有需要每次刷新页面，验证码也可以刷新，同样需要重写这个run方法，让获取验证码的方法(getVerifyCode) 带上参数 true。

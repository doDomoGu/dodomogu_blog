---
title: 配置Yii2的request，使其可支持接收Json和Xml格式的数据
tags:
  - Yii
date: 2018-01-24 10:56:42
---

## 配置Yii2 request的parsers选项，使之可以通过Yii::\$app->request->post()来接收 Json 和 Xml格式的数据  

Yii2 接收 POST 数据是使用 Yii::$app->request->post(); ，但是如果发送过来的数据格式是 json 或 xml 的时候，通过这个方法就无法获取到数据了，Yii2 这么强大的组件型框架肯定想到了这一点。  

对于 json 的解析 Yii2 已经写好了 JsonResponseFormatter，在配置文件里面配置一下即可使用。 

Base版的config/web.php  或者 advanced版的app/config/main.php  

    'components' =>[
        'request' => [
            'parsers' => [
                'application/json' => 'yii\web\JsonParser',
                'text/json' => 'yii\web\JsonParser',
            ],
        ],
    ],

配置好之后访问提交过来的数据就太简单啦

    # json raw data
    {"username": "bob"}

    # access data
    echo Yii::$app->request->post("username");
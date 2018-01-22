---
title: Hexo 安装搭建及常用操作
tags:
  - Hexo
  - 笔记
date: 2018-01-22 15:33:16
---


# Hexo 安装搭建及常用操作 #
## 开篇：  
Hexo官网：https://hexo.io/zh-CN/   
Next主题包：https://github.com/iissnan/hexo-theme-next

## 简单的搭建
安装Hexo
> npm install -g hexo

进入工作目录，进行初始化
> cd 工作目录  
hexo init

安装依赖包
> npm install

运行
> hexo server 

查看结果
> http://localhost:4000/

# Hexo的操作命令

简化操作方法：

增加新文章  
> hexo new "[article_title]"   
hexo n

增加新草稿在_drafts目录  
> hexo new draft "[article_title]"

将草稿发布到_posts目录
> hexo publish "[article_title]"  
hexo p

生成Html静态页面
> hexo generate    
hexo g

安装主题：
将主题安装在themes/[主题名称]目录下  
    git clone [https://github.com/iissnan/hexo-theme-next](https://github.com/iissnan/hexo-theme-next) themes/next   
    或  
    git clone [https://github.com/MOxFIVE/hexo-theme-yelee.git](https://github.com/MOxFIVE/hexo-theme-yelee.git) themes/yelee  

这里选取了一个主题 Next  
修改主题配置： _config.yml 文件中 theme: next

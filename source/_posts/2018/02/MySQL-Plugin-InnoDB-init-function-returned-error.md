---
title: MySQL Plugin 'InnoDB' init function returned error. 错误原因及解决方法
tags:
  - MySQL
date: 2018-02-01 15:44:47
---


MySQL Plugin 'InnoDB' init function returned error
---
{% qnimg MySQL-Plugin-InnoDB-init-function-returned-error/WX20180201-153330@2x.png title:错误日志 'alt:MySQL 错误日志' extend:-w1100 %}

见上图错误日志，看到"allocate memory"就应该知道是内存不足了。 
 
因为我用的是最低配的阿里云服务器只有512M内存，InnoDB缓冲会占用机器内存，我们调整MySQL配置选项 innodb_buffer_pool_size = 16M

{% qnimg MySQL-Plugin-InnoDB-init-function-returned-error/WX20180201-154040@2x.png title:MySQL配置文件 alt:修改MySQL配置文件 extend:-w1100 %}
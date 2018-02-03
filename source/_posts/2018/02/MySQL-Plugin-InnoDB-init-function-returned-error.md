---
title: MySQL Plugin 'InnoDB' init function returned error. 错误原因及解决方法
tags:
  - MySQL
date: 2018-02-01 15:44:47
---


MySQL Plugin 'InnoDB' init function returned error
---

![错误日志](http://blog-source.dodomogu.com/WX20180201-153330@2x.png "MySQL 错误日志")

见上图错误日志，看到"allocate memory"就应该知道是内存不足了。  
因为我用的是最低配的阿里云服务器只有512M内存，InnoDB缓冲会占用机器内存，我们调整MySQL配置选项 innodb_buffer_pool_size = 16M


![MySQL配置文件](http://blog-source.dodomogu.com/WX20180201-154040@2x.png "修改MySQL配置文件")
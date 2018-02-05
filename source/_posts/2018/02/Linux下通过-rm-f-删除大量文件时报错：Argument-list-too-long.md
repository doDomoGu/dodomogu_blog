---
title: Linux下通过 rm -f 删除大量文件时报错：Argument list too long
date: 2018-02-05 14:14:36
tags:
    - Linux
---
在使用 <span class="code-inline">npm install</span> 安装项目时, 发生了 <span class="code-inline">No space left on device</span>，看样子是磁盘满了，但是发现磁盘还比较空，但是Linux其实是有文件数(node:节点数)的限制，使用 <span class="code-inline">df -i</span> 可以查看。

由于 Linux 在执行 cron 时，会将 cron 执行脚本中的 output 和 warning 信息，都会以邮件的形式发送 cron 所有者， 而由于客户环境中的 sendmail 和 postfix 没有正常运行，导致邮件发送不成功，全部小文件堆积在了 maildrop 目录下面，而且没有自动清理转换的机制，所以长达一年的时间，此目录已堆积了大量的文件。查看 man cron 的信息，可以知道会发送给 cron owner.

于是尝试删除这个目录下的内容，但是执行 <span class="code-inline">rm -rf ./*</span> 竟然提示参数列表过长

```linux
-bash: /bin/rm: Argument list too long
```

后来使用如下命令通过管道的方式删除：

```linux
ls | xargs rm -f
```

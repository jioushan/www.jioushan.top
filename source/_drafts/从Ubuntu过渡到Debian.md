---
title: 从Ubuntu过渡到Debian
tags: []
id: '1305'
categories:
  - - uncategorized
---

首先声明 此文章 尽限 在我使用过程之余 经常出现问题以及解决方式！有些方式出现原因不同，故因解决方式也不同。

希望在这篇文章中遇到的问题你若也碰到，能过帮到你！

有时候我认为去写一个经常使用的操作命令性的文章是没有意义的。但是有时并不排除 大多数人使用Linux SSH /CMD 的同时 都是copy

借着我为数不多 重置系统的同时，写些内容来帮助到阅读它的人！

通过默认的ssh登录至Linux 系统，对我而言 我想我首先要做的就是变更为key登录

这里我建议移步至我另一篇文章

网卡配置

`/etc/network/interfaces`

DNS 配置

debian的dns配置保存在文件 `/etc/resolv.conf` 里面

重启网卡命令

`sudo service networking restart`
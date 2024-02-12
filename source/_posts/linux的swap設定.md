---
title: Linux的Swap設定
tags:
  - Swap
id: '1352'
categories:
  - - Linux
date: 2022-11-25 19:26:28
---

```
free -m
```

查看內存情況或

```
swapon --show
```

查看目前的Swap分配情況！

## 創建Swap

```
fallocate -l 1G /swapfile

chmod 600 /swapfile
```

設置激活Swap分區

```
mkswap /swapfile

swapon /swapfile
```

编辑 /etc/fstab 文件使Swap分配永久

```
vim /etc/fstab
```

在此文件內尾部填入以下參數

```
/swapfile swap swap defaults 0 0
```

验证 Swap 分区

```
swapon --show
```

## 调整 Swappiness 值

Swappiness 值代表着系统使用 Swap 的频率，从 0-100，数值越高越频繁使用。

查看系统默认：

```
cat /proc/sys/vm/swappiness
```

修改：

```
sysctl vm.swappiness=10
```

持久化：

```
vim /etc/sysctl.conf
```

添加一行：

```
vm.swappiness=60
```

具体数值需要根据实际情况调整。

## #刪除Swap

先取消激活 Swap 分区：

```
swapoff -v /swapfile
```

然后编辑 `/etc/fstab` 文件，删除之前添加的那行：

```
/swapfile swap swap defaults 0 0
```

最后，删除 Swap 文件：

```
rm /swapfile
```

本教程：[來源](https://meta.appinn.net/t/topic/27359) 若有侵權，請聯繫我刪除！
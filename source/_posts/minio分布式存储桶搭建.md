---
title: Minio分布式存储桶搭建
tags:
  - docker
  - Minio
  - 分布式存储
id: '1227'
categories:
  - - 杂谈
date: 2022-03-04 13:50:44
---

好久没写字了，水一篇！

MINIO 是啥？（不介绍了，自行度娘）

涉及到因为这个软件 开源维护得也太快了

可能过去搭建过它的小伙伴认为它是这样的

![](https://imgconvert.csdnimg.cn/aHR0cHM6Ly9sZWVoYW8ub3NzLWNuLXNoZW56aGVuLmFsaXl1bmNzLmNvbS8yMDIwLTAxLTIxLTE0MTc0OS5wbmc?x-oss-process=image/format,png)

可如今它却变成这样

![](https://blog.min.io/content/images/size/w2000/2021/04/console_header--2-.png)

部署**分布式存储** 我们按照它[官方的文档](https://docs.min.io/)来部署。但是如果一遍就OK 那我们也把官方想的太简单了。

踩了些坑 让我头疼了两天，和过去踩的那些坑相比这个太头疼了。索性我水了这篇文章。

因为咱部署的是server （服务器）端

MC用户端 基本上会命令行 或者第三方工具接入。我就不多言赘了。（除非您没用过存储桶。（自行度娘

我们这边采用它官方的[Docker Compose](https://docs.min.io/docs/deploy-minio-on-docker-compose.html) 部署

**步骤一**

所以麻烦您的Linux 安装下compose和docker

**步骤二**

wget下这两个文件（没有wget的自行安装 wget）

[https://github.com/minio/minio/blob/master/docs/orchestration/docker-compose/docker-compose.yaml](https://github.com/minio/minio/blob/master/docs/orchestration/docker-compose/docker-compose.yaml?raw=true)

[https://github.com/minio/minio/blob/master/docs/orchestration/docker-compose/nginx.conf](https://github.com/minio/minio/blob/master/docs/orchestration/docker-compose/nginx.conf?raw=true)

**步骤三**

然后再按照官方的命令

```
$ docker-compose pull

$ docker-compose up
```

然后他就运行在您的服务器进程上了，but您想通过域名访问它，建议自行研究nginx反代（反向代理）

进程占用端口 9000，9001，9002；

Yaml里面写到的 可以部署前自行修改

MINIO\_ROOT\_USER: minio

MINIO\_ROOT\_PASSWORD: minio123
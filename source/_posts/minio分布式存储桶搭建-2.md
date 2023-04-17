---
title: Minio distributed bucket construction
tags: []
id: '1232'
categories:
  - - 未分类
date: 2022-03-04 13:50:44
---

I haven't written in a long time, water!

What is MINIO? (Not introduced, self-made)

It comes to because this software is open source and maintained too quickly

Maybe the friends who have built it in the past think it is like this

![](https://imgconvert.csdnimg.cn/aHR0cHM6Ly9sZWVoYW8ub3NzLWNuLXNoZW56aGVuLmFsaXl1bmNzLmNvbS8yMDIwLTAxLTIxLTE0MTc0OS5wbmc?x-oss-process=image/format,png)

But now it's like this

![](https://blog.min.io/content/images/size/w2000/2021/04/console_header--2-.png)

Deploy **distributed storage** We deploy it according to [its official documentation](https://docs.min.io/). But if it's OK all at once, then we also think the official is too simple.

Stepping on some pits gave me a headache for two days, which was too much of a headache compared to the pits I had stepped on in the past. Simply I watered this article.

Because we are deploying the server (server) side

The MC client basically connects the command line or third-party tools. I won't dwell on it. (Unless you haven't used a bucket.) (Self-made wife.)

We're using its official [Docker Compose](https://docs.min.io/docs/deploy-minio-on-docker-compose.html) deployment here

**Step 1**

So trouble your Linux installation under compare and docker

**Step 2**

wget under these two files (no wget self-installed wget)

[https://github.com/minio/minio/blob/master/docs/orchestration/docker-compose/docker-compose.yaml](https://github.com/minio/minio/blob/master/docs/orchestration/docker-compose/docker-compose.yaml?raw=true)

[https://github.com/minio/minio/blob/master/docs/orchestration/docker-compose/nginx.conf](https://github.com/minio/minio/blob/master/docs/orchestration/docker-compose/nginx.conf?raw=true)

**Step 3**

Then follow the official order

```
$ docker-compose pull

$ docker-compose up
```

Then he is running on your server process, but you want to access it through the domain name, it is recommended to study the nginx anti-generation (reverse proxy) yourself

Process occupies ports 9000, 9001, 9002;

What is written in Yaml can be modified before deployment

MINIO\_ROOT\_USER: minio

MINIO\_ROOT\_PASSWORD: minio123
---
title: RIPE 注册及字段创建
tags:
  - APNIC
  - JSMSR
  - NetWork
  - RIPE
id: '1316'
categories:
  - - Network
date: 2022-05-31 17:35:38
---

BGP Player

作为接下来即以后要讲述的企划！

这部分文字的重要性，而我认为此篇文字 将为JNE（Jsmsr Experimental Network）重要开篇！

[JSMSR](http://www.jsmsr.com) **only ipv6**

RPIE 注册教程

本文字 来源于 夜空 [文章](https://web.archive.org/web/20190227042014/https:/www.ykhut.com/archives/72/)

## RIPE账号注册与必要字段创建

首先 您应该注册一个ripe账户，建议常用邮箱 以便于维护 找寻

**注册地址：**[](https://web.archive.org/web/20190227042014/https://www.ykhut.com/go/aHR0cHM6Ly9hY2Nlc3MucmlwZS5uZXQvcmVnaXN0cmF0aW9u)[https://access.ripe.net/registration](https://web.archive.org/web/20190227042014/https://www.ykhut.com/go/aHR0cHM6Ly9hY2Nlc3MucmlwZS5uZXQvcmVnaXN0cmF0aW9u)

通过邮箱验证之后 您应当在控制面板 创建一些 字段和值

**首先创建person 和 maintainer**

![](https://cdn2.jioushan.top/LightPicture/2022/05/febc1e3387234cf3.png)

点击create创建此字段

**mntner:** 维护者的字段名，纯英文，可包含"-"和"\_"，建议格式为_\*_\-MNT，例如YekongTAT-MNT

**person:** 维护者的称呼，可以写全名或其他名称。可包含英文、数字和.\`'\_-

**address:** 地址  
**phone:** 手机号，建议格式为+国家区号.手机号，例如+85211112222

创建之后

![](https://cdn2.jioushan.top/LightPicture/2022/05/2e16817713d65b4f.png)

person with primary key

"MNS89-RIPE"

以及

mntner with primary key "MoeQing-MNT"  
这两个分别为admin-c以及mntner/mnt-ref，如果以后遇到需要填写这两个字段的，那么填写这两个即可。  
一切完成后即可下一步。

* * *

**接下来 创建role对象**

和前面相同，选择"role"对象创建即可

![](https://cdn2.jioushan.top/LightPicture/2022/05/0c875d5eab923282.png)

role: 起名字环节，建议格式XXX NOC  
address: 与前面相同  
nic-hdl： 可保持默认。

然后 点击nic-hdl 旁边的 **+**

我们新建一项 abuse-mailbox字段，输入你的邮箱即可，然后就可以提交了。

之后您会得到这样的字段 role "MN12319-RIPE"，这个为**abuse-c**,如果以后遇到需要填写这两个字段的，那么填写这个即可。

* * *

**创建organisation对象**

![](https://cdn2.jioushan.top/LightPicture/2022/05/5bac71c3a6ea019b.png)

字段解释：  
organisation: 可保持默认。  
org-name: 组织名称，可包含字母数字"-"和"\_"，名称的第一个字符必须是字母，最后一个字符必须是字母或数字。某些单词由RPSL保留，不能使用。

org-type: 保持默认，也无法更改。  
address: 地址栏，如果你要申请ASN请填写证件国家对应的地址。  
e-mail: 填写你的邮箱。  
abuse-c: 上文提到过，请填写role相关字段。  
mnt-ref: 添加维护者对象。上文提到过，请填写mntner

请保存好以上资料。如有遗忘，请通过ripe数据库查询功能反向查询到内容

感谢此原文章由夜空所写，本篇为搬运/补档，便于查询 理解 通过ripe IRR 数据库练手即在其他区域网络自治中心 维护字段信息，其内容大同小异。更多内容，以后将细讲！
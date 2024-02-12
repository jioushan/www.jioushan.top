---
title: 通過Cloudflare使用PTR
tags:
  - cloudflare
  - prefix
id: '1347'
categories:
  - - Linux
date: 2022-11-25 19:12:33
---

#此教程感謝一位朋友幫助！

總所周知當我們使用mtr的時候  
或者besttrace的時候，  

![](https://cdn2.jsmsr.com/LightPicture/2022/11/dc0810d41d145e4a.png)

比方說這張

我們能看到每一跳 其實是IP地址的，但為何一個ip地址卻顯示出主機名呢？  
  
這裡我們便需要dns服務中的一種類型，PTR 指針！

請理解RDNS

言簡意賅，直接說教程吧。

#首先

copy您的prefix至這類的反碼計算  
[工具網址](https://adminhacks.com/subnet/ip6.arpa.html) [備用](https://www.coderstool.com/ipv6-subnet-calculator)計算站點  
將得出的反碼通過cloud flare 正常**添加域名**方式 添加到cloudflare！

一步一步，免費計畫，到這一步，cloudflare的服務器要求域名的DNS到cloudflare分配給您的DNS地址

#第二步

聯繫您這個prefix的lir/具有您prefix大段的控制者/管理員  
將此prefix的分配機構添加如下信息！  
本文這裡只拿ripe操作來舉例子！  
首先創建一個domain: 類型  
1.填寫您的prefix 反碼  
2.填入cloudflare分配給您的nserver:（nameserver）

3.您這個prefix的管理信息

最後提交！至此，若沒有提升任何抱錯，即跳轉去cloudflare刷新域名，即可看到您對此反碼的控制權！  
例如截圖  
  

![](https://cdn2.jsmsr.com/LightPicture/2022/11/cf1d1b0dbad3e3e9.png)

#若您提交出現任何抱錯，請聯繫分配給您這個prefix管理者/控制者「以協助你將您的反碼修改至您的DNSserver

#最後的最後，您可以在cloudflare的DNS控制台，新建一條PTR類型的紀錄  
前面是ip地址反碼，（注意也是反碼，因為PTR類型要求地址必為反碼）  
內容填寫您要他人在發現您路由時出現的域名信息！  
內容均有您來控制！  
  
#您可以通過這裡查詢您的PTR生效紀錄 [網址](https://mxtoolbox.com/SuperTool.aspx?)  
  
至此，教程結束！
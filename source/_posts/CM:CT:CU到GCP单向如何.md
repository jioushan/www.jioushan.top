---
title: >-
  How about the three major domestic operators for the route tracking of large
  factories.
tags: []
id: '1147'
categories:
  - - note
date: 2020-01-12 05:10:54
---

![](https://cdn2.jsmsr.com/LightPicture/2022/03/c2d3e705fbdbf55b.jpg)

Previously written SS tutorials. But one-click scripting or something. Fool's errands.  
Rack your brains for delay! Although it is very much a wool wool. Just write about some experience.

How about the three major domestic operators for the chicken lines of the big factories.

#### GCP tw  
cause:

**The mobile routing table is that there are pits**  
in the same node, next door telecom, Unicom, the delay is not more than 80  
mobile one run, almost 200

Opened a few **GCP tw/jp** Some people say that hk Unicom will also go around the city. For direct connection. GCP Unicom/Telecom Preferred TW  
Mobile is running around San Jose. It's terribly uncomfortable. To avoid this delay. Simply do the website 80/443 port acceleration, you can choose.  
Cloudflare CDN(hk) nodes are mobile-friendly. The delay does not exceed 60ms

Let's talk about the hosts of other homes. Mainly about **JP, mild involves hk, tw, sg** will also be said

At present, there are only mobile home wide nodes, and it is simply based on the test data of Shandong Mobile to say some experience.

#### vu（vultr）

JP direct san jose circle. ok？ Don't think. And vu's 104 nodes must not be opened. Pixiv is blocked. Not much more

Now the VU should be moving north beijing exit  
I once drove to the vu 66 node very fragrant. But that might be really good luck.

#### digitalocean

  
At present, foreign website server hosts use this (can I say that there are many sites running on it?). Can not be stopped), it is estimated that it will be changed around the end of this  
year. The sg used should be very telecom-friendly. Unicom can also be used. Speaking of moving. Walk the Hong Kong ntt. Overall it was ok. But  
digitalocean doesn't have jp. Digitalocean is suitable for us/sg

#### azure jp/hk

  
Mobile preferred. For other telecom Unicom, it is right to choose hk. JP walked also hk. Will be hk detour.  
The three networks are almost the same, Unicom, and telecommunications are not as good as choosing aws.

#### AWS lightsail jp

  
Telecom is better than China Unicom. The move is the worst.

Moving away from the Beijing exit directly connected, the Japanese equinix machine room should be.

AWS's US Mobile is the **Shanghai** export

1/12 date  
A bit of a gamble luck lately. GCP hk

Choose **asia-east2-b** for this district. **34.92./** This segment moves around Tokyo, Japan. Delay around 110. Catch up with me next door azure jp100ms up

More fragrant at the back **35.220./** This segment moves directly to Hong Kong. North Beijing export - > Guangdong - >HK 50ms too fragrant. Guangzhou latency is estimated to be 1x ms

![](https://cdn2.jsmsr.com/LightPicture/2022/03/93c1eeaee6cc0671.png)

Authentic incense

![](https://cdn2.jsmsr.com/LightPicture/2022/03/a40b347c35e6fabd.png)

GCP osaka (Osaka) Do not touch. Looked at the GCP instructions. Feelings Osaka split out IP no matter which district, a computer room. IP how the whole will travel around the world. Just go around the beauty. London also  
tours. Pure is a waste of time.

GCP (Telecom/Unicom) > AWS lightsail (Telecom/Unicom) > azure (three networks one. Too average. ）

Linode and ECS (Ali International) have not been used. There used to be kagoya nodes. Similar to azure. Direct jp (osaka) Unfortunately, no more.  
When I use it, I'm making up the file.

#### linode

[Click on this connection](https://paste.ubuntu.com/p/RNMgKVGCtv/) to get the routing information of linode to various operators in China!
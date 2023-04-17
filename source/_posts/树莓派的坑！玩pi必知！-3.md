---
title: The pit of the Raspberry Pi! Play pi must know!
tags: []
id: '1170'
categories:
  - - uncategorized
date: 2019-09-06 21:13:55
---

Ubuntu usage, debian shows really simple to ugly. It doesn't matter. Familiarize yourself with the vim editor. Nono just joted down two commands!

Ctrl+O Save. Enter confirm Ctrl+x to exit. If you exit directly (if you modify the content), you will also be asked if you want to save. Enter confirmation is good.

Switch to su root administrator mode!

```
sudo passwd root
```

 After executing this command, you will be prompted to enter the root password twice (to make sure that you remember the password). 

```
sudo passwd --unlock root
```

Enter the password to unlock the root user

Use the command below to switch to root administrator

```
su root
```

## **Raspberry Pi source swap !!! (Note the pit)**

The source of the University of Science and Technology of China should be much better. Of course, you are abroad, where there is a problem of changing the source. It wouldn't be so bad!

This post is a way to change [the source of the University of Science and Technology!](https://www.jianshu.com/p/768f0181672b) Just follow this source swap!!! (for Raspberry Pi 3B)

But be careful not

```
sudo reboot
```

This is **the reboot** command. The problem with the pit here is that you switched the source. Raspberry Pi **reboot failed** . A red light is on constantly. The green light is gone. This is the system does not read ah. That's the problem. Until I later found the cause of the problem!

Do not directly upgrade when changing the source, plus dis-upgrade can be, direct upgrade seems to make pi can not boot, you will find the green light regular flashing four times.

After brushing the system, the source is directly upgraded and then restarted, and the probability is that it cannot be restarted!!!

My god, I wrote N secondary mirror images. It's going to be re-burned again! Before the database could not be installed, UbuntuMate burned into their own TV how to change is not to display the screen this is to complete the initial settings!

Officially this debian pit has quite a few. Before switching back to the Raspberry Pi official source load database can be found. But the idea of that rate I unloaded was too real.

**About the Raspberry Pi for domestic sources. Because the system source is different, the software cannot be downloaded and installed conflicts!**

(For Raspberry Pi 4B) ( [Tsinghua Source](https://mirrors.tuna.tsinghua.edu.cn/help/raspbian/) )

```
deb http://mirrors.tuna.tsinghua.edu.cn/raspberrypi/ buster main ui
deb-src http://mirrors.tuna.tsinghua.edu.cn/raspberrypi/ buster main ui
```

Change the strash to buster  
i.e. deb http://mirrors.tuna.tsinghua.edu.cn/raspberrypi/ buster main ui

When I step on the pit again I will come back!!! Keep making it up!
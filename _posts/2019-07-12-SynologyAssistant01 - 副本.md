---
layout: post
title: 手把手教你黑群晖（一）
img: post-1.jpg
date: 2019-07-12
tag: 技术
category: 技术
---




本人是在虚拟机环境下安装的，所以准备工具用到VMware Fusion。

准备工具：

- VMware Fusion
- XPEnoboot_DS3615xs_5.2-5592.1.iso
- DSM_DS3615xs_5592.pat
- Synology Assistant

> 第一步：创建虚拟机

选择Linux2.6.x 64位

![手把手教你黑群晖（一）](http://p9.pstatp.com/large/11f70004a40f80776c4f)

![手把手教你黑群晖（一）](http://p1.pstatp.com/large/11fd00027d9215239d45)

> 第二步：选择ISO文件,并设置网卡为桥接模式

![手把手教你黑群晖（一）](http://p1.pstatp.com/large/11fb0004a7d9466e5ef2)

![手把手教你黑群晖（一）](http://p9.pstatp.com/large/11980002845d0276e4e7)

> 第三步：选择启动磁盘为CD/DVD**（很重要，不然安装完重启会发现启动不鸟）**

![手把手教你黑群晖（一）](http://p3.pstatp.com/large/11f90004b0155c324bdb)

![手把手教你黑群晖（一）](http://p9.pstatp.com/large/11fb0004b2363cbccb74)

> 第四步：运行虚拟机，选择Install/Upgrade,回车

![手把手教你黑群晖（一）](http://p1.pstatp.com/large/11f90004a744e589c8f1)

![手把手教你黑群晖（一）](http://p9.pstatp.com/large/11f70004ab2eb8b6691a)

当屏幕显示DiskStation Login，这个时候打开Synology Assistant,点击搜索，会出现你的虚拟机，显示状态为未安装

![手把手教你黑群晖（一）](http://p3.pstatp.com/large/11fc0004aa4326a024c5)

右键选择安装

![手把手教你黑群晖（一）](http://p3.pstatp.com/large/11fc0004aa42331afcd9)

进入设置向导，选择安装文件（DSM_DS3615xs_5592.pat），然后按提示一直下一步，进入安装进度界面，大概等待10几分钟安装完成。

![手把手教你黑群晖（一）](http://p3.pstatp.com/large/11f70004b0a64d0ffa84)

打开Synology Assistant，这时状态会变为已就绪，双击就会自动打开网页进入登陆界面，输入你刚刚设置的账号密码尽情享受吧！！！

![手把手教你黑群晖（一）](http://p1.pstatp.com/large/11fb0004b4a17603340a)

![手把手教你黑群晖（一）](http://p3.pstatp.com/large/11f70004b2a9e2e2c7cc)

> **下一篇会教你们怎样把把你的群晖洗白！**
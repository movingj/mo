---
layout: post
title: 手把手教你黑群晖（二）
img: post-1.jpg
date: 2019-07-12
tag: 技术
category: 技术
---

> 接上一篇，（一）说了怎样在虚拟机安装黑群晖，这一篇就说怎样把它洗白。
>
> 准备工具：
>
> 1. UltraISO
> 2. XPEnoboot_DS3615xs_5.2-5592.1.iso
>
> 把XPEnoboot引导的iso解压出来，找到 **isolinux.cfg** 文件，用记事本打开。
> ![手把手教你黑群晖（二）](http://p9.pstatp.com/large/11f700066fed2b62e0d7)
>
> 首先修改SN码为对应型号的序列号，查找文本把所有sn后面的值改为：B8LWN06204（这是经过计算之后得到的）。一共有三处
>
> 
> 然后是更改MAC地址，群晖设备MAC地址都是默认00-11-32开头的，然后在所有pid后面加上 
> mac1=001132C3468F，也是有三处的，修改完之后如图所示。
>
> ![手把手教你黑群晖（二）](http://p1.pstatp.com/large/11fc00067520f96a0187)
>
> 修改好保存文件。
>
> 用 UltraISO 打开你的.iso文件，在下方找到你刚修改好的文件的路径，右键那个文件，选择Add
>
> ![手把手教你黑群晖（二）](http://p9.pstatp.com/large/1198000452a8230a9f24)
>
> 弹出询问框，选择YES
>
> ![手把手教你黑群晖（二）](http://p1.pstatp.com/large/11fb00067c22b188439e)
>
> 替换好文件之后点击菜单栏保存。
>
> ![手把手教你黑群晖（二）](http://p1.pstatp.com/large/11fc00067709e2baa4c4)
>
> 打开VMWare Fusion选择你的虚拟机，CD/DVD 选择修改好的iso文件，运行虚拟机，打开Synology Assistant 搜索，这时会显示在网络物理地址 和型号会分别显示修改好的MAC地址和SN，如图。
>
> ![手把手教你黑群晖（二）](http://p9.pstatp.com/large/11f8000070f91dad0d36)
>
> 进入群晖系统，会发现QuickConnect 等远程功能可以使用了，不会像之前那样报错。
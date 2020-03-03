---
layout: post  
title:  "如何在Windows XP 家庭版中安装IIS"
date:  2007-06-15 04:52:00
author: Pickle Cai  
categories: EduBlog  
keywords: 
description:   
tags:	pickle   
cover:  "/assets/cover.jpg"  

---

来源：中华电脑书库，http:http://www.pcbookcn.com/article/1872.htm



       常见的Windows XP有两个版本，Professional和Home版。这两个版本大体上是相同的，只是在细节方面，Professional版比Home版多了一些功能。例如Professional版的XP支持双CPU，多国语言，加入域，EFS文件加密，以及IIS（Internet Information Services）。但是用过Windows XP Home Edition（家庭版）的朋友都会遗憾，这个系统平台没有IIS组件的安装选项，也不支持PWS（Personal Web Server），因此无法建立Web服务器来学习调试ASP动态网页。不过令人庆幸的是，国外已有行家琢磨出了一个让IIS落户WinXP 家庭版的解决方法。



       解决的思路是通过编辑Windows 组件配置文件，在Windows组件中恢复IIS安装，再按正常的方法添加IIS，详细步骤包括：



1、在X:Windowsinf目录（X为Windows XP的盘符）下打开安装信息文件sysoc.inf，

在[Components]区域中找到iis=iis.dll,OcEntry,iis.inf,hide,7这一行。

可以发现，WinXP 家庭版是把IIS组件安装选项隐藏了，因此要把该信息改为

iis=iis.dll,OcEntry,iis2.inf,,7，保存退出。



2、在Windows 2000安装光盘（Professional、Server、Advanced Server版本都可以）中找到iis.dl_和iis.if_两个文件，一起拷贝到硬盘某个目录（如C:）。打开开始菜单中的“命令提示符”，使用Expand命令解开iis.dl_和iis.if_，命令格式为：

expand  C:iis.dl_  C:iis2.dll

expand  C:iis.in_  C:iis2.inf

完成后，C盘目录下会生成iis2.dll和iis2.inf两个新文件。



3、最后，分别将iis2.dll和iis2.inf两个文件相应拷入X:Windowsinf和X:Windowssystem32Setup系统目录。



      至此，在“添加/删除程序”中点击“添加/删除Windows组件”，你会兴奋的发现，久违的Internet信息服务（IIS）重新出现了！接下来就是循规蹈矩安装IIS。但需要提醒一点，在安装过程中若跳出定位相关文件时，请把目录指向Windows 2000安装光盘下的I386目录。



      好了，再请大家注意，在Windows XP家庭版、专业版中安装的IIS，同时并发连接数限制了只有10个，因此建议想用IIS搭建Web服务器学习ASP的朋友，最好选用Windows 2000 Advanced Server系统平台。



      在windows xp下安装了iis后，只支持一个站点，而且没有站点管理，最大只能建立10个并发连接。总之，xp的home与Professional版本，毕竟是工作站操作系统而不是服务器平台。如果你喜欢玩具，那么就凑合着用xp吧





		    

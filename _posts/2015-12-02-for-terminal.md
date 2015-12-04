---
layout: post  
title:  "抛弃鼠标：For win党"  
date:   2015-12-02 08:21:30  
author: Pickle Cai  
categories: Myself  
keywords: pickle,terminal,os  
description: 这是一篇关于win环境下常用命令的教程。  
tags:	pickle   
cover:  "/assets/funterminal.png"  

---  

## 关于命令行  

本篇大部分命令都能在winpowshell下成执行，极少数命令执行时的表现有所不同。不能执行的命令单独列出。

### preface
操作系统都是从命令行开始的。20年前，第一批学计算机的那些人，除了金山打字通，就是在输入dos命令。不过那会儿还不叫命令行，因为别无可选，大概是windows3.1或者什么版本吧，学校机房的这些机器，只有很少机器装了。大部分机，就是开机，看彩色的五角星闪过，进入黑乎乎的界面，听从老师的命令，敲下命令，然后在金山打字通或者wps的界面出现后，眼前一亮，哦，终于离开令人生畏的黑色界面了。  

令人生畏，这个词无关乎界面颜色。  

现在，重新回来挑战！  

### 新知  

1. bash  
> bash，Unix shell的一种，在1987年由布莱恩·福克斯为了GNU计划而编写。1989年发布第一个正式版本，原先是计划用在GNU操作系统上，但能运行于大多数类Unix系统的操作系统之上，包括Linux与Mac OS X v10.4都将它作为默认shell。它也被移植到Microsoft Windows上的Cygwin与MinGW，或是可以在MS-DOS上使用的DJGPP项目。在Novell NetWare与Android在上也有移植。1990年后，Chet Ramey成为了主要的维护者。为Bourne shell的后继兼容版本与开放源代码版本，它的名称来自Bourne shell（sh）的一个双关语（Bourne again / born again）：Bourne-Again SHell。  
> ——[bash - 维基百科](https://zh.wikipedia.org/wiki/Bash)  

2. mac的区别  
 - mac等不分盘符，文件以文件树的形式组织。  
 - .开头为隐藏文件。  
 - 文件名和命令，大小写敏感。  
 - 类unix系统不用文件扩展名决定内容或用途。  

### 基本命令实践  

#### 1. 试运行  
1. 路径命令  
 - pwd  
全称是print work directory，显示当前路径。    
在win powshell下：  
![](http://i5.tietuku.com/2df0ef42dc0f0847.png)    
 
 - cd 
改变路径。  
四种用法，cd后要加空格再加后续符号。  
![](http://7xotr7.com1.z0.glb.clouddn.com/15-12-2/78500236.jpg)  
命令行进去 后的默认位置，为“主目录”。  
相对路径：开始于当前目录  
在win powshell下：  
![](http://7xotr7.com1.z0.glb.clouddn.com/15-12-2/32169051.jpg)    

2. 查看命令  
 - ls  
查看目录内容。  
在win powshell下：  
![](http://7xotr7.com1.z0.glb.clouddn.com/15-12-2/42389593.jpg)  
ls配合相对路径用法：  
![](http://7xotr7.com1.z0.glb.clouddn.com/15-12-2/98101821.jpg)  
相对路径中.和~的区别：  
![](http://7xotr7.com1.z0.glb.clouddn.com/15-12-2/14338391.jpg)  

 - 其他查看命令：  
![](http://7xotr7.com1.z0.glb.clouddn.com/15-12-2/49623554.jpg)
 - cat  
在win powshell下：  
![](http://7xotr7.com1.z0.glb.clouddn.com/15-12-2/61137155.jpg)  

3. 创建和删除命令  
（分别为make和remove）  
 - mkdir  
创建目录。  
在win powshell下：   
![](http://7xotr7.com1.z0.glb.clouddn.com/15-12-2/52003107.jpg)  
 - rmdir  
删除空目录。  
在win powshell下，执行后直接返回当前路径，无结果显示。但到目录中查看或者使用dir，会发现空目录已删除。  
**注意：这种删除是不经过回收站的。到回收站查看，不存在刚刚已删除的空文件夹。**  
在win powshell下，当文件夹非空时，使用该命令会给出提示和选择：  
![](http://7xotr7.com1.z0.glb.clouddn.com/15-12-2/16817198.jpg)  
 - 创建文件  
![](http://7xotr7.com1.z0.glb.clouddn.com/15-12-2/85279120.jpg)
在win powshell下，echo可以执行，其他不能。    
![](http://7xotr7.com1.z0.glb.clouddn.com/15-12-2/81321629.jpg)
 - rm  
删除文件或有内容的文件夹。参数 - r用来删除有内容的文件夹。    
![](http://7xotr7.com1.z0.glb.clouddn.com/15-12-2/25256439.jpg)  
在win powshell下：   
删除文件：  
![](http://7xotr7.com1.z0.glb.clouddn.com/15-12-2/18714824.jpg)  
删除文件夹，比较带参数 -r和不带参数的区别：  
![](http://7xotr7.com1.z0.glb.clouddn.com/15-12-2/24416488.jpg)  
**删除的危险命令**  
强制删除，且无确认信息！  
![](http://7xotr7.com1.z0.glb.clouddn.com/15-12-2/39814387.jpg)  

4. 复制和移动命令  
 - cp 
即copy，复制。  
![](http://7xotr7.com1.z0.glb.clouddn.com/15-12-2/62666702.jpg)  
用图形界面复制会更方便。但隐藏文件的复制使用命令行。    
在win powshell下：  
![](http://7xotr7.com1.z0.glb.clouddn.com/15-12-2/21724161.jpg)  
复制完并不提示。但到那个目录下去查看会看到新复制的文件。  
 - mv 
即move，移动。作用：移动，改名。    
![](http://7xotr7.com1.z0.glb.clouddn.com/15-12-2/2181154.jpg)  
在win powshell下：  
可以移动，命令执行完没有提示。  
加了参数 -v，就有提示了：  
![](http://7xotr7.com1.z0.glb.clouddn.com/15-12-2/62937300.jpg)
可以改名，但要用空格代替.  
![](http://7xotr7.com1.z0.glb.clouddn.com/15-12-2/88818743.jpg)

#### 2. win下不可行  
 - cd-（或加空格），未成功。    
 - ls
ls的其他几个用法在powshell中不可用：  
![](http://7xotr7.com1.z0.glb.clouddn.com/15-12-2/97114727.jpg)  
 - file和less  
在win powshell下不可运行：   
![](http://7xotr7.com1.z0.glb.clouddn.com/15-12-2/74601566.jpg)    
![](http://7xotr7.com1.z0.glb.clouddn.com/15-12-2/77121652.jpg)  
 - touch和> 
![](http://7xotr7.com1.z0.glb.clouddn.com/15-12-2/31363595.jpg)  
 - cp  
参数 -l，应该要提示，在win下不提示。  
 - rm  
删除的确认参数： -i  
![](http://7xotr7.com1.z0.glb.clouddn.com/15-12-2/34915702.jpg)
在win powshell下的表现是这样的：  
![](http://7xotr7.com1.z0.glb.clouddn.com/15-12-2/3558620.jpg)

#### 3. 问题  

 - 使用了~后，再用省略了/的用法就会出错。   
![](http://7xotr7.com1.z0.glb.clouddn.com/15-12-2/81854137.jpg)  
 - 复制中的连续递归复制是什么意思？文件特性复制又是什么意思？  
懂了，循环递归就是连子文件夹一起操作，直至文件夹最深层。  

### 工具使用  

#### 1. 试运行  
1. 时间  
 - date 
![](http://7xotr7.com1.z0.glb.clouddn.com/15-12-2/73325330.jpg)  
在win powshell下：   
![](http://7xotr7.com1.z0.glb.clouddn.com/15-12-2/52783349.jpg)

#### 2. win下不可行     
 - date  
带参数的用法：  
![](http://7xotr7.com1.z0.glb.clouddn.com/15-12-2/39777723.jpg)
 - cal  
![](http://7xotr7.com1.z0.glb.clouddn.com/15-12-2/3879752.jpg)
在win powshell下：   
![](http://7xotr7.com1.z0.glb.clouddn.com/15-12-2/62121380.jpg)  
 - bc   
![](http://7xotr7.com1.z0.glb.clouddn.com/15-12-2/68352055.jpg)
在win powshell下：  
![](http://7xotr7.com1.z0.glb.clouddn.com/15-12-2/13184512.jpg) 
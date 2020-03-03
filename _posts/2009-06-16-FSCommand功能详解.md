---
layout: post  
title:  FSCommand功能详解  
date:  2009-06-16 11:47  
author: Pickle Cai  
categories: EduBlog  
keywords: 
description:   
tags:	pickle   
cover:  "/assets/cover.jpeg"  

---  
    
fscommand(cmd_string, arg_string) 执行主机端指令。



 





cmd_string指定所要执行的指令名，可为FlashPlayer的指令或浏览器javascript函数。arg_string声明该指令所用到的参数。





FlashPlayer的指令有（只能在独立播放器时使用）： 

"fullscreen" 是否全屏播放，参数为true或false 

"allowscale" 是否允许通过拉伸窗口缩放影片，参数为true或false 

"showmenu" 是否在播放器显示菜单，参数为true或false 

"trapallkeys" 是否屏蔽播放器的快捷键（如Esc表示停止播放并恢复 

"save" 隐藏属性,作用是存变量到文本文件.视窗显示），参数为true或false。但Alt+F4系统快捷键（关闭窗口）依然可用。 

"exec" 运行arg_string所指定的文件。



		    
 中国教育在线·教育人


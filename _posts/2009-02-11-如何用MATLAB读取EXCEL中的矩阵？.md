---
layout: post  
title:  '"' + 如何用MATLAB读取EXCEL中的矩阵？  + '"'
date:  2009-02-11 02:49 + ":00" 
author: Pickle Cai  
categories: EduBlog  
keywords: 
description:   
tags:	pickle   
cover:  "/assets/cover.jpeg"  

---  
    


打开Matlab后，使用open打开你要的文件的文件夹，在下拉框中显示所有文件，然后选中你要的EXCEL文件就好了。如果EXCEL有几张工作表的话，可能会出错，应该保留一个工作表就可以，也不必重命名了，命名有大小写之分。 

help xlsread，还可以考虑exlink 

将EXCEL文件保存为CSV(逗号分割符）格式，同时删除表头，只留下矩阵（否则只能打开第一行）就可以直接打开了。缺省的变量名为A_____1，自己再改名就可以了。版主介绍的exlink我以前用过，也可以，但没有这种方法方便。



本文来自: 人大经济论坛(http://www.pinggu.org) 详细出处参考：http:http://www.pinggu.org/bbs/Archive_view_71_380841.html



		    
 中国教育在线·教育人


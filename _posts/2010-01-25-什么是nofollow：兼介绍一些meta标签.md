---
layout: post  
title:  什么是nofollow：兼介绍一些meta标签  
date:  2010-01-25 03:32  
author: Pickle Cai  
categories: EduBlog  
keywords: 
description:   
tags:	pickle   
cover:  "/assets/cover.jpeg"  

---  
    
Meta标签即内嵌在你网页中的特殊的html标签，它包含着关于你网页的一些隐藏信息，能让搜索引擎更好地理解你的网站内容的种类。



Yahoo!支持：





noodp——防止搜索引擎调用ODP上面的描述性语句。

Google支持：





noindex——告诉Google不要索引含此标签的网页。但根据实际经验，Google并非100%遵守。 

nofollow——告诉Google不要关注含此标签的网页里的特定链接。这是为了解决链接spam而设计的Meta标签。 

noarchive——告诉Google不要保存含此标签的网页的快照。 

nosnippet——告诉Google不要在搜索结果页的列表里显示含此标签的网站的描述语句，并且不要在列表里显示快照链接。

看到这个才发现，居然真有这样的事情。createblog中，直接会对链接自动加上rel="nofollow"代码。这段字是在a和href之间的。



eg.:

为防止所有支持元标记的搜索引擎使用此信息生成网页描述，请使用下列元标记：



要特别防止 Google 使用此信息生成网页描述，请使用下列元标记：

如果使用漫游器元标记提供其他说明，可以结合使用这些元标记:

  

		    
 中国教育在线·教育人


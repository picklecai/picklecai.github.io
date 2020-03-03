---
layout: post  
title:  "Google URL 语法"
date:  2009-10-21 05:51:00
author: Pickle Cai  
categories: Tech  
keywords: 
description:   
tags:	pickle   
cover:  "/assets/cover.jpg"  

---

每个Google查询都可以用一个URL来指向搜索结果页面。Google的搜索结果页面不是静态的，而是在你点击Search（搜索）按钮或者打开一个链接到结果页面的URL时动态创建的。





1.基本部分：起始URL





URL的第一部分“www.google.com/search”是Google的搜索脚本。这个URL以及它后面的问号称作基本部分（base）或者叫起始URL。如果浏览这个URL，你将看到一个美观的、空白页面。



search后面的问号表示参数即将传递给搜索脚本。



2.带参数的URL





参数是指命令搜索脚本实际所做的事情。参数之间用"&"符号进行分隔，每个参数由一个变量名、等于号(=)和该变量的值所组成。



大多数情况所需要的唯一的URL参数是一个查询（q参数）。这样就可以构造出最简单的Google URL：www.google.com/search?q=***。



例如，考虑查询pickle。当你输入这个查询之后，Google立即转向类似于下面的URL：



www.google.com/search?q=pickle。



带参数的URL基本语法如下所示：



www.google.com/search?variable1=value&variable2=value



这个URL包含了非常简单的字符。更为复杂的URL将包含某些必须由等价的十六进制代码表示的特定字符。



3.特殊字符





在查询URL中需要包含特殊字符时，这些特殊字符用十六进制表示。用%表示接下来的输入为十六进制所代表的特殊字符。例如：20表示空格，22表示双引号。



可以在Google中搜索"ascii table"来快速地查看字符的十六进制编码。



4.参数





参数变量表：



 



语言表：



一些参数的值为语言限定(lr)代码。lr的值命令Google只返回指定语言的页面。例如lr=lang_ar只返回以阿拉伯语所书写的页面。



 





理解hl和lr的不同：



变量hl可改变Google的消息和链接的语言。它既和限定结果页面语言的变量lr不同，也和把页面由一种语言翻译成另外一种语言的翻译服务不同。



图1.17显示出把变量hl的值设为DA（Danish，丹麦语）之后，搜索单词food的结果页面。注意到Google的消息和链接都是丹麦语，而搜索的结果却用英语显示。因为我们并没有要求Google限定或者修改查询。











498)this.style.width=498;" height=267> 



（点击查看大图）图1.17　使用变量hl



为了更好地理解变量hl和lr之间的不同，可以尝试把查询food重新提交为一个lr搜索，如图1.18所示。注意URL的不同：此时的结果比之前少了许多，结果是以丹麦语所写，Google增加了一个"丹麦语网页"（Search Danish）的按钮，且Google的消息和链接语言为英语。不同于选项hl（表1.4列出了hl域的值），选项lr可以改变我们的搜索结果。我们要求Google只返回用丹麦语书写的页面。













498)this.style.width=498;" height=263> 



（点击查看大图）图1-18 使用语言限制



hl语言域的值



 

 

		    



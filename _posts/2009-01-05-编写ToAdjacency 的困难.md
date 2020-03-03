---
layout: post  
title:  编写ToAdjacency 的困难  
date:  2009-01-05 09:44  
author: Pickle Cai  
categories: EduBlog  
keywords: 
description:   
tags:	pickle   
cover:  "/assets/cover.jpeg"  

---  
    
From ：长方形表格；



To：邻接的正方形矩阵；



Problem Space：





用array、matrix或什么形式来存储？ 

cell数组如何判断是否为空？ 

cell数组如何赋值？ 有关系赋1无关系赋0如何实现？ 

cell如何判断元素是否已经出现？ 

这一段很奇怪，

for b1=2:m-1;

    for b2=2:m-1;

        if isnan(b{b1,b2})

            b{b1,b2}=0;

        end

    end

end

无论如何总是不执行“b{b1,b2}=0;”，真不明白为什么。而且手动为b的成员赋值0是可以的。

Resolved：





用cell元组（元胞）来存储。可以存储不同类别的元素。 

if ~isnan(a{i,j})

            b{1,m+1}=a{i,j};

            b{m+1,1}=a{i,j};

            m=m+1;

end              %用isnan判空，并将“m＝m＋1”挪到if-end里面来，即实现该功能了。 

m=2;                            %用m记录累积人数；

b={};

b{1,1}=[];

for i=1:97;

    m1=m;                       %用m1记录上一行累积人数；

    for j=1:6;

        if ~isnan(a{i,j})  

            b{1,m}=a{i,j};      %搭建邻接矩阵的框架

            b{m,1}=a{i,j};             

            for b1=m1:m

                for b2=m1:m     %给邻接矩阵赋值

                    b{b1,b2}=1;

                    b{b1,b1}=0;

                end

            end  

            m=m+1;                

        end

    end    

end 

判断元素已出现，拟将原有元素另列数组，然后读取数据时与另列的数组作比较，若出现相同则出现过。但是~strcmp似乎根本就通不过调试。怎么办？

		    
 中国教育在线·教育人


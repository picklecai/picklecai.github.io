
    ---
    layout: post  
    title:  会用sumif和sumifs了  
    date:  2009-08-26 11:53  
    author: Pickle Cai  
    categories: EduBlog  
    keywords: 
    description:   
    tags:	pickle   
    cover:  "/assets/cover.jpeg"  

    ---  
    
原文是COUNTIFS($M$6:$M$2001,">=" & $AV14,$M$6:$M$2001,"单元格列中，只允许1或0的存在。所以只要countifs来计数一下即可。



今天早上Jimmy说这样太烦琐，所以改成了可以输入1到30之间的任意整数。然后countifs就出问题了。肯定的哪，这个计数结果会准确才怪。于是搜索了一下有没有条件求和（我的office没有帮助文件的），居然有。分别是sumif和sumifs。而且发现sumifs是07版本才有的。



于是照葫芦画瓢，改作：



SUMIFS($N$6:$N$2000,$N$6:$N$2000,">0",$M$6:$M$2000,">="& $AV6, $M$6:$M$2000,"sumifs的函数参数分别为：sum_range，criteria_range1，criteria1，[criteria_range2，criteria2]，……



sum_range自然是求和的目标列，criteria_range1是条件数据列，criteria1是条件本身。大于数值，就直接用双引号；大于某单元格数值，就在双引号后用&连接单元格名称。



 



另外前天学了两条：



一是冻结拆分的好处；



二是数据有效性的应用。



我本来以为数据有效性这个下拉箭头的表现，是由于用了web控件呢。原来还是这样的模子。



		    
 中国教育在线·教育人


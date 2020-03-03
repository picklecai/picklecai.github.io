
    ---
    layout: post  
    title:  又想到matlab了  
    date:  2009-04-03 02:14  
    author: Pickle Cai  
    categories: EduBlog  
    keywords: 
    description:   
    tags:	pickle   
    cover:  "/assets/cover.jpeg"  

    ---  
    
好开心啊，关键时刻，又想到了matlab。编程意识有所提升，虽然还不强烈。



刚才的思路虽然好，可是为了怎么来比较结点组，动了许多歪脑筋。一会儿将聚类结果作为属性值放进netdraw中，一会儿打算在excel中故伎重施，想想都不对。于是到网上查有没有相关工具和函数，自然是没有。可是突然想到可以自己写程序。啊！伟大的matlab！哈哈，暂时假装诗人一下，于是写了一个小的依旧是for当家的程序，决定作为附录2，先贴在这里。



然后发现光附录就有300个字了……



做完这些之后，算是把前天跟昨天的漏洞补了。不过用词非常土。自己看着昨天那个excel计算重叠，也觉得土得要命。



ps.补漏洞之后，新文已有19000字了。



 



附录2：计算集合的交和差



function compare（a{I},b{J})



m=1;n=1;



c={};d={};



for i=1:I



    for j=1:J



        if isequal(a{i},b{j})



            c{m}=b{j};



            b{j}=[];



            m=m+1;



        end



    end



end



for j=1:J



    if ~isempty(b{j})



        d{n}=b{j};



        n=n+1;



    end



end



 



		    
 中国教育在线·教育人


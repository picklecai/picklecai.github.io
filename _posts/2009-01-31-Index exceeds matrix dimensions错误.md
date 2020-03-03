
    ---
    layout: post  
    title:  Index exceeds matrix dimensions错误  
    date:  2009-01-31 04:10  
    author: Pickle Cai  
    categories: EduBlog  
    keywords: 
    description:   
    tags:	pickle   
    cover:  "/assets/cover.jpeg"  

    ---  
    
for c1=2:m;                     %c数组去除重复且顺序不变

    for c2=1:c1-1;

       if strcmpi(c{c1},c{c2})

           for c3=(c1+1):m

               c{(c3)-1}=c{c3};

           end

           c{c3}=[];

           %删除c{c1};

       end

    end

end



 



运行结果：



??? Index exceeds matrix dimensions.



Error in ==> ToAdjcency at 26

               c{(c3)-1}=c{c3};



 



搜索“ Index exceeds matrix dimensions.”，意思是矩阵的维数错误，检查矩阵运算的维数是否符合要求，应确保矩阵的size相容。



不明白。



 



断点调试，发现出错处c1＝21，c2＝19，c3=278。



c数组：……c19='金雪标' ；c20='高运川' ；c21='于金莲' ；'c22='黎安琪' ……



a数组：……a19='金雪标' ；a20='高运川' ；a21='金雪标' ；a22='于金莲' ……



说明错误是在删除c{c1}时发生的。



 



极耐心地把断点设在if处，不遗余力地按F11，直至c3＝278，这才明白，问题出在m的值上。c数组一共才277个元素，可是我的m值却是279！！！触目惊心，花了一天的功夫，才解决了这个隐藏着的毒虫。



在for之前加一句：



m=m-2；



 



现在的问题是：删除空怎么删？



'邱扶东' '方芳' [ ] [ ] [ ] [ ] [ ] [ ] [ ] [ ]……



 



断点调试真是个好方法。现在改写为：



m=m-2;

for c1=2:m;                     %c数组去除重复且顺序不变

    for c2=1:c1-1;

       if strcmpi(c{c1},c{c2})  %若出现重复，则删除后一个：c{c1};

           for c3=c1+1:m

               c{c3-1}=c{c3}; 

           end

           c(c3)=[];

           m=m-1;

       end

    end

end

运行后，到最后一步仍然出错：



??? Index exceeds matrix dimensions.



Error in ==> ToAdjcency at 25

       if strcmpi(c{c1},c{c2})  %若出现重复，则删除后一个：c{c1};



估摸着问题在于：



最后一步，c数组还有225个元素，但是c1此时的值为226，所以超出界限出错了。



怎么改？



09-02-05



这个问题绞了几天脑汁，最后一气之下把for c1=2:m;改为for c1=2:225（即最后的m值），居然就真的好了。不过心里清楚得很，这是治标不治本的改法。想解决问题，还得继续重来。幸亏，想到了办法……



		    
 中国教育在线·教育人


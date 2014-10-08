# ArrayList 和 Vector

这两个类都实现了List接口(List接口继承了Collection接口).

他们都是有序集合,即存储在这两个集合中的元素的位置都是有顺序的,相当于一种动态的数组

并且其中的数据是允许重复的

ArrayList与Vector的区别

* Vector是线程安全的,
也就是线程同步的,
而ArrayList是线程序不安全的.
对于Vector&ArrayList,
Hashtable&HashMap,
要记住线程安全的问题,
记住Vector与Hashtable是旧的,
是java一诞生就提供了的,
它们是线程安全的,
ArrayList与HashMap是java2时才提供的,
它们是线程不安全的.


* ArrayList与Vector都有一个初始的容量大小,
当存储进它们里面的元素的个数超过了容量时,
就需要增加ArrayList与Vector的存储空间,
Vector默认增长为原来两倍,而ArrayList的增长策略在文档中没有明确规定（从源代码看到的是增长为原来的1.5倍）.ArrayList与Vector都可以设置初始的空间大小,
Vector还可以设置增长的空间大小,
而ArrayList没有提供设置增长空间的方法.

**总结：即Vector增长原来的一倍,ArrayList增加原来的0.5倍. Vector 线程安全, ArrayList 不是.**


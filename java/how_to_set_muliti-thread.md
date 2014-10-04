# 如何实现 muliti-thread?

* 继续Thread类
* 实现Runable接口

# Thread 与 Runnable?

实现Runnable接口比继承Thread类所具有的优势：

* 适合多个相同的程序代码的线程去处理同一个资源

* 可以避免java中的单继承的限制

* 增加程序的健壮性，代码可以被多个线程共享，代码和数据独

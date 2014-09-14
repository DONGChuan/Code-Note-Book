# Gabage Collection

**什么是GC**

GC是垃圾收集的意思（Gabage Collection）,
内存处理是编程人员容易出现问题的地方,
忘记或者错误的内存回收会导致程序或系统的不稳定甚至崩溃,
Java提供的GC功能可以自动监测对象是否超过作用域从而达到自动回收内存的目的,
Java语言没有提供释放已分配内存的显示操作方法.

**垃圾回收器的基本原理是什么?**

当程序员创建对象时，GC就开始监控这个对象的 地址、大小以及使用情况.
通常，GC采用有向图的方式记录和管理堆（heap）中的所有对象。通过这种方式确定哪些对象是"可达的"， 哪些对象是"不可达的".当GC确定一些对象为"不可达"时(比如设置为 null)，GC就有责任回收这些内存空间.

**有什么办法主动通知虚拟机进行垃圾回收?**

可以.程序员可以手动执行System.gc(),通知GC运行,但是Java语言规范并不保证GC一定会执行.
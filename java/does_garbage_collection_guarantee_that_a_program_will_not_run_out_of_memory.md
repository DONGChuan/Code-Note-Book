# Does garbage collection guarantee that a program will not run out of memory?

Non.
程序员可能创建了一个对象,
以后一直不再使用这个对象,
这个对象却一直被引用,
这个对象无用但是却无法被垃圾回收器回收的
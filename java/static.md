# Static 关键字

Static 关键字表明一个成员变量或者是成员方法可以在没有所属的类的实例的情况下直接被访问

声明为 **static 的方法**有以下几条限制：

1. 仅能调用其他的 static 方法
2. 只能访问 static 变量.
3. 不能以任何方式引用 this 或 super
4. 不能被覆盖.

声明为 **static 的变量**实质上就是全局变量.
(+ final 就是全局**常**量).
当声明一个对象时,
并不产生 static 变量的拷贝,
而是该类所有的实例变量共用同一个 static 变量.

对于静态类，只能用于嵌套类内部类中。

## Reference

- [Static class in Java - GeeksforGeeks](http://www.geeksforgeeks.org/static-class-in-java/)

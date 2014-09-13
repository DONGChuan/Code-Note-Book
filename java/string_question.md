# 执行后，原始的String对象中的内容到底变了没有？

    String s = "Hello";
    s = s + " world!";

没有.
因为String被设计成不可变(immutable)类,
所以它的所有对象都是不可变对象.

在这段代码中,
s原先指向一个String对象,
内容是 "Hello",然后我们对s进行了+操作,
这时，s不指向原来那个对象了,
而指向了另一个 String对象,
内容为"Hello world!",
原来那个对象还存在于内存之中,
只是s这个引用变量不再指向它了.

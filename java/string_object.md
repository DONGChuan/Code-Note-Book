# 创建了几个String Object?二者之间有什么区别？

    String s = new String("xyz");

两个或一个,
”xyz”对应一个对象,
这个对象放在字符串常量缓冲区,
常量”xyz”不管出现多少遍,
都是缓冲区中的那一个.
New String每写一遍,
就创建一个新的对象,
它一句那个常量”xyz”对象的内容来创建出一个新String对象.
如果以前就用过’xyz’,
这句代表就不会创建”xyz”自己了,
直接从缓冲区拿.


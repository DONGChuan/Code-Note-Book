# integer 通过 == 比较

    Integer a=10;
    Integer b=10;
    Integer c=new Integer(10);
    Integer d=new Integer(10);

    System.out.println(a==b);
    System.out.println(c==d);

    System.out.println(a.equals(b));
    System.out.println(c.equals(d));

    System.out.println(a.equals(c));


结果为

    true
    false
    true
    true
    true

== 比较的是对象的引用
当且仅当比较的两个引用指向同一对象才返回true

再看一个例子

    Integer a = 127;
    Integer b = 127;
    Integer c = 128;
    Integer d = 128;
    System.out.println(a == b);
    System.out.println(c == d);


结果为

    true
    false


Integer i = XXX
看看Integer 的源代码就知道了,
其实就是Integer 把-128-127(一个字节的二进制补码) 之间的每个值都建立了一个对应的Integer 对象,
类似一个缓存.
由于Integer 是不可变类,
因此这些缓存的Integer 对象可以安全的重复使用.
Integer i = XXX,
就是Integer i = Interger.valueOf(XXX),
首先判断XXX 是否在-128-127 之间,
如果是直接return 已经存在的对象,
所以是同一个引用.
否则就只能 new 一个了,
那就是不同的引用了.

## Reference

- [java - Why does 128==128 return false but 127==127 return true in this code? - Stack Overflow](http://stackoverflow.com/questions/1700081/why-does-128-128-return-false-but-127-127-return-true-in-this-code)

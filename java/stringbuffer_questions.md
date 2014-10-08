# StringBuffer 相关问题

**题目一**

    StringBuffer 和 StringBuilder

* StringBuilder 比 StringBuffer 快
* 当需要保证线程安全的时候用 StringBuffer
* StringBuffer 是 synchronized, StringBuilder 不是.

String 类一般被认为是不可改变的.
如果需要对一个String做许多修改就需要使用StringBuffer或者StringBuilder.

在Oracle里的定义就是
"A mutable sequence of characters."

另外需要注意 String 类是 final 类不可以被继承. 有时候会在考察 final 关键字的时候考这个.



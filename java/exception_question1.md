# 异常选择题

**题目一**

下面哪个不对

1. RuntimeException is the superclass of those exceptions that must be thrown during the normal operation of the JVM

2. A method is not required to declare in its throws clause any subclasses of RuntimeExeption that might be thrown during the execution of the method but not caught.

3. An RuntimeException is a subclass of Throwable that indicates serious problems that a reasonable application should not try to catch.

4. NullPointerException is one kind of RuntimeException

答案是 3

RuntimeException an unchecked exception. It doesn't need to be explicitly declared or catched.

**题目二**

特殊情况就是里面加 return

举个例子去理解

    public int getNumber() {

        int a = 0;

        try {
            String s = "t"; ------------------------（1）
            a = Integer.parseInt(s);-----------（2）
            return a;
        } catch (NumberFormatException e) {
            a = 1;-----------------------------------（3）
            return a;-------------------------------（4）
        } finally {
            a = 2;-----------------------------------（5）
        }
    }

1、程序中标记的代码的执行顺序?
2、改程序的最后返回值(外部调用时)?

程序按顺序从上到下执行到(2),
字符"t"转换成整数失败,
产生异常并被捕获,
于是对a赋值成1,
并将此值作为此方法的返回值（可以这么认为,
该方法有一个存放返回值的空间,
此时将1放在此处).
由于存在finally块,
在返回前将该方法的内部变量a修改成2.
所以程序将按标记的顺序执行,
外部调用该方法时得到的结果是1

先执行try或catch里里面的代码，然后再执行finally，再执行try或catch里面的return.

**题目三**

写出你最常见到的5个runtime exception

ClassCastException
IllegalArgumentException
NullPointerException
IndexOutOfBoundsException
ArrayIndexOutOfBoundsException

**题目四**

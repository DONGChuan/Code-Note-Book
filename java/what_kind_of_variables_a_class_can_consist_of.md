# 一个类是由哪些变量构成的?

* Local variable 本地变量
* instance variables 实例变量
* class variables 类变量

**Local variable**

在方法体, 构造体内部定义的变量
在方法结束的时候就被摧毁

**instance variables**

在类里但是不在方法里
在类被载入的时候被实例化

**class variables**

在类里但在方法外,
加了 static 关键字.
也可以叫做静态变量

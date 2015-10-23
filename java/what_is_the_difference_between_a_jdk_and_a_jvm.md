# JDK JRE JVM?

* 解释它们的区别
* 为什么 JVM 不是平台独立的

**JDK**

Java Development Kit 用作开发, 包含了JRE, 编译器和其他的工具(比如: JavaDoc，Java调试器), 可以让开发者开发、编译、执行Java应用程序.

**JRE**

Java 运行时环境是将要执行 Java 程序的 Java 虚拟机, 可以想象成它是一个容器, JVM 是它的内容.

JRE = JVM + Java Packages Classes(like util, math, lang, awt,swing etc)+runtime libraries.

**JVM**

Java virtual machine (Java 虚拟机) 是一个可以执行 Java 编译产生的 Java class 文件 (bytecode) 的虚拟机进程, 是一个纯的运行环境.

**JVM 不是平台独立的**

Java被设计成允许应用程序可以运行在任意的平台, 而不需要程序员为每一个平台单独重写或者是重新编译. Java虚拟机让这个变为可能, 因为它知道底层硬件平台的指令长度和其他特性.

## Reference

[Diff between JRE and JVM](http://stackoverflow.com/questions/2812549/what-is-the-difference-between-the-jre-and-jvm)

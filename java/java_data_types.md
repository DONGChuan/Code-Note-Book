# Java Data Types - Java 数据类型

JVM 可以操作的数据类型分为两类: primitive types 和 reference types. 类型检查通常在编译期完成，不同指令操作数的类型可以通过虚拟机的字节码指令本身确定。

## Primitive type

JVM 所支持的基本数据类型有：数值类型(Numeric types), 布尔类型(Boolean type) 和 returnAddress 类型。其中数值类型又可以分为整型和浮点型两种。

- 整型：byte(8 bit), short(16 bit), int(32 bit), long(64 bit), char(16 bit unsigned)
- 浮点型：float(32 bit), double(64 bit)
- 布尔型：boolean 通常用 int 型表示，Oracle 中用 byte 表示
- returnAddress：一条字节码指令的操作码

## Reference type

引用类型分为三种：Class Types, Array Types 和 Interface Types, 这些引用类型的值分别由类实例、数组实例和实现了某个接口的类实例或者数组实例动态创建。引用类型中有一特殊的值`null`, 引用类型的默认值就是 null.

## 形式参数传递

基本类型作为形式参数传递不会改变实际参数，引用类型作为形式参数传递会改变实际参数。JDK1.5之后含有基本类型的包装类型，即自动拆装箱的功能，故将基本类型的相应对象作为参数传递时会自动拆箱为基本类型，故也不改变实际参数的值。

## Reference

- [Chapter 2. The Structure of the Java Virtual Machine](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-2.html)

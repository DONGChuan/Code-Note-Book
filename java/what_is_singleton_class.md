# Singleton 单例模式

Java中单例模式定义：“一个类有且仅有一个实例，并且自行实例化向整个系统提供。”

```java
public class Singleton {
    private Singleton() {
        // do something
    }
    private static class SingletonHolder {
        private static final Singleton INSTANCE = new Singleton();
    }
    public static final Singleton getInstance() {
        return SingletonHolder.INSTANCE;
    }
}
```

多选题注意
* 一是单例模式的类只提供私有的构造函数
* 二是类定义中含有一个该类的静态私有对象
* 三是该类提供了一个静态的公有的函数用于创建或获取它本身的静态私有对象。

## Reference

- [深入浅出单实例Singleton设计模式 | 酷壳 - CoolShell.cn](http://coolshell.cn/articles/265.html)

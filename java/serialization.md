# 序列化 serialization

Serialization is a mechanism by which you can save the state of an object by converting it to a byte stream.

JAVA中实现serialization主要靠两个类:

* ObjectOuputStream
* ObjectInputStream

他们是JAVA IO系统里的OutputStream和InputStream的子类

自定义序列化的作用如下：

1. Persist only meaningful data. 
2. Manage serialization between different versions of your class. 
3. Avoid exposing the serialization mechanism to client API.

## Reference

- [The Java HotSpot: Customizing Java Serialization [Part 2]](http://javawithswaranga.blogspot.com/2011/09/customizing-java-serialization-part-2.html)

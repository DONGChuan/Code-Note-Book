# HashMap 和 Hashtable

Hashtable是基于陈旧的Dictionary类的
HashMap是Java 1.2引进的Map接口的一个实现

Hashtable是线程安全的，也就是说是同步的
而HashMap是线程序不安全的，不是同步的

只有HashMap可以让你将空值null作为一个表的条目的key或value. 但是 HashTable 不允许


# HashMap HashTable LinkedHashMap TreeMap

不允许键重复，值可以重复。

HashMap是一个最常用的Map, 它根据键的hashCode值存储数据,
根据键可以直接获取它的值,
具有很快的访问速度.
HashMap最多只允许一条记录的键为null,
不允许多条记录的值为null.
HashMap不支持线程的同步,
如果需要同步,
可以用Collections.synchronizedMap(HashMap map)方法使HashMap具有同步的能力.

Hashtable与HashMap类似,
不同的是:
它不允许记录的键或者值为空;
它支持线程的同步.

LinkedHashMap保存了记录的插入顺序,
在用Iteraor遍历LinkedHashMap时,
先得到的记录肯定是先插入的.
在遍历的时候会比HashMap慢.
有HashMap的全部特性.

TreeMap能够把它保存的记录根据键排序,
默认是按升序排序,
也可以指定排序的比较器.
当用Iteraor遍历TreeMap时,
得到的记录是排过序的.
TreeMap的键和值都不能为空.

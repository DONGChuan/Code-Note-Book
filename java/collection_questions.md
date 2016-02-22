# Collection 相关问题

**题目一**

    You need to store elements in a collection that guarantees that no duplicates are stored and all elements can be access in nature order, which interface provies that capabiliy?

    A. java.util.Map
    B. java.util.Collection
    C. java.util.List
    D. java.util.Set

答案 D

**题目二**

    List, Set, Map是否继承自Collection接口,它们有什么区别?

List，Set是，Map不是

Set 不允许有重复的元素.且没有顺路 Set取元素时,没法说取第几个,只能以Iterator接口取得所有的元素,再逐一遍历各个元素.

List表示有先后顺序的集合并且允许重复

Map与List和Set不同，存储一对key/value，不能存储重复的key

**题目三**

```
public static void main(){
    Map<String,String> map = new HashMap<String,String>();
    map.out(String.valueOf(System.currentTimeMillis())+"a",1);
    map.out(String.valueOf(System.currentTimeMillis())+"a",2);
    map.out(String.valueOf(System.currentTimeMillis())+"a",3);
    for(Map.Entry<String,String> entry : map.entrySet()){
        System.out.printf(entry.getValue());
    }
}```

输出顺序是 123顺序无法确定. Map 中的键是 Set. Set 顺序是随机的.

# equals 与 ==

* == 比较对象的引用
* equals 比较对象的值

**题目一**
```
public class Test{
    public static void main(String[] args){
        String s1 = "abc";
        String s2 = s1;
        String s3 = new String("abc");
        String s4 = new String("abc");
        String s5 = "abc";

        System.out.println(s1==s5);
        System.out.println(s1==s2);
        System.out.println(s1.equals(s2));
        System.out.println(s3==s4);
        System.out.println(s1.equals(s4));
        System.out.println(s3.equals(s4));
    }
}```

输出是 true true true false true true

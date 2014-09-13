# equals() 与 hashcode()

### **Equal **

如果需要比较对象的值，就需要equal方法了.
看一下JDK中equal方法的实现：

    public boolean equals(Object obj) {
        return (this == obj);
    }

也就是说，默认情况下比较的还是对象的地址. 所以如果把对象放入Set中等操作，就需要重写eqaul方法了

重写之后的 equals() 比较的就是对象的内容了


### **hashcode **

When inserting an object into a hastable you use a key. The hash code of this key is calculated, and used to determine where to store the object internally. When you need to lookup an object in a hashtable you also use a key. The hash code of this key is calculated and used to determine where to search for the object.

The hash code only points to a certain "area" (or list, bucket etc) internally. Since different key objects could potentially have the same hash code, the hash code itself is no guarantee that the right key is found. The hashtable then iterates this area (all keys with the same hash code) and uses the key's equals() method to find the right key. Once the right key is found, the object stored for that key is returned.

So, as you can see, a combination of the hashCode() and equals() methods are used when storing and when looking up objects in a hashtable.

**If equal, then same hash codes too.**
**Same hash codes no guarantee of being equal.**

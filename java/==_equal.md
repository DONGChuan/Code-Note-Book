# == 和 equal 的区别

总结

* **== 比地址**

* **equel 覆写之后比内容**

The “==” operator compares the objects’ **location(s) in memory**

    String obj1 = new String("xyz");

    String obj2 = new String("xyz");
    // If String obj2 = obj1, the output will be true

    if(obj1 == obj2)
       System.out.printlln("obj1==obj2 is TRUE");
    else
      System.out.println("obj1==obj2 is FALSE");

      Resultat: obj1==obj2 is FALSE


By default, the equals() method actually behaves the same as the “==” operator ( 在object类里 ). But, the equals method is actually meant to compare the contents of 2 objects, and not their location in memory. (因为每个类都继承了 object 类并覆写了这个方法)

    String obj1 = new String("xyz");

    String obj2 = new String("xyz");

    if(obj1.equals(obj2))
       System.out.printlln("obj1==obj2 is TRUE");
    else
      System.out.println("obj1==obj2 is FALSE");

     Resultat: obj1==obj2 is TRUE

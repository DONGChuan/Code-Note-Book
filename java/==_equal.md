# == 和 equal 的区别

* **== 比较引用的地址**
* **equel 比较引用的内容** (Object 类本身除外)


    String obj1 = new String("xyz");
    String obj2 = new String("xyz");

    // If String obj2 = obj1, the output will be true

    if(obj1 == obj2)
        System.out.printlln("obj1==obj2 is TRUE");
    else
        System.out.println("obj1==obj2 is FALSE");

    // It will print obj1==obj2 is False
    // If String obj2 = obj1, the output will be true

默认的, equals() 方法实际上和 “==” 在 object 类里是一样的. 但是这个方法在每一个子类里都会被覆写用来比较引用的内容 (因为每个类都继承了 object 类并覆写了这个方法)

    String obj1 = new String("xyz");
    String obj2 = new String("xyz");

    if(obj1.equals(obj2))
       System.out.printlln("obj1==obj2 is TRUE");
    else
      System.out.println("obj1==obj2 is FALSE");

     Resultat: obj1==obj2 is TRUE

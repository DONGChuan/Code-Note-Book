# super 关键词

* 调用父类 (Superclass) 的成员或者方法
* 调用父类的构造函数


1. 调用父类 (Superclass) 的成员或者方法

如果你的方法覆写一个父类成员的方法, 你可以通过 super 关键字调用父类的方法. 考虑下面的父类:

    public class Superclass {

        public void printMethod() {
                System.out.println("Printed in Superclass.");
            }
    }

下面是一个子类 (subclass), 叫做 Subclass, 覆写了 printMethod():

    public class Subclass extends Superclass {

        // overrides printMethod in Superclass
        public void printMethod() {
            super.printMethod();
            System.out.println("Printed in Subclass");
        }
        public static void main(String[] args) {
            Subclass s = new Subclass();
            s.printMethod();
        }
    }

输出

    Printed in Superclass.
    Printed in Subclass


2. 调用父类的构造函数

使用 **super** 关键字调用父类的构造函数. 下面的 MountainBike 类是 Bicycle 类的子类. 它调用了父类的构造方法并加入了自己的初始化代码:

    public MountainBike(int startHeight,
                        int startCadence,
                        int startSpeed,
                        int startGear) {
        super(startCadence, startSpeed, startGear);
        seatHeight = startHeight;
    }

调用父类的构造体必须放在**第一行**.

使用

    super();

或者:

    super(parameter list);

通过 super(), 父类的无参构造体会被调用. 通过 super(parameter list), 父类对应参数的构造体会被调用.

注意: 构造体如果没有显式的调用父类的构造体, Java 编译器自动调用父类的无参构造. 如果父类没有无参构造, 就会报错 ( compile-time error).

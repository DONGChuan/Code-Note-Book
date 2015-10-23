# 多态 Polymorphism

多态就是指一个变量, 一个方法或者一个对象可以有不同的形式.

多态主要分为

* 重载overloading


    就是一个类里有两个或更多的函数，名字相同而他们的参数不同.

* 覆写overriding


    是发生在子类中！也就是说必须有继承的情况下才有覆盖发生. 当你继承父类的方法时, 如果你感到哪个方法不爽，功能要变，那就把那个函数在子类中重新实现一遍.

**例子**

重载 静态捆绑 (static binding) 是 Compile 时的多态

    EmployeeFactory.create(String firstName, String lastName){...}
    EmployeeFactory.create(Integer id, String lastName){...}

覆写 动态捆绑 (dynamic binding) 是 runtime 多态

    public class Animal {
        public void makeNoise()
        {
            System.out.println("Some sound");
        }
    }

    class Dog extends Animal{
        public void makeNoise()
        {
            System.out.println("Bark");
        }
    }

    class Cat extends Animal{
        public void makeNoise()
        {
            System.out.println("Meawoo");
        }
    }


    public class Demo
    {
        public static void main(String[] args) {
            Animal a1 = new Cat();
            a1.makeNoise(); //Prints Meowoo

            Animal a2 = new Dog();
            a2.makeNoise(); //Prints Bark
        }
    }

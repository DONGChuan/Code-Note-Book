# 基础程序题

**题目一**

    class Base{}

    class Agg extends Base{
        public String getFields(){
            String name = "Agg";
            return name;
        }
    }

    public class Avf{
        pulic static void main(String argv[]){
            Base a = new Agg();
            //here
        }
    }

下面哪个选项的代码替换到//here会调用getFields方法,使出书结果是Agg

    A. System.out.println(a.getFields());
    B. System.out.println(a.name);
    C. System.out.println((Base)a.getFields());
    D. System.out.println(((Agg)a).getFields());

答案 D

Base 类要引用 Agg 类的实例需要把 Base 类显示地转换成 Agg 类,然后调用 Agg 类中的方法. 如果 a 是 Base 类的一个实例,是不存在这个方法的,必须把 a 转换成 Agg 的一个实例

**题目二**

    class A{

        public A(){
            System.out.println("A");
        }
    }

    public class B extends A{

        public B(){
            System.out.println("B");
        }

        public static void main(String[] args){
            A a = new B();
            a = new A();
        }
    }

输出结果是 A B A

**题目三**

    class A{
        public void print(){
            System.out.println("A");
        }
    }

    class B extends A{
        public void print(){
            System.out.println("B");
        }
    }

    public class Test{
        ..
        B objectB = new B();
        objectB.print();

        A as = (A) objectB;
        as.print();

        A asg = objectB;
        asg.print();

        as = new A();
        as.print();
        ..
    }

输出为 B B B A

**题目四**

    public class Test {
        public static void main(String[] args){
            Father father = new Father();
            Father child = new Child();
            System.out.println(father.getName());
            System.out.println(child.getName());
        }
    }

    class Father{
        public static String getName(){
            return "Father";
        }
    }

    class Child extends Father{
        public static String getName(){
            return "Child";
        }
    }

输出是 Father Father 因为这里的方法 getName 是静态的. 具体执行哪一个,则要看是由哪个类来调用的.












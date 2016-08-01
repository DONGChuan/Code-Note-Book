# abstract 相关问题

**题目一**

什么是抽象类

1. A class with no methods
2. A class with no concrete subclasses
3. A class with at least one undefiend message
4. None of above

答案是 4 我们是可以定义一个抽象空类的

    abstract class emptyAb {}

**题目二**

    abstract class Base{
        abstract public void myfunc();
    }

    public class Abs extends Base{
        public static void main(String argv[]){
            Abs a = new Abs();
            a.amethod();
        }

        public void amethod(){
            System.out.println("A method");
        }
    }

运行的结果

1. 输出 A method
2. The code will compile but complain at run time
3. The compiler will complain errors in Abs class

答案是 3

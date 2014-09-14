# this 程序题

**题目一**

    class Tester{
        int var;
        Tester(double var){this.var = (int)var};
        Tester(int var){this("hello");
        Tester(String s){
            this();
            System.out.println(s);
        }

        Tester(){ System.out.println("good-bye");}
    }

Tester t = new Tester(5) 的输出是什么?

    good-bye
    hello


**题目二**

貌似和 this 无关但是很重要
    public class Base {
    	int i;

    	Base(){
    		add(1);
    		System.out.println(i);
    	}

    	void add(int v){
    		i+=v;
    		System.out.println(i);
    	}
    }

    public class MyBase extends Base{
    	MyBase(){
    		System.out.println("MyBase");
    		add(2);
    	}

    	void add(int v){
    		System.out.println("MyBase Add");
    		i+=v*2;
    		System.out.println(i);
    	}
    }

    public class Test {
    	public static void main(String[] args) {
    		go(new MyBase());
    	}

    	static void go(Base b){
    		b.add(8);
    	}
    }

输出的结果是 22

子类会首先调用父类的构造函数,在父类的构造函数 Base() 中执行 add() 方法. 但这个 add() 方法由于是在新建 MyBase 对象时调用的. 所以是执行的 MyBase 中的 add 方法

在Java中，子类的构造过程中，必须 调用其父类的构造函数,
是因为有继承关系存在时,
子类要把父类的内容继承下来,
通过什么手段做到的？
这样：
当你new一个子类对象的时候,
必须首先要new一个父类的对像出来,
这个父类对象位于子类对象的内部,
所以说，子类对象比父类对象大,
子类对象里面包含了一个父类的对象,
这是内存中真实的情况.

构造方法是new一个对象的时候,
必须要调的方法,
这是规定,
要new父类对象出来,
那么肯定要调用其构造方法,
所以
**第一个规则：子类的构造过程中，必须 调用其父类的构造方法**

一个类,
如果我们不写构造方法,
那么编译器会帮我们加上一个默认的构造方法,
所谓默认的构造方法,
就是没有参数的构造方法,
但是如果你自己写了构造方法,
那么编译器就不会给你添加了

所以有时候当你new一个子类对象的时候，肯定调用了子类的构造方法，但是在子类构造方法中我们并没有显示的调用基类的构造方法，就是没写，如：super(); 并没有这样写，但是

**第二个规则：如果子类的构造方法中没有显示的调用基类构造方法，则系统默认调用基类无参数的构造方法**

注意：如果子类的构造方法中既没有显示的调用基类构造方法，而基类中又没有默认无参的构造方法，则编译出错，所以，通常我们需要显示的：super(参数列表)，来调用父类有参数的构造函数


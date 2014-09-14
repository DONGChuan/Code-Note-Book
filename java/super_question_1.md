# Super 程序题

**题目一**

    class Base{
        Base(){
            System.out.println("Base");
        }
    }

    public class Checket extends Base{
        Checket(){
            System.out.println("Checket");
            super();
        }
        public static void main(String argv[]){
            Checket a = new Checket();
        }
    }

输出是什么？ 是 compile time error. super() 必须放在前面.

放在前面之后,输出为 Base Checket

**题目二**

    import java.util.Date;

    public class Test extends Date{

        public static void main(String[] args) {
           new Test().test();
        }

        public void test(){
           System.out.println(super.getClass().getName());
        }
    }

返回的结果是 Test

因为super.getClass().getName() 调用了父类的 getClass() 方法, 返回当前类

如果想得到父类的名称，应该用如下代码：

    getClass().getSuperClass().getName()

**题目三**

    public abstract class Car {

        String name = "Car";

        public String getName(){
        	return name;
        }

        public abstract void demarre();
    }

    public class B extends Car{
    	String name = "B";

        public String getName(){
        	return name;
        }

    	public void demarre() {
    		System.out.println(getName() + " demarre");
    	}
    }

    public class C extends B{
    	String name = "C";

        public String getName(){
        	return name;
        }

    	public void demarreWithSuper() {
    		System.out.println(super.getName() + " demarre");
    	}

    	public void demarreNoSuper() {
    		System.out.println(getName() + " demarre");
    	}
    }

    public class D extends B{
        public String getName(){
        	return name;
        }

    	public void demarreNoSuper() {
    		System.out.println(getName() + " demarre");
    	}
    }

    public class Test {
    	public static void main(String[] args) {
    		B b = new B();
    		b.demarre();

    		Car bCar = new B();
    		bCar.demarre();

    		C c = new C();
    		c.demarre(); // c 里并没有定义这个函数
    		c.demarreWithSuper();
    		c.demarreNoSuper();

    		D d = new D();
    		d.demarre();

    		transfer(c);    // TransferC
    		transfer((B)c); // TransferB
    		transfer(d);    // TransferB
    	}

        	public static void transfer(B b){
        		System.out.println("TransferB");
        		b.demarre();
        	}

        	public static void transfer(C c){
        		System.out.println("TransferC");
        		c.demarre();
        	}
    	}
    }

输出是
B demarre
B demarre
C demarre
B demarre
C demarre
B demarre
TransferC
C demarre
TransferB
C demarre
TransferB
B demarre

# super.getClass()

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

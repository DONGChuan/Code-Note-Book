# 同步 synchronized

举个例子

    public class Synchronized Counter {
        private int c = 0;

        public synchronized void increment() {
            c++;
        }

        public synchronized void decrement() {
            c--;
        }

        public synchronized int value() {
            return c;
        }
    }

如果 count 是这个类的实例化将有两个效果:

* 不可能同时调用同一个对象的同一个方法, 防止造成冲突.同一时间只有一个线程可以调用这对象的同步方法.比如在一个账户里同时存钱和转账.

* 当一个同步方法退出时,
*它会和随后一个同步方法的调用自动建立happens-before关系. 这保证了所有线程都知道对象的状态改变了.


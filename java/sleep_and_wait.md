# sleep() 和 wait() 的区别

举个例子

```
sleep(1000)```
 会把把线程放到一边, 直到**整整**一秒之后才再次启动

```
wait(1000)```

则是把线程放到一边**至多**一秒. 如果碰到 notify() 或者 notifyAll() 就会提前启动. 

而且 wait() 方法是在 Object 类里. 而 sleep() 是在 Thread 类里.

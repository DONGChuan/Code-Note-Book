# servlet 生命周期?

1.  读取 Servlet 类
2.  创建 Servlet 实例
3.  Web 容器调用 Servlet 的 init() 方法
4.  响应客户端请求通过Servlet中service()方法中相应的doXXX()方法
5.  调用 Servlet 的 destroy()

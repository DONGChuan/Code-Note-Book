# 创建 servlet

Servlet 在容器中运行时，其实例的创建及销毁等是由容器进行控制.

Servlet 的创建有两种方法。

1. 客户端请求对应的 Servlet 时，创建 Servlet 实例.大部分Servlet 都是这种 Servlet.
2. 通过在 web.xml 中设置load-on-startup来创建servlet实例，这种实例在Web 应用启动时，立即创建 Servlet 实例


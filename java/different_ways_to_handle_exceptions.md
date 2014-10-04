# 处理异常的方法

1. By wrapping the desired code in a try block followed by a catch block to catch the exceptions.

2. List the desired exceptions in the throws clause of the method and let the caller of the method hadle those exceptions.

这两种方法有什么区别

In the first approach as a programmer of the method,
you urself are dealing with the exception.
This is fine if you are in a best position to decide should be done in case of an exception.
Whereas if it is not the responsibility of the method to deal with it's own exceptions, then do not use this approach. In this case use the second approach.

In the second approach we are forcing the caller of the method to catch the exceptions, that the method is likely to throw. This is often the approach library creators use. They list the exception in the throws clause and we must catch them. 

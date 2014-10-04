# 每一个 try 都必须有一个 catch 吗?

不是必须的. It should be followed by either a catch block OR a finally block. And whatever exceptions are likely to be thrown should be declared in the throws clause of the method.

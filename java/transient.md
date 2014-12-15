# Transient 关键字

当持久化对象时,
可能有一个特殊的对象数据成员,
我们不想用 serialization 机制来保存它. 为了在一个特定对象的一个域上关闭serialization,
可以在这个域前加上关键字transient.


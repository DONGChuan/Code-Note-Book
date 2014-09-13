# What is SessionFactory in Hibernate?

SessionFactory 是一个创建 hibernate Session 对象的工厂.

它可以作为单一的 data store 及也是线程安全的，
使多个线程可以使用相同的 SessionFactory.

一个 Java JEE 应用只有一个 SessionFactory 如果只有一个数据库的话

当创建之后关于 Object/Relational mapping 的元数据是不能改的.


# Singleton 单列模式?

Java中单例模式定义：“一个类有且仅有一个实例，并且自行实例化向整个系统提供。”

    public class SingletonClass{

    　　private static SingletonClass instance = null;

    　　public static SingletonClass getInstance(){
        　　if(instance==null){
        　　      synchronized(SingletonClass.class){
        　　          if(instance==null){
        　　          instance = new SingletonClass();
        　　          }
        　　      }
        　　}
        　　return instance;
    　　}
    　　private SingletonClass(){
    　　      //do something
    　　}
    　}

多选题注意
* 一是单例模式的类只提供私有的构造函数
* 二是类定义中含有一个该类的静态私有对象
* 三是该类提供了一个静态的共有的函数用于创建或获取它本身的静态私有对象。

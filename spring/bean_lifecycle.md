# Bean lifecycle

1. Instantiate - 容器在 XML 文件里找到定义并实例化它们

2. Populate properties - 使用 DI 填充属性

3. Set Bean Name - If the bean implements BeanNameAware interface, spring passes the bean's id to setBeanName() method.

4. Set Bean factory - If Bean implements BeanFactoryAware interface, spring passes the beanfactory to setBeanFactory() method.

5. Pre Initialization - 也叫 postprocess. Spring 调用 postProcesserBeforeInitialization() 方法.

6. Initialize beans - If the bean implements IntializingBean,its afterPropertySet() method is called. If the bean has init method declaration, the specified initialization method is called.

7. Post Initialization - 调用 postProcessAfterInitialization() 方法

8. Ready to use - 现在可以用它们了.

9. Destroy - If the bean implements DisposableBean , it will call the destroy() method .

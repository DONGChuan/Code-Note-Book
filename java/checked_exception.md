# Checked 异常与 Runtime 异常


* Runtime exceptions are those exceptions that are thrown at runtime because of either wrong input data or because of wrong business logic etc. These are not checked by the compiler at compile time.，例如，数组脚本越界（ArrayIndexOutOfBoundsException），空指针异常（NullPointerException）、类转换异常（ClassCastException

* Checked exception are those which the Java compiler forces you to catch. e.g. IOException are checked Exceptions.

编译器**强制 checked 异常必须try..catch处理或用throws声明**继续抛给上层调用方法处理,
这就是为什么叫**checked异常**,
而 Runtime 异常可以处理也可以不处理,
所以,
编译器不强制用try..catch处理或用throws声明,
所以 Runtime 异常也称为unchecked异常


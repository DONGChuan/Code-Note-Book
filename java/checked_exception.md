# Checked 异常与 Runtime 异常


* Runtime exceptions 是 runtime 阶段碰到的异常. 在编译的时候不需要检查 (checked). 例如,
数组脚本越界（ArrayIndexOutOfBoundsException) ,
空指针异常（NullPointerException）,
类转换异常（ClassCastException).

* Checked exception 是在编译阶段的异常，并且强制检查.

编译器**强制 checked 异常必须try..catch处理或用throws声明**继续抛给上层调用方法处理,
这就是为什么叫**checked异常**,
而 Runtime 异常可以处理也可以不处理,
所以,
编译器不强制用try..catch处理或用throws声明,
所以 Runtime 异常也称为unchecked异常


# Checked 异常与 Runtime 异常


* Runtime 异常是软件本身缺陷所导致的问题，也就是编程没编好,
写代码不够小心,
软件使用者无法克服和恢复这种问题,
但在这种问题下还可以让软件系统继续运行或者让软件死掉，例如，数组脚本越界（ArrayIndexOutOfBoundsException），空指针异常（NullPointerException）、类转换异常（ClassCastException

* Checked 异常是运行环境的变化或异常所导致的问题，是用户能够克服的问题，例如，网络断线，硬盘空间不够，发生这样的异常后，程序不应该死掉

编译器**强制 checked 异常必须try..catch处理或用throws声明**继续抛给上层调用方法处理,
这就是为什么叫**checked异常**,
而 Runtime 异常可以处理也可以不处理,
所以,
编译器不强制用try..catch处理或用throws声明,
所以 Runtime 异常也称为unchecked异常


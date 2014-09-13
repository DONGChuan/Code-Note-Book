# 作用域的区别

| 作用域 | 当前类 | 同一个 package | 子孙类 | 其他 package |
| -- | -- | -- | -- | -- |
| public | O| O | O | O |
| protected | O | O | O | X |
| friendly | O | O | X | X |
| private | O | X | X | X |


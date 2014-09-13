#  sorted 和 ordered collection

sorted collection是在内存中通过 java 比较器进行排序的
ordered collection是在数据库中通过 order by 进行排序的

建议使用 ordered collection 避免 OutOfMemoryError 问题.



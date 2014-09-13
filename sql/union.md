# 合并

How can you combine two tables/views together? For instance one table contains 100 rows and the other one contains 200 rows, have exactly the same fields and you want to show a query with all data (300 rows).

    SELECT column_name FROM table_name1
    UNION
    SELECT column_name FROM table_name2

注意

* UNION 内部的 SELECT 语句必须拥有相同数量的列.
* 列也必须拥有相似的数据类型.
* 每条 SELECT 语句中的列的顺序必须相同.

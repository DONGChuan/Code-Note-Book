# statement 和 prepared statement?


Statement每次执行sql语句,数据库都要执行sql语句的编译.
最好用于仅执行一次查询并返回结果的情形，效率高于PreparedStatement.

Prepared statements offer better performance, as they are **pre-compiled**. Use when you plan to use the SQL statements **many times**.

Prepared statements are more secure because they use bind variables, which can prevent SQL injection attack.

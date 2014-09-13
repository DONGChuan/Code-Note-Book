# Where 和 Having

WHERE 从句一般是在行的层级去筛选数据 (before grouping). HAVING 从句一般在 GROUP BY 之后所以是在 "groups" 的基础上删选.

更准确的说在 SQL 中增加 HAVING 子句原因是 WHERE 关键字无法与合计函数一起使用

**因为在查询过程中聚合语句(sum,min,max,avg,count)要比having子句优先执行.而where子句在查询过程中执行优先级别优先于聚合语句(sum,min,max,avg,count)**

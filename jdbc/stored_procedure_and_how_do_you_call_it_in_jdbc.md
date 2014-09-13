# Stored Procedure?

A stored procedure is a group of SQL statements that form a logical unit and perform a particular task. (粗俗的可以理解为一个定义好的方法, 提供输入就会得到对应的输出)

    CallableStatement cs = con.prepareCall("{call MY_SAMPLE_STORED_PROC}");
    ResultSet rs = cs.executeQuery();

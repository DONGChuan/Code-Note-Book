# What are the steps in the JDBC connection?

Step 1 : Register the database driver by using :
Class.forName(\" driver classs for that specific database\" );

Step 2 : Now create a database connection using :

Connection con = DriverManager.getConnection(url,username,password);

Step 3: Now Create a query using :

Statement stmt = Connection.Statement(\"select * from TABLE NAME\");

Step 4 : Exceute the query :

stmt.exceuteUpdate();

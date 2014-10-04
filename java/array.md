# 数组相关问题

**题目一**

    Which of the following are valid array declaration for srings of 50 chars?

    A. char c[][];
    B. String []s;
    C. String s[50];
    D. Object s[50];

答案 B

    int [][] iArray;
    int []iArray[];
    intt iArray[][];

都是可以得, 但数组不能直接指定列数或者行数. 正确的方式应该在创建数组对象是.

比如

    int iArray[][] = new int[3][4]

**题目二**

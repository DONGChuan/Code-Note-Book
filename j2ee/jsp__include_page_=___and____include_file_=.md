# 两者的区别
Both the tags include information from one JSP page in another. The differences are:

< jsp : include page = ... >

This is like a function call from one jsp to another jsp. It is executed each time the client page is accessed by the client. This approach is useful while modularizing a web application. If the included file changes then the new content will be included in the output automatically.

<% @ include file = ... >

In this case the content of the included file is textually embedded in the page that have < % @ include file=".."> directive. In this case when the included file changes, the changed content will not get included automatically in the output. This approach is used when the code from one jsp file required to include in multiple jsp files.

# <jsp:forward page= ...> 和 response.sendRedirect(url)?

jsp:forward 把 request object 传递给服务器里的另外一个 servlet 或者 JSP. 新的 servlet 或者 JSP 继续处理同一个 request and the 但浏览器并不知道这些. 在浏览器里的 URL 不变.

response.sendRedirect() 创建了一个新的 request object, 不携带旧的 request object 的信息. The first request handler JSP page tells the browser to make a new request to the target servlet or JSP page. 在浏览器里的 URL 改变.

# 都有哪些 bean scope?

* singleton: Return a single bean instance per Spring IoC container

* prototype:  Return a new bean instance each time when requested

* request: Return a single bean instance per HTTP request

* session: Return a single bean instance per HTTP session

* global-session: Return a single bean instance per global HTTP session

**默认的是 singleton**


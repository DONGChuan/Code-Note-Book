
# JSP 的生命周期?

1. Compilation
2. Initialization
3. Execution
4. Cleanup

详细解释

Compilation: When a browser asks for a JSP, the JSP engine first checks to see whether it needs to compile the page. If the page has never been compiled, or if the JSP has been modified since it was last compiled, the JSP engine compiles the page.

编译的三个步骤:

1. Parsing the JSP.
2. Turning the JSP into a servlet.
3. **Compiling the servlet.**

Initialization: When a container loads a JSP it invokes the jspInit() method before servicing any requests

Execution: Whenever a browser requests a JSP and the page has been loaded and initialized, the JSP engine invokes the _jspService() method in the JSP.The _jspService() method of a JSP is invoked once per a request and is responsible for generating the response for that request and this method is also responsible for generating responses to all seven of the HTTP methods ie. GET, POST, DELETE etc.

Cleanup: The destruction phase of the JSP life cycle represents when a JSP is being removed from use by a container.The jspDestroy() method is the JSP equivalent of the destroy method for servlets.

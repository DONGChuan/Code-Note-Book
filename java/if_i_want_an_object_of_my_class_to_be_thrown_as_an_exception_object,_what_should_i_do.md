# If I want an object of my class to be thrown as an exception object, what should I do?

The class should extend from Exception class. Or you can extend your class from some more precise exception type also.

# If my class already extends from some other class what should I do if I want an instance of my class to be thrown as an exception object?

One can not do anytihng in this scenarion. Because Java does not allow multiple inheritance and does not provide any exception interface as well.

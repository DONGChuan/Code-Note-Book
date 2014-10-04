# If I write return at the end of the try block, will the finally block still execute?

Yes even if you write return as the last statement in the try block and no exception occurs, the finally block will execute. The finally block will execute and then the return.

# If I write System.exit (0); at the end of the try block, will the finally block still execute?

No in this case the finally block will not execute because when you say System.exit (0); the control immediately goes out of the program, and thus finally never executes.

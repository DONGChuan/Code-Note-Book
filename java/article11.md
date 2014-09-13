# Article11

How could Java classes direct program messages to the system console, but error messages, say to a file?


The class System has a variable out that represents the standard output, and the variable err that represents the standard error device. By default, they both point at the system console. This how the standard output could be re-directed:

    Stream st = new Stream(new FileOutputStream("output.txt"));

    System.setErr(st);
    System.setOut(st);

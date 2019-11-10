## Consider static factory methods instead of constructors

### Advantage - Static factory methods have names
A class can have only a single constructor with a given signature. Programmers
have been known to get around this restriction by providing two constructors
whose parameter lists differ only in the order of their parameter types. This is a
really bad idea. The user of such an API will never be able to remember which
constructor is which and will end up calling the wrong one by mistake.

### Disadvantage - They are not readily distinguishable from other static methods
They do not stand out in API
documentation in the way that constructors do, so it can be difficult to figure out
how to instantiate a class that provides static factory methods instead of constructors.
The Javadoc tool may someday draw attention to static factory methods. In
the meantime, you can reduce this disadvantage by drawing attention to static factories
in class or interface comments, and by adhering to common naming conventions.

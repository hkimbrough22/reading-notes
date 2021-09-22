# Code 401 - Reading Notes

<!-- All references used were from Code 401 reading
assignment 03 -->

## Maps, Primitives, File I/O
### Primitives versus Objects
[comment]: <> (Maps, Primitives, File I/O)
Primitives - int, boolean, char
Reference Types - Integer, Boolean, Character

The decision what object is to be used is based on what application performance we try to achieve, how much available memory we have, the amount of available memory and what default values we should handle.
- boolean – 1 bit
- byte – 8 bits
- short, char – 16 bits
- int, float – 32 bits
- long, double – 64 bits 
- As we've seen, the primitive types are much faster and require much less memory. Therefore, we might want to prefer using them.

### Exceptions
[comment]: <> (https://docs.oracle.com/javase/tutorial/essential/exceptions/definition.html)
Method creates an object and hands it off to the runtime system. 
The exception object contains information about the error, including its type and the state of the program when the error occurred. 
This is called throwing an exception.

After, the runtime system attempts to handle the exception.
The set of items in an ordered list of methods that had been called to get to the method where the error occurred. The list of methods is known as the call stack.

Searches the call stack to handle the exception. This block of code is called an exception handler. Proceeds through the call stack in the reverse order in which the methods were called. An exception handler is considered appropriate if the type of the exception object thrown matches the type that can be handled by the handler.

The exception handler chosen is said to catch the exception.

[BACK TO HOME](../README.md)

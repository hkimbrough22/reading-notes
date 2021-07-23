# Code 201 - Reading Notes
<!-- All notes were taken from Reading assignment 10 references in Jon Duckett's book -->
## Debugging
### The Console and Dev Tools
- Understand order of execution, execution context, and variable scope
- Execution - Global Context, Function Context, and Eval Context
- Variable - Global scope, function-level scope
#### The Stack
- The JS interpreter processes one line of code at a time and when a statement needs data from another function it stacks (or piles) the new function on top of the current task.
-Lexical scope - linked to the object they were defined within.
### Common Problems
- Error
- SyntaxError
- ReferenceError
- TypeError
- RangeError
- URIError
- EvalError
### Error Handling
- Debug
- `try`, `catch`, `throw`, `finally` statements
- Identify where the problem is and what it is
- Use browser dev tools and JS console with `console.log()`
- `console.info()`, `console.warn()`, `console.error()`
- Can pause the execution of a script on any line using breakpoints and then check the values of variables stored at that point
- `debugger`
- `throw new Error ('message')` to create your own descriptive message of an error


[BACK TO HOME](../README.md)
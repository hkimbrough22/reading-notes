# Notes from 01 July
## Javascript Continued
### Operators
- JavaScript has unary, binary, and ternary operators (the conditional operator).
- A unary operator requires a single operand, either before or after the operator:
- `x++` or `++x`.
- A binary operator requires two operands: one before the operator and one after the operator.
- Meaning "operand1 operator operand2".
- `3+4` or `x*y`

- JavaScript has the following operators:
1. Assignment operators
2. Comparison operators
3. Arithmetic operators
4. Bitwise operators
5. Logical operators
6. String operators
7. Conditional (ternary) operator
8. Comma operator
9. Unary operators
10. Relational operators


### JavaScript Arithmetic Operators
- Operator, Description
- `+` Addition
- `-` Subtraction
- `*` Multiplication
- `**` Exponentiation (ES2016)
- `/`	Division
- `%`	Modulus (Division Remainder)
- `++` Increment
- `--` Decrement


### Functions
- A JavaScript function is a block of code designed to perform a particular task.
- A JavaScript function is executed when "something" calls the function to commence.
- Functions are one of the fundamental properties of JavaScript. In JavaScript a function is similar to a procedure; a set of statements that performs a task or calculates a value
- To use a function, you must declare and define it somewhere in the scope from which you wish to call it. 
- We create functions so that we can reuse code: Define the code once, and use it many times. You can use the same code many times with different arguments, to produce different results.

#### Function declarations
- A function declaration (or definition/statement) lists the function keyword, followed by:
1. The name of the function.
2. A list of parameters to the function, enclosed in parentheses and separated by commas.
3. The JavaScript statements that define the function, enclosed in curly brackets, {...}.
- For example, the following code defines a simple function named square:
`function square(number) {`
  `return number * number;`
`}`
- The function `square` takes one parameter, called `number`. The function consists of one statement that says to return the parameter of the function (that is, `number`) multiplied by itself. The statement `return` specifies the value returned by the function:
`return number * number;`

#### Function Expressions
- Functions can also be created by a function expression.
- Such a function can be anonymous; it does not have to have a name. 
- The main difference between a function expression and a function declaration is the function name, which can be omitted in function expressions to create anonymous functions.
- However, a name can be provided with a function expression. Providing a name allows the function to refer to itself, and also makes it easier to identify the function in a debugger's stack traces.


### Control flow
- The control flow is the order in which the computer executes statements in a script.
- Code is run in order from the first line in the file to the last line, unless the computer runs across the (extremely frequent) structures that change the control flow, such as conditionals and loops. 
- For example, imagine a script used to validate user data from a webpage form. The script submits validated data, but if the user, say, leaves a required field empty, the script prompts them to fill it in. To do this, the script uses a conditional structure or if...else, so that different code executes depending on whether the form is complete or not:
`if (field==empty) {`
    `promptUser();`
`} else {`
 `   submitForm();`
`}`
- A typical JavaScript includes many control structures, including conditionals, loops and functions. Parts of a script may also be set to execute when events occur.
- For example, the above excerpt might be inside a function that runs when the user clicks the Submit button for the form. The function could also include a loop, which iterates through all of the fields in the form, checking each one in turn.


### Fun Facts
- Adding two numbers, will return the sum, but adding a number and a string will return a string.
- `===`	equal value and equal type
- `!=` not equal
- `!==`	not equal value or not equal type
- `&&` logical and
- `||` logical or
- `!` logical not
- `typeof` Returns the type of a variable
- Variables declared within a JavaScript function, become LOCAL to the function. Local variables can only be accessed from within the function.

[BACK TO MAIN](README.md)
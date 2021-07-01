# Notes from 01 July, Assignment 2
## Javascript Loops
### What is a loop?
- Loops offer a quick and easy way to do something repeatedly.
- There are many different kinds of loops, but they all essentially do the same thing: they repeat an action some number of times.

- You can think of a loop as a computerized version of the game where you tell someone to take X steps in one direction, then Y steps in another. For example, the idea "Go five steps to the east" could be expressed this way as a loop:

- `for (let step = 0; step < 5; step++) {`
- `// Runs 5 times, with values of step 0 through 4.`
- ` console.log('Walking east one step');`
- `}`

### Javascript Loop Statements
- for statement
- do...while statement
- while statement
- labeled statement
- break statement
- continue statement
- for...in statement
- for...of statement
- for statement

### For Statement
- A for loop repeats until a specified condition evaluates to false. 
- A for statement looks as follows:
`for ([initialExpression]; [conditionExpression]; [incrementExpression])`
- `statement`
- When a for loop executes, the following occurs:
1. The initializing expression `initialExpression`, if any, is executed. This expression usually initializes one or more loop counters, but the syntax allows an expression of any degree of complexity. This expression can also declare variables.
2. The `conditionExpression` expression is evaluated. If the value of `conditionExpression` is true, the loop statements execute. If the value of `conditionExpression` is false, the for loop terminates. (If the condition expression is omitted entirely, the condition is assumed to be true.)
3. The `statement` executes.
4. If present, the update expression `incrementExpression` is executed.
5. Control returns to Step 2.

### While Statement
- A while statement executes its statements as long as a specified condition evaluates to true. A while statement looks as follows:
`while (condition)`
  `statement`
- If the `condition` becomes false, `statement` within the loop stops executing and control passes to the statement following the loop.
- The `condition` test occurs before `statement` in the loop is executed. 
- If the `condition` returns true, `statement` is executed and the `condition` is tested again. If the `condition` returns false, execution stops, and control is passed to the statement following `while`.
- The following while loop iterates as long as n is less than 3:
`let n = 0;`
`let x = 0;`
`while (n < 3) {`
 ` n++;`
  `x += n;`
`}`
- With each iteration, the loop increments n and adds that value to `x`. Therefore, `x` and `n` take on the following values:
1. After the first pass: n = 1 and x = 1
2. After the second pass: n = 2 and x = 3
3. After the third pass: n = 3 and x = 6
4. After completing the third pass, the condition `n < 3` is no longer true, so the loop terminates.

[BACK TO MAIN](README.md)
# Code 401 - Reading Notes

<!-- All references used were from Code 401 reading
assignment 02 -->

<!-- https://perso.ensta-paris.fr/~diam/java/online/notes-java/language/10basics/import.html -->
<!-- https://www.baeldung.com/java-loops -->

## Java Imports

- Package = directory. Java classes can be grouped together in packages. A package name is the same as the directory (folder) name which contains the .java files. You declare packages when you define your Java program, and you name the packages you want to use from other libraries in an import statement.

Order of statements
1. Package statment (optional).
2. Imports (optional).
3. Class or interface definitions.

`import javax.swing.*`

There are 166 packages containing 3279 classes and interfaces in Java 5. However, only a few packages are used in most programming. GUI programs typically use at least the first three imports.

- `import java.awt.*;`	Common GUI elements.
- `import java.awt.event.*;`	The most common GUI event listeners.
- `import javax.swing.*;`	More common GUI elements. Note "javax".
- `import java.util.*;`	Data structures (Collections), time, Scanner, etc classes.
- `import java.io.*;`	Input-output classes.
- `import java.text.*;` Some formatting classes.
- `import java.util.regex.*;` Regular expression classes.

## Loops

- Looping is a feature which executes a set of instructions until the controlling Boolean-expression evaluates to false.

- Java provides different types of loops to fit any programming need. Each loop has its own purpose and a suitable use case to serve.

- Here are the types of loops that we can find in Java:

1. Simple for loop
    - `for (int i = 0; i < 5; i++) {
    System.out.println("Simple for loop: i = " + i);
}`
2. Enhanced for-each loop
    - `int[] intArr = { 0,1,2,3,4 };
for (int num : intArr) {
    System.out.println("Enhanced for-each loop: i = " + num);
}`
3. While loop
    - `int i = 0;
while (i < 5) {
    System.out.println("While loop: i = " + i++);
}`
4. Do-While loop
    - `int i = 0;
do {
    System.out.println("Do-While loop: i = " + i++);
} while (i < 5);`

[BACK TO HOME](../README.md)

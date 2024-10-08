# Basic Syntax and Operations

JavaScript is a powerful and versatile programming language that is widely used for web development. In this section, we will cover the basic syntax and operations of JavaScript, including variables, data types, operators, and control structures such as if statements and loops. By the end of this section, you should have a solid understanding of these fundamental concepts.

## Variables

In JavaScript, variables are used to store data. You can declare a variable using the `var`, `let`, or `const` keywords. Here's a quick overview of each:

- `var`: The original way to declare variables in JavaScript. It has function scope.
- `let`: Introduced in ES6, it has block scope and is generally preferred over `var`.
- `const`: Also introduced in ES6, it is used to declare variables that cannot be reassigned. It has block scope.

**Examples:**

```javascript
var name = "Alice"; // Using var
let age = 30;       // Using let
const pi = 3.14159; // Using const

console.log(name); // Outputs: Alice
console.log(age);  // Outputs: 30
console.log(pi);   // Outputs: 3.14159
```

## Data Types

JavaScript has several data types that you can use to store different kinds of values. The main data types are:

- **Number**: For numeric values (both integers and floating-point numbers).
- **String**: For text.
- **Boolean**: For true or false values.
- **Object**: For complex data structures.
- **Undefined**: For variables that are declared but not assigned a value.
- **Null**: For explicitly empty or non-existent values.
- **Symbol**: For unique identifiers (introduced in ES6).
- **BigInt**: For integers with arbitrary precision (introduced in ES11).

**Examples:**

```javascript
let num = 42;               // Number
let message = "Hello";      // String
let isActive = true;        // Boolean
let user = { name: "Bob" }; // Object
let nothing;                // Undefined
let empty = null;           // Null

console.log(typeof num);       // Outputs: number
console.log(typeof message);   // Outputs: string
console.log(typeof isActive);  // Outputs: boolean
console.log(typeof user);      // Outputs: object
console.log(typeof nothing);   // Outputs: undefined
console.log(typeof empty);     // Outputs: object (this is a quirk in JavaScript)
```

## Operators

JavaScript supports a wide range of operators for performing different kinds of operations. Here are some of the most commonly used operators:

- **Arithmetic Operators**: `+`, `-`, `*`, `/`, `%`, `++`, `--`
- **Assignment Operators**: `=`, `+=`, `-=`, `*=`, `/=`, `%=`
- **Comparison Operators**: `==`, `===`, `!=`, `!==`, `>`, `<`, `>=`, `<=`
- **Logical Operators**: `&&`, `||`, `!`
- **String Operators**: `+` (concatenation)

**Examples:**

```javascript
let a = 10;
let b = 5;

console.log(a + b); // Outputs: 15
console.log(a - b); // Outputs: 5
console.log(a * b); // Outputs: 50
console.log(a / b); // Outputs: 2
console.log(a % b); // Outputs: 0

a += 5; // Equivalent to a = a + 5
console.log(a); // Outputs: 15

console.log(a == 15);  // Outputs: true
console.log(a === 15); // Outputs: true
console.log(a != 10);  // Outputs: true
console.log(a !== 10); // Outputs: true

let isTrue = true;
let isFalse = false;

console.log(isTrue && isFalse); // Outputs: false
console.log(isTrue || isFalse); // Outputs: true
console.log(!isTrue);           // Outputs: false

let greet = "Hello";
let name = "World";
console.log(greet + " " + name); // Outputs: Hello World
```

## Control Structures

Control structures allow you to control the flow of execution in your program. The most common control structures in JavaScript are if statements and loops.

**If Statements**

If statements are used to execute a block of code based on a condition.

**Example:**

```javascript
let num = 10;

if (num > 5) {
  console.log("Number is greater than 5");
} else if (num === 5) {
  console.log("Number is equal to 5");
} else {
  console.log("Number is less than 5");
}
```

**Loops**

Loops are used to execute a block of code multiple times. The most common types of loops in JavaScript are `for`, `while`, and `do...while`.

**For Loop:**

```javascript
for (let i = 0; i < 5; i++) {
  console.log(i); // Outputs: 0, 1, 2, 3, 4
}
```

**While Loop:**

```javascript
let i = 0;
while (i < 5) {
  console.log(i); // Outputs: 0, 1, 2, 3, 4
  i++;
}
```

**Do...While Loop:**

```javascript
let i = 0;
do {
  console.log(i); // Outputs: 0, 1, 2, 3, 4
  i++;
} while (i < 5);
```

# Conclusion

This section has provided a detailed look at the basic syntax and operations in JavaScript, covering variables, data types, operators, and control structures. These foundational elements are crucial for anyone looking to develop skills in JavaScript programming. Understanding these concepts will allow you to write more complex and functional JavaScript code as you continue to learn and grow as a developer.

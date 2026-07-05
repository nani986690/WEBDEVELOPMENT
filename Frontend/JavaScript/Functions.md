# JavaScript Functions

Functions are reusable blocks of code that perform a specific task. Instead of writing the same code multiple times, we write it once inside a function and call it whenever needed.

---

# Table of Contents

1. Function Declaration
2. Arrow Functions
3. Parameters & Arguments
4. Return Values
5. Callback Functions
6. Practice Questions
7. Interview Questions

---

# 1. Function Declaration

A function declaration creates a reusable block of code.

## Syntax

```javascript
function functionName() {

}
```

## Example

```javascript
function greet() {
    console.log("Hello World");
}

greet();
```

### Output

```
Hello World
```

### Explanation

- `function` is the keyword used to create a function.
- `greet` is the function name.
- `()` holds the parameters.
- `{}` contains the function body.
- `greet()` calls (executes) the function.

---

# Example: Print Your Name

```javascript
function printName(name) {
    console.log(name);
}

printName("Vinod");
```

### Output

```
Vinod
```

### Explanation

The value `"Vinod"` is passed into the function through the parameter `name`, and the function prints it.

---

# 2. Arrow Functions

Arrow functions provide a shorter syntax for writing functions.

## Syntax

```javascript
const functionName = () => {

};
```

## Example

```javascript
const greet = () => {
    console.log("Hello");
};

greet();
```

### Output

```
Hello
```

---

## Short Arrow Function

If there is only one statement, braces and `return` can be omitted.

```javascript
const greet = () => console.log("Hello");

greet();
```

---

# 3. Parameters & Arguments

## Parameters

Parameters are variables listed in the function definition.

```javascript
function greet(name) {

}
```

Here,

`name` is a parameter.

---

## Arguments

Arguments are the actual values passed to the function.

```javascript
greet("Vinod");
```

Here,

`"Vinod"` is an argument.

---

## Example

```javascript
function add(a, b) {
    console.log(a + b);
}

add(10, 20);
```

### Output

```
30
```

### Explanation

```
a = 10
b = 20

10 + 20 = 30
```

---

# 4. Return Values

A function can return a value using the `return` keyword.

## Example

```javascript
function add(a, b) {
    return a + b;
}

let result = add(5, 10);

console.log(result);
```

### Output

```
15
```

### Explanation

Instead of printing inside the function, `return` sends the value back to the caller.

---

# Arrow Function with Return

```javascript
const multiply = (a, b) => {
    return a * b;
};

console.log(multiply(4, 5));
```

### Output

```
20
```

---

## Short Arrow Function

```javascript
const multiply = (a, b) => a * b;

console.log(multiply(4, 5));
```

---

# Example: Square of a Number

```javascript
const square = (num) => num * num;

console.log(square(6));
```

### Output

```
36
```

---

# Even or Odd Function

```javascript
function check(num) {
    if (num % 2 === 0) {
        console.log("Even");
    } else {
        console.log("Odd");
    }
}

check(7);
```

### Output

```
Odd
```

### Explanation

If the remainder after dividing by 2 is zero, the number is even.

Otherwise, it is odd.

---

# 5. Callback Functions

A callback is a function passed as an argument to another function.

## Why use callbacks?

Sometimes we want another function to run only after one function finishes.

---

## Example

```javascript
function greet(name, callback) {
    console.log("Hello " + name);
    callback();
}

function welcome() {
    console.log("Welcome to JavaScript!");
}

greet("Vinod", welcome);
```

### Output

```
Hello Vinod
Welcome to JavaScript!
```

---

## Explanation

```
greet("Vinod", welcome);

↓

name = "Vinod"

callback = welcome

↓

console.log("Hello Vinod")

↓

callback()

↓

welcome()

↓

Welcome to JavaScript!
```

---

# Callback Example with Calculation

```javascript
function calculate(a, b, operation) {
    console.log(operation(a, b));
}

function multiply(a, b) {
    return a * b;
}

calculate(5, 4, multiply);
```

### Output

```
20
```

### Explanation

```
calculate()

↓

operation = multiply

↓

multiply(5,4)

↓

20
```

---

# Anonymous Callback

```javascript
function process(callback) {
    callback();
}

process(function () {
    console.log("Task Completed");
});
```

---

# Arrow Callback

```javascript
function process(callback) {
    callback();
}

process(() => {
    console.log("Task Completed");
});
```

---

# Real World Callback Example

```javascript
button.addEventListener("click", function () {
    console.log("Button Clicked");
});
```

Whenever the button is clicked, the callback function executes.

---

# Practice Questions

## Easy

### Question 1

Create a function that prints your name.

Example Output

```
Vinod
```

---

### Question 2

Create a function that adds two numbers.

Example

```
add(10,20)
```

Output

```
30
```

---

### Question 3

Create an arrow function that multiplies two numbers.

Example

```
multiply(5,6)
```

Output

```
30
```

---

### Question 4

Create a function that returns the square of a number.

Example

```
square(7)
```

Output

```
49
```

---

### Question 5

Create a function that checks whether a number is even or odd.

Example

```
check(15)
```

Output

```
Odd
```

---

## Medium

### Question 6

Create a callback function that prints

```
Task Completed
```

---

### Question 7

Create a function that accepts a callback and executes it.

Expected Output

```
Hello Vinod
Welcome!
```

---

### Question 8

Create a calculate function that accepts another function.

```
calculate(10,5,add)
```

Output

```
15
```

---

### Question 9

Create another callback that performs subtraction.

---

### Question 10

Create a callback using an arrow function.

---

# Interview Questions

## What is a function?

A reusable block of code used to perform a specific task.

---

## What is an Arrow Function?

A shorter syntax for writing functions introduced in ES6.

---

## Difference between Parameters and Arguments

| Parameters | Arguments |
|------------|-----------|
| Variables in function definition | Actual values passed to the function |

Example

```javascript
function greet(name) {

}

greet("Vinod");
```

Parameter → `name`

Argument → `"Vinod"`

---

## What is the difference between console.log() and return?

### console.log()

Prints a value.

```javascript
console.log(10);
```

### return

Sends a value back to the caller.

```javascript
return 10;
```

---

## What is a Callback Function?

A callback is a function passed as an argument to another function.

Example

```javascript
greet("Vinod", welcome);
```

Here,

`welcome` is the callback.

---

# Summary

✅ Function Declaration

✅ Arrow Functions

✅ Parameters

✅ Arguments

✅ Return

✅ Callback Functions

These concepts form the foundation for advanced JavaScript topics like asynchronous programming, promises, async/await, event handling, and APIs.

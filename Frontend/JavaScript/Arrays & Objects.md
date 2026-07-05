# JavaScript Arrays & Objects

Arrays and Objects are two of the most important data structures in JavaScript.

- **Arrays** store multiple values in a single variable.
- **Objects** store data in key-value pairs.

---

# Table of Contents

1. Arrays
2. Array Methods
   - forEach()
   - map()
   - filter()
   - find()
3. Objects
4. Object Methods
5. Destructuring
6. Spread Operator (...)
7. Practice Questions
8. Interview Questions

---

# 1. Arrays

An array is a collection of values stored in a single variable.

## Syntax

```javascript
let arrayName = [value1, value2, value3];
```

## Example

```javascript
let fruits = ["Apple", "Banana", "Orange"];

console.log(fruits);
```

### Output

```
["Apple", "Banana", "Orange"]
```

---

## Accessing Elements

```javascript
let fruits = ["Apple", "Banana", "Orange"];

console.log(fruits[0]);
console.log(fruits[1]);
console.log(fruits[2]);
```

### Output

```
Apple
Banana
Orange
```

---

## Updating an Element

```javascript
let fruits = ["Apple", "Banana", "Orange"];

fruits[1] = "Mango";

console.log(fruits);
```

### Output

```
["Apple","Mango","Orange"]
```

---

## Array Length

```javascript
let numbers = [10,20,30,40];

console.log(numbers.length);
```

### Output

```
4
```

---

# 2. Array Methods

---

# forEach()

The `forEach()` method executes a function for every element in the array.

## Syntax

```javascript
array.forEach(function(element){

});
```

---

## Example

```javascript
let numbers = [1,2,3,4];

numbers.forEach(function(num){
    console.log(num);
});
```

### Output

```
1
2
3
4
```

---

## Arrow Function

```javascript
numbers.forEach((num)=>{
    console.log(num);
});
```

---

## Explanation

```
Array

↓

1

↓

2

↓

3

↓

4
```

Each element is passed one by one into the callback function.

---

# map()

Creates a **new array** by transforming every element.

Original array remains unchanged.

---

## Syntax

```javascript
let newArray = array.map(function(element){

});
```

---

## Example

```javascript
let numbers = [1,2,3,4];

let square = numbers.map((num)=>{
    return num*num;
});

console.log(square);
```

### Output

```
[1,4,9,16]
```

---

## Explanation

```
1 → 1

2 → 4

3 → 9

4 → 16
```

Returns a new array.

---

# filter()

Returns only the elements that satisfy a condition.

---

## Example

```javascript
let numbers = [10,15,20,25,30];

let even = numbers.filter((num)=>{
    return num % 2 === 0;
});

console.log(even);
```

### Output

```
[10,20,30]
```

---

## Explanation

```
10 ✔

15 ✘

20 ✔

25 ✘

30 ✔
```

Only matching values are returned.

---

# find()

Returns the **first** matching element.

---

## Example

```javascript
let numbers = [10,15,20,25];

let result = numbers.find((num)=>{
    return num > 18;
});

console.log(result);
```

### Output

```
20
```

---

## Explanation

```
10 ✘

15 ✘

20 ✔

Stop Searching
```

Only the first match is returned.

---

# Difference

| Method | Returns |
|---------|----------|
| forEach() | Nothing |
| map() | New Array |
| filter() | Matching Array |
| find() | First Matching Value |

---

# Objects

Objects store data as key-value pairs.

---

## Syntax

```javascript
let person = {
    key : value
};
```

---

## Example

```javascript
let person = {
    name: "Vinod",
    age: 23,
    city: "Hyderabad"
};

console.log(person);
```

---

## Access Properties

### Dot Notation

```javascript
console.log(person.name);
```

Output

```
Vinod
```

---

### Bracket Notation

```javascript
console.log(person["age"]);
```

Output

```
23
```

---

## Update Property

```javascript
person.city = "Chennai";

console.log(person);
```

---

## Add Property

```javascript
person.country = "India";

console.log(person);
```

---

## Delete Property

```javascript
delete person.age;

console.log(person);
```

---

# Object Methods

Objects can also contain functions.

```javascript
let student = {

    name:"Vinod",

    greet:function(){

        console.log("Hello");

    }

};

student.greet();
```

Output

```
Hello
```

---

# Destructuring

Destructuring extracts values from arrays or objects into variables.

---

# Array Destructuring

```javascript
let numbers = [10,20,30];

let [a,b,c] = numbers;

console.log(a);
console.log(b);
console.log(c);
```

Output

```
10
20
30
```

---

# Skip Values

```javascript
let numbers=[10,20,30];

let [a,,c]=numbers;

console.log(a);
console.log(c);
```

Output

```
10
30
```

---

# Object Destructuring

```javascript
let person = {

    name:"Vinod",

    age:23

};

let {name,age}=person;

console.log(name);

console.log(age);
```

Output

```
Vinod

23
```

---

# Rename Variables

```javascript
let person = {

    name:"Vinod"

};

let {name:userName}=person;

console.log(userName);
```

Output

```
Vinod
```

---

# Spread Operator (...)

The spread operator expands arrays or objects.

---

# Copy an Array

```javascript
let arr1=[1,2,3];

let arr2=[...arr1];

console.log(arr2);
```

Output

```
[1,2,3]
```

---

# Merge Arrays

```javascript
let arr1=[1,2];

let arr2=[3,4];

let arr3=[...arr1,...arr2];

console.log(arr3);
```

Output

```
[1,2,3,4]
```

---

# Copy Object

```javascript
let person={

    name:"Vinod",

    age:23

};

let copy={...person};

console.log(copy);
```

---

# Merge Objects

```javascript
let obj1={

    name:"Vinod"

};

let obj2={

    city:"Hyderabad"

};

let obj3={...obj1,...obj2};

console.log(obj3);
```

Output

```
{

name:"Vinod",

city:"Hyderabad"

}
```

---

# Difference

| Feature | Purpose |
|----------|----------|
| map() | Transform every element |
| filter() | Keep matching elements |
| find() | Return first match |
| forEach() | Iterate over elements |
| Destructuring | Extract values |
| Spread (...) | Copy or merge arrays/objects |

---

# Practice Questions

## Easy

### Question 1

Print every element of an array using `forEach()`.

---

### Question 2

Use `map()` to double every number.

Input

```
[1,2,3]
```

Output

```
[2,4,6]
```

---

### Question 3

Use `filter()` to return only odd numbers.

Input

```
[10,15,20,25]
```

Output

```
[15,25]
```

---

### Question 4

Use `find()` to return the first number greater than 50.

---

### Question 5

Create an object named `student` with

- name
- age
- course

Print each property.

---

## Medium

### Question 6

Destructure an array into three variables.

---

### Question 7

Destructure an object into variables.

---

### Question 8

Merge two arrays using the spread operator.

---

### Question 9

Merge two objects.

---

### Question 10

Use `map()` to return the square of every number.

---

# Interview Questions

## What is an array?

A collection of multiple values stored in a single variable.

---

## What is an object?

A collection of key-value pairs.

---

## Difference between map() and forEach()

| map() | forEach() |
|--------|-----------|
| Returns new array | Returns undefined |
| Used for transformation | Used for iteration |

---

## Difference between filter() and find()

| filter() | find() |
|-----------|---------|
| Returns all matching elements | Returns first matching element |

---

## What is Destructuring?

Extracting values from arrays or objects into separate variables.

---

## What is the Spread Operator?

The spread operator (`...`) expands arrays or objects. It is commonly used to copy and merge data.

---

# Summary

✅ Arrays

✅ Array Methods (`forEach`, `map`, `filter`, `find`)

✅ Objects

✅ Object Methods

✅ Array Destructuring

✅ Object Destructuring

✅ Spread Operator

These concepts are essential for working with data in JavaScript and are widely used in modern frameworks like React, Angular, and Vue.

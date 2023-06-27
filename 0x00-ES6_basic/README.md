# ES6 JavaScript Basics

This repository contains a collection of basic examples and explanations of ES6 (ECMAScript 2015) features in JavaScript. ES6 introduced several new features and improvements to the language, making JavaScript more powerful and expressive.

## Table of Contents

- [Features Covered](#features-covered)
- [Getting Started](#getting-started)
- [Examples](#examples)
- [Contributing](#contributing)
- [License](#license)

## Features Covered

The repository covers the following ES6 features:

1. [let](#let)
2. [const](#const)
3. [Arrow Functions](#arrow-functions)
4. [Default Parameters](#default-parameters)
5. [Template Literals](#template-literals)
6. [Spread Operator](#spread-operator)
7. [Destructuring Assignment](#destructuring-assignment)
8. [Classes](#classes)
9. [Modules](#modules)
10. [Promises](#promises)

## Getting Started

To use the code in this repository, follow these steps:

1. Clone the repository:

```bash
git clone https://github.com/your-username/es6-javascript-basics.git
```

2. Navigate to the project directory:

```bash
cd es6-javascript-basics
```

3. Open the code files in your preferred text editor or IDE.

## Examples

Each ES6 feature has its own dedicated example file that demonstrates its usage. Here's a brief overview of the examples provided:

### let

The `let` keyword is used for block-scoped variables.

```javascript
let x = 10;
if (true) {
  let x = 20;
  console.log(x); // Output: 20
}
console.log(x); // Output: 10
```

### const

The `const` keyword is used for block-scoped variables that cannot be reassigned.

```javascript
const PI = 3.14;
console.log(PI); // Output: 3.14
PI = 3.1415; // Throws an error
```

### Arrow Functions

Arrow functions provide a concise syntax for writing anonymous functions.

```javascript
const add = (a, b) => a + b;
console.log(add(2, 3)); // Output: 5
```

### Default Parameters

Default parameters allow you to assign default values to function parameters.

```javascript
const greet = (name = "Anonymous") => {
  console.log(`Hello, ${name}!`);
};
greet(); // Output: Hello, Anonymous!
greet("John"); // Output: Hello, John!
```

### Template Literals

Template literals enable string interpolation and multiline strings.

```javascript
const name = "Alice";
const age = 25;
console.log(`My name is ${name} and I'm ${age} years old.`);
```

### Spread Operator

The spread operator allows you to spread elements of an array or object.

```javascript
const arr = [1, 2, 3];
console.log(...arr); // Output: 1 2 3

const obj = { x: 1, y: 2 };
const newObj = { ...obj, z: 3 };
console.log(newObj); // Output: { x: 1, y: 2, z: 3 }
```

### Destructuring Assignment

Destructuring assignment allows you to extract values from arrays or objects.

```javascript
const numbers = [1, 2, 3];
const [a, b, c] = numbers;
console.log(a, b, c); // Output: 1 2 3

const person

 = { name: "Alice", age: 25 };
const { name, age } = person;
console.log(name, age); // Output: Alice 25
```

### Classes

ES6 introduced a class syntax for creating objects and implementing inheritance.

```javascript
class Rectangle {
  constructor(width, height) {
    this.width = width;
    this.height = height;
  }

  getArea() {
    return this.width * this.height;
  }
}

const rectangle = new Rectangle(5, 3);
console.log(rectangle.getArea()); // Output: 15
```

### Modules

ES6 modules allow you to organize and share JavaScript code across files.

```javascript
// math.js
export const add = (a, b) => a + b;
export const subtract = (a, b) => a - b;

// main.js
import { add, subtract } from "./math.js";
console.log(add(2, 3)); // Output: 5
console.log(subtract(5, 2)); // Output: 3
```

### Promises

Promises provide a way to handle asynchronous operations and their results.

```javascript
const fetchData = () => {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      const data = "Hello, world!";
      resolve(data);
    }, 2000);
  });
};

fetchData()
  .then((result) => {
    console.log(result); // Output: Hello, world!
  })
  .catch((error) => {
    console.error(error);
  });
```


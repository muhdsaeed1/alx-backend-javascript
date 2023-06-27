# ES6 JavaScript Promises

This repository contains examples and explanations of using Promises in ES6 (ECMAScript 2015) JavaScript. Promises provide a way to handle asynchronous operations and their results, making it easier to write and manage asynchronous code.

## Table of Contents

- [Examples](#examples)
- [Getting Started](#getting-started)

## Examples

The repository provides the following examples of working with Promises:

- [Basic Promise](#basic-promise)
- [Chaining Promises](#chaining-promises)
- [Handling Errors](#handling-errors)
- [Promise.all](#promise-all)

### Basic Promise

A basic example demonstrating the creation and usage of a Promise.

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

### Chaining Promises

An example showcasing how to chain multiple Promises together.

```javascript
const fetchUser = () => {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      const user = { name: "Alice", age: 25 };
      resolve(user);
    }, 2000);
  });
};

const fetchPosts = (user) => {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      const posts = ["Post 1", "Post 2", "Post 3"];
      resolve({ user, posts });
    }, 2000);
  });
};

fetchUser()
  .then((user) => {
    return fetchPosts(user);
  })
  .then((data) => {
    console.log(data); // Output: { user: { name: "Alice", age: 25 }, posts: ["Post 1", "Post 2", "Post 3"] }
  })
  .catch((error) => {
    console.error(error);
  });
```

### Handling Errors

An example demonstrating error handling with Promises.

```javascript
const fetchData = () => {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      const error = "Something went wrong!";
      reject(error);
    }, 2000);
  });
};

fetchData()
  .then((result) => {
    console.log(result);
  })
  .catch((error) => {
    console.error(error); // Output: Something went wrong!
  });
```

### Promise.all

An example showcasing the use of `Promise.all` to handle multiple Promises simultaneously.

```javascript
const fetchUser = () => {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      const user = { name: "Alice", age: 25 };
      resolve(user);
    }, 2000);
  });
};

const fetchPosts = () => {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      const posts = ["Post 1", "Post 2", "Post 3"];
      resolve(posts);
    }, 2000);
  });
};

Promise.all([fetchUser(), fetchPosts()])
  .then((results) => {
    const [user, posts] = results;
    console.log(user, posts); // Output: { name: "Alice", age: 25 } ["Post 1", "Post 2", "Post 3"]
  })
  .catch((error) => {
    console.error(error);
  });
```



Feel free to explore and modify the examples to understand Promises better.

## Getting Started

To use the code in this repository, follow these steps:

1. Clone the repository:

```bash
git clone https://github.com/your-username/es6-javascript-promises.git
```

2. Navigate to the project directory:

```bash
cd es6-javascript-promises
```

3. Open the code files in your preferred text editor or IDE.

That's it! You can now experiment with the examples and learn more about Promises in JavaScript.

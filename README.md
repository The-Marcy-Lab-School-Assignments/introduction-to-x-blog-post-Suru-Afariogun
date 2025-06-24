# Blog Title

By [your name]

(Customize these headings!)

## Introduction

- Why should someone learn the language/framework that you are learning?
- What is it used for? How popular is it? Who is it for (developers or users)?
- Incorporate real-world analogies when appropriate and useful.

## Core syntax/features. 

- For programming languages: data types, variables, code blocks, functions, conditionals, arrays and objects, and iteration. Include code snippets with explanations.

- For frameworks (including React and Express): setup/installation/configurations, core concepts, key methods or approaches. Include code snippets with explanations.

## Compare and Contrast

- For programming languages: What are the key differences between the new language and JavaScript? What are the commonalities?
- For frameworks (including React and Express): What are the alternatives to this framework? Can you compare this framework to anything we've learned in the Core Curriculum? What are the tradeoffs when choosing this framework compared to the alternatives?

## Conclusion & Tips for learning this language/framework.

- Wrap things up
- Provide links to resources that you used to help you learn the language.

---

````markdown
# Introduction to Higher-Order Functions and Conditionals for Programmers

## Introduction

In my Capstone, I'm revisiting key JavaScript concepts that show up everywhere in real-world code: **Higher-Order Functions (H.O.Fs)** and **conditional logic**. These two patterns are the backbone of how developers write readable, powerful programs in frameworks like **React** and **Express**.

This post is for student developers who already know the basics of JavaScript and want to level up their functional thinking and control flow skills. We'll dive into `map`, `forEach`, `filter`, and get hands-on with `if`, `else`, and other conditionals.

---

## Why Learn H.O.Fs and Conditionals?

JavaScript is known for treating **functions** as **"building blocks"** , meaning you can pass them around like data. That’s where Higher-Order Functions come in. They're essential for writing **clean**, **reusable**, and **declarative** code.

Meanwhile, conditionals like `if` and `else` let your program **make decisions**, which is basically the core of all logic. Whether you're deciding what UI to render in React or which database query to run in Express, conditionals are an invaluable tool.

---

## Core Concepts and Syntax

### What is a Higher-Order Function?

A **Higher-Order Function** is any function that does **one or both** of the following:

- Takes another function as an argument
- Returns a function as its result

**Example:**

```js
function greet(name) {
  return 'Hello, ' + name;
}

function loudGreet(callback, name) {
  return callback(name).toUpperCase();
}

console.log(loudGreet(greet, 'Suru')); // output = "HELLO, SURU"
```

In real projects, we often use H.O.Fs like `map`, `forEach`, and `filter` to work with arrays.

---

### `.map()` – Transforming Arrays

`map()` is used to **transform** every element in an array and return a **new array**.

**Example:**

```js
const numbers = [1, 2, 3];
const doubled = numbers.map((num) => num * 2);
console.log(doubled); // [2, 4, 6]
```

Like a vending machine turning dollars into snacks.

---

### `.forEach()` – Loop with side effects

`forEach()` lets you loop through each item, but it **doesn't return a new array**. It's best used when you're doing something like printing or updating UI.

**Example:**

```js
const names = ['Ali', 'Zara', 'Suru'];
names.forEach((name) => {
  console.log('Hello, ' + name);
});
```

---

### `.filter()` – Keep what you want

`filter()` returns a **new array** with only the elements that **pass a condition**.

**Example:**

```js
const ages = [12, 25, 18, 30];
const adults = ages.filter((age) => age >= 18);
console.log(adults); // [25, 18, 30]
```

Like a bouncer letting only adults into a club.

---

## Conditionals:

Conditionals let your program **decide what to do based on logic**.

### Basic `if/else`

```js
const age = 20;

if (age >= 18) {
  console.log("You're an adult.");
} else {
  console.log("You're a minor.");
}
```

### ➕ `else if` for multiple branches

```js
const score = 85;

if (score >= 90) {
  console.log('Grade: A');
} else if (score >= 80) {
  console.log('Grade: B');
} else {
  console.log('Grade: C or below');
}
```

### Ternary Operator

A shorter version of `if/else`, often used in React:

```js
const loggedIn = true;
console.log(loggedIn ? 'Welcome back!' : 'Please log in.');
```

---

## Compare and Contrast

### JavaScript vs Other Languages

- In JavaScript, H.O.Fs are common because **functions are objects**, so you can pass them around.
- In languages like Python, similar ideas exist (`map`, `lambda`), but aren't as central in frontend frameworks.

### React and H.O.Fs

- React relies heavily on `.map()` to render components.
- Conditional rendering in React often uses ternary operators or `&&`.

---

### Tips:

- Practice writing your own H.O.Fs
- Start with simple `if/else` and level up to ternaries
- Take Codecademy courses focused on H.O.F and basic JS.

### Resources:

- [w3Schools: map()](https://www.w3schools.com/jsref/jsref_map.asp)
- [w3Schools: filter()](https://www.w3schools.com/jsref/jsref_filter.asp)
- [w3Schools: Functions](https://www.w3schools.com/programming/prog_functions.php)
- [w3Schools: if...else](https://www.w3schools.com/js/js_if_else.asp)

---

## Conclusion

Understanding H.O.Fs and conditionals is a game-changer for JavaScript developers. They make your code more flexible, readable, and powerful — especially when you're working with frameworks like React or Express.

Whether you're mapping over data or branching your app's logic, these tools give you real control over behavior. Master these, and you'll be building smarter code in no time!
````

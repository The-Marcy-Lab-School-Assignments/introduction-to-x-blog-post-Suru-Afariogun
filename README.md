```markdown

```

# Higher-Order Functions and Conditionals

By Suru Afariogun

## Intro

During my Capstone, I’ve been brushing up on the basics—stuff I kind of knew already, but never really _got_ until I saw how it actually works in real projects. The two biggest ones for me have been **Higher-Order Functions (H.O.Fs)** and **Conditionals**.

If you’ve been coding in JavaScript for a bit, you’ve probably used `map`, `forEach`, `filter`, and the classic `if` and `else` blocks. But if you’re like me, maybe no one ever explained _why_ these are so important—or gave examples that actually stuck. That’s what this post is for.

---

## Why You Should Even Care

Here’s the deal: in JavaScript, you can treat functions like objects. That means you can pass them around just like numbers or strings. That’s what Higher-Order Functions are all about—they either **take another function in** or **return a new one out**.

On the flip side, **conditionals** like `if`, `else`, or the ternary operator let your program _decide_ what to do. Kinda like traffic lights for your logic—red light? Go this way. Green? Go that way.

If you’ve ever used **React** or **Express**, trust me—this stuff is everywhere.

---

## So What _Is_ a Higher-Order Function?

A **Higher-Order Function** is any function that either:

- Accepts another function as a parameter, or
- Returns a function as its result

Here’s a simple one:

```js
function greet(name) {
  return 'Hello, ' + name;
}

function loudGreet(callback, name) {
  return callback(name).toUpperCase();
}

console.log(loudGreet(greet, 'Suru')); // "HELLO, SURU"
```

One way to think about it: the `greet` function is like your regular speaking voice, and `loudGreet` is like putting a megaphone in front of your mouth—it takes the regular message and blasts it louder.

---

## `.map()` – Transforming Arrays

`.map()` is used when you want to create a new version of an array, with each element changed in some way.

```js
const numbers = [1, 2, 3];
const doubled = numbers.map((num) => num * 2);
console.log(doubled); // [2, 4, 6]
```

You can picture this like going through a car wash: the same number of cars go in and come out, but now they’re all clean. The structure doesn’t change, just the look of each piece inside.

---

## `.forEach()` – Just Do Something

`.forEach()` goes through each item in an array and does something with it—but it doesn’t give you anything back.

```js
const names = ['Ali', 'Zara', 'Suru'];
names.forEach((name) => {
  console.log('Hello, ' + name);
});
```

This works more like reading off names during roll call. You say each one out loud, but you’re not collecting anything new in the process.

---

## `.filter()` – Pick What Matters

`.filter()` gives you a new array, but only with the items that match a condition you set.

```js
const ages = [12, 25, 18, 30];
const adults = ages.filter((age) => age >= 18);
console.log(adults); // [25, 18, 30]
```

This is like a security guard at a concert checking IDs and only letting people in if they’re 18 or older. The ones that don’t meet the rule get left outside.

---

## Conditionals: Making Choices in Code

Conditionals let your code think for itself and choose what to do. Without them, it’s just following orders blindly.

### `if/else` – The Basics

```js
const age = 20;

if (age >= 18) {
  console.log("You're an adult.");
} else {
  console.log("You're a minor.");
}
```

Just like checking someone’s age before letting them into a rated-R movie—you either let them in or turn them away based on the condition.

---

### `else if` – More Than Two Paths

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

Kind of like grading a test: first you check if it’s an A, if not maybe it’s a B, and if it’s not that either, it drops down to a lower grade.

---

### Ternary Operator – One-Liner Choice

```js
const loggedIn = true;
console.log(loggedIn ? 'Welcome back!' : 'Please log in.');
```

This is like flipping a coin and saying “heads, I go out; tails, I stay in”—all in one quick move.

---

## React and Real Code

In **React**, you use `.map()` to loop through data and show components. For example:

```js
const todos = ['Buy milk', 'Do homework', 'Call mom'];

const list = todos.map((todo, i) => <li key={i}>{todo}</li>);
```

And conditionals help you decide what to show the user:

```js
{
  isLoggedIn ? <Profile /> : <Login />;
}
```

Or:

```js
{
  hasNotifications && <BellIcon />;
}
```

All of this helps React apps feel smarter and more dynamic, like they know what the user needs in the moment.

---

## Some Advice That Helped Me:

- Try building your own simple Higher-Order Functions to really understand them.
- Don’t worry if ternaries feel weird at first—nail `if/else` first, then move up.
- Think of real-life decisions when writing logic—it helps make it click.

---

## Resources That Helped Me

- [w3Schools: map()](https://www.w3schools.com/jsref/jsref_map.asp)
- [w3Schools: filter()](https://www.w3schools.com/jsref/jsref_filter.asp)
- [w3Schools: Functions](https://www.w3schools.com/programming/prog_functions.php)
- [w3Schools: if...else](https://www.w3schools.com/js/js_if_else.asp)

---

## Final Thoughts

Learning about Higher-Order Functions and conditionals changed the way I think when I write code. It’s not just about making things work—it’s about making smart decisions with your code.

At the end of the day, this stuff makes your projects **easier to manage**, **cleaner to read**, and **stronger to scale**. Whether you’re building an app, a website, or just a homework assignment—it’s tools like these that will make your code go from "it works" to "this makes sense".

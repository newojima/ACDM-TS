# ACDM-TS

<p>Link:
  <a href="https://www.youtube.com/watch?v=BwuLxPH8IDs">TypeScript Course for Beginners 2020 - Learn TypeScript from Scratch! (Jan 21, 2020)</p>
  </a>

<p>Free TypeScript Introduction for Beginners: Get Started with TypeScript, learn the Basics, its Features, Workflows and how to use it!</p>

<details>
<summary>Timestamps</summary>

- Getting Started 00:00
- What is TypeScript: 01:57
- Installing & Using TypeScript 06:31
- The Advantages of TypeScript 19:53
- Course Outline 22:59
- How to Get the Most out of This Course 27:16
- Setting Up our Development Environment 30:29
- The Course Project Setup 33:36
- Module Introduction 40:56
- Using Types 41:23
- TypeScript Types vs JavaScript Types 51:43
- Numbers, Strings and Booleans 56:37
- Type Assignment and Type Inference 01:02:20
- Object Types 01:07:59
- Array Types 01:15:31
- Tuples 01:21:01
- Enums 01:27:21
- The Any Type 01:34:26
- Union Types 01:36:30
- Literal Types 01:43:01
- Type Aliases 01:50:55
- Function Return Types and Void 01:53:55
- Function Types 02:01:21
- Function Types and Callbacks 02:06:55
- The Unknown Type 02:11:18
- The Never Type 02:15:02
- Wrap Up 02:19:12
- Module Introduction 02:21:04
- Watch Node 02:21:50
- Compiling the Entire Project 02:23:55
- Include and Exclude Files 02:27:42
- Setting a Compilation Target 02:33:55
- Understanding TypeScript Libs 02:37:59
- More Options 02:43:31
- Source Maps 02:45:12
- Rootdir and Outdir 02:47:12
- noemit on Error 02:52:43
- Strict Compilation Options 02:55:35
- Code Quality Options 03:06:39
- Debugging with Visual Studio Code 03:11:02
- Wrap Up 03:15:22
</details>

---

## 157 - What is TypeScript

- Superset of JS
  - A language that builds up on JS
  - A tool that helps developers write better code easier.
  - Adds new features and advantages compiled to JS.
- Browser can't execute it, instead it acts as a tool to compile to JS.

### Why TypeScript?

- Prevent unwanted behavior at runtime
- mitigation strategies: add if check to add function and validate & santise user input.
- Developers can still write invalid code

---

## 631 - Installing & Using TypeScript

index.html

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>631 - Installing & Using TypeScript</title>
  </head>
  <body>
    <input type="number" id="num1" placeholder="Number 1" />
    <input type="number" id="num2" placeholder="Number 2" />
    <button>Add!</button>

    <script src="./js-only.js" defer></script>
  </body>
</html>
```

js-only.js

```javascript
const button = document.querySelector("button");
const input1 = document.getElementById("num1");
const input2 = document.getElementById("num2");

function add(num1, num2) {
  if (typeof num1 === "number" && typeof num2 === "number") {
    return num1 + num2;
  } else {
    return +num1 + +num2;
  }
}

button.addEventListener("click", () => {
  console.log(add(input1.value, input2.value));
});
```

if you notice, the values are just gonna be strings that are concatenated instead of adding them.

we can however check the type of the values being passed in js file:

```javascript
function add(num1, num2) {
  if (typeof num1 === "number" && typeof num2 === "number") {
    return num1 + num2;
  } else {
    return +num1 + +num2;
  }
}
```

### Installing and Setting Up TS

- install node.js && sudo npm i -g typescript or just npm i -g typescript
- cd to the directory
- touch using-ts.ts:

```typescript
const button = document.querySelector("button");
const input1 = document.getElementById("num1")! as HTMLInputElement;
const input2 = document.getElementById("num2")! as HTMLInputElement;

function add(num1: number, num2: number) {
  return num1 + num2;
}

button.addEventListener("click", () => {
  console.log(add(+input1.value, +input2.value));
});
```

then tsc using-ts.ts, then switch the js-only to using-ts.js at index.html. then ull see it works properly

## 1953 - The Advantages of TypeScript

- Types
- Next-gen Js Features
- non-js features like interfaces or generics
- meta-programming features like decorators
- rich configuration options
- modern tooling that helps even in non-typescript projects

## 2259 - Course Outline

<details>
<summary>Course Outline</summary>
- TypeScript Basics
- Compiler & Configuration Deep Dive
- Working with next-gen js code
- classes and interfaces
- advanced types and ts features
- generics
- decorators
- full project
- working with namespaces and modules
- webpack and ts
- third party libs and ts
- react+ts & nodejs+ts
</details>

## 3336 - The Course Project Setup

## 4056 - Module Introduction

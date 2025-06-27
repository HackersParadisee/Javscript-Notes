# JavaScript-Notes

---

## 📘 Chapter 1: Setup and Configuration – Dev Container with GitHub Codespaces

Before writing any JavaScript or Node.js code, it’s important to have a consistent and reliable development environment — and that’s where GitHub Codespaces come in. Codespaces provide a full-featured, cloud-based coding environment with preinstalled tools, a terminal, and VS Code-like editor, all accessible directly from the browser. By setting up a Dev Container, you ensure that every developer (including your future self) works in the same environment with the correct Node.js version, required extensions, and project dependencies. This setup avoids the common “works on my machine” issues and saves time spent configuring systems, making your workflow cleaner, portable, and more professional.

---

**Step 1: Open GitHub Repository in Codespace**  
Navigate to your repository on GitHub.  
Click the **Code** button, then choose:  
> **Codespaces > Create codespace on main**

---

**Step 2: Add Dev Container Configuration**  
Once inside the Codespace, open the **Command Palette**:  
> Press `Ctrl+Shift+P` (or `F1`)  
Search for and select:  
> `Dev Containers: Add Dev Container Configuration Files`

---

**Step 3: Choose a Template**  
From the available templates, select:  
> `Node.js`  
Then, choose the Node.js version you need (e.g., `Node.js 20`).

This will create a `.devcontainer` folder with the following files:
- `devcontainer.json`
- A Docker-based image definition or reference

---

**Step 4: Optional – Customize Configuration**  
You can edit the `devcontainer.json` file to automatically include useful VS Code extensions and to install dependencies after setup:

```json
"customizations": {
  "vscode": {
    "extensions": [
      "dbaeumer.vscode-eslint",
      "esbenp.prettier-vscode"
    ]
  }
},
"postCreateCommand": "npm install"
```
---
---

## 📘 Chapter 2: JavaScript Basics – Keywords, Literals, and Comments

Before diving into logic and functions, it's essential to understand some of the fundamental building blocks of JavaScript — **keywords**, **literals**, and **comments**. These elements form the foundation of how you write and structure JavaScript code.

---

### What are Keywords in JavaScript?

**Keywords** are reserved words that have a predefined meaning in JavaScript. You cannot use them as variable names, function names, or identifiers because they are part of the language syntax.

They are used to perform specific operations or declare certain structures, such as variables, loops, or functions.

**Examples of JavaScript keywords:**

- `var`, `let`, `const` – used to declare variables  
- `if`, `else`, `switch` – used for conditional logic  
- `for`, `while`, `do` – used for loops  
- `function`, `return` – for defining functions  
- `break`, `continue`, `typeof`, `new`, `class`, `this`, `try`, `catch`, `finally`

**Example:**
```js
let age = 25;  // 'let' is a keyword to declare a variable
```
---
### What are Literals in JavaScript?

**Literals** in JavaScript are fixed values that you use directly in your code. They are not variables, but actual values that get assigned to variables or used in expressions. JavaScript provides several types of literals for different kinds of data.

**Types of JavaScript Literals:**

- **String Literal:** Represents textual data. Example: `"Hello World"`
- **Number Literal:** Represents numeric values. Example: `42`, `3.14`
- **Boolean Literal:** Represents logical values. Example: `true`, `false`
- **Array Literal:** Represents a list of values. Example: `[1, 2, 3]`
- **Object Literal:** Represents a collection of key-value pairs. Example: `{ name: "Yash", age: 21 }`
- **Null Literal:** Represents an empty or non-existent value. Example: `null`

**Example:**
```js
const siteName = "Hackers Paradise"; // "Hackers Paradise" is a string literal
const isLoggedIn = true;             // true is a boolean literal
const numbers = [1, 2, 3];           // [1, 2, 3] is an array literal
```
---
### What are Comments in JavaScript?

**Comments** in JavaScript are lines of code that are not executed by the JavaScript engine. They are used to explain the code, make it more readable, or temporarily disable parts of the code during testing or debugging.

There are two main types of comments in JavaScript:

1. **Single-line Comments**  
   Begin with `//` and continue to the end of the line.

2. **Multi-line Comments**  
   Begin with `/*` and end with `*/`. These can span multiple lines.

**Examples:**

```js
// This is a single-line comment

/*
  This is a multi-line comment.
  It can span multiple lines and is useful
  for adding detailed descriptions or documentation.
*/

let result = a + b; // Add two numbers
```
---
---
## 📘 Chapter 3: Variables in JavaScript

Variables are one of the most fundamental concepts in JavaScript. A variable is used to **store data** that can be referenced and manipulated later in the program. JavaScript allows you to declare variables using three keywords: `var`, `let`, and `const`.

---

### What is a Variable?

A **variable** is a named container for storing data values. Think of it as a label attached to a value that you can refer to later in your code.

```js
let age = 25; // 'age' is a variable storing the value 25
```
### Declaring Variables

In JavaScript, you can declare variables using three keywords: `var`, `let`, and `const`. Each has different behavior and scope rules.

---

#### 1. `var` – Function Scoped (Not Recommended)

- Declared variables are **function-scoped**
- Can be **redeclared and updated**
- Is **hoisted** (moved to the top of the function), but initialized as `undefined`

```js
var x = 10;
var x = 20; // Redeclaration allowed
console.log(x); // 20
```
#### 2. `let` – Block Scoped (Modern and Recommended)

The `let` keyword was introduced in ES6 (ECMAScript 2015) and is the preferred way to declare variables that may change later in your program. It is **block-scoped**, meaning it is only accessible within the `{}` block where it is declared.

**Key Characteristics:**

- Scope: Limited to the block `{}` in which it's declared
- Re-declaration: ❌ Not allowed in the same scope
- Reassignment: ✅ Allowed
- Hoisting: ✅ Hoisted but in a "Temporal Dead Zone" (TDZ) — cannot be accessed before declaration

**Example:**

```js
let message = "Hello";
message = "Welcome"; // Allowed
console.log(message); // Output: Welcome
```
#### 3. `const` – Block Scoped and Constant

The `const` keyword was introduced in ES6 and is used to declare **variables that should never be reassigned**. Like `let`, it is **block-scoped**, but once a `const` variable is assigned, its reference cannot be changed.

**Key Characteristics:**

- Scope: Block-scoped (limited to `{}` where it's declared)
- Re-declaration: ❌ Not allowed in the same scope
- Reassignment: ❌ Not allowed
- Must be initialized at the time of declaration
- Hoisting: ✅ Hoisted but in a "Temporal Dead Zone" (TDZ)

**Example:**

```js
const pi = 3.14;
console.log(pi); // Output: 3.14

// pi = 3.14159; ❌ Error: Assignment to constant variable
```







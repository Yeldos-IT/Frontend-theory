# JavaScript (JS) Basics

JavaScript is a programming language that adds interactivity and functionality to web pages.

---

## **Core Concepts**

### **1. Connecting JS to HTML:**
- Inline: Include JS directly in the HTML file:
  ```html
  <script>
    console.log('Hello, World!');
  </script>
  ```
- External file: Link a separate JavaScript file:
  ```html
  <script src="script.js"></script>
  ```

### **2. Variables:**
- Declaring variables:
  ```javascript
  let x = 10; // Mutable variable
  const y = 20; // Immutable variable
  var z = 30; // Old syntax (avoid using)
  ```

### **3. Data Types:**
- Common types: `string`, `number`, `boolean`, `null`, `undefined`, `object`, `symbol`.
- Example:
  ```javascript
  let name = "Alice"; // string
  let age = 25; // number
  let isStudent = true; // boolean
  ```

### **4. Functions:**
- Standard functions:
  ```javascript
  function greet() {
    console.log("Hello!");
  }
  greet(); // Call the function
  ```
- Arrow functions:
  ```javascript
  const greet = () => console.log("Hello!");
  ```

### **5. Conditional Statements and Loops:**
- Conditionals:
  ```javascript
  if (age > 18) {
    console.log("Adult");
  } else {
    console.log("Minor");
  }
  ```
- Loops:
  ```javascript
  for (let i = 0; i < 5; i++) {
    console.log(i);
  }
  ```

### **6. Arrays and Objects:**
- Arrays:
  ```javascript
  let fruits = ["apple", "banana", "cherry"];
  console.log(fruits[0]); // apple
  ```
- Objects:
  ```javascript
  let person = { name: "Alice", age: 25 };
  console.log(person.name); // Alice
  ```

### **7. DOM Manipulation:**
- Access and modify HTML elements:
  ```javascript
  let element = document.getElementById("myElement");
  element.textContent = "Hello, JS!";
  ```

---

## **Advanced Concepts**

### **1. Asynchronous Programming:**
- Promises:
  ```javascript
  fetch('https://api.example.com')
    .then(response => response.json())
    .then(data => console.log(data));
  ```
- `async/await` syntax:
  ```javascript
  async function getData() {
    let response = await fetch('https://api.example.com');
    let data = await response.json();
    console.log(data);
  }
  ```

### **2. Modules:**
- Export and Import:
  ```javascript
  // script1.js
  export const greet = () => console.log("Hello!");

  // script2.js
  import { greet } from './script1.js';
  greet();
  ```

---

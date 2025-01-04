# JavaScript (JS) — Полный теоретический обзор

## **1. Основы JavaScript**

### **Переменные:**
- `let`: Для переменных, значение которых может изменяться.
- `const`: Для переменных с неизменяемым значением.
- `var`: Устаревшее, избегать использования.
```javascript
let age = 25;
const name = "Alice";
```

### **Типы данных:**
- Примитивные: `string`, `number`, `boolean`, `null`, `undefined`, `symbol`, `bigint`.
- Объектные: `object`, массивы, функции.
```javascript
const isActive = true; // boolean
const user = { name: "Alice", age: 25 }; // object
```

### **Операторы:**
- Арифметические: `+`, `-`, `*`, `/`, `%`, `**`.
- Сравнения: `==`, `===`, `!=`, `!==`, `>`, `<`, `>=`, `<=`.
- Логические: `&&`, `||`, `!`.

---

## **2. Функции**

### **Объявление функций:**
```javascript
function greet(name) {
  return `Hello, ${name}!`;
}
```

### **Стрелочные функции:**
```javascript
const greet = (name) => `Hi, ${name}!`;
```

### **Параметры по умолчанию:**
```javascript
function greet(name = "Guest") {
  return `Hello, ${name}!`;
}
```

---

## **3. Управляющие структуры**

### **Условия:**
```javascript
if (age > 18) {
  console.log("Adult");
} else {
  console.log("Minor");
}
```

### **Циклы:**
- `for`: Итерация через заданный диапазон.
```javascript
for (let i = 0; i < 5; i++) {
  console.log(i);
}
```

- `while`: Повторение, пока условие истинно.
```javascript
let count = 0;
while (count < 5) {
  console.log(count);
  count++;
}
```

---

## **4. Объекты и массивы**

### **Объекты:**
```javascript
const user = { name: "Alice", age: 25 };
console.log(user.name); // Alice
```

### **Массивы:**
```javascript
const fruits = ["apple", "banana", "cherry"];
console.log(fruits[0]); // apple
```

### **Деструктуризация:**
```javascript
const { name, age } = user;
const [firstFruit, secondFruit] = fruits;
```

---

## **5. Асинхронное программирование**

### **Промисы:**
```javascript
const fetchData = () => {
  return new Promise((resolve, reject) => {
    setTimeout(() => resolve("Data loaded"), 1000);
  });
};
fetchData().then((data) => console.log(data));
```

### **async/await:**
```javascript
async function fetchData() {
  const response = await fetch("https://api.example.com");
  const data = await response.json();
  console.log(data);
}
```

---

## **6. DOM Manipulation**

### **Поиск элементов:**
```javascript
const element = document.querySelector("#id");
```

### **Изменение содержимого:**
```javascript
element.textContent = "New Text";
```

### **Стили и классы:**
```javascript
element.style.color = "red";
element.classList.add("active");
```

---

## **7. Web APIs**

### **Fetch API:**
Для выполнения HTTP-запросов.
```javascript
fetch("https://api.example.com")
  .then((response) => response.json())
  .then((data) => console.log(data));
```

### **LocalStorage:**
Для хранения данных в браузере.
```javascript
localStorage.setItem("key", "value");
const value = localStorage.getItem("key");
```

### **Geolocation API:**
Для определения местоположения.
```javascript
navigator.geolocation.getCurrentPosition((position) => {
  console.log(position.coords.latitude);
});
```

---

## **8. Модули**

### **Экспорт и импорт:**
```javascript
// module.js
export const greet = () => console.log("Hello!");

// main.js
import { greet } from "./module.js";
greet();
```

---

## **9. Классы и прототипы**

### **Классы:**
```javascript
class Person {
  constructor(name) {
    this.name = name;
  }
  greet() {
    console.log(`Hello, ${this.name}!`);
  }
}
const alice = new Person("Alice");
alice.greet();
```

### **Прототипы:**
```javascript
function Animal(name) {
  this.name = name;
}
Animal.prototype.speak = function () {
  console.log(`${this.name} makes a sound.`);
};
```

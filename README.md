# Домашнє завдання 6 – Класи

## Опис
Шосте домашнє завдання з JavaScript.  
Практика створення та використання класів, приватних властивостей, методів екземплярів, ключового слова `this` та рефакторингу об’єктів.

## Технології / стек
- JavaScript (ES6+)
- Класи (`class`)
- Приватні властивості (`#`)
- Методи екземплярів
- Ключове слово `this`
- Методи масивів: `push()`, `splice()` або `filter()`
- Методи рядків: `padStart()`, `padEnd()`
- Рефакторинг об’єктів → правильне використання `this`

## Функціонал

| Файл       | Завдання / клас                          | Що робить                                                                 |
|------------|------------------------------------------|---------------------------------------------------------------------------|
| task-1.js  | Об’єкт `customer` (рефакторинг)          | Виправлення методів об’єкта — додавання `this` для доступу до властивостей |
| task-2.js  | Клас `Storage`                           | Управління приватним масивом товарів: отримання, додавання, видалення     |
| task-3.js  | Клас `StringBuilder`                     | Робота з приватним рядком: додавання символів на початок / кінець / обидва боки |

## Приклади роботи (виведення в консоль)

Всі тестові виклики вже присутні в кінці кожного файлу та залишені для перевірки ментором.

Приклади результатів:

```js
// task-1.js
customer.setDiscount(0.15);
console.log(customer.getDiscount());     // 0.15
customer.addOrder(5000, "Steak");
console.log(customer.getBalance());      // 19750
console.log(customer.getOrders());       // ["Burger", "Pizza", "Salad", "Steak"]

// task-2.js
const storage = new Storage(["Nanitoids", "Prolonger", "Antigravitator"]);
console.log(storage.getItems());         // ["Nanitoids", "Prolonger", "Antigravitator"]
storage.addItem("Droid");
console.log(storage.getItems());         // ["Nanitoids", "Prolonger", "Antigravitator", "Droid"]
storage.removeItem("Prolonger");
console.log(storage.getItems());         // ["Nanitoids", "Antigravitator", "Droid"]
storage.removeItem("Scaner");            // нічого не видаляє
console.log(storage.getItems());         // ["Nanitoids", "Antigravitator", "Droid"]

// task-3.js
const builder = new StringBuilder(".");
console.log(builder.getValue());         // "."
builder.padStart("^");
console.log(builder.getValue());         // "^."
builder.padEnd("^");
console.log(builder.getValue());         // "^.^"
builder.padBoth("=");
console.log(builder.getValue());         // "=^.^="

```
## Демо / деплой
Активне демо доступне за [посиланням](https://artemilliushchenko.github.io/goit-js-hw-06/)

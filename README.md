# 🟦 TypeScript Starter Project (GoIT HW-05)

Цей проєкт демонструє базове налаштування середовища для роботи з TypeScript,
компіляцію коду та запуск у браузері через локальний сервер.

---

## 🚀 Технології

- TypeScript
- Node.js
- @web/dev-server
- HTML5

## ⚙️ Налаштування середовища

### 1. Встановлення залежностей

npm install

### 2. Запуск проєкту

npm start

Після цього відкриється браузер з локальним сервером.

### 3. Компіляція TypeScript

tsc

Або в режимі слідкування:

tsc -w

## Команди встановлення

npm init -y npm install --save-dev typescript npm install --save-dev
@web/dev-server

## 🛠️ Налаштування TypeScript

Файл tsconfig.json:

- rootDir: ./src — вихідні файли
- outDir: ./dist — зкомпільовані файли
- module: es2020 — підтримка ES-модулів
- lib: ["dom", "ES2021"] — доступ до DOM API
- sourceMap: true — для debugging
- strictNullChecks: true — сувора перевірка null

🧠 Як працює код

📌 concatenation.ts

Функція приймає два рядки і виводить їх у консоль:

function concatenation(firstWord: string, secondWord: string) {
console.log(`${firstWord} ${secondWord}`); }

📌 index.ts

- знаходить кнопку та input
- додає обробник кліку
- викликає функцію concatenation

button.addEventListener('click', () => { concatenation(input.value, 'hello!');
});

🌐 HTML

<script type="module" src="./dist/index.js"></script>

⚠️ defer не потрібен, тому що type="module" вже працює як defer.

🐞 Debugging

Увімкнено sourceMap: true, що дозволяє:

- бачити TypeScript код у DevTools
- ставити breakpoints
- зручно відлагоджувати код

❗ Важливо

- Проєкт працює тільки через сервер (не через file://)
- Використовується ES Modules
- Необхідно запускати через npm start

✅ Результат

Користувач вводить текст у поле → натискає кнопку → у консолі з’являється
результат:

yourText hello!

# Ми також можемо стежити за зміною файлу в режимі реального часу, виконавши команду:

tsc test.ts -watch

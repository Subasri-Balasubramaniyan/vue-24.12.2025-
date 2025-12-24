📘 Phase 1: Modern Web Foundation (ES6+)

This project is part of the Vue 3 learning roadmap.
Before starting Vue 3, it is important to understand modern JavaScript (ES6+) concepts, because Vue 3 is built entirely on them.

This repository covers:

JavaScript reactivity basics

Async/Await

ES Modules (import/export)

Arrow functions

📂 Project Structure
modules/
│
├── package.json
├── main.js
├── math.js
├── user.js
└── README.md

⚙️ Prerequisites

Node.js v18 or above

VS Code (recommended)

Basic JavaScript knowledge

Check Node version:

node -v

🔹 1. Reactivity Basics
let vs const
let count = 1;
count = 2;

const name = "Vue";
// name = "React"; ❌ Not allowed

Objects & Arrays (Passed by Reference)
const user1 = { name: "Subasri" };
const user2 = user1;

user2.name = "Developer";

console.log(user1); // name changed


📌 Vue uses this behavior to track changes and update UI automatically.

🔹 2. Async / Await

Used for handling API calls.

async function getUsers() {
  const response = await fetch("https://jsonplaceholder.typicode.com/users");
  const data = await response.json();
  console.log(data);
}

getUsers();


✔ Cleaner than .then()
✔ Widely used in Vue lifecycle hooks

🔹 3. ES Modules (import / export)
Exporting a function

📄 math.js

export function add(a, b) {
  return a + b;
}


📄 main.js

import { add } from "./math.js";

console.log(add(5, 3));

Default Export

📄 user.js

export default function getUser() {
  return { name: "Subasri", role: "Student" };
}


📄 main.js

import getUser from "./user.js";

console.log(getUser());

🔹 4. Arrow Functions
const greet = name => "Hello " + name;
console.log(greet("Subasri"));

With Arrays
const numbers = [1, 2, 3];
const doubled = numbers.map(n => n * 2);

console.log(doubled);


📌 Arrow functions are heavily used in Vue 3 Composition API.

📦 package.json Configuration

To enable ES modules in Node.js:

{
  "name": "modules",
  "version": "1.0.0",
  "type": "module"
}

▶️ How to Run the Project

1️⃣ Open terminal in project folder
2️⃣ Run:

node main.js


✔ Output will be shown in terminal

⚠️ VS Code Warning (SchemaStore)

You may see this warning:

Problems loading reference 'https://www.schemastore.org/package'


🔹 This is NOT an error
🔹 It does NOT affect your code or Vue
🔹 Happens due to internet/DNS restriction

✅ Safe to ignore

Optional fix:

{
  "json.schemaDownload.enable": false
}

🎯 Why This Phase Is Important for Vue 3
Concept	Used in Vue 3
const / let	State handling
Reference types	Reactivity
Async/Await	API calls
ES Modules	Component system
Arrow functions	Composition API

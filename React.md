 # React Interview Notes (Beginner to Core Concepts)

---

## ✅ What is React?
- React is a **JavaScript library** for building **user interfaces (UI)**.
- Used to create **Single Page Applications (SPA)**.
- Based on **component-based architecture**.

**Interview One-Liner:**  
React is a JavaScript library used to build fast and interactive user interfaces.

---

## ✅ Why We Use React
- Fast UI with **Virtual DOM**
- **Reusable components**
- **Automatic re-rendering**
- Easy to manage **large applications**
- Huge community & job demand

**Interview One-Liner:**  
 # React Interview Notes (Beginner to Core Concepts)

---

## ✅ What is React?
- React is a **JavaScript library** for building **user interfaces (UI)**.
- Used to create **Single Page Applications (SPA)**.
- Based on **component-based architecture**.

**Interview One-Liner:**  
React is a JavaScript library used to build fast and interactive user interfaces.

---

## ✅ Why We Use React
- Fast UI with **Virtual DOM**
- **Reusable components**
- **Automatic re-rendering**
- Easy to manage **large applications**
- Huge community & job demand

**Interview One-Liner:**  
We use React because it makes UI fast, reusable, and scalable.

---

## ✅ DOM, Virtual DOM & React Fiber

### ✅ What is DOM?
- Real DOM is the **actual UI in the browser**
- Direct updates are **slow**
- Causes reflow & repaint

### ✅ What is Virtual DOM?
- A **JavaScript copy of the Real DOM**
- Stored in **memory**
- React updates this first → **fast**

### ✅ What Happens When State Changes?
1. New Virtual DOM is created  
2. Old vs New Virtual DOM compared  
3. Only the changed part is updated in Real DOM  

### ✅ React Fiber Engine
- React’s **internal rendering engine**
- Makes rendering:
  - Non-blocking
  - Priority-based
- Can:
  - Pause
  - Resume
  - Stop low-priority work

**Final Flow:**  
State change → Virtual DOM → Fiber → Real DOM update

---

## ✅ When React Re-renders

### ✅ React Re-renders When:
- State changes (`setState`, `useState`)
- Props change
- Parent component re-renders
- Context value changes
- `key` value changes

### ❌ React Does NOT Re-render When:
- A normal variable changes
- DOM is updated manually

---

## ✅ JSX – Main Topics

- JSX is **JavaScript + HTML/XML**
- Must return a **single parent**
- Uses **`className` instead of `class`**
- JavaScript inside `{ }`
- Supports **expressions, not statements**
- Converts to **`React.createElement()`**
- Can render **components**
- All tags must be **closed**
- **Conditional rendering** using `&&`, `?:`
- **Lists rendering** using `.map()`
- **Fragments**: `<> </>`

---

## ✅ JSX Expressions vs Statements

### ✅ Allowed (Expressions)
```jsx
{name}
{10 + 5}
{isLogin ? "Yes" : "No"}
{isAdmin && <Admin />}
```

### ❌ Not Allowed (Statements)
```jsx
if(){}
for(){}
while(){}
```

### ✅ How to Use Statements in React

#### Using if Outside JSX
```jsx
let msg;
if (isLogin) msg = "Welcome";
return <h1>{msg}</h1>;
```

#### Using Ternary
```jsx
{isLogin ? "Welcome" : "Login Please"}
```

#### Using &&
```jsx
{isAdmin && <AdminPanel />}
```

#### Replacing for with .map()
```jsx
{items.map(item => <li>{item}</li>)}
```

---

## ✅ Import & Export

### ✅ Two Types
- Named Export
- Default Export

### ✅ Named Export
- Must use `{ }`
- Name must be same
- Can export many

```js
export const add = (a,b) => a + b;
export const sub = (a,b) => a - b;

import { add, sub } from "./math";
```

### ✅ Rename with `as`
```js
import { add as plus } from "./math";
```

### ✅ Default Export
- Only one default
- No `{ }`
- Can be imported with ANY name

```js
const multiply = (a,b) => a * b;
export default multiply;

import mul from "./math";
```

### ✅ Both Together
```js
export const add = (a,b) => a + b;
export default multiply;

import multiply, { add } from "./math";
```

### ✅ Interview Key Line
- Default export → no `{ }`, any name
- Named export → `{ }`, same name (or `as`)

---

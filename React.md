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
# React Components – Short Summary

- A **component** is a reusable piece of UI.
- React apps are built by **combining multiple components**.
- Components make code:
  - Reusable  
  - Easy to maintain  
  - Easy to debug  

## ✅ Types of Components
- **Functional Components** (modern, most used)
- Class Components (old, rarely used)

## ✅ Rules of Components
- Must start with a **Capital letter**
- Must **return JSX**
- One component should do **one main job**

## ✅ Components Use:
- **Props** → to receive data
- **State** → to manage dynamic data

## ✅ When a Component Re-renders
- State changes
- Props change
- Parent re-renders
- Context changes

## ✅ Interview One-Liner
Components are reusable UI blocks in React used to build scalable and maintainable applications.
# ✅ React Props – Detailed Summary (Interview Ready)

---

## ✅ 1. What are Props?
- **Props = Properties**
- Props are used to **pass data from Parent → Child component**
- They work like **function arguments** for components
- Used to make components **dynamic and reusable**

✅ Example idea:
Parent sends → name, age  
Child receives → displays name, age

---

## ✅ 2. Why We Need Props
We need props to:
- ✅ Reuse the same component with different data
- ✅ Pass data between components
- ✅ Avoid hardcoding values
- ✅ Make UI dynamic
- ✅ Keep components independent and modular

Without props:
- You must create multiple similar components
- Code becomes repetitive and inefficient

---

## ✅ 3. How Props Work (Data Flow)
- Data always flows in **one direction**
- From **Parent → Child**
- This is called:
> ✅ **One-Way Data Flow**

---

## ✅ 4. Props are Read-Only (Immutable)
- ❌ Props **cannot be changed inside child**
- ✅ Props are controlled by the **parent**
- If data must change → use **state**

Reason:
- Keeps data **predictable**
- Makes debugging **easy**
- Prevents unexpected behavior

---

## ✅ 5. Props vs State (Core Difference)

| Feature | Props | State |
|--------|--------|--------|
| Comes from | Parent Component | Same Component |
| Can be changed? | ❌ No | ✅ Yes |
| Used for | Passing data | Dynamic data |
| Ownership | Parent | Component itself |
| Re-render on change | ✅ Yes | ✅ Yes |

---

## ✅ 6. Advantages of Props
- ✅ Reusable components
- ✅ Clean and modular code
- ✅ Easy to debug
- ✅ Easy to test
- ✅ Better code organization
- ✅ Useful in team projects

---

## ❌ 7. Disadvantages of Props
- ❌ Props drilling in large apps
- ❌ Too many props make code messy
- ❌ Cannot modify props directly
- ❌ Deep component trees become hard to manage

---

## ❌ 8. Props Drilling
- Passing data through many unnecessary components
- Example:
App → A → B → C → D  
(Only D needs the data, but all receive it)

Problems:
- Messy code
- Hard debugging
- Poor maintainability

---

## ✅ 9. Why Context is Needed Instead of Props
- Context is used to:
  - ✅ Avoid props drilling
  - ✅ Share global data easily

Use Context for:
- Auth data
- Theme
- Cart data
- User info

---

## ✅ 10. Props vs Context

| Feature | Props | Context |
|--------|--------|----------|
| Used for | Local data | Global data |
| Data flow | Parent → Child | Any component |
| Props drilling | ✅ Happens | ❌ Avoided |
| Setup | Simple | Advanced |
| Re-render scope | Small | Can be global |

✅ Context is **NOT a replacement** for props  
✅ Both are used **together**

---

## ✅ 11. Passing Functions as Props
- Used for **Child → Parent communication**
- Parent sends function
- Child calls it on button click, submit, etc.

Used in:
- Buttons
- Forms
- Delete/update actions

---

## ✅ 12. When to Use Props
Use props when:
- Data is required by **few components**
- Data flows only **1–2 levels deep**
- You want **simple and clean logic**

---

## ✅ 13. When NOT to Rely on Props Only
- When many deep components need the same data
- When props drilling becomes heavy  
→ Use **Context API**

---

## ✅ 14. Most Powerful Interview One-Liners

- **“Props are immutable data passed from parent to child components to make UI dynamic and reusable.”**
- **“Props follow one-way data flow in React.”**
- **“Props drilling is solved by Context API.”**
- **“Context is not a replacement for props, it is used for global data.”**

---

✅ END OF PROPS SUMMARY

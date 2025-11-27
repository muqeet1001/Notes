# React – Introduction

## ✅ What is React?
- React is a **JavaScript library** used to build **user interfaces (UI)**.
- It is mainly used to create **Single Page Applications (SPA)**.
- It works using **components** (small reusable UI parts).

**Interview One-Liner:**  
React is a JavaScript library used to build fast and interactive user interfaces using components.

------

## ✅ Why We Use React?
- Fast UI updates using Virtual DOM  
- Reusable components  
- Automatic re-rendering when data changes  
- Easy to manage large applications  
- Strong job demand and community support  

**Interview One-Liner:**  
We use React because it makes UI fast, reusable, and easy to manage for large applications.
---
# DOM, Virtual DOM & React Fiber Engine

## ✅ 1. What is DOM?
- **DOM (Document Object Model)** is the **actual UI shown in the browser**.
- It is created from **HTML elements**.
- When DOM updates, the browser:
  - Recalculates layout
  - Repaints the screen  
- Because of this, **direct DOM updates are slow**.

---

## ✅ 2. What is Virtual DOM?
- Virtual DOM is a **JavaScript copy of the Real DOM**.
- It is stored in **memory**, not directly on the screen.
- React **updates the Virtual DOM first**, not the Real DOM.
- Since it is in memory, it is **very fast**.

---

## ✅ 3. What Happens When State Changes?
When you call `setState()` or `useState()`:
1. React creates a **new Virtual DOM**
2. React compares it with the **old Virtual DOM**
3. It finds **only what has changed**
4. Only that change is sent to the **Real DOM**

✅ This is the main reason why React is **fast**.

---

## ✅ 4. How React Fiber Engine Uses DOM & Virtual DOM
- **React Fiber is the internal rendering engine of React**
- It controls:
  - When to compare
  - What to update
  - Which update is more important

### What Fiber Can Do:
- Break rendering into **small tasks**
- Can:
  - Pause rendering
  - Resume rendering
  - Stop low-priority work
  - Focus on high-priority updates (like button clicks)

✅ Because of Fiber, React is **smooth, fast, and responsive**.

---

## ✅ 5. Final One-Line Interview Flow
State changes → Virtual DOM updates → Fiber compares → Only changed part updates in Real DOM.

---
# When React Re-renders

## ✅ React Re-renders When:
- State changes (`setState`, `useState`)
- Props change
- Parent component re-renders
- Context value changes
- `key` value changes

---

## ❌ React Does NOT Re-render When:
- A normal variable changes
- DOM is updated manually


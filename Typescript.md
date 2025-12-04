| Topic | JavaScript | TypeScript |
|------|------------|-------------|
| Definition | A scripting language | JavaScript + Data Types |
| Data Types | Not strict | Strict (string, number, boolean) |
| Wrong Input | Allowed | Not allowed |
| Error Detection | At runtime | Before running (compile time) |
| Large Projects | Hard to manage | Easy to manage |
| Code Safety | Low | High |
| Runs Directly? | ✅ Yes | ❌ No (converts to JS first) |

---

### JavaScript Example (Problem)

```js
function greet(name) {
  return "Hello " + name;
}

greet(42); // ❌ Wrong but allowed



function greet(name: string): string {
  return `Hello ${name}`;
}

greet("Amit"); // ✅ Correct
greet(42);     // ❌ Error

```

# TypeScript to JavaScript – Behind the Scenes (Short Summary)

This video explains how **TypeScript (TS) code is converted into JavaScript (JS)** step by step.

## ✅ 1. Write TypeScript Code
You start by writing a `.ts` file in the editor.

## ✅ 2. Lexer (Tokenization)
- Breaks the code into **tokens** (keywords, variables, symbols).
- Catches basic errors like:
  - Missing `;`
  - Missing brackets or quotes

## ✅ 3. Parser (AST Creation)
- Converts tokens into an **Abstract Syntax Tree (AST)**.
- AST shows the **structure of your code in tree form**.

## ✅ 4. Binder (TypeScript Special Step)
- Creates:
  - **Symbol tables**
  - **Parent pointers**
  - **Flow nodes** (for `if/else`, conditions)
- Helps prepare the code for deep type checking.

## ✅ 5. Checker (Type Checking)
- Checks all **types and variables**.
- Runs multiple times for accuracy.
- Finds:
  - Type mismatches
  - Wrong assignments
  - Structural type errors

## ✅ 6. Emitter (Final Output)
- Removes all **TypeScript-only syntax** (types, interfaces, annotations).
- Generates:
  - `.js` file (main output)
  - `.d.ts` file (type declarations)
  - Source map files

## ✅ Final Result
You get **pure JavaScript** that browsers and Node.js can run.

> Simple line:
**TypeScript only checks types — JavaScript is what actually runs.**


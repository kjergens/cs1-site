# Introduction to Programming with Scratch

---

## 1.3.1 What Is Scratch?

Scratch is a **block-based visual programming language**. Instead of typing code, you drag and snap together colored blocks that represent instructions. The result is a program — the same fundamental thing you'll build in Java.

You've used Scratch in middle school. In this unit, we're using it deliberately: every concept you see in Scratch has a direct equivalent in Java. The goal is not to become a Scratch expert — it's to see the structure of programming before we add Java's syntax on top.

---

## 1.3.2 Core Programming Concepts in Scratch (and in Java)

### 1. Sequence

Programs run **top to bottom**, one instruction at a time, in order.

In Scratch, blocks in a script execute from the top block down. If you want something to happen first, it goes on top.

In Java, statements inside `main` execute in order, line by line.

---

### 2. Variables

A **variable** is a named container for a value that can change.

In Scratch: use **Make a Variable**, give it a name, and use **set [ ] to** and **change [ ] by** blocks.

In Java:
```java
int score = 0;
score = score + 1;
```

Same idea — a name, a value, the ability to update it.

---

### 3. Conditionals

A **conditional** runs code only if a condition is true.

In Scratch: `if < > then` and `if < > then / else` blocks.

In Java:
```java
if (score > 10) {
    System.out.println("You win!");
} else {
    System.out.println("Keep going.");
}
```

The diamond-shaped condition slots in Scratch correspond to the `( )` in Java's `if` statement.

---

### 4. Loops

A **loop** repeats code multiple times without copy-pasting.

| Scratch block | Java equivalent |
|---|---|
| `forever` | `while (true)` |
| `repeat (10)` | `for (int i = 0; i < 10; i++)` |
| `repeat until < >` | `while (!condition)` |

The idea is the same: a chunk of code that runs again and again, either a fixed number of times or until a condition is met.

---

### 5. Events

In Scratch, scripts start when something happens — "when green flag clicked", "when key pressed".

In Java, the equivalent is the **main method** — the entry point where your program begins:
```java
public static void main(String[] args) {
    // your program starts here
}
```

---

## 1.3.3 The Bridge

| Scratch concept | Java equivalent |
|---|---|
| Script (blocks top to bottom) | Statements in `main` |
| Variable block | `int x = 0;` |
| `if < > then` | `if (condition) { }` |
| `repeat (n)` | `for` loop |
| `forever` / `repeat until` | `while` loop |
| When green flag clicked | `public static void main(...)` |
| Say [ ] | `System.out.println(...)` |

Every program you write this year — in Scratch or Java — uses these same building blocks. The language changes; the structure doesn't.

# While Loops

---

## Key Concept: Repetition

An `if` statement runs code once — if the condition is true, the block runs and the program moves on.

A `while` loop is different: after the block runs, the program goes **back to check the condition again**. If it's still true, the block runs again. This continues until the condition becomes false.

---

## Syntax

```java
while (condition) {
    // code to repeat
}
```

---

## Example: Counting with a While Loop

```java
int x = 0;
while (x <= 4) {
    System.out.println("Number: " + x);
    x += 1;
}
```

Trace:
- `x = 0`: `0 <= 4` is true → print `Number: 0` → `x` becomes `1`
- `x = 1`: `1 <= 4` is true → print `Number: 1` → `x` becomes `2`
- `x = 2`: `2 <= 4` is true → print `Number: 2` → `x` becomes `3`
- `x = 3`: `3 <= 4` is true → print `Number: 3` → `x` becomes `4`
- `x = 4`: `4 <= 4` is true → print `Number: 4` → `x` becomes `5`
- `x = 5`: `5 <= 4` is **false** → loop exits

Output:
```
Number: 0
Number: 1
Number: 2
Number: 3
Number: 4
```

---

## The Infinite Loop Problem

If the condition never becomes false, the loop runs forever — an **infinite loop**. This usually means the loop variable is never updated.

**Broken — infinite loop:**
```java
int x = 0;
while (x <= 4) {
    System.out.println("Number: " + x);
    // x never changes — this runs forever
}
```

**Fixed — x is incremented:**
```java
int x = 0;
while (x <= 4) {
    System.out.println("Number: " + x);
    x += 1;   // x changes → loop eventually ends
}
```

---

## Key Points

- The loop checks its condition **before** every iteration
- If the condition is `true`, the loop body executes
- When the condition becomes `false`, the loop exits
- **Without an update step, the loop can run forever**
- A well-designed while loop ensures the condition eventually becomes false

---

## When to Use While vs. For

Use a `while` loop when you **don't know in advance** how many times the loop will run — for example, reading input until the user types `"quit"`.

Use a `for` loop when you **do know** how many times it will run. (Covered in Unit 4.)

---

## Check Your Understanding

1. What is the output of this code?
```java
int count = 10;
while (count > 7) {
    System.out.println(count);
    count--;
}
```

2. What change would make this an infinite loop? How would you fix it?
```java
int n = 1;
while (n < 100) {
    System.out.println(n);
}
```

3. Write a while loop that prints the even numbers from 2 to 10.

---

## Answer Key

1.
```
10
9
8
```
`count` starts at 10, decrements each iteration. When `count = 7`, `7 > 7` is false and the loop exits.

2. `n` is never incremented — infinite loop. Fix: add `n *= 2;` (or `n++`, etc.) inside the loop body.

3.
```java
int n = 2;
while (n <= 10) {
    System.out.println(n);
    n += 2;
}
```

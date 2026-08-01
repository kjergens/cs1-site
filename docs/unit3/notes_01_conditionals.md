# Conditional Code Blocks

---

## Section 1: What Is a Conditional Block?

A **conditional block** lets your program decide whether to run certain code based on whether a condition is `true` or `false`. Think of it like a fork in the road — the program chooses one path depending on the situation.

You've already worked with two types of code blocks:
1. **class block** — the outermost block defining a class
2. **main method block** — where our program runs

A conditional block is a third type, nested inside the main method.

---

## Section 2: Comparison Operators

To create conditions, we use **comparison operators**. These compare two values and return either `true` or `false`.

| Operator | Meaning | Example | Result |
|---|---|---|---|
| `<` | less than | `2 < 6` | `true` |
| `>` | greater than | `10 > 5` | `true` |
| `==` | equal to | `10 == 5` | `false` |
| `!=` | not equal to | `7 != 7` | `false` |
| `<=` | less than or equal to | `3 <= 3` | `true` |
| `>=` | greater than or equal to | `4 >= 5` | `false` |

These operators don't return numbers — they return `true` or `false`.

---

## Section 3: The boolean Type

**`boolean`** variables store either `true` or `false`. You can save the result of a comparison:

```java
boolean flag = 2 < 6;   // flag is true because 2 is less than 6
```

Using a boolean can make your code read like a sentence.

---

## Section 4 The `if` Statement

```java
if (condition) {
    // runs only if condition is true
}
```

**Example:**
```java
int age = 17;

if (age >= 18) {
    System.out.println("You are old enough to vote!");
}
System.out.println("Done.");
```

Output for `age = 17`:
```
Done.
```

`17 >= 18` is `false`, so the message is skipped. `"Done."` prints regardless because it's outside the `if` block.

---

## Section 5: The `if` / `else` Statement

`else` runs only if the `if` condition is `false`.

```java
if (age >= 18) {
    System.out.println("You are old enough to vote!");
} else {
    System.out.println("Sorry, you are not old enough to vote.");
}
System.out.println("Done.");
```

Output for `age = 17`:
```
Sorry, you are not old enough to vote.
Done.
```

Only **one** of the `if` or `else` blocks runs — never both.

---

## Section 6: The `else if` Statement

Use `else if` to check multiple conditions in sequence:

```java
int number = 2;

if (number > 0) {
    System.out.println("The number is positive!");
} else if (number == 0) {
    System.out.println("The number is zero.");
} else {
    System.out.println("The number is negative.");
}
```

Java stops at the **first** condition that is `true` and skips the rest. If none are true, the `else` block runs as a catch-all.

---

## Section 7: Key Takeaways

- Conditional blocks let your program make decisions
- Conditions use comparison operators to evaluate to `true` or `false`
- `boolean` variables store `true` or `false`
- Only the block whose condition is `true` runs — the others are skipped
- `else if` lets you chain multiple conditions

---

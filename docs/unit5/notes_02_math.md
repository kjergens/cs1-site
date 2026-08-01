# Chapter 2: The Math Class

---

## Section 1: Overview

Java's built-in `Math` class provides useful mathematical methods. You don't need to import anything — `Math` is always available.

In this unit you'll learn nine of them: `Math.max`, `Math.min`, `Math.sqrt`, `Math.abs`, `Math.pow`, `Math.round`, `Math.ceil`, `Math.floor`, and `Math.random`.

---

## Section 2: Math.max(x, y) and Math.min(x, y)

`Math.max` returns the larger value. `Math.min` returns the smaller.

```java
int a = Math.max(5, 10);     // 10
int b = Math.min(5, 10);     // 5

double r = Math.max(5.3, 10.8);   // 10.8
double s = Math.min(5.3, 10.8);   // 5.3
```

---

## Section 3: Math.sqrt(x)

Returns the square root of `x`. Always returns a `double`.

```java
double a = Math.sqrt(64);    // 8.0
double b = Math.sqrt(2);     // 1.4142135...
```

---

## Section 4: Math.abs(x)

Returns the absolute (positive) value of `x`.

```java
int i    = Math.abs(-4);     // 4
double a = Math.abs(-4.7);   // 4.7
```

---

## Section 5: Math.pow(x, y)

Returns `x` raised to the power of `y`. Always returns a `double`.

```java
double d = Math.pow(2, 8);   // 256.0  (2⁸ = 256)
double e = Math.pow(3, 3);   // 27.0
```

Note: even if the result is a whole number, `Math.pow` returns a `double` (e.g., `256.0`, not `256`).

---

## Section 6: Rounding Methods

| Method | Behavior | Example | Result |
|---|---|---|---|
| `Math.round(x)` | Rounds to nearest integer | `Math.round(4.6)` | `5` |
| `Math.ceil(x)` | Always rounds **up** | `Math.ceil(4.1)` | `5.0` |
| `Math.floor(x)` | Always rounds **down** | `Math.floor(4.9)` | `4.0` |

All three take a `double` as input.

```java
double a = Math.round(4.6);   // 5.0  (over .5 rounds up)
double b = Math.ceil(4.1);    // 5.0  (any decimal rounds up)
double c = Math.floor(4.9);   // 4.0  (any decimal rounds down)
```

---

## Section 7: Math.random()

Returns a random `double` between `0.0` (inclusive) and `1.0` (exclusive).

```java
double rand = Math.random();        // e.g., 0.7342...
```

To get a random number in a larger range, multiply:

```java
double rand = Math.random() * 10;   // 0.0 to 9.999...
```

To get a random integer from 0 to n-1:

```java
int roll = (int)(Math.random() * 6);   // 0, 1, 2, 3, 4, or 5
```

---

## Unit 5 Chapter 2 Homework

Use the Java `Math` methods from the notes above to answer each question.

1. What does `Math.max(14, 9)` return?
2. What does `Math.min(6.2, 3.8)` return?
3. What does `Math.sqrt(81)` return?
4. What does `Math.abs(-27)` return?
5. What does `Math.pow(4, 3)` return?
6. What does `Math.round(7.3)` return?
7. What does `Math.ceil(5.1)` return?
8. What does `Math.floor(9.9)` return?
9. What `Math` expression generates a random number between `0.0` and `0.9999...`?
10. Write a line of Java code that declares a `double` variable called `r` and assigns it a random number between `0.0` and `10.0`.

---

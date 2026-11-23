# Chapter 2: While Loops

---

## Section 1: Key Concept: Repetition

An `if` statement runs code once — if the condition is true, the block runs and the program moves on.

A `while` loop is different: after the block runs, the program goes **back to check the condition again**. If it's still true, the block runs again. This continues until the condition becomes false.

The structure of a while loop is this:


```java
while (condition) {
    // code to repeat
}
```

---

## Section 2: Example: Counting with a While Loop

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

## Section 3: The Infinite Loop Problem

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

## Section 4: Key Points

- The loop checks its condition **before** every iteration
- If the condition is `true`, the loop body executes
- When the condition becomes `false`, the loop exits
- **Without an update step, the loop can run forever**
- A well-designed while loop ensures the condition eventually becomes false


---


## Homework

!!! attention
    ### HW 9 - Unit 3 Chapter 2: While Loops

    1. What does this loop print?
    ```java
    int x = 1;
    while (x <= 5) {
        System.out.println(x);
        x++;
    }
    ```

    2. Trace through this loop. What is the final value of `total`?
    ```java
    int total = 0;
    int i = 1;
    while (i <= 4) {
        total += i;
        i++;
    }
    ```

    3. Write a while loop that prints the numbers 10 down to 1 (one per line).

    4. This loop is supposed to print `"Hi"` 3 times, but it runs forever. What's wrong, and how would you fix it?
    ```java
    int count = 0;
    while (count < 3) {
        System.out.println("Hi");
    }
    ```

    5. Write a while loop that starts at `100` and keeps dividing by `2`, printing each result, stopping once the value is less than `1`.

    #### FizzBuzz Challenge

    Write a program that prints the numbers from 1 to 500, with these rules:

    - For numbers divisible by both 3 and 5, print `"FizzBuzz"` instead of the number (hint: use the modulus operator `%`)
    - For numbers divisible by 3, print `"Fizz"` instead of the number
    - For numbers divisible by 5, print `"Buzz"` instead of the number
    - For all other numbers, print the number itself

    **Example output (numbers 1–15):**
    ```
    1
    2
    Fizz
    4
    Buzz
    Fizz
    7
    8
    Fizz
    Buzz
    11
    Fizz
    13
    14
    FizzBuzz
    ```

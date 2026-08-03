# Chapter 3: Operators and Re-assignment

---

## Section 1: Re-assignment

### Using assignment operator (=)

A variable's value isn't fixed — once declared, you can give it a new value at any time. This is called **re-assignment**.

```java
int score = 50;
score = score + 10;   // score is now 60
score = score * 2;    // score is now 120
```

**Key points:**
- After the initial declaration (`int score = 50;`), later lines don't repeat the type — just `score = ...;`
- The right side of `=` is evaluated first, using the variable's *current* value — then the result is stored back into the variable
- Assigning one variable to another (`int b = a;`) copies the current value at that moment. Later changing `a` does **not** change `b`.

---

### Increment and Decrement

**`++`** increases a variable by 1. **`--`** decreases a variable by 1. They're shorthand for the most common kind of re-assignment.

```java
int count = 0;
count++;   // same as: count = count + 1;   → count is 1
count++;   // → count is 2

int lives = 3;
lives--;   // same as: lives = lives - 1;   → lives is 2
```

**Key points:**
- `count++;` is exactly equivalent to `count = count + 1;`
- `lives--;` is exactly equivalent to `lives = lives - 1;`
- These stand alone as statements — they don't print or return a value by themselves

---

### Using Compound Assignments

Compound assignment operators combine an operation with re-assignment in one step.

| Operator | Equivalent to | Example |
|---|---|---|
| `+=` | `x = x + n` | `x += 7;` |
| `-=` | `x = x - n` | `x -= 3;` |
| `*=` | `x = x * n` | `x *= 2;` |
| `/=` | `x = x / n` | `x /= 4;` |

```java
int points = 100;
points += 50;   // points is now 150
points -= 30;   // points is now 120
points *= 2;    // points is now 240
```

**Key points:**
- `x += 7;` means "take `x`, add 7, store the result back in `x`" — read it right to left, not as "x equals plus 7"
- Watch out for `=+` vs `+=` — same two characters, different order, and they mean very different things in Java
- Compound assignment works with `+`, `-`, `*`, `/`, and more

---

## Homework

!!! attention
    ### Unit 2 Chapter 3 Homework

    *Assigned Class 9 · Due Class 10*

    #### Part A: Evaluate the Expression

    Assume the following variables are declared:
    ```java
    int a = 10;
    int b = 3;
    double x = 10.0;
    ```

    Write the result of each expression. If the result is a decimal, include the `.0`.

    1. `a + b`
    2. `a - b`
    3. `a * b`
    4. `a / b`
    5. `x / b`
    6. `a % b`
    7. `a % 2`
    8. `b % a`

    **Think about it:** Problems 4 and 5 look similar. Why are the answers different?

    #### Part B: Trace the Re-assignments

    Show the value of the variable after each line executes.

    9.
    ```java
    int score = 50;          // score = ____
    score = score + 10;      // score = ____
    score = score * 2;       // score = ____
    score = score - 5;       // score = ____
    ```

    10.
    ```java
    int n = 8;               // n = ____
    n = n / 3;               // n = ____
    n = n + 1;               // n = ____
    ```

    11.
    ```java
    int a = 5;               // a = ____
    int b = a;                // b = ____
    a = 99;                   // a = ____
                               // b = ____ (did b change?)
    ```

    #### Part C: Increment and Decrement

    12. What does `count++` do? Write an equivalent statement using `=` and `+`.
    13. What will the following code print?
    ```java
    int count = 0;
    count++;
    count++;
    count++;
    System.out.println(count);
    ```
    14. What will the following code print?
    ```java
    int lives = 3;
    System.out.println(lives);
    lives--;
    System.out.println(lives);
    lives--;
    System.out.println(lives);
    ```

    #### Part D: Compound Assignment

    15. Rewrite each statement using a compound assignment operator (`+=`, `-=`, `*=`, `/=`):

    | Original | Rewrite with compound operator |
    |---|---|
    | `x = x + 7;` | |
    | `x = x - 3;` | |
    | `x = x * 2;` | |
    | `x = x / 4;` | |

    16. What will the following code print?
    ```java
    int points = 100;
    points += 50;
    points -= 30;
    points *= 2;
    System.out.println(points);
    ```
    17. What will the following code print?
    ```java
    int n = 20;
    n /= 4;
    n += 3;
    n++;
    System.out.println(n);
    ```

    #### Part E: Find the Bug

    Each snippet below has exactly one error. Identify the line and describe the problem.

    18.
    ```java
    int total = 0;
    total =+ 10;
    System.out.println(total);
    ```
    (This code compiles and runs — but does not do what the programmer intended. What does `=+` actually do?)

    19.
    ```java
    int x = 7;
    int y = 0;
    System.out.println(x / y);
    ```

# Unit 3: Check Your Understanding

!!! information

    1. What is the output of this code?
    ```java
    int x = 5;
    if (x > 10) {
        System.out.println("big");
    } else if (x > 3) {
        System.out.println("medium");
    } else {
        System.out.println("small");
    }
    ```

    2. What is the difference between `=` and `==`?

    3. Write an `if/else` that prints `"even"` if a number is divisible by 2, and `"odd"` otherwise. (Hint: use `%`)

    4. What is the output of this code?
    ```java
    int count = 10;
    while (count > 7) {
        System.out.println(count);
        count--;
    }
    ```

    5. What change would make this an infinite loop? How would you fix it?
    ```java
    int n = 1;
    while (n < 100) {
        System.out.println(n);
    }
    ```

    6. Write a while loop that prints the even numbers from 2 to 10.

    7. Write a boolean expression that checks whether a number `n` is between 1 and 100, inclusive. Why wouldn't `n >= 1 || n <= 100` work as a range check?

    ---

    ### Answer Key

    1. `medium` — `5 > 10` is false, `5 > 3` is true, so the second block runs.

    2. `=` is **assignment** (store a value in a variable). `==` is **comparison** (check if two values are equal). Mixing them up is one of the most common bugs in Java.

    3. 
    ```java
    if (number % 2 == 0) {
        System.out.println("even");
    } else {
        System.out.println("odd");
    }
    ```

    4.
    ```
    10
    9
    8
    ```
    `count` starts at 10, decrements each iteration. When `count = 7`, `7 > 7` is false and the loop exits.

    5. Variable `n` is never incremented leading to an infinite loop. Fix: add `n *= 2;` (or `n++`, etc.) inside the loop body.

    6.
    ```java
    int n = 2;
    while (n <= 10) {
        System.out.println(n);
        n += 2;
    }
    ```

    7. `n >= 1 && n <= 100` — both conditions must be true at once, which is what actually narrows the check to a range. `n >= 1 || n <= 100` doesn't work because it's true for *every* number: any `n` satisfies at least one side (either it's ≥ 1, or it's ≤ 100, or both), so the check never actually excludes anything.

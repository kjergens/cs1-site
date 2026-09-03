# Unit 4: Practice Quiz

!!! information

    *Ungraded self-check — use this to prepare for Quiz 3. Answer key is at the bottom; don't peek until you've tried every question. Covers the same skills as the real quiz: tracing for loops, counting iterations, filling in loop headers, finding/fixing bugs, and writing your own loop.*

    1. What is the output of the following code?
    ```java
    for (int i = 0; i < 6; i++) {
        System.out.print(i + " ");
    }
    ```

    2. In the for loop `for (int i = 0; i < 10; i++)`, what is the purpose of `i < 10`?
    - A. It sets the starting value of `i`
    - B. It checks whether the loop should continue
    - C. It updates `i` after each iteration
    - D. It declares a new variable

    3. How many times does the following loop execute?
    ```java
    for (int i = 5; i <= 25; i += 5) {
        System.out.println(i);
    }
    ```

    4. Fill in the blank so the loop prints `8, 6, 4, 2`:
    ```java
    for (int i = 8; i >= 1; _________) {
        System.out.println(i);
    }
    ```

    5. The following loop is supposed to print the numbers 1 through 10, but it has a bug. Identify the bug and write the corrected loop.
    ```java
    for (int i = 1; i < 10; i++) {
        System.out.println(i);
    }
    ```

    6. Write a for loop that prints every even number from 2 to 12.

    ---

    ### Answer Key

    1. **`0 1 2 3 4 5 `**

    2. **B.** It checks whether the loop should continue

    3. **5 times** — `i` goes 5, 10, 15, 20, 25 (step 5, `<= 25`)

    4. **`i -= 2`**

    5. Bug: `i < 10` stops the loop before printing `10` — off-by-one at the end. Corrected:
    ```java
    for (int i = 1; i <= 10; i++) {
        System.out.println(i);
    }
    ```

    6. 
    ```java
    for (int i = 2; i <= 12; i += 2) {
        System.out.println(i);
    }
    ```

    **Study tip:** Question 5's bug (`<` instead of `<=` cutting off the last number) is the single most common for-loop mistake — if you missed it, try tracing the loop by hand, writing out each value of `i` and whether the condition is still true, rather than just reading the code.

# Unit 3: Practice Quiz

!!! information

    *Ungraded self-check — use this to prepare for Quiz 2. Answer key is at the bottom; don't peek until you've tried every question. Covers the same skills as the real quiz: if/else if/else chains, boolean logic, and while loops (tracing, writing, and filling in blanks).*

    1. What does the following code print?
    ```java
    int score = 78;
    if (score >= 90) {
        System.out.println("A");
    } else if (score >= 80) {
        System.out.println("B");
    } else {
        System.out.println("C");
    }
    ```

    2. Which boolean expression is true when `x` is between 10 and 20, inclusive?
    - A. x >= 10 && x <= 20
    - B. x > 10 && x < 20
    - C. x >= 10 || x <= 20
    - D. x > 10 || x < 20

    3. What is the output of the following code?
    ```java
    int n = 1;
    while (n <= 4) {
        System.out.print(n * 3 + " ");
        n++;
    }
    ```

    4. Fill in the blank so the loop prints the numbers 1 through 6:
    ```java
    int i = 1;
    while ( _________________ ) {
        System.out.println(i);
        i++;
    }
    ```

    5. Write a Java if-else statement that checks whether a variable named `windChill` is less than `20` and prints `"Bundle up!"` if true, otherwise prints `"Mild out."`

    6. Write a while loop that prints the following output:
    ```
    15
    12
    9
    6
    3
    ```

    ---

    ### Answer Key

    1. **`C`** — `score = 78`: not `>= 90`, not `>= 80`

    2. **A.** `x >= 10 && x <= 20`

    3. **`3 6 9 12 `** — `n` goes 1→4, printing `n*3` each time

    4. **`i <= 6`**

    5. 
    ```java
    if (windChill < 20) {
        System.out.println("Bundle up!");
    } else {
        System.out.println("Mild out.");
    }
    ```

    6. 
    ```java
    int i = 15;
    while (i >= 3) {
        System.out.println(i);
        i -= 3;
    }
    ```

    **Study tip:** if you missed Question 2, review why `||` versions are wrong here — `x > 10 || x < 20` is actually true for *every* number, since any `x` satisfies at least one side. `&&` is what actually narrows things down to a range.

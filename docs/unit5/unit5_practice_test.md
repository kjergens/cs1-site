# Practice Test #2 (Units 3 - 5)

!!! information

    *Ungraded self-check — use this to prepare for Test 2. Answer key is at the bottom; don't peek until you've tried every question. Covers the same skills as the real test: conditionals, while loops, for loops, string methods, and the Math class.*

    ### Conditionals & While Loops

    1. What is the output of the following code?
    ```java
    int temp = 55;
    if (temp > 80) {
        System.out.println("Hot");
    } else if (temp > 60) {
        System.out.println("Warm");
    } else {
        System.out.println("Cold");
    }
    ```

    2. What is the output of the following code?
    ```java
    int n = 2;
    while (n <= 6) {
        System.out.print(n + " ");
        n += 2;
    }
    ```

    3. How many times does the body of this loop execute?
    ```java
    int x = 0;
    while (x < 30) {
        x += 5;
    }
    ```

    4. What is wrong with the following loop? Explain in one sentence.
    ```java
    int count = 10;
    while (count > 0) {
        System.out.println(count);
    }
    ```

    5. Write a Java while loop that counts down from 7 to 1, printing each number on its own line. After the loop ends, print `"Liftoff!"`.

    ### For Loops

    6. What is the output of the following code?
    ```java
    for (int k = 2; k <= 8; k += 2) {
        System.out.print(k + " ");
    }
    ```

    7. How many times does the body of this loop execute?
    ```java
    for (int i = 0; i <= 15; i += 4) {
        System.out.println("Hi");
    }
    ```

    8. Fill in the missing part so this loop prints: `9 6 3`
    ```java
    for (int x = 9; x >= 1; _________) {
        System.out.print(x + " ");
    }
    ```

    9. What is wrong with this for-loop header? Explain in one sentence.
    ```java
    for (int m = 0, m < 10, m++) {
    ```

    10. What does this code print?
    ```java
    String word = "banana";
    int count = 0;
    for (int i = 0; i < word.length(); i++) {
        if (word.charAt(i) == 'a') {
            count++;
        }
    }
    System.out.println(count);
    ```

    11. Fill in the blanks to make this loop print all even numbers from 4 to 16 (including 16):
    ```java
    for (int i = 4; i <= _______; _______) {
        System.out.println(i);
    }
    ```

    ### Strings

    12. (True / False) String objects in Java are immutable.

    13. Fill in the blank: the String method that returns a new String with every letter converted to uppercase is `___________________`.

    14. What is the output of this code?
    ```java
    String phrase = "Coding is great";
    System.out.println(phrase.substring(7, 9));
    ```

    15. What is the output of this code?
    ```java
    String word = "kayak";
    System.out.println(word.substring(0, word.length() / 2 + 1));
    ```

    ### Math Class

    16. What are the exact return values?<br>
    [ ] a) `Math.pow(3, 4)` → \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_<br>
    [ ] b) `Math.max(7, Math.min(15, 9))` → \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

    17. What single expression using the Math class gives a random integer from 1 to 6 (inclusive), to simulate a die roll?

    18. Write one line using `Math` that gives the larger of these two values: the square root of `100` and the absolute value of `-12`.

    19. What does `Math.random()` return? Choose the most accurate description.<br>
    [ ] A. always 0.0<br>
    [ ] B. always 1.0<br>
    [ ] C. a value ≥ 0.0 and < 1.0<br>
    [ ] D. an integer between 1 and 10

    ---

    ### Answer Key

    1. **`Cold`** — `55` is not `> 80` and not `> 60`

    2. **`2 4 6 `** — `n` goes 2, 4, 6, then stops (`8 > 6`)

    3. **6 times** — `x` goes 0, 5, 10, 15, 20, 25 (body runs), then `x = 30` fails `< 30`

    4. `count` is never updated — it stays `10` forever, so `count > 0` is always true. **Infinite loop.**

    5. 
    ```java
    int n = 7;
    while (n >= 1) {
        System.out.println(n);
        n--;
    }
    System.out.println("Liftoff!");
    ```

    6. **`2 4 6 8 `**

    7. **4 times** — `i` goes 0, 4, 8, 12 (body runs), then `i = 16` fails `<= 15`

    8. **`x -= 3`**

    9. Bug: uses **commas instead of semicolons** to separate the header's three parts. Should be `for (int m = 0; m < 10; m++)`.

    10. **3** — `"banana"` has `'a'` at indices 1, 3, 5

    11. Blanks: **`16`**, **`i += 2`**

    12. **True**

    13. **`toUpperCase()`**

    14. **`is`** — `"Coding is great".substring(7, 9)` (indices 7–8)

    15. **`kay`** — `word.length()` is `5`, so `length()/2` is `2`, `+1` is `3`; `substring(0, 3)` = indices 0–2

    16. a) **`81.0`** (`Math.pow` always returns `double`) b) **`9`** (`Math.min(15,9)=9`, then `Math.max(7,9)=9`)

    17. **`(int)(Math.random() * 6) + 1`**

    18. **`Math.max(Math.sqrt(100), Math.abs(-12))`** — evaluates to `12.0`

    19. **C.** a value ≥ 0.0 and < 1.0

    **Study tip:** Question 15 is the trickiest one here — it's the same "compute an index from `.length()`" skill worth double-checking your integer division (`length()/2` truncates) if you got it wrong.

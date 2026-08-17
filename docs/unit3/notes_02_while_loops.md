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

## Section 6: When to Use While vs. For

Use a `while` loop when you **don't know in advance** how many times the loop will run — for example, reading input until the user types `"quit"`.

Use a `for` loop when you **do know** how many times it will run. (Covered in Unit 4.)

---

## In-Class Activity: FortuneTeller (Partner Activity)

!!! attention
    ### FortuneTeller — In-Class Partner Activity

    *Complete with a partner in class, in JuiceMind.com — go to Teams/Classes, select our CS section, then Code Sandbox.*

    Create a new Code Sandbox named `FortuneTeller` (language: Java). Start from this template:

    ```java
    import java.util.Random;

    public class Main {
        public static void main(String[] args) {

            // 1. Generate random number (DO NOT CHANGE)
            Random random = new Random();
            int num = random.nextInt(100) + 1;

            // 4. Display greeting with fortune number
            // YOUR CODE HERE

            // 5. Use if-else statements for fortune rules
            // YOUR CODE HERE

            // 6. Display ending message
            // YOUR CODE HERE

        }
    }
    ```

    Finish writing the program. It should:

    - Generate a random number `num` between 1 and 100 (already provided)
    - Display a personalized fortune message based on `num`, using the rules below
    - End with: `"Thanks for using Fortune Teller!"`

    | Range | Type | Message |
    |---|---|---|
    | 1–33 | Negative | "Tough times ahead - watch out for surprises!" |
    | 34–66 | Neutral | "An average day - nothing special happens." |
    | 67–100 | Positive | "Great luck awaits you - amazing things coming!" |

    **Additional rules (these override the ranges above):**

    - If the number is exactly `50`: `"Perfectly balanced - a day of harmony!"`
    - If the number is exactly `100`: `"JACKPOT! The best day of your life!"`
    - If the number is exactly `1`: `"Yikes! Total disaster ahead - stay in bed!"`

    **Hint:** use the logical operator `&&` for multiple conditions (see Chapter 1, Section 7).

    **Sample output:**
    ```
    Hello! Your fortune number is: 85
    Great luck awaits you - amazing things coming!
    Thanks for using Fortune Teller!
    ```
    ```
    Hello! Your fortune number is: 1
    Yikes! Total disaster ahead - stay in bed!
    Thanks for using Fortune Teller!
    ```

---

## Homework

!!! attention
    ### HW 9 - Unit 3 Chapter 2: While Loops

    #### Part A: While Loop Practice

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

    #### Part B: FizzBuzz

    *Complete in JuiceMind.com — go to Teams/Classes, select our CS section, then Code Sandbox.*

    Create a new Code Sandbox named `FizzBuzz` (language: Java). Write a program that prints the numbers from 1 to 500, with these rules:

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

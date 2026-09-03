# Unit 2: Practice Test

!!! information

    *Ungraded self-check — use this to prepare for Test 1. Answer key is at the bottom; don't peek until you've tried every question. Covers the same skills as the real test: binary conversion, binary addition, Scratch vocabulary, Java syntax basics, operators, string concatenation, and Scanner.*

    1. For the binary number `01101`, what is the correct decimal representation?
    - A. 11
    - B. 12
    - C. 13
    - D. 14

    2. For the decimal number `20`, write the binary representation: _______

    3. Add the following two binary numbers, showing your work:
    ```
      1101
    + 0101
    ```

    4. Match each Scratch block to its function:

    | Scratch Block | Function |
    |---|---|
    | `"turn 15 degrees"` | |
    | `"wait 1 seconds"` | |
    | `"if < > then / else"` | |
    | `"when I receive [message]"` | |

    Functions: *(a) Pauses the script for a set amount of time. (b) Runs one set of code if a condition is true, another if false. (c) Rotates the sprite by a set amount. (d) Starts a script when a broadcast is received.*

    5. In MIT Scratch, what is the purpose of `Make a Block` (custom block)?
    - A. It creates a new sprite
    - B. It allows you to group and reuse code like a function
    - C. It changes the background color
    - D. It only stores variables

    6. If your Java class is named `Robot`, what must the file name be?
    - A. HelloWorld.java
    - B. Class.java
    - C. Public Main
    - D. Robot.java

    7. Which of the following correctly declares a `double` variable named `price` and initializes it to `9.99`?
    - A. double price = 9.99;
    - B. price double = 9.99;
    - C. double price(9.99);
    - D. 9.99 = double price;

    8. What is the result of `15 % 4`?
    - A. 3.75
    - B. 3
    - C. 4
    - D. 11

    9. What does `y` equal after this code runs?
    ```java
    int y = 1;
    y += 4;
    y + 1;
    ```
    - A. 6
    - B. 5
    - C. 1
    - D. Error

    10. What is the output of the following print statements?
    ```java
    System.out.println(5 + 2 + " points");
    System.out.println("points: " + 5 + 2);
    ```

    11. What will be printed by the following code?
    ```java
    String subject = "Math";
    int grade = 95;
    System.out.println("Subject: " + subject + ", Grade: " + grade + ".");
    ```

    12. Fill in the blanks to complete this program, which asks for the user's favorite color and prints it back:
    ```java
    import java.util.Scanner;

    public class Example {
        public static void main(String[] args) {
            String color = "";
            Scanner scan = new Scanner(System.in);

            System.out.println("What is your favorite color?");
            color = _______________________________;

            System.out.println("Nice, I like " ______________ " too!");
        }
    }
    ```

    13. Name two different data types in Java and give a brief example of when you would use each.

    14. What is the difference between the operators `++` and `+=`? Write a short code example showing each.

    ---

    ### Answer Key

    1. **C) 13** — `01101` = 8+4+0+1

    2. **10100**

    3. **10010** — `1101 (13) + 0101 (5) = 18`

    4. `"turn 15 degrees"` → (c); `"wait 1 seconds"` → (a); `"if < > then / else"` → (b); `"when I receive [message]"` → (d)

    5. **B)** allows you to group and reuse code like a function

    6. **D) Robot.java** — file name must match the class name

    7. **A)** `double price = 9.99;`

    8. **B) 3** — `15 % 4`

    9. **D) Error** — `y + 1;` alone isn't a valid Java statement (a bare arithmetic expression can't stand on its own — only assignments, `++`/`--`, method calls, and object creation can). `y` would be `5` after `y += 4` *if* the code compiled, but it doesn't.

    10. `5 + 2 + " points"` → **`7 points`** (arithmetic first, left to right, then concatenation). `"points: " + 5 + 2` → **`points: 52`** (once a String appears, everything after is concatenation, left to right)

    11. **`Subject: Math, Grade: 95.`**

    12. `color = scan.nextLine();` (or `scan.next()`), then `System.out.println("Nice, I like " + color + " too!");`

    13. Open-ended — any 2 valid types with a reasonable example (e.g. `int` for counting, `String` for text, `double` for decimals, `boolean` for true/false flags)

    14. `++` increments by exactly 1 (`x = x + 1`); `+=` adds any specified amount (`x = x + n`). Example: `int x = 5; x++;  // x is 6` vs. `int y = 5; y += 3;  // y is 8`

    **Study tip:** Question 9 is the same trap that shows up on the real test — a bare expression like `y + 1;` with nothing done with the result (no assignment, no print) doesn't compile in Java. If you missed it, that's the one thing worth re-reading before the real test.

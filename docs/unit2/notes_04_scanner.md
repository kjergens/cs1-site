# Chapter 4: Scanner and User Input

---

## Section 1: Why Scanner?

- Lets your program talk to the user
- Reads what the user types on the keyboard
- Can read different types: `String`, `int`, `double`, etc.

---

## Section 2: Import (do this once at the top)

```java
import java.util.Scanner;
```

---

## Section 3: Create the Scanner Object

```java
Scanner scan = new Scanner(System.in);   // "System.in" = keyboard
```

`scan` is now your input object. You can name it anything (`scan`, `input`, `keyboard`), but be consistent.

---

## Section 4: Reading Different Kinds of Input

### Read one word — `next()`
```java
String word = scan.next();
```
Reads the next word (up to a space). Everything becomes a `String` — even if the user types `42`, it is the `String` `"42"`, not the number `42`.

### Read a whole line — `nextLine()`
```java
String line = scan.nextLine();
```
Reads everything the user types until they press Enter, including spaces.

### Read an int — `nextInt()`
```java
int age = scan.nextInt();
```
Reads an integer. If the user types `42`, `age` stores the `int` `42`.

### Read a double — `nextDouble()`
```java
double price = scan.nextDouble();
```
Reads a decimal number. If the user types `3.14`, `price` stores the `double` `3.14`.

---

## Section 5: Mini Examples

### Example 1 — Reading a full line as a String
```java
import java.util.Scanner;

public class Greet {
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        System.out.println("Enter your full name: ");
        String name = scan.nextLine();
        System.out.println("Hello, " + name + "!");
    }
}
```
Sample run:
```
Enter your full name:
Clarissa 123
Hello, Clarissa 123!
```

### Example 2 — Reading int and double
```java
import java.util.Scanner;

public class NumbersExample {
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        System.out.print("Enter your age: ");
        int age = scan.nextInt();
        System.out.print("Enter your GPA: ");
        double gpa = scan.nextDouble();
        System.out.println("You are " + age + " years old.");
        System.out.println("Your GPA is " + gpa + ".");
    }
}
```

---

## Section 6: Important: The nextLine() Trap

When `nextLine()` comes **after** `next()`, `nextInt()`, or `nextDouble()`, it often **skips** a line.

**Broken code:**
```java
System.out.print("Enter your age: ");
int age = scan.nextInt();
System.out.print("Enter your name: ");
String name = scan.nextLine();   // ← gets skipped — reads empty ""
```

**Why?** `nextInt()` reads only the number. When the user presses Enter, a newline character (`\n`) is left waiting in the input buffer. `nextLine()` sees that leftover newline and returns an empty `String`.

**The fix — add an extra `nextLine()` to clear the buffer:**
```java
System.out.print("Enter your age: ");
int age = scan.nextInt();
scan.nextLine();                 // clears the leftover newline
System.out.print("Enter your name: ");
String name = scan.nextLine();   // now this works
```

**Rule of thumb:** If you go from `nextInt()` or `nextDouble()` → `nextLine()`, add one extra `nextLine()` in between.

---

## Section 7: Converting Strings to int or double

`nextLine()` always returns a `String`. If you need a number, convert after:

### String → int
```java
String text = scan.nextLine();
int number = Integer.parseInt(text);
```

### String → double
```java
String text = scan.nextLine();
double number = Double.parseDouble(text);
```


---

## Homework

!!! attention
    ### Unit 2 Chapter 4 Homework

    *Assigned Class 10 · Due Class 11*

    #### Part A: Scanner Methods

    Match each thing you want to read to the correct Scanner method (word bank: `nextInt()`, `nextDouble()`, `next()`, `nextLine()`):

    - A whole number → ?
    - A decimal number → ?
    - One word (stops at a space) → ?
    - A full line of text (including spaces) → ?

    #### Part B: Complete the Code

    2. Fill in the blanks so this program reads an integer and prints it doubled:
    ```java
    _____________ java.util.Scanner;

    public class Double {
        public static void main(String[] args) {
            Scanner sc = new Scanner(_____________);

            System.out.print("Enter a number: ");
            int n = sc._____________;

            System.out.println("Doubled: " + _____________);
        }
    }
    ```

    3. Fill in the blanks so this program greets the user by name:
    ```java
    import java.util.Scanner;

    public class Greeter {
        public static void main(String[] args) {
            Scanner _____________ = new Scanner(System.in);

            System.out.print("What is your name? ");
            String name = _____________.next();

            System.out.println("Hello, " + _____________ + "!");
        }
    }
    ```

    #### Part C: Predict the Output

    For each program, the user's input is given — write what the program prints.

    4. User types `8`:
    ```java
    Scanner sc = new Scanner(System.in);
    System.out.print("Enter a number: ");
    int x = sc.nextInt();
    System.out.println("You entered: " + x);
    System.out.println("One more: " + (x + 1));
    ```

    5. User types `Maya`:
    ```java
    Scanner sc = new Scanner(System.in);
    System.out.print("Enter your name: ");
    String name = sc.next();
    System.out.println(name + name);
    System.out.println(name.length());
    ```

    6. User types `4` then `7`:
    ```java
    Scanner sc = new Scanner(System.in);
    System.out.print("First number: ");
    int a = sc.nextInt();
    System.out.print("Second number: ");
    int b = sc.nextInt();
    System.out.println(a + " + " + b + " = " + (a + b));
    ```

    7. User types `5`:
    ```java
    Scanner sc = new Scanner(System.in);
    System.out.print("Enter a number: ");
    int n = sc.nextInt();
    System.out.println(n + 2);
    System.out.println("n + 2");
    ```
    What is the difference between `n + 2` and `"n + 2"`?

    #### Part D: Write the Program

    8. Write a complete Java program (including import and `main`) that:
       - Asks the user: `"Enter your age: "`
       - Reads the age as an integer
       - Prints: `"In 10 years you will be "` followed by their age plus 10

    9. Write a complete Java program that:
       - Asks the user for two decimal numbers (prompt each separately)
       - Prints their average

    #### Part E: Find the Bug

    Each snippet has exactly one error. Identify the line and describe the problem.

    10.
    ```java
    public class Hello {
        public static void main(String[] args) {
            Scanner sc = new Scanner(System.in);
            System.out.print("Name: ");
            String name = sc.next();
            System.out.println("Hi " + name);
        }
    }
    ```

    11.
    ```java
    import java.util.Scanner;

    public class Age {
        public static void main(String[] args) {
            Scanner sc = new Scanner(System.in);
            System.out.print("Enter your age: ");
            int age = sc.nextDouble();
            System.out.println("Age: " + age);
        }
    }
    ```

    12.
    ```java
    import java.util.Scanner;

    public class Square {
        public static void main(String[] args) {
            Scanner sc = new Scanner(System.in);
            System.out.print("Enter a number: ");
            sc.nextInt();
            System.out.println("Squared: " + n * n);
        }
    }
    ```

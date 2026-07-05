# Scanner and User Input

---

## 1. Why Scanner?

- Lets your program talk to the user
- Reads what the user types on the keyboard
- Can read different types: `String`, `int`, `double`, etc.

---

## 2. Import (do this once at the top)

```java
import java.util.Scanner;
```

---

## 3. Create the Scanner Object

```java
Scanner scan = new Scanner(System.in);   // "System.in" = keyboard
```

`scan` is now your input object. You can name it anything (`scan`, `input`, `keyboard`), but be consistent.

---

## 4. Reading Different Kinds of Input

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

## 5. Mini Examples

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

## 6. Important: The nextLine() Trap

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

## 7. Converting Strings to int or double

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

## Check Your Understanding

1. What import statement is required to use Scanner?
2. Write the line that creates a Scanner named `input` that reads from the keyboard.
3. True or False: `scan.nextLine()` can read a sentence with spaces.
4. If the user types `42` and you read it with `scan.nextLine()`, what type is stored?
5. Why does `nextLine()` sometimes return an empty string when it follows `nextInt()`?
6. How do you fix the `nextLine()` trap?
7. What method converts the `String` `"999"` to the `int` `999`?

---

## Answer Key

1. `import java.util.Scanner;`
2. `Scanner input = new Scanner(System.in);`
3. True
4. The `String` `"42"` — not the number
5. `nextInt()` leaves a newline in the buffer; `nextLine()` reads it immediately and returns `""`
6. Add `scan.nextLine();` after `nextInt()` (or `nextDouble()`) to consume the leftover newline
7. `Integer.parseInt("999")`

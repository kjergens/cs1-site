# Java Program Structure, Printing, and Operators

---

## 2.1.1 Program Structure

Every Java program requires a class definition. The `main` method is the entry point — where your program starts running.

```java
public class HelloWorld {
    public static void main(String[] args) {
        // Code goes here
    }
}
```

**Key rules:**
- The class name must match the file name (`HelloWorld.java` for class `HelloWorld`)
- Code blocks are enclosed in curly braces `{}`
- Statements end with a semicolon `;`
- Java is case-sensitive
- Comments: `//` for single-line, `/* */` for multi-line

---

## 2.1.2 Printing

**`System.out.println()`** — prints text or values with a new line at the end.

**`System.out.print()`** — prints without a new line.

```java
System.out.println("Hello, World!");       // Prints: Hello, World!
System.out.print("No new line");           // Stays on same line
System.out.println("Age: " + age);        // Concatenates string and variable
```

**Key points:**
- Use `+` to concatenate strings with variables or other strings
- `println` adds a new line; `print` does not

---

## 2.1.3 Arithmetic Operations

| Operator | Meaning | Example | Result |
|---|---|---|---|
| `+` | Addition | `5 + 3` | `8` |
| `-` | Subtraction | `5 - 3` | `2` |
| `*` | Multiplication | `5 * 3` | `15` |
| `/` | Division | `15 / 3` | `5` |
| `%` | Modulus (remainder) | `7 % 3` | `1` |

**Key points:**
- Integer division (`int / int`) truncates decimal parts — `7 / 2` gives `3`, not `3.5`
- Use `double` for precise decimal results
- Modulus (`%`) returns the remainder after division
- Operator precedence: `*`, `/`, `%` before `+`, `-`. Use `()` to override.

---

## 2.1.4 Comparison Operators

Java can compare values and produce a `boolean` result (`true` or `false`).

| Operator | Meaning | Example | Result |
|---|---|---|---|
| `==` | Equal to | `5 == 5` | `true` |
| `!=` | Not equal to | `5 != 3` | `true` |
| `>` | Greater than | `10 > 5` | `true` |
| `<` | Less than | `2 < 4` | `true` |
| `>=` | Greater or equal | `5 >= 5` | `true` |
| `<=` | Less or equal | `3 <= 4` | `true` |

```java
System.out.println(10 > 5);  // true
System.out.println(3 == 3);  // true
System.out.println(7 <= 6);  // false
```

**Key points:**
- A comparison always produces a `boolean` — never a number
- Don't confuse `==` (comparison) with `=` (assignment) — mixing these up is one of the most common beginner bugs
- Java converts `boolean`s to text automatically, so you can combine comparisons with strings using `+`: `"Is 10 > 5? " + (10 > 5)` prints `Is 10 > 5? true`

---

## Unit 2 Homework 0 — Java to Scratch (teacher will give you worksheet)

---

## Unit 2 Homework 1 — Java Structure and Operators

There are five parts, plus an ungraded bonus for optional enrichment. Each part has a short background, then exercises — read the background, then answer the exercises that follow.

### Part 1: Java Program Structure

```java
public class MyFirstProgram {
    public static void main(String[] args) {
        // This is a comment.
    }
}
```

1.1. What do you think happens if you run the program above?
1.2. If you rename the class to `HelloJava`, what should the file name be?

### Part 2: Printing in Java

```java
public class Greet {
    public static void main(String[] args) {
        System.out.println("My name is");
        System.out.println("Java Beginner!");
    }
}
```

2.1. Predict the output of the code above.
2.2. Write a simple program that prints your name.

### Part 3: Arithmetic Operations

3.1. Predict the output for each line:
```java
a. System.out.println(8 * 6 % 3 + 9);
b. System.out.println((12 / 3) + (4 - 2) * 5);
```
3.2. Write a print statement that calculates `(10 + 5) * 2 % 7`, then predict the result.

### Part 4: Comparison Operators

4.1. Predict the output (true or false) for each line:
```java
a. System.out.println(8 != 8);
b. System.out.println(15 >= 10 + 5);
c. System.out.println((20 / 4) < 6);
```
4.2. Write a print statement comparing whether `9 * 2` is greater than or equal to `20 - 3`. Predict what it prints.

### Part 5: Combining Printing, Strings, and Operations

You can join strings, math, and comparisons using `+`. Java automatically converts numbers and booleans to text.

```java
System.out.println("The sum is: " + (5 + 3));
System.out.println("Is 10 > 5? " + (10 > 5));
System.out.println("Result: " + (8 * 6 % 3 + 9));
```

5.1. Predict the output of:
```java
System.out.println("Answer: " + (10 - 2 * 3) + ". Is it positive? " + (10 - 2 * 3 > 0));
```
5.2. Write a full program that prints: `The result of 7 + 5 % 2 is: [result]. Is it even? [true/false]` (hint: use `result % 2 == 0` to check if even).

### Bonus Challenge (optional, ungraded)

Write a program that prints:
```
What is 4 * 5? Answer: [result]
Is the answer greater than 10? [true/false]
```

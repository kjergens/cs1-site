# Java Program Structure, Variables, and Operations

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

## 2.1.4 Variables and Data Types

A variable is a named container for storing data. It must be declared with a type before use.

### Numeric Types

**`int`** — whole numbers (e.g., `5`, `-10`)

**`double`** — decimal numbers (e.g., `3.14`, `-0.001`)

```java
int age = 25;
double price = 19.99;
```

```java
int a = 10;
int b = 3;
int sum  = a + b;   // 13
int diff = a - b;   // 7
int prod = a * b;   // 30
int quot = a / b;   // 3  (integer division — truncates)
int rem  = a % b;   // 1

double c = 10.0;
double d = 3.0;
double div = c / d; // 3.3333...
```

### Non-Numeric Types

**`boolean`** — stores `true` or `false`

**`char`** — stores a single character, enclosed in single quotes

**`String`** — stores a sequence of characters, enclosed in double quotes

```java
boolean isActive = true;
char grade = 'A';
String name = "Alice";
```

**Key points:**
- `boolean` is used for true/false logic (e.g., in conditions)
- `char` uses single quotes; `String` uses double quotes
- `String` is a class, not a primitive type, and supports text manipulation
- Use `+` to concatenate `String` with other types (e.g., `"Age: " + 25`)

---

## 2.1.5 Check Your Understanding

1. Write a Java program that declares two `int` variables, adds them, and prints the result.
2. Modify the program to use `double` instead and perform division.
3. Write a program that prints your name and age on separate lines.
4. What is the result of `25 % 4`?
5. What is the result of `7 / 2` if both are declared as `int`?

# Variables and Data Types

---

## 2.2.1 Variables and Data Types

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

## Homework 6 — Variables and Data Types

*Assigned Class 8 · Due Class 9*

### Part 1: Identify the Data Type

For each value below, name the Java data type that best represents it (`int`, `double`, `boolean`, `String`, or `char`):

1. `42`
2. `"Hello, world!"`
3. `3.14`
4. `'A'`
5. `true`
6. `"false"`
7. `0`
8. `'7'`

### Part 2: Declare and Initialize Variables

Write a single Java statement to declare and initialize each variable described. Use the correct data type.

9. An integer named `score` with value `100`
10. A decimal number named `gpa` with value `3.75`
11. A boolean named `isLoggedIn` set to `false`
12. A String named `greeting` with value `"Good morning"`
13. A char named `grade` with value `'B'`

### Part 3: Predict the Output

What will each snippet print? Write your answer exactly as it would appear on screen.

14.
```java
int x = 10;
int y = 3;
System.out.println(x);
System.out.println(y);
System.out.println(x + y);
```

15.
```java
String first = "Ada";
String last = "Lovelace";
System.out.println(first + last);
System.out.println(first + " " + last);
```

16.
```java
int age = 17;
String name = "Jordan";
System.out.println(name + " is " + age + " years old.");
```

17.
```java
double price = 2.5;
int quantity = 4;
System.out.println("Total: " + price * quantity);
```

### Part 4: Find the Bug

Each snippet below has exactly one error. Identify the line with the error and explain what's wrong. You don't need to fix it — just describe the problem.

18.
```java
int count = "five";
System.out.println(count);
```

19.
```java
char initial = "K";
System.out.println(initial);
```

20.
```java
String message = 'hello';
System.out.println(message);
```

21.
```java
double temperature = 98.6
System.out.println(temperature);
```

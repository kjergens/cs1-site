# Chapter 2: Variables and Data Types

---

## Section 1: Variables and Data Types

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

## Homework

!!! attention
    ### HW 5 - Unit 2 Chapter 2: Variables and Data Types

    1. For each value below, name the Java data type that best represents it (`int`, `double`, `boolean`, `String`, or `char`):
        a. `42`
        b. `"Hello, world!"`
        c. `3.14`
        d. `'A'`
        e. `true`
        f. `"false"`
        g. `0`
        h. `'7'`
    2. Declare and initialize an integer named `score` with value `100`
    3. Declare and initialize a decimal number named `gpa` with value `3.75`
    4. Declare and initialize a boolean named `isLoggedIn` set to `false`
    5. Declare and initialize a String named `greeting` with value `"Good morning"`
    6. Declare and initialize a char named `grade` with value `'B'`
    7. Predict the output. What will output if this code is run?
    ```java
    int x = 10;
    int y = 3;
    System.out.println(x);
    System.out.println(y);
    System.out.println(x + y);
    ```
    8. Predict the output. What will output if this code is run?
    ```java
    int age = 17;
    String name = "Jordan";
    System.out.println(name + " is " + age + " years old.");
    ```
    9. Predict the output. What will output if this code is run?
    ```java
    double price = 2.5;
    int quantity = 4;
    System.out.println("Total: " + price * quantity);
    ```
    10. Identify the line with the error and explain what's wrong. 
    ```java
    int count = "five";
    System.out.println(count);
    ```
    11. Identify the line with the error and explain what's wrong. 
    ```java
    char initial = "K";
    System.out.println(initial);
    ```
    12. Identify the line with the error and explain what's wrong. 
    ```java
    double temperature = 98.6
    System.out.println(temperature);
    ```

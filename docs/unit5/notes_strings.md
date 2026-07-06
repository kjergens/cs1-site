# Strings

---

## 5.1.1 Overview

In Java, a `String` is used to store text. It is **not** a simple primitive like `int` or `double` — it is a special type called an **object**, which means it comes with built-in methods you can call on it.

**Key idea: Strings are immutable.** Once a `String` is created, it cannot be changed. Any method that seems to change it actually creates a brand-new `String`. To save the result, you must reassign it.

---

## 5.1.2 Declaring Strings

```java
String greeting = "Hello World!";
String message = "Welcome to Java";

String empty = "";       // empty string
String nothing;          // declared but not initialized
```

---

## 5.1.3 Adding to a String

Use `+=` to append text:

```java
String s = "cat";
s += "s";   // s is now "cats"
```

**Important:** `+=` only works if the `String` already has a value, even if that value is `""`.

```java
// OK
String s = "";
s += "toy";   // s is now "toy"

// ERROR — no initial value
String t;
t += "toy";   // won't compile
```

---

## 5.1.4 Common String Methods

### `length()`
Returns the number of characters in the String. Spaces count.

```java
String text = "Java";
int len = text.length();   // 4
```

### `toUpperCase()` and `toLowerCase()`
```java
String shout   = "hello".toUpperCase();   // "HELLO"
String whisper = "HELLO".toLowerCase();   // "hello"
```

### `equals()` and `equalsIgnoreCase()`
Use these to compare Strings — **never use `==`**.

```java
String a = "Hello";
String b = "hello";

a.equals(b)             // false — capital H differs
a.equalsIgnoreCase(b)   // true — ignores case
```

### `substring(start, end)`
Pulls out part of a String. Counting starts at **0**. The end index is **not included**.

```java
String word = "Hello";
String part = word.substring(1, 4);   // "ell"
```

Index reference for `"Hello"`:
```
H  e  l  l  o
0  1  2  3  4
```
`substring(1, 4)` takes characters at positions 1, 2, 3 → `"ell"`

---

## 5.1.5 Immutability — Methods Don't Change the Original

```java
String s = "JAVA";
s.toLowerCase();            // does NOT change s
System.out.println(s);      // still prints "JAVA"
```

To actually use the result, save it:

```java
String s = "JAVA";
s = s.toLowerCase();        // reassign
System.out.println(s);      // prints "java"
```

---

## 5.1.6 Check Your Understanding

1. What is one difference between a primitive (like `int`) and a `String`?
2. What does `+=` do when used with a `String`?
3. If you call `toUpperCase()` on a `String` but don't reassign, does the original change?
4. Which method checks if two Strings are equal while ignoring case?
5. What does `"elephant".substring(2, 5)` return?

---

## 5.1.7 Answer Key

1. Primitives store simple values directly. `String` is an object — it comes with built-in methods and is immutable.
2. It appends the new text to the end of the existing String (and saves the result back to the variable).
3. No. Strings are immutable; the method returns a new String but doesn't modify the original.
4. `equalsIgnoreCase()`
5. `"eph"` — positions 2, 3, 4 of `"elephant"` (e=0, l=1, e=2, p=3, h=4)

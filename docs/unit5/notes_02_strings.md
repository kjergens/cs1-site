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



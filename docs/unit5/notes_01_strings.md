# Chapter 1: Strings

---

## Section 1: Overview

In Java, a `String` is used to store text. It is **not** a simple primitive like `int` or `double` — it is a special type called an **object**, which means it comes with built-in methods you can call on it.

**Key idea: Strings are immutable.** Once a `String` is created, it cannot be changed. Any method that seems to change it actually creates a brand-new `String`. To save the result, you must reassign it.

---

## Section 2: Declaring Strings

```java
String greeting = "Hello World!";
String message = "Welcome to Java";

String empty = "";       // empty string
String nothing;          // declared but not initialized
```

---

## Section 3: Adding to a String

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

## Section 4: Common String Methods

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

### `substring(start)` — single argument

Leave out `end` and `substring` returns everything from `start` to the end of the string.

```java
String s = "Java Programming";
String part = s.substring(5);   // "Programming"
```

### `charAt(index)`

Returns the single character at a given index (0-based).

```java
String word = "Hello";
char c = word.charAt(1);   // 'e'
```

Valid indices run from `0` to `length() - 1`. Calling `charAt()` with an index that's too large (or negative) throws an error.

### `indexOf(str)`

Returns the index where a substring first appears, or `-1` if it isn't found.

```java
String s = "Hello World";
int i = s.indexOf("World");   // 6
int j = s.indexOf("xyz");     // -1 (not found)
```

There's also a `contains(str)` method that just returns `true`/`false` for whether a substring exists — use `indexOf()` instead when you also need to know *where* the match is, not just whether it exists.

### `replace()`, `replaceAll()`, and `replaceFirst()`

All three swap out characters or patterns for something else, but they differ:

| Method | Replaces | Uses regex? |
|---|---|---|
| `replace(oldChar, newChar)` | every occurrence of a character | No |
| `replaceAll(regex, replacement)` | every match of a pattern | Yes |
| `replaceFirst(regex, replacement)` | only the first match of a pattern | Yes |

```java
String s = "banana";
s.replace('a', 'A');        // "bAnAnA" — every 'a' becomes 'A'
s.replaceAll("a", "X");     // "bXnXnX" — same result here, but replaceAll can use pattern syntax
s.replaceFirst("a", "*");   // "b*nana" — only the first 'a' changes
```

For simple single-character swaps, `replace()` and `replaceAll()` produce the same result — the real difference is that `replaceAll`/`replaceFirst` treat their first argument as a *regular expression* pattern, not just literal text, so they can match more complex patterns.

---

## Section 5: Immutability — Methods Don't Change the Original

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

## Unit 5 Chapter 1 Homework

*Reference: [w3schools Java String methods](https://www.w3schools.com/java/java_ref_string.asp)*

### Part A: Definitions (Fill in the Blank)

1. The `length()` method returns the __________ of characters in a String.
2. `substring(beginIndex, endIndex)` returns a __________ of the original string from `beginIndex` up to (but not including) `endIndex`.
3. `charAt(index)` returns the __________ at the specified index (0-based).
4. `indexOf(String str)` returns the __________ index of the first occurrence of `str`, or __________ if not found.
5. `replace(char oldChar, char newChar)` replaces __________ occurrences of `oldChar` with `newChar`.
6. `replaceAll(String regex, String replacement)` uses __________ to match and replace patterns.
7. `equals(Object obj)` checks if two strings have the __________ content and are of the same __________.
8. `equalsIgnoreCase(String anotherString)` compares two strings for equality, ignoring __________ differences.

### Part B: True or False

9. `s.length()` counts spaces and special characters.
10. `"hello".substring(1, 3)` returns `"he"`.
11. `charAt(0)` returns the last character of a string.
12. `indexOf("a")` returns `-1` if `"a"` is not in the string.
13. `replaceAll()` can use regular expressions.
14. `replace()` and `replaceAll()` behave the same for simple character replacement.
15. `equals()` and `==` always mean the same thing for Strings.
16. `equalsIgnoreCase()` returns `true` for `"Java"` and `"JAVA"`.

### Part C: Short Answer

1. What is the difference between `replace()` and `replaceAll()`?
2. Why might `indexOf()` be preferred over `contains()` in some cases?
3. Explain why `"hello".charAt(5)` causes an error.
4. When would you use `substring(2)` instead of `substring(2, 5)`?

### Part D: Code Output Prediction

Predict the output of each line, given:
```java
String s = "Java Programming";
```

1. `s.length()` → ?
2. `s.substring(5)` → ?
3. `s.substring(0, 4)` → ?
4. `s.charAt(7)` → ?
5. `s.indexOf("gram")` → ?
6. `s.indexOf("Python")` → ?
7. `s.replace('a', 'A')` → ?
8. `s.replaceAll("a", "X")` → ?
9. `s.replaceFirst("a", "*")` → ?
10. `s.equals("java programming")` → ?
11. `s.equalsIgnoreCase("JAVA programming")` → ?

---



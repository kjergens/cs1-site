# For Loops

---

## 4.2 Check Your Understanding

1. What is the output of this loop?
```java
for (int i = 1; i <= 5; i++) {
    System.out.print(i + " ");
}
```

2. Rewrite this `while` loop as a `for` loop:
```java
int x = 10;
while (x >= 0) {
    System.out.println(x);
    x -= 2;
}
```

3. How many times does this loop run?
```java
for (int i = 0; i < 7; i++) {
    System.out.println("hello");
}
```

---

### 4.2.1 Answer Key

1. `1 2 3 4 5` (all on one line with spaces)

2.
```java
for (int x = 10; x >= 0; x -= 2) {
    System.out.println(x);
}
```

3. 7 times (`i` goes from 0 to 6 inclusive).

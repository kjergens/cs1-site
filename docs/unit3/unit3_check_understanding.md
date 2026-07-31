# Unit 3: Check Your Understanding

1. What is the output of this code?
```java
int count = 10;
while (count > 7) {
    System.out.println(count);
    count--;
}
```

2. What change would make this an infinite loop? How would you fix it?
```java
int n = 1;
while (n < 100) {
    System.out.println(n);
}
```

3. Write a while loop that prints the even numbers from 2 to 10.

---

### Answer Key

1.
```
10
9
8
```
`count` starts at 10, decrements each iteration. When `count = 7`, `7 > 7` is false and the loop exits.

2. `n` is never incremented — infinite loop. Fix: add `n *= 2;` (or `n++`, etc.) inside the loop body.

3.
```java
int n = 2;
while (n <= 10) {
    System.out.println(n);
    n += 2;
}
```

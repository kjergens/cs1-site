# Chapter 2: Advanced For Loops

---

## Section 1: Stepping by Custom Increments

For loops don't have to change by 1 each time — the update part can add, subtract, or multiply by any amount.

```java
for (int i = 0; i <= 10; i += 2) {
    System.out.println(i);
}
```
Output: `0 2 4 6 8 10`

```java
for (int i = 20; i >= 5; i -= 5) {
    System.out.println(i);
}
```
Output: `20 15 10 5`

**Key points:**
- The update doesn't have to be `++` or `--` — it can be `+= n` or `-= n` for any step size
- Counting down needs a `>=` or `>` condition (not `<`), since `i` decreases each time
- Double check that the step size actually reaches the stopping condition — a step in the wrong direction creates an infinite loop

---

## Section 2: Aggregation

**Aggregation** means combining values from every iteration into a single running total — a running sum or product. This requires a variable declared *before* the loop that gets updated *inside* the loop.

```java
int sum = 0;
for (int i = 1; i <= 5; i++) {
    sum += i;
}
System.out.println(sum);  // 15
```
Trace: `sum` starts at `0`, then becomes `1`, `3`, `6`, `10`, `15` as `i` goes from 1 to 5.

```java
int product = 1;
for (int i = 1; i <= 4; i++) {
    product *= i;
}
System.out.println(product);  // 24
```

**Key points:**
- The aggregator variable (`sum`, `product`, etc.) must be declared *outside* the loop, or its value resets every iteration
- Use `+=` for running sums, `*=` for running products
- A product aggregator should start at `1`, not `0` — multiplying by `0` zeroes out the whole result

---

## Section 3: Nested Loops

A loop inside another loop is a **nested loop**. The inner loop runs to completion for every single iteration of the outer loop.

```java
for (int row = 1; row <= 3; row++) {
    for (int col = 1; col <= 4; col++) {
        System.out.print("* ");
    }
    System.out.println();
}
```
Output:
```
* * * *
* * * *
* * * *
```

Trace: the outer loop runs 3 times (`row = 1, 2, 3`). Each time, the inner loop runs completely (`col = 1` through `4`) before the outer loop advances.

**Key points:**
- The inner loop's variable (e.g. `col`) resets and runs fully each time the outer loop advances
- An empty `System.out.println();` just moves to a new line — useful for finishing one row before starting the next
- Making the inner loop's limit depend on the outer loop's variable (e.g. `j <= row`) creates growing or shrinking patterns, like a triangle

---

## Unit 4 Chapter 2 Homework

### Part 1: Predict the Output — Loop Patterns

Write exactly what each loop prints, one value per line.

1.
```java
for (int i = 5; i >= 1; i--) {
    System.out.println(i);
}
```
2.
```java
for (int i = 0; i <= 10; i += 2) {
    System.out.println(i);
}
```
3.
```java
for (int i = 1; i <= 9; i += 2) {
    System.out.println(i);
}
```
4.
```java
for (int i = 20; i >= 5; i -= 5) {
    System.out.println(i);
}
```
5. How many times does this loop body execute?
```java
for (int i = 100; i >= 1; i--) {
    System.out.println(i);
}
```

### Part 2: Write the Loop Header

Fill in the for loop header so the loop produces the described output. The loop body is `System.out.println(i);`.

6. Prints: `10 9 8 7 6 5 4 3 2 1`
```java
for (_____________ ; _____________ ; _____________) {
    System.out.println(i);
}
```
7. Prints: `0 3 6 9 12 15`
```java
for (_____________ ; _____________ ; _____________) {
    System.out.println(i);
}
```
8. Prints: `50 45 40 35 30 25`
```java
for (_____________ ; _____________ ; _____________) {
    System.out.println(i);
}
```

### Part 3: Aggregation

9. Trace through this code. What is the final value of `sum`?
```java
int sum = 0;
for (int i = 1; i <= 5; i++) {
    sum += i;
}
System.out.println(sum);
```
10. What does this code print?
```java
int product = 1;
for (int i = 1; i <= 4; i++) {
    product *= i;
}
System.out.println(product);
```
11. Write a for loop that adds up all even numbers from 2 to 20 (inclusive) and prints the total. (Hint: you can either step by 2, or check inside the loop with `%`.)
12. Write a for loop that counts how many numbers from 1 to 50 are divisible by 3, and prints that count.

### Part 4: Nested Loops

13. What does this code print? Draw it out carefully — the inner loop finishes completely before the outer loop advances.
```java
for (int row = 1; row <= 3; row++) {
    for (int col = 1; col <= 4; col++) {
        System.out.print("* ");
    }
    System.out.println();
}
```
14. What does this code print?
```java
for (int i = 1; i <= 4; i++) {
    for (int j = 1; j <= i; j++) {
        System.out.print("# ");
    }
    System.out.println();
}
```
15. Write nested loops that print this pattern exactly:
```
1
1 2
1 2 3
1 2 3 4
1 2 3 4 5
```

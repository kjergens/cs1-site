# For Loops

---

## Section 1: For Loop vs. While Loop

A `for` loop is another way to repeat code while a condition is true — just like a `while` loop. The difference is that a `for` loop keeps the **initialization**, **condition**, and **update** all in one line. In a `while` loop, those pieces are spread across separate lines.

**Use a `for` loop** when you know how many times the loop will run.  
**Use a `while` loop** when you're not sure how many iterations you'll need.

**The same loop, two ways:**
```java
// While loop
int i = 0;
while (i < 5) {
    System.out.println(i);
    i++;
}

// For loop — same behavior, more compact
for (int i = 0; i < 5; i++) {
    System.out.println(i);
}
```

---

## Section 2: Parts of a For Loop

```java
for (initialization; condition; update) {
    // loop body
}
```

| Part | Purpose |
|---|---|
| **Initialization** | Sets the starting value of the loop variable. Runs once before the loop begins. |
| **Condition** | Checked before each iteration. If `true`, loop continues; if `false`, loop exits. |
| **Update** | Runs after each iteration — usually increments or decrements the loop variable. |
| **Loop body** | The code inside the curly braces that runs each iteration. |

---

## Section 3: Code Examples

### Count from 0 to 4
```java
for (int i = 0; i < 5; i++) {
    System.out.println(i);
}
```
Output: `0 1 2 3 4` (one per line)

### Count from 0 to 5 (inclusive)
```java
for (int i = 0; i <= 5; i++) {
    System.out.println(i);
}
```
Output: `0 1 2 3 4 5` — note the `<=` instead of `<`.

### Count down
```java
for (int i = 3; i > 0; i--) {
    System.out.println(i);
}
```
Output: `3 2 1`

---

## Section 4: Why Curly Braces Matter

**With curly braces** — both statements are inside the loop:
```java
for (int i = 0; i < 3; i++) {
    System.out.println(i);
    System.out.println("~~~");
}
```
Output:
```
0
~~~
1
~~~
2
~~~
```

**Without curly braces** — only the first statement is inside the loop:
```java
for (int i = 0; i < 3; i++)
    System.out.println(i);
System.out.println("---");
```
Output:
```
0
1
2
---
```

Always use curly braces. Omitting them is a common source of bugs.

---

## Section 5: Key Vocabulary

| Term | Definition |
|---|---|
| **Increment** | Add to a variable, usually by 1 (`i++` or `i += 1`) |
| **Decrement** | Subtract from a variable, usually by 1 (`i--` or `i -= 1`) |
| **Loop body** | The code inside the loop's curly braces |
| **Iteration** | One complete pass through the loop body |
| **Loop variable** | The variable that controls the loop (usually `i`) |

---
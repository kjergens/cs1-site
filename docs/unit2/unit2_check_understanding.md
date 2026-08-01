# Unit 2: Check Your Understanding

1. What is the result of `25 % 4`?
2. What is the result of `7 / 2` if both are declared as `int`?
3. What does `8 != 8` evaluate to?
4. Write a comparison that checks whether `15` is greater than or equal to `20 - 3`. What does it evaluate to?
5. Write a Java program that declares two `int` variables, adds them, and prints the result.
6. Modify the program to use `double` instead and perform division.
7. Write a program that prints your name and age on separate lines.
8. What is the value of `n` after: `int n = 8; n = n / 3; n = n + 1;`?
9. Rewrite `x = x - 5;` using a compound assignment operator.
10. What will this print? `int count = 0; count++; count++; System.out.println(count);`
11. If `int a = 5; int b = a; a = 99;` — does `b` change? Why or why not?
12. What import statement is required to use Scanner?
13. Write the line that creates a Scanner named `input` that reads from the keyboard.
14. True or False: `scan.nextLine()` can read a sentence with spaces.
15. If the user types `42` and you read it with `scan.nextLine()`, what type is stored?
16. Why does `nextLine()` sometimes return an empty string when it follows `nextInt()`?
17. How do you fix the `nextLine()` trap?
18. What method converts the `String` `"999"` to the `int` `999`?

---

### Answer Key

**1.** `5` Explanation: 25 / 4 = 5 **Remainder 5**

**2.** `3` Explanation: 7 / 2 = 3.5, dropping the decimal value = **3**

**3.** `false`

**4.** `15 >= (20 - 3)` **false**

**5.**
```java
int a = 4;
int b = 6;
System.out.println(a + b);
```

**6.**
```java
double a = 4.0;
double b = 6.0;
System.out.println(a / b);
```

**7.**
```java
System.out.println("Your Name");
System.out.println(17);
```

**8.** `n = 3` — `8 / 3` is integer division (`2`, remainder dropped), then `2 + 1 = 3`

**9.** `x -= 5;`

**10.** `3`

**11.** No, `b` does not change — `int b = a;` copies `a`'s value (`5`) into `b` at that moment. Changing `a` afterward doesn't affect `b`, since they're separate variables.

**12.**  `import java.util.Scanner;`
**13.** `Scanner input = new Scanner(System.in);`
**14.** True
**15.** The `String` `"42"` — not the number
**16.** `nextInt()` leaves a newline in the buffer; `nextLine()` reads it immediately and returns `""`
**17.** Add `scan.nextLine();` after `nextInt()` (or `nextDouble()`) to consume the leftover newline
**18.** `Integer.parseInt("999")`


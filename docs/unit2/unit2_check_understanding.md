# Unit 2: Check Your Understanding

!!! information

	1. What is the result of `25 % 4`?
	2. What is the result of `7 / 2` if both are declared as `int`?
	3. What does `8 != 8` evaluate to?
	4. Write a comparison that checks whether `15` is greater than or equal to `20 - 3`. What does it evaluate to?
	5. Write a Java program that declares two `int` variables, adds them, and prints the result.
	6. Modify the program to use `double` instead and perform division.
	7. Write a program that prints your name and age on separate lines.
	8. What is wrong with the following code?
	```java
	int x = 5;
	x + 3;
	```
	9. What is printed by the following code?
	```java
	System.out.println(2 + 3 + " days");
	System.out.println("Total: " + 2 + 3);
	```
	10. What is the value of `n` after: `int n = 8; n = n / 3; n = n + 1;`?
	11. Rewrite `x = x - 5;` using a compound assignment operator.
	12. What will this print? `int count = 0; count++; count++; System.out.println(count);`
	13. If `int a = 5; int b = a; a = 99;` — does `b` change? Why or why not?
	14. What import statement is required to use Scanner?
	15. Write the line that creates a Scanner named `input` that reads from the keyboard.
	16. What method converts the `String` `"999"` to the `int` `999`?

	---

	### Answer Key

	**1.** `1` Explanation: 25 ÷ 4 = 6 remainder **1** — `%` returns the remainder, not the quotient

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

	**8.** Line 2, `x + 3;`, isn't a valid Java statement on its own — a bare expression like this doesn't compile. Only assignments, `++`/`--`, method calls, and object creation can stand alone as statements.

	**9.**
	```
	5 days
	Total: 23
	```
	Line 1: `2 + 3` is evaluated as arithmetic first (both are numbers), giving `5`, then concatenated with `" days"`. Line 2: once the `String` `"Total: "` appears, everything after becomes concatenation, left to right — `"Total: " + 2` → `"Total: 2"`, then `+ 3` → `"Total: 23"`.

	**10.** `n = 3` — `8 / 3` is integer division (`2`, remainder dropped), then `2 + 1 = 3`

	**11.** `x -= 5;`

	**12.** `2` — `count` starts at 0, then two `count++;` statements bring it to 2

	**13.** No, `b` does not change — `int b = a;` copies `a`'s value (`5`) into `b` at that moment. Changing `a` afterward doesn't affect `b`, since they're separate variables.

	**14.**  `import java.util.Scanner;`
	**15.** `Scanner input = new Scanner(System.in);`
	**16.** `Integer.parseInt("999")`

# Unit 4: Check Your Understanding

!!! information

	1. What is the output of this loop?
	```java
	for (int i = 1; i <= 5; i++) {
	    System.out.print(i + " ");
	}
	```

	2. How many times does this loop run?
	```java
	for (int i = 0; i < 7; i++) {
	    System.out.println("hello");
	}
	```

	3. Rewrite this `while` loop as a `for` loop:
	```java
	int x = 10;
	while (x >= 0) {
	    System.out.println(x);
	    x -= 2;
	}
	```

	4. What is the final value of `total`?
	```java
	int total = 0;
	for (int i = 1; i <= 4; i++) {
	    total += i * 2;
	}
	```

	5. What does this nested loop print?
	```java
	for (int i = 1; i <= 2; i++) {
	    for (int j = 1; j <= 3; j++) {
	        System.out.print(i + "" + j + " ");
	    }
	}
	```

	---

	### Answer Key

	1. `1 2 3 4 5` (all on one line with spaces)

	2. 7 times (`i` goes from 0 to 6 inclusive).

	3. 
	```java
	for (int x = 10; x >= 0; x -= 2) {
	    System.out.println(x);
	}
	```

	4. `20` — `total` becomes `2, 6, 12, 20` as `i` goes from 1 to 4 (`i * 2` is `2, 4, 6, 8`).

	5. `11 12 13 21 22 23 ` — the outer loop runs twice (`i = 1, 2`); for each, the inner loop runs 3 times (`j = 1, 2, 3`).


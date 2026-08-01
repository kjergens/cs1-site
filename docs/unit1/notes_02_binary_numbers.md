# Binary Numbers

---

## Section 1: Binary — Everything Is a Binary Number

Numbers themselves are stored in **binary** (base 2) — using only the digits `0` and `1`.

### Review: Base 10 (Decimal)

In the number system you use every day, each position represents a power of 10:

```
  4    2    7
  ↑    ↑    ↑
 10²  10¹  10⁰
(100) (10)  (1)

Value: 4×100 + 2×10 + 7×1 = 427
```

### Base 2 (Binary)

Binary works the same way, but each position represents a power of 2:

```
  1    0    1    1
  ↑    ↑    ↑    ↑
  2³   2²   2¹   2⁰
 (8)  (4)  (2)  (1)

Value: 1×8 + 0×4 + 1×2 + 1×1 = 11
```

Each `0` or `1` is called a **bit**. 8 bits = 1 **byte**.

---

## Section 2: Converting Binary → Decimal

Write out the positional values (powers of 2), multiply each bit, then add.

**Example: `1101`**

| Bit | Position value | Contribution |
|---|---|---|
| 1 | 8 | 8 |
| 1 | 4 | 4 |
| 0 | 2 | 0 |
| 1 | 1 | 1 |

**Total: 8 + 4 + 0 + 1 = 13**

**Common powers of 2 to memorize:**

| 2⁰ | 2¹ | 2² | 2³ | 2⁴ | 2⁵ | 2⁶ | 2⁷ |
|---|---|---|---|---|---|---|---|
| 1 | 2 | 4 | 8 | 16 | 32 | 64 | 128 |

---

## Section 3: Converting Decimal → Binary

Repeatedly divide by 2 and record the remainders. Read remainders bottom to top.

**Example: 13 → binary**

```
13 ÷ 2 = 6  remainder 1  ← last bit
 6 ÷ 2 = 3  remainder 0
 3 ÷ 2 = 1  remainder 1
 1 ÷ 2 = 0  remainder 1  ← first bit

Read bottom to top: 1101
```

Check: `1101` = 8 + 4 + 0 + 1 = 13 ✓

---

## Unit 1 Chapter 2 Homework

*Assigned Class 1 · Due Class 2*

**Instructions:** Show all work. For conversion problems, write out the place values (powers of 2). For addition problems, show the carry row above each column.

### Part 1: Converting Binary to Decimal

1. Convert the binary number `110101` to decimal. Show each bit's place value.
2. What is the highest decimal value that can be represented with a 6-bit binary number? Explain why in one sentence.
3. In the binary number `10110`, list the decimal value represented by each bit position, from right (least significant) to left (most significant).

### Part 2: Converting Decimal to Binary

4. Convert the decimal number `47` to binary. Show your work (repeated division or place-value method).
5. Convert the decimal number `29` to binary. Then count how many 1s appear in your answer.

### Part 3: Binary Addition

6. Add the binary numbers `1011` and `1101`. Show the carry row.

```
  carry:
   1011
+  1101
------
```

7. Add the binary numbers `11101` and `11011`. Show the carry row.

```
  carry:
  11101
+ 11011
-------
```

8. **Challenge:** Convert `10011` and `10101` from binary to decimal. Add them in decimal. Then convert the decimal sum back to binary.

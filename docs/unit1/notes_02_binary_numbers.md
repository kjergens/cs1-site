# Chapter 2: Binary Numbers

---

## Section 1: Binary — Everything Is a Binary Number

Numbers themselves are stored in **binary** (base 2) — using only the digits `0` and `1`.

### Review: Base 10 (Decimal)

In the number system you use every day, each position represents a power of 10:

```
  4    2    7
  ↑    ↑    ↑
 10²  10¹  10⁰
(100) (10) (1)

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

## Section 2: Converting to and from Binary

### Convert from binary

Write out the positional values (powers of 2), multiply each bit, then add.

**Example: `1011`**

```
  1    0    1    1
  ↑    ↑    ↑    ↑
  2³   2²   2¹   2⁰
 (8)  (4)  (2)  (1)

Value: 1×8 + 0×4 + 1×2 + 1×1 = 11
```


**Common powers of 2 to memorize:**

 128   64   32   16    8    4    2    1
  2⁷   2⁶   2⁵   2⁴   2³   2²   2¹   2⁰


---

### Convert to binary

#### Division method

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

#### Places method

Set up your powers of two like this:


```
  _    _    _    _    _
 16    8    4    2    1
  2⁴   2³   2²   2¹   2⁰

```

Start with the left (most significant) digit, and fill in a 1 or 0. For example for the number `13`

1. The left-most digit is 16. 16 is bigger than 13 so put 0:

```
  0    _    _    _    _
 16    8    4    2    1
  2⁴   2³   2²   2¹   2⁰

```

2. The next digit is 8. 8 fits into to 13 so put a 1:
```
  0    1    _    _    _
 16    8    4    2    1
  2⁴   2³   2²   2¹   2⁰
```

3. The 8 is accounted for so (13 - 8) = 5 remains. The next spot is 4. 4 fits into 5 so put 1 there:
```
  0    1    1    _    _
 16    8    4    2    1
  2⁴   2³   2²   2¹   2⁰
```

4. 4 is accounted for so (5 - 4) = 1 remains. The next spot is 2. 2 is bigger than 1 so put a 0 there:
```
  0    1    1    0    _
 16    8    4    2    1
  2⁴   2³   2²   2¹   2⁰
```

5. 1 still remains. The next spot is 1. 1 fits into 1 so put a 1 there:
```
  0    1    1    0    1
 16    8    4    2    1
  2⁴   2³   2²   2¹   2⁰
```

1 is accounteed for so 1 - 1 = 0, 0 remains so we're done! `13` converted to binary is `01101`.

---

## Homework

!!! attention
    ### Unit 1 Chapter 2 Homework

    *Assigned Class 1 · Due Class 2*

    **Instructions:** Show all work. For conversion problems, write out the place values (powers of 2). For addition problems, show the carry row above each column.

    #### Part A: Converting Binary to Decimal

    1. Convert the binary number `110101` to decimal. Show each bit's place value.
    2. What is the highest decimal value that can be represented with a 6-bit binary number? Explain why in one sentence.
    3. In the binary number `10110`, list the decimal value represented by each bit position, from right (least significant) to left (most significant).

    #### Part B: Converting Decimal to Binary

    4. Convert the decimal number `47` to binary. Show your work (repeated division or place-value method).
    5. Convert the decimal number `29` to binary. Then count how many 1s appear in your answer.

    #### Part C: Binary Addition

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

    8. **Extra Challenge: (ungraded)** Convert `10011` and `10101` from binary to decimal. Add them in decimal. Then convert the decimal sum back to binary.

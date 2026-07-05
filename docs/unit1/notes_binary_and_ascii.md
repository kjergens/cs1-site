# Binary and ASCII

---

## 1. ASCII — Letters Are Numbers

Computers only understand numbers. So how do they store text?

**ASCII** (American Standard Code for Information Interchange) is a system that assigns a number to every character: letters, digits, punctuation, and special characters.

| Character | ASCII Value |
|---|---|
| `A` | 65 |
| `B` | 66 |
| `Z` | 90 |
| `a` | 97 |
| `z` | 122 |
| `0` | 48 |
| `9` | 57 |
| space | 32 |

When your program stores the String `"Hello"`, the computer stores the numbers `72 101 108 108 111`. Text is always numbers underneath.

---

## 2. Binary — Everything Is a Binary Number

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

## 3. Converting Binary → Decimal

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

## 4. Converting Decimal → Binary

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

## 5. Binary Addition

Binary addition uses the same rules as decimal, just with 2 digits:

| + | 0 | 1 |
|---|---|---|
| **0** | 0 | 1 |
| **1** | 1 | 10 (write 0, carry 1) |

**Example: `1010 + 0111`**

```
  1 0 1 0
+ 0 1 1 1
---------
  carry: 1 1 1
  result: 1 0 0 0 1 → 17
```

Check: 10 + 7 = 17 ✓

Key rule: `1 + 1 = 10` in binary (write 0, carry 1). `1 + 1 + 1 = 11` (write 1, carry 1).

---

## Check Your Understanding

**1.** What is the decimal value of binary `10110`?

**2.** Convert 25 to binary.

**3.** Add in binary: `0110 + 0101`

**4.** What ASCII value represents the letter `'A'`? What about `'a'`?

**5.** Why does `'a'` have a higher ASCII value than `'A'`?

---

## Answer Key

**1.** `10110`: 16 + 0 + 4 + 2 + 0 = **22**

**2.** 25 → binary:
```
25 ÷ 2 = 12  r 1
12 ÷ 2 =  6  r 0
 6 ÷ 2 =  3  r 0
 3 ÷ 2 =  1  r 1
 1 ÷ 2 =  0  r 1
```
Read bottom to top: **11001** (check: 16+8+0+0+1 = 25 ✓)

**3.** `0110 + 0101`:
```
  0 1 1 0
+ 0 1 0 1
---------
  1 0 1 1  → 8+2+1 = 11
```
Check: 6 + 5 = 11 ✓

**4.** `'A'` = 65, `'a'` = 97

**5.** Lowercase letters come after uppercase in the ASCII table — they were assigned higher numbers when the standard was designed.

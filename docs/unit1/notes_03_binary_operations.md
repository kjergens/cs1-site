# Chapter 3: Binary Arithmetic

---

## Section 1: Binary Addition

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

## Section 2: Binary Multiplication

Binary multiplication works like decimal long multiplication — multiply by each digit and shift, then add the partial products. Since binary digits are only `0` or `1`, each partial product is either all zeros (if that digit is 0) or a copy of the original number shifted left (if that digit is 1).

**Example: `110 × 11`**

```
      1 1 0     (6)
    ×     1 1   (3)
    -----------
      1 1 0     ← 110 × 1 (rightmost bit of 11)
    1 1 0       ← 110 × 1, shifted one place left (next bit of 11)
    -----------
    1 0 0 1 0   → 18
```

Add the partial products using binary addition (`110 + 1100 = 10010`).

Check: 6 × 3 = 18 ✓

Key rule: multiplying by `0` gives a row of all zeros; multiplying by `1` copies the number, shifted left to line up under that bit. Then add all the partial product rows together.

---

## Homework

!!! attention
    ### HW2: Unit 1 Chapter 3: Binary Arithmetic

    *Assigned Class 2 · Due Class 3*

    #### Part A: Binary Addition

    Add the following binary numbers:

    1. `1011 + 0110`
    2. `11001 + 10110`
    3. `1111 + 111`
    4. `101010 + 11011`
    5. `1001110 + 0110011`

    #### Part B: Binary Multiplication

    Multiply the following binary numbers:

    6. `101 × 11`
    7. `1101 × 101`
    8. `111 × 10`
    9. `1010 × 110`
    10. `10011 × 101`

    **Bonus (challenge):** `11101 × 1011`

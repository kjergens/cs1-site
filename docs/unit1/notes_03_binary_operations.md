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

## Section 2: Binary Subtraction

Binary subtraction works the same way decimal subtraction does: if a column doesn't have enough to subtract, **borrow a 1** from the next column over. That borrowed 1 is worth `10` (two) once it lands in the column that needed it, since each place value is double the one before it.

**Example: `1010 − 0100`**

```
  1 0 1 0
- 0 1 0 0
---------
  0 1 1 0
```

Check: 10 − 4 = 6 ✓

Key rule: when the top digit in a column is smaller than the bottom digit (`0 − 1`), borrow a 1 from the next column to the left — it becomes a `10` in the column that needed it, same idea as borrowing in decimal subtraction.

### The Basic Rule of Binary Borrowing
When you must calculate 0 - 1, you cannot do it without help. You must borrow from the next column to the left: 

- The column you borrow from drops its value by 1 (changing a 1 to a 0).
   
- The current column receives a value of 2 (written as 10 in binary).
   
- You subtract: 10 (binary) - 1 (binary) = 1 (binary). 


### Borrowing Across Multiple Zeros
If the immediate column to the left is a 0, you cannot borrow from it directly. You must keep moving left until you find a 1: 

- The 1 you finally find turns into a 0.
  
- Any intermediate 0s that you skipped turn into 1s.
  
- The column that actually needed the borrow becomes 10 (which is 2 in decimal). 

---

## Section 3: Binary Multiplication

Binary multiplication works like decimal long multiplication — multiply by each digit and shift, then add the partial products. Since binary digits are only `0` or `1`, each partial product is either all zeros (if that digit is 0) or a copy of the original number shifted left (if that digit is 1).

**Example: `110 × 11`**

```
      0 1 1 0   (6)
    ×   0 1 1   (3)
   -----------
      0 1 1 0     ← 1 x 0110 
    0 1 1 0       ← 1 x 0110, shifted one place left 
  0 0 0 0         ← 0 × 0110, shifted another place left 
  -------------
 0 0 1 0 0 1 0    → 18
```

Check: 6 × 3 = 18 ✓

Key rule: multiplying by `0` gives a row of all zeros; multiplying by `1` copies the number, shifted left to line up under that bit. Then add all the partial product rows together.

!!! information "Fun fact: multiplying by 2 is just a shift"
    To multiply a binary number by 2, shift every digit one place to the left. Each digit's place value doubles when it moves one spot left, so if every digit is worth twice as much, the whole number is twice as much too — no actual multiplication required.

---

## Homework

!!! attention
    ### HW 2: Unit 1 Chapter 3: Binary Arithmetic

    *Assigned Class 3 · Due Class 4*

    #### Part A: Binary Addition

    Add the following binary numbers:

    1. `1011 + 0110`
    2. `11001 + 10110`
    3. `1111 + 111`
    4. `101010 + 11011`
    5. `1001110 + 0110011`

    #### Part B: Binary Subtraction

    Subtract the following binary numbers:

    6. `1101 − 0110`
    7. `1010000 − 0110111`

    #### Part C: Binary Multiplication

    Multiply the following binary numbers:

    8. `101 × 11`
    9. `1101 × 101`
    10. `111 × 10`
    11. `1010 × 110`
    12. `10011 × 101`

    **Bonus Challenge (ungraded):** `11101 × 1011`

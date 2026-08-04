# Unit 1: Check Your Understanding

!!! information

    1. What is the decimal value of binary `10110`?
    2. Convert 25 to binary.
    3. Add in binary: `0110 + 0101`
    4. What ASCII value represents the letter `'A'`? What about `'a'`?
    5. Why does `'a'` have a higher ASCII value than `'A'`?
    6. Multiply in binary: `110 × 101`

    ---

    ### Answer Key

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

    **6.** `110 × 101`:
    ```
        1 1 0     (6)
      ×   1 0 1   (5)
      -----------
        1 1 0     ← 110 × 1 (bit 0)
      0 0 0       ← 110 × 0 (bit 1)
    1 1 0         ← 110 × 1 (bit 2)
      -----------
    1 1 1 1 0     → 30
    ```
    Check: 6 × 5 = 30 ✓

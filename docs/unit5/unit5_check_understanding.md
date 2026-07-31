# Unit 5: Check Your Understanding

1. What is one difference between a primitive (like `int`) and a `String`?
2. What does `+=` do when used with a `String`?
3. If you call `toUpperCase()` on a `String` but don't reassign, does the original change?
4. Which method checks if two Strings are equal while ignoring case?
5. What does `"elephant".substring(2, 5)` return?
6. What does `Math.max(12, 7)` return?
7. What does `Math.min(3.5, 8.2)` return?
8. What does `Math.sqrt(49)` return?
9. What does `Math.abs(-15)` return?
10. What does `Math.pow(3, 4)` return?
11. What does `Math.ceil(2.001)` return?
12. What is the range of values returned by `Math.random()`?

---

### Answer Key

1. Primitives store simple values directly. `String` is an object — it comes with built-in methods and is immutable.
2. It appends the new text to the end of the existing String (and saves the result back to the variable).
3. No. Strings are immutable; the method returns a new String but doesn't modify the original.
4. `equalsIgnoreCase()`
5. `"eph"` — positions 2, 3, 4 of `"elephant"` (e=0, l=1, e=2, p=3, h=4)
6. `12`
7. `3.5`
8. `7.0`
9. `15`
10. `81.0`
11. `3.0`
12. `0.0` up to but not including `1.0`
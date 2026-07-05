# Project 2: Word Guessing Adventure

**CS1 — Ms. Jergens**

---

## Summary

**Learning Goal:** Build a text-based word-guessing game inspired by Wordle. You'll practice variables, `if` statements, `while` loops, `Scanner` for input, and String methods to create a complete interactive program.

**Game Objective:** The player gets up to 6 guesses to find all the letters in a secret 4-letter word. If they succeed, they advance to Level 2: up to 3 tries to guess the full word.

---

## String Methods You'll Need

| Method | What it does | Example |
|---|---|---|
| `.length()` | Number of characters | `"cave".length()` → `4` |
| `.contains()` | Checks if a substring is inside | `"cave".contains("a")` → `true` |
| `.equals()` | Compares two Strings exactly | `"cave".equals("Cave")` → `false` |

---

## Example Game Session

```
Welcome to Word Guessing Adventure!

============== LEVEL 1: Guess the letters ==============
The secret word has 4 letters. All letters are unique. You have 6 guesses.

Guess a letter: a
Correct! Letters: a

Guess a letter: b
Incorrect! Letters: a

Guess a letter: c
Correct! Letters: ac

Guess a letter: e
Correct! Letters: ace

Guess a letter: v
Correct! Letters: acev

Congratulations! You guessed all the letters.

============== LEVEL 2: Guess the word ==============
Guess the secret word. You have 3 guesses.
Letters: acev

Guess the word: evca
Incorrect! Letters: acev

Guess the word: cave
Correct!

Congratulations! You guessed the secret word.
```

---

## Coding Tips: Level 1

Create variables to track:
- The secret word
- The correctly guessed letters (as a String, starting `""`)
- The number of guesses used
- The maximum number of guesses (6)

Use a `Scanner` and a loop where each iteration:

1. Prompts the user for a letter and reads it
2. Converts input to lowercase for consistency
3. Checks: Is the letter in the secret word? Has it already been guessed?
4. If new and correct: add it to your correct-guesses String
5. If not: inform the user (incorrect guesses still count toward the limit)

The loop should end when:
- All letters are found: `correctGuesses.length() == secretWord.length()`, **or**
- The player reaches the 6-guess limit

**Input validation:** If the player enters more than one character or a non-letter, reprompt them.

---

## Coding Tips: Level 2

If the player completes Level 1, move to the full-word guess. Show them their discovered letters and give up to 3 attempts.

Each attempt:
- Prompt for a full-word guess
- Compare it to the secret word using `.equals()`
- If correct: win message
- If incorrect: reduce remaining attempts and give feedback

---

## Required Import

```java
import java.util.Scanner;
```

---

## Level-Up (Optional)

**Small:** Display incorrect guesses so the user doesn't repeat them; auto-win Level 2 if letters were guessed in order.

**Medium:** Add a Level 3 with a harder word; support words with repeated letters.

**Advanced:** Use an API to get a random word; implement full Wordle rules (correct position, wrong position, not in word).

---

## Grading Rubric

| Category | Points |
|---|---|
| Program compiles and runs without errors | 10 |
| Level 1: correct letter-guessing logic, tracks guesses, ends appropriately | 30 |
| Level 2: correct full-word guessing with up to 3 attempts | 20 |
| Input handling & user experience (clear prompts, handles invalid/repeated guesses) | 10 |
| Code quality & style (readable, meaningful variable names, proper formatting) | 10 |
| Working style / process / productivity (consistent progress, ability to explain code) | 20 |
| **Total** | **100** |

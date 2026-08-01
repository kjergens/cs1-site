# Introduction to Programming with Scratch

---

## Section 1: What Is Scratch?

Scratch is a **block-based visual programming language**. Instead of typing code, you drag and snap together colored blocks that represent instructions. The result is a program — the same fundamental thing you'll build in Java.

You've used Scratch in middle school. In this unit, we're using it deliberately: every concept you see in Scratch has a direct equivalent in Java. The goal is not to become a Scratch expert — it's to see the structure of programming before we add Java's syntax on top.

---

## Section 2: Core Programming Concepts in Scratch (and in Java)

### 1. Sequence

Programs run **top to bottom**, one instruction at a time, in order.

In Scratch, blocks in a script execute from the top block down. If you want something to happen first, it goes on top.

In Java, statements inside `main` execute in order, line by line.

---

### 2. Variables

A **variable** is a named container for a value that can change.

In Scratch: use **Make a Variable**, give it a name, and use **set [ ] to** and **change [ ] by** blocks.

In Java:
```java
int score = 0;
score = score + 1;
```

Same idea — a name, a value, the ability to update it.

---

### 3. Conditionals

A **conditional** runs code only if a condition is true.

In Scratch: `if < > then` and `if < > then / else` blocks.

In Java:
```java
if (score > 10) {
    System.out.println("You win!");
} else {
    System.out.println("Keep going.");
}
```

The diamond-shaped condition slots in Scratch correspond to the `( )` in Java's `if` statement.

---

### 4. Loops

A **loop** repeats code multiple times without copy-pasting.

| Scratch block | Java equivalent |
|---|---|
| `forever` | `while (true)` |
| `repeat (10)` | `for (int i = 0; i < 10; i++)` |
| `repeat until < >` | `while (!condition)` |

The idea is the same: a chunk of code that runs again and again, either a fixed number of times or until a condition is met.

---

### 5. Events

In Scratch, scripts start when something happens — "when green flag clicked", "when key pressed".

In Java, the equivalent is the **main method** — the entry point where your program begins:
```java
public static void main(String[] args) {
    // your program starts here
}
```

---

## Section 3: From Scratch to Java

| Scratch concept | Java equivalent |
|---|---|
| Script (blocks top to bottom) | Statements in `main` |
| Variable block | `int x = 0;` |
| `if < > then` | `if (condition) { }` |
| `repeat (n)` | `for` loop |
| `forever` / `repeat until` | `while` loop |
| When green flag clicked | `public static void main(...)` |
| Say [ ] | `System.out.println(...)` |

Every program you write this year — in Scratch or Java — uses these same building blocks. The language changes; the structure doesn't.

---

## Unit 1 Chapter 4 Homework

*Assigned Class 2 · Due Class 3 · Submission: upload your `.sb3` file to the Schoology assignment*

Scratch is a visual programming language developed by MIT. It lets you build programs by snapping together blocks — no curly braces, semicolons, or typos to worry about. It's a great way to see programming logic in action before we move to Java.

The Scratch interface has three main areas:

- **Block palette** (left): all the blocks you can use, organized by category
- **Scripts area** (middle): where you drag and connect blocks to build programs
- **Stage** (right): where your program runs — the cat (your sprite) lives here

The stage uses a coordinate system where `(0, 0)` is the center. The cat starts there.

Work through the activities below **in order** — each one builds on or modifies the previous. Don't start a new activity in a separate area; change your existing code as instructed.

### Activity 1: Say Hello

Drag a "when green flag clicked" block to the scripts area. Attach a "say [ ] for [ ] seconds" block to it. Make the cat say `Hello, world!` for 2 seconds.

Click the green flag to test it.

**Checkpoint:** What is the "input" to the say block? What is the "side effect" of calling it?

### Activity 2: Ask and Answer

Modify your Activity 1 code:

- Replace the say block with an "ask [ ] and wait" block. Use the prompt: `What's your name?`
- After the ask block, add a "say [ ] for [ ] seconds" block that uses the "join" operator to say `Hello, ` joined with the answer variable.

Click the green flag, type your name, and verify the cat greets you by name.

**Checkpoint:** Where does the answer variable come from? What category is it in?

### Activity 3: Text to Speech

- Click "Add Extension" (bottom-left of the block palette). Find and add the Text to Speech extension.
- Add a "speak [ ]" block after your say block. Pass it the same joined greeting (`Hello, ` + answer).

Now when you run the program, the cat should both display and speak the greeting.

### Activity 4: Sound Loop

Detach the blocks from "when green flag clicked" and move them off to the side (keep them — you may want them later).

Build a new script: when green flag clicked → "play sound [Meow] until done".

Click the green flag. The cat should meow once.

### Activity 5: Repeat

Modify your Activity 4 code: wrap the play sound block inside a "repeat [3]" loop.

Click the green flag. The cat should meow 3 times.

**Checkpoint:** What would happen if you changed the repeat number to 0? To 10?

### Activity 6: Define a Block (Custom Function)

- In the block palette, click "My Blocks" → "Make a Block". Name it `meow`.
- Inside the define `meow` block definition, place a "play sound [Meow] until done" block.
- Back in your main script, replace the play sound block inside the repeat loop with your new `meow` block.

Test it — behavior should be identical to Activity 5, but now using a custom block.

**Checkpoint:** Why is it useful to define a named block even if it only contains one line?

### Activity 7: Add a Parameter

Edit your `meow` block:

- Click "My Blocks" → right-click `meow` → "Edit"
- Add a number input called `n`
- Rename the block to `meow n times`
- Inside the definition, wrap the play sound block in a "repeat [n]" loop

Update your main script to call `meow n times` with a number of your choice. Remove the separate repeat wrapper — the loop is now inside the block.

Test with different values of `n`.

**Checkpoint:** What is `n` called in programming? (Hint: we saw this word in Activity 1.)

### Activity 8: Sensing — Touching

Detach your current script from "when green flag clicked" and set it aside.

Build a new script: a `forever` loop containing "if touching the edge → play sound [Meow] until done".

Run it and slowly drag the sprite toward the edge of the stage. The cat should meow when it touches the boundary.

**Experiment:** what happens if you add a "move [10] steps" block inside the forever loop?

**Checkpoint:** What category is the "touching" block in? What other sensing blocks exist?

### Activity 9: Video Motion

- Click "Add Extension" → add the Video Sensing extension.
- Build a script: when video motion > `30` → play sound [Meow] until done.

Test it by moving in front of your camera. The cat should react to motion.

### Activity 10: Bring It Together (Extension)

Now that you know events, variables, loops, custom blocks, sensing, and sound — combine them. Build a program that does all of the following:

- When the green flag is clicked, ask the user their name and greet them by name (from Activity 2)
- Then use your `meow n times` block to meow a number of times equal to the number of letters in the user's name (hint: look in the Operators category for a block that finds the length of a string)
- Add a costume change each time the cat meows so it looks like the cat is "talking"

This is a challenge — it may take trial and error. That's normal.

**Reflection** (write 2–3 sentences in a comment block in Scratch or in the Schoology text box): What was the hardest part of Activity 10? What concept from today's homework do you think will show up again when we start Java?

**How to submit:** In Scratch, go to File → Save to your computer — this downloads a `.sb3` file. Upload the `.sb3` to the Schoology assignment. (Backup option: if you can't download the file, Share your project in Scratch via File → Share, and paste the project link as a Schoology comment.)

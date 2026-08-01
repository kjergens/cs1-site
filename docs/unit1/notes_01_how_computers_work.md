# How Computers Work

---

## Section 1: Hardware vs. Software

A computer has two sides: **hardware** (the physical parts) and **software** (the instructions that tell hardware what to do).

This course is about software — specifically, writing programs in Java. But it helps to know what's running underneath.

---

## Section 2: Key Hardware Components

| Component | What it does |
|---|---|
| **CPU** (Central Processing Unit) | The "brain" — executes instructions |
| **RAM** (Random Access Memory) | Fast, temporary storage for programs that are running |
| **Storage** (SSD/hard drive) | Permanent storage — files, programs, the OS |
| **Input devices** | Keyboard, mouse, microphone — how data gets in |
| **Output devices** | Monitor, speakers, printer — how results come out |

---

## Section 3: How They Work Together

When you run a program:

1. The program is loaded from **storage** into **RAM**
2. The **CPU** reads instructions from RAM one at a time
3. The CPU executes each instruction (add numbers, compare values, display output)
4. Results go to **output** (screen, file, etc.)

RAM is fast but temporary — everything in it disappears when you shut down. Storage is slow but permanent.

---

## Section 4: Everything Is Data

The most important idea in this unit: **computers only understand numbers.** Everything — text, images, sound, video, programs — is stored as numbers. The rest of the unit explores how.

---

## Section 5: ASCII — Letters Are Numbers

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

## Unit 1 Chapter 1 Homework

*Assigned Class 1 · Due Class 1 in class*

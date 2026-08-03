# Chapter 1: How Computers Work

---

## Hardware vs. Software

A computer has two sides: **hardware** (the physical parts) and **software** (the instructions that tell hardware what to do).

This course is about software — specifically, writing programs in Java. But it helps to know what's running underneath.

---

### Key Hardware Components

| Component | What it does |
|---|---|
| **CPU** (Central Processing Unit) | The "brain" — executes instructions |
| **RAM** (Random Access Memory) | Fast, temporary storage for programs that are running |
| **Storage** (SSD/hard drive) | Permanent storage — files, programs, the OS |
| **Input devices** | Keyboard, mouse, microphone — how data gets in |
| **Output devices** | Monitor, speakers, printer — how results come out |

---

### How They Work Together

When you run a program:

1. The program is loaded from **storage** into **RAM**
2. The **CPU** reads instructions from RAM one at a time
3. The CPU executes each instruction (add numbers, compare values, display output)
4. Results go to **output** (screen, file, etc.)

RAM is fast but temporary — everything in it disappears when you shut down. Storage is slow but permanent.

---

## Everything Is Data

The most important idea in this unit: **computers only understand numbers.** Everything — text, images, sound, video, programs — is stored as numbers. The rest of the unit explores how.

---

### ASCII — Letters Are Numbers

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
!!! attention 
	###Unit 1 Chapter 1 Homework

    *Assigned Class 1 · Due Class 1 in class · Graded as Community Building/Class Engagement — try your best, no points off for incorrect answers*

    #### Part A: Terminology

    Match each description to its component: `CPU`, `RAM`, `Hard Drive/SSD`, `Motherboard`, `Monitor`.

    1. Stores data and programs for quick access during operation
	2. The "brain" of the computer that performs calculations and executes instructions
	3. Displays the output of the computer's processing, like text or images
	4. Long-term storage for files, programs, and the operating system
	5. Connects all components, allowing them to communicate

	#### Part B: True/False (+ short answer)

	Transistors are tiny electronic switches that control the flow of electricity in a computer. They're the foundation of modern computing.

	1. True or False: Transistors can act as switches, turning electrical signals on or off.
	2. True or False: A single modern computer chip can contain billions of transistors.
	3. True or False: Transistors are only used in the CPU and not in other parts of a computer.
	4. True or False: Transistors work by using materials like silicon to control electrical flow.
	5. **Short answer:** If transistors are like light switches, how do you think combining millions of them allows a computer to perform complex tasks like playing a video game?

	#### Part C: Fill in the blanks (+ short answer)

	1. **Timeline:** fill in the blanks using each term once — `1943`, `ENIAC`, `1971`, `Microprocessor`, `1984`, `Apple Macintosh`, `1822`, `Difference Engine`.
	    - ______: Charles Babbage designs the ______, a mechanical calculator considered an early precursor to modern computers.
	    - ______: The ______, one of the first general-purpose electronic computers, is built using vacuum tubes.
	    - ______: Intel introduces the first ______, putting the power of a computer's CPU on a single chip.
	    - ______: The ______ is released, making personal computers user-friendly with a graphical interface.
	2. **Short answer:** The ENIAC weighed over 30 tons and took up an entire room! What allowed computers to become small enough to fit in your pocket?

	#### Part D: Binary

	Computers don't think like humans, but they process information using binary code (0s and 1s). Transistors help create these 0s and 1s by controlling electrical signals.

	Convert the following decimal numbers to binary (hint: divide by 2 repeatedly and note the remainders):

	1. `5` = ______ (binary)
	2. `12` = ______ (binary)
	3. Your age = ______ (binary)


# AI Tutor for AOOP 2026

## Part A: True or False

### AI Tutor Learning Cycle (ATLC) — Suggested Student Prompt:

```

I just learned Tuples, Lists, Aliasing, Mutability, Cloning in today’s lecture.

Act as my AI Tutor.

1. Generate 5 True/False questions, one question at a time, to test my conceptual understanding of today’s topic.
2. Focus on concepts and reasoning, not memorization or Python syntax.
3. After I answer, do not immediately tell me the correct answer.
4. If my answer or reasoning is incorrect, give me a hint, counterexample, or follow-up question.
5. Let me revise my answer before explaining the concept.
6. Adjust the difficulty based on my responses.
7. After five questions, ask me to identify one question that may be ambiguous, misleading, too easy, or technically questionable.
8. Finish by asking me what misconception I corrected and what I am still unsure about.
```

### AI Tutor Learning Record

```
Topic: Recursion and Dictionaries
Date: 9/16

1. Check My Understanding

Questions completed: 5 / 5

Answers revised after AI hints: 1 / 5


2. My Misconception

Before: I thought...

A recursive function only needed to call itself repeatedly until the
answer appeared.

I did not fully understand why a base case was necessary, or why the
recursive call had to work on a smaller version of the same problem.


Now: I understand...

A recursive function needs at least one base case that can be solved
directly.

The recursive step should reduce the original problem into a simpler
version of the same problem.

Each recursive call should move closer to the base case.

Otherwise, the function may continue calling itself forever and create
infinite recursion.


3. Challenge the AI

One AI-generated question I challenged:

"If a function calls itself, then it is a correct recursive solution."


Why?

[ ] Ambiguous
[X] Oversimplified
[X] Technically questionable
[ ] Too easy
[ ] Other: __________


Brief explanation:

Simply calling itself does not make a recursive function correct.

A recursive solution also needs a valid base case and a recursive step
that reduces the problem toward that base case.

If the input does not become simpler, the recursion may never stop.


4. One-Minute Reflection

One thing I am still unsure about:

I am still practicing how to identify the correct base case and how to
decide what the smaller recursive problem should be.

I also want to become more confident about tracing the different
function calls and understanding which local variables belong to each
recursive call.
```

## Part B: **LeetCode-style** Lecture Code Transfer

AI Tutor Learning Cycle (ATLC) — Suggested Student Prompt:

```
I have just studied the following lecture code from today’s OCW programming lecture.

[LECTURE CODE]

Act as my AI Tutor.

Based on the concepts and programming patterns demonstrated in the lecture code, generate ONE new LeetCode-style programming challenge.

Requirements:

1. Test the same core concept as the lecture code.
2. Do not simply ask me to reproduce or slightly modify the lecture example.
3. Create a new problem that requires me to transfer what I learned.
4. Use only programming concepts that have been covered in the course so far.
5. Provide:
    * Problem statement
    * Input/output specification
    * Constraints
    * 2–3 examples
6. Do NOT provide code, pseudocode, or the solution.

Before I write code:

7. Ask me to explain my proposed algorithm.
8. Ask me to identify which concept from the lecture code I am applying.
9. If my reasoning is incorrect, give me a hint or counterexample instead of the answer.

After I write my code:

10. Test my solution using normal and edge cases.
11. If my code fails, help me identify the problem without rewriting the solution for me.
12. Ask me to revise my solution.

Finally, ask me to explain:

* Why my solution works
* Its time complexity
* What idea from the lecture code I transferred to this new problem
```

### AI Tutor Learning Record — Coding Challenge

```
Name: 程婕茵
Date: 9/16
Topic: Recursion and Dictionaries


1. Today's Challenge

Core concept from today's OCW lecture:

The main concept was recursion.

A recursive solution reduces a problem into a smaller version of the
same problem.

A correct recursive function needs at least one base case and a
recursive step that eventually reaches the base case.

The lecture also introduced dictionaries as another mutable object
type that stores information using keys and values.


AI-generated coding challenge title:

Recursive Word Frequency Counter


2. My Initial Approach - Before AI Help

Before asking AI for hints, briefly describe how you planned to solve
the problem.

My approach:

I planned to go through the list of words and store the count of each
word in a dictionary.

If the word was already in the dictionary, I would increase its value.

If the word was not in the dictionary, I would create a new entry.

At first, I was thinking about using a normal for loop because that was
the most familiar approach.


3. AI Tutor Help

Did you ask the AI Tutor for help?

[ ] No - I solved it independently
[X] Yes - I received one or more hints


The most useful hint/question from AI was:

The AI asked me:

"What is the smallest version of the problem that you can solve
directly?"


It helped me realize that:

When the index reaches the end of the word list, there is nothing left
to process.

That can be used as the base case.

It also helped me see that after processing one word, the remaining
problem is simply to process the next word and everything after it.


4. My Revision

Did you change your approach or code after interacting with AI?

[ ] No
[X] Yes


What did you change, and why?

I changed my approach from an iterative solution to a recursive
solution.

I added an index parameter to keep track of which word should be
processed.

I also added a base case that stops when the index reaches the length of
the list.

For every recursive call, I increase the index by 1.

I made this change so that each recursive call works on a smaller
remaining portion of the input.


5. Verification

My final program:

[X] Passed the provided examples
[X] Passed additional edge cases
[ ] Still has unresolved problems


One edge case I tested:

Input:

words = []

Expected output:

{}

Actual output:

{}

The recursive function immediately reaches the base case because the
starting index is equal to the length of the empty list.


6. One-Minute Reflection

What idea from the OCW lecture did you transfer to this new problem?

I transferred the idea of decrease-and-conquer.

Instead of trying to process the entire list at once, the recursive
function handles one word and then solves the same problem for the
remaining words.

I also used a dictionary to associate each word with its frequency.


One thing I understand better now:

I understand that a recursive solution needs both:

1. a base case
2. a recursive step that moves toward the base case

I also understand how a dictionary can be updated using keys and
values.


One thing I am still unsure about:

I am still unsure about how recursion uses memory when many function
calls are waiting to return.

I also want more practice deciding whether recursion or iteration is
the better choice for a problem.

```

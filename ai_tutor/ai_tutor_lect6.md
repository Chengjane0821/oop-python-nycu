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
Topic: Recursion and Dictionaries
Date: 9/16


1. Programming Challenge

Challenge Title:
Recursive Word Frequency Counter


Problem Summary:

I was given a list of words.

I needed to count how many times each word appeared and return the
result as a dictionary.

However, instead of using a loop to process the list, I had to solve
the problem recursively.

The dictionary should use each word as a key and the number of
occurrences as the corresponding value.


Example:

words = [
    "cat",
    "dog",
    "cat",
    "bird",
    "dog",
    "cat"
]

Expected output:

{
    "cat": 3,
    "dog": 2,
    "bird": 1
}


2. My Proposed Algorithm

I define a recursive helper function that processes one position in the
list at a time.

The function receives:

- the list of words
- the current index
- a dictionary storing the counts

The base case happens when the index reaches the length of the list.

At that point, there are no more words to process, so the dictionary is
returned.

For the recursive step, I get the current word.

If the word already exists as a key in the dictionary, I increase its
count by 1.

Otherwise, I add the word to the dictionary with a count of 1.

Then I recursively call the function using the next index.


3. Lecture Concept I Applied

The main concepts I applied are:

- Recursion
- Base cases
- Recursive steps
- Dictionaries
- Keys and values
- Mutability

The most important recursion idea is that a large problem can be
reduced to a smaller version of the same problem.

In this challenge, processing the whole list becomes:

process the current word

and then

process the remaining words.

The dictionary is useful because each word can be stored as a key and
its frequency can be stored as the value.

Because dictionaries are mutable, the recursive calls can update the
same dictionary object while processing the list.


4. My Solution

def count_words(words):
    counts = {}

    def helper(index):
        if index == len(words):
            return

        word = words[index]

        if word in counts:
            counts[word] += 1
        else:
            counts[word] = 1

        helper(index + 1)

    helper(0)

    return counts


5. Test Cases

Normal Case:

words = [
    "cat",
    "dog",
    "cat",
    "bird",
    "dog",
    "cat"
]

Expected output:

{
    "cat": 3,
    "dog": 2,
    "bird": 1
}


Edge Case 1: Empty List

words = []

Expected output:

{}


Edge Case 2: One Repeated Word

words = [
    "apple",
    "apple",
    "apple",
    "apple"
]

Expected output:

{
    "apple": 4
}


Edge Case 3: All Different Words

words = [
    "red",
    "blue",
    "green"
]

Expected output:

{
    "red": 1,
    "blue": 1,
    "green": 1
}


6. Why My Solution Works

The base case is:

if index == len(words):
    return

This stops the recursion when every word has been processed.

For each recursive call, the index increases by 1.

Therefore, every call moves closer to the base case.

For each word, the dictionary stores the number of times that word has
appeared.

If the key already exists, its value is increased.

If the key does not exist, a new dictionary entry is created.

After processing the current word, the recursive call processes the
next word.

Therefore, every element is processed exactly once.


7. Time and Space Complexity

Let:

n = number of words in the input list

Each word is processed once.

Dictionary lookup and update are treated as O(1) on average.

Therefore, the total time complexity is:

O(n)

The dictionary may contain up to n different words.

Therefore, the dictionary requires:

O(n)

additional space.

The recursive call stack may also contain up to n calls.

Therefore, the recursion uses:

O(n)

stack space.


8. What Idea I Transferred from the Lecture

The main idea I transferred from Lecture 6 is that recursion works by
reducing a problem to a smaller version of the same problem.

A recursive function needs a base case that can be solved directly.

It also needs a recursive step that moves the input closer to that base
case.

I also used a dictionary to store key-value pairs.

In this challenge, each word is a key and its frequency is the value.

I learned that dictionaries are mutable, so their contents can be
updated while the recursive function is running.


9. Reflection

One thing I learned:

I learned that recursion is not only about a function calling itself.

The important part is that each call should solve a smaller version of
the same problem and eventually reach a base case.


One misconception I corrected:

Before, I thought recursion automatically stopped when the answer was
finished.

Now, I understand that the programmer must explicitly define a base
case.

Without a correct base case, recursion may continue indefinitely.


One thing I am still unsure about:

I am still practicing how to trace recursive calls in my head,
especially when several calls are active at the same time.

I also want to better understand when recursion is clearer than using a
loop.

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

# Source: https://python.datalumina.com/basics/python-syntax

## 

[​](https://python.datalumina.com/#what-is-syntax)

What is syntax?

Every programming language has its own rules - its syntax. It’s like grammar in human languages. You can’t just write words in any order and expect people to understand. The same goes for programming. Python’s syntax is known for being clean and readable. But it still has rules you must follow, or your code won’t run.

## 

[​](https://python.datalumina.com/#the-importance-of-syntax)

The importance of syntax

Think about these two sentences:

- “The cat sat on the mat” ✓ (correct English)
- “Cat the on mat sat the” ✗ (same words, wrong order)

Programming is the same:

```
# Correct Python
if age > 18:
    print("Adult")

# Wrong - Python won't understand
age > 18 print("Adult")
```

## 

[​](https://python.datalumina.com/#python’s-unique-feature-indentation)

Python’s unique feature: Indentation

Most languages use `{}` brackets. Python uses indentation (spaces):

```
# Python - clean and readable
if temperature > 30:
    print("It's hot!")
    print("Turn on AC")

# Other languages (like JavaScript)
if (temperature > 30) {
    console.log("It's hot!");
    console.log("Turn on AC");
}
```

### 

[​](https://python.datalumina.com/#indentation-rules)

Indentation rules

```
# CORRECT - consistent 4 spaces
if score > 90:
    print("A grade")
    if score == 100:
        print("Perfect!")

# WRONG - mixing spaces
if score > 90:
  print("A grade")    # 2 spaces
    if score == 100:  # 4 spaces
      print("Perfect!")  # 6 spaces
```

Python won’t run if your indentation is wrong. This is the #1 beginner mistake!

## 

[​](https://python.datalumina.com/#python-style-guide-pep8)

Python style guide (PEP8)

Beyond just syntax rules that make code run, Python has style guidelines that make code readable. These are called PEP8 (Python Enhancement Proposal 8) - the official style guide for Python code. PEP8 covers things like:

- Using 4 spaces for indentation (not tabs)
- Limiting lines to 79 characters
- Naming conventions (like `user_name` instead of `userName`)
- Where to put spaces around operators

Throughout this course, when there are multiple ways to write something, we’ll follow PEP8. This means you don’t have to think about style choices - just follow the standard and your code will be readable by other Python developers.

Following PEP8 isn’t required for code to run, but it makes your code look professional and easier for others to read.

You can read the full PEP8 guide at [https://peps.python.org/pep-0008/](https://peps.python.org/pep-0008/).

## 

[​](https://python.datalumina.com/#that’s-all-for-now)

That’s all for now

Syntax is just how you write Python code - the rules you follow. Right now, remember these basics: Python cares about spelling, order, and especially indentation. As we move through the course, you’ll naturally pick up the specific syntax rules for each concept.

## 

[​](https://python.datalumina.com/#what’s-next)

What’s next?

Now that you understand Python’s rules, let’s see what happens when we break them!

[**Python errors**\\ \\ Understanding when code doesn’t run](https://python.datalumina.com/basics/python-errors)

[Suggest edits](https://github.com/daveebbelaar/python-course/edit/main/basics/python-syntax.mdx)

[Intro to programming](https://python.datalumina.com/basics/intro-to-programming) [Python errors](https://python.datalumina.com/basics/python-errors)

Ctrl+I
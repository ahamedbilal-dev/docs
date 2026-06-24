# Source: https://python.datalumina.com/basics/comments

## 

[​](https://python.datalumina.com/#what-are-comments)

What are comments?

Comments are notes for humans that Python ignores. They’re like sticky notes in your code that explain what’s happening. Why write comments?

- Help others understand your code
- Help future you remember what you did
- Disable code temporarily
- Document complex logic

## 

[​](https://python.datalumina.com/#single-line-comments)

Single-line comments

Use `#` to start a comment:

```
# This is a comment
print("Hello")  # This is also a comment

# You can have multiple lines
# of comments by starting
# each line with a hash

age = 25  # Store user's age
```

## 

[​](https://python.datalumina.com/#multi-line-comments)

Multi-line comments

For longer explanations, use triple quotes:

```
"""
This is a multi-line comment.
It can span several lines.
Great for longer explanations.
"""

def calculate_tip(bill):
    """
    Calculate 20% tip for a restaurant bill.
    Takes the bill amount and returns the tip.
    """
    return bill * 0.20
```

Technically, triple quotes create a string that Python doesn’t use. Real multi-line comments don’t exist in Python, but this works the same way!

## 

[​](https://python.datalumina.com/#when-to-use-comments)

When to use comments

**Good comments explain WHY, not WHAT:**

```
# Good: Explains why
# Using 1.0625 because sales tax in CA is 6.25%
total = subtotal * 1.0625

# Bad: States the obvious
# Multiply subtotal by 1.0625
total = subtotal * 1.0625
```

## 

[​](https://python.datalumina.com/#best-practices)

Best practices

Use descriptive variable names instead of comments when possible. `days_in_week = 7` is clearer than `d = 7 # days`.

## 

[​](https://python.datalumina.com/#temporary-comments)

Temporary comments

Use comments to disable code temporarily:

```
print("Starting process...")
# print("Debug info")  # Uncomment for debugging
new_method()
# old_method()  # Keeping for reference
```

## 

[​](https://python.datalumina.com/#common-mistakes)

Common mistakes

Outdated comments

```
# Bad: Says 15% but does 20%
# Calculate 15% tip
tip = bill * 0.20

# Good: Accurate
# Calculate 20% tip (standard)
tip = bill * 0.20
```
Over-commenting obvious code

```
# Bad: Too obvious
x = 5  # Set x to 5
y = 10  # Set y to 10

# Good: Only explain complex parts
x = 5
y = 10
position = x + y  # Convert to linear index
```

## 

[​](https://python.datalumina.com/#what’s-next)

What’s next?

Now that you know the basics and how to document your code, let’s explore the different types of data Python can work with!

## Data types

Numbers, text, and more

[Suggest edits](https://github.com/daveebbelaar/python-course/edit/main/basics/comments.mdx)

[Variables](https://python.datalumina.com/basics/variables) [Data types](https://python.datalumina.com/data-types)

⌘I
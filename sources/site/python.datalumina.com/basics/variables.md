# Source: https://python.datalumina.com/basics/variables

## 

[​](https://python.datalumina.com/#what-are-variables)

What are variables?

A variable is like a labeled box where you can store information. You give it a name and put a value inside. Later, you can use that name to get the value back. In real life:

- Your name is a “variable” that stores what people call you
- Your age is a “variable” that stores a number
- Your favorite color is a “variable” that stores text

In Python, we create variables to store data our programs need to remember.

## 

[​](https://python.datalumina.com/#creating-your-first-variable)

Creating your first variable

Here’s how to create a variable:

```
name = "Alice"
age = 25
is_student = True
```

Let’s break this down:

- `name` is the variable name
- `=` means “store the value on the right in the variable on the left”
- `"Alice"` is the value we’re storing

## 

[​](https://python.datalumina.com/#naming-rules)

Naming rules

Python has rules for variable names: **Allowed:**

```
user_name = "Dave"      # lowercase with underscores (Python style)
userName = "Dave"       # camelCase (works but not Python style)
age2 = 30              # numbers are OK (not at start)
_private = "secret"    # underscore at start is OK
```

**Not allowed:**

```
2age = 30              # Can't start with number
my-name = "Dave"       # No hyphens (Python thinks it's subtraction)
my name = "Dave"       # No spaces
class = "Python"       # Can't use Python keywords
```

### 

[​](https://python.datalumina.com/#python-naming-convention)

Python naming convention

In Python, we use lowercase letters with underscores between words. This is called “snake\_case” and it’s the standard way to name variables in Python.

```
# Good Python style
first_name = "Alice"
user_age = 25
is_logged_in = True
shopping_cart_total = 49.99

# Avoid camelCase (this is for other languages)
firstName = "Alice"  # Works, but not Python style
userAge = 25
isLoggedIn = True
```

Use descriptive names for your variables! Instead of `x` or `temp`, use names like `user_score` or `file_path`. Your future self (and teammates) will thank you when reading the code later.

## 

[​](https://python.datalumina.com/#changing-variables)

Changing variables

Variables can change (that’s why they’re called variables!):

```
# Start with one value
score = 0
print(score)  # Shows: 0

# Change it
score = 10
print(score)  # Shows: 10

# Change it again
score = score + 5
print(score)  # Shows: 15
```

## 

[​](https://python.datalumina.com/#common-mistakes)

Common mistakes

Forgetting quotes around text

```
# Wrong
name = Alice  # Python looks for a variable called Alice

# Right
name = "Alice"  # This creates text
```
Using undefined variables

```
# Wrong
print(score)  # Error: score doesn't exist yet
score = 10

# Right
score = 10
print(score)  # Now it works
```
Confusing = and ==

```
# = means "store"
age = 25

# == means "compare" (we'll learn this later)
if age == 25:
    print("Quarter century!")
```

## 

[​](https://python.datalumina.com/#what’s-next)

What’s next?

Before we explore data types, let’s learn about comments - a crucial tool for making your code readable.

[**Comments**\\ \\ Document your code clearly](https://python.datalumina.com/basics/comments)

[Suggest edits](https://github.com/daveebbelaar/python-course/edit/main/basics/variables.mdx)

[Code formatting](https://python.datalumina.com/basics/formatting) [Comments](https://python.datalumina.com/basics/comments)

Ctrl+I
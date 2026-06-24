# Source: https://python.datalumina.com/basics/formatting

## 

[​](https://python.datalumina.com/#what-is-code-formatting)

What is code formatting?

Writing clean, consistent code is important. Code formatting means organizing your code so it’s easy to read and follows Python’s style guidelines.

## 

[​](https://python.datalumina.com/#basic-formatting-principles)

Basic formatting principles

Follow these basic rules for readability:

### 

[​](https://python.datalumina.com/#indentation)

Indentation

Use 4 spaces for indentation (not tabs):

```
def greet(name):
    if name:
        print(f"Hello, {name}!")
    else:
        print("Hello!")
```

### 

[​](https://python.datalumina.com/#spacing)

Spacing

Add spaces around operators and after commas:

```
# Good
x = 1 + 2
numbers = [1, 2, 3, 4]

# Bad
x=1+2
numbers=[1,2,3,4]
```

### 

[​](https://python.datalumina.com/#blank-lines)

Blank lines

Use blank lines to separate functions and logical sections:

```
def first_function():
    pass

def second_function():
    pass
```

### 

[​](https://python.datalumina.com/#line-length)

Line length

Keep lines under 80-100 characters. Break long lines for readability:

```
# Good - readable
long_string = (
    "This is a very long string that "
    "spans multiple lines for readability"
)

# Bad - too long
long_string = "This is a very long string that spans multiple lines for readability but keeps going and going"
```

Later in the course, you’ll learn about Ruff - a tool that automatically formats your code. But understanding these basics first helps you write better code naturally.

## 

[​](https://python.datalumina.com/#automatic-formatting-with-ruff)

Automatic formatting with Ruff

Want to format your code automatically? Check out the Ruff guide in the tools section:

## Code quality with Ruff

Automatically format and lint your code

## 

[​](https://python.datalumina.com/#what’s-next)

What’s next?

Now that you understand formatting, let’s learn about variables!

## Variables

Learn how to store and use data in Python

[Suggest edits](https://github.com/daveebbelaar/python-course/edit/main/basics/formatting.mdx)

[Python errors](https://python.datalumina.com/basics/python-errors) [Variables](https://python.datalumina.com/basics/variables)

⌘I
# Source: https://python.datalumina.com/advanced/error-handling

## 

[​](https://python.datalumina.com/#what-is-error-handling)

What is error handling?

Errors happen. Files might not exist, APIs might be down, users might enter invalid data. Error handling lets your program deal with these problems gracefully instead of crashing.

## 

[​](https://python.datalumina.com/#where-do-errors-come-from)

Where do errors come from?

**Errors you make** as a programmer:

- Typos and syntax mistakes (VS Code shows yellow squiggly lines)
- Logic errors like dividing by zero (only show up when code runs)
- Using variables before defining them
- Calling methods that don’t exist

**Errors beyond your control**:

- User enters “abc” when you need a number
- File gets deleted after your program starts
- Internet connection drops during API call
- External service returns unexpected data

You might think “why not just write correct code?” But even perfect code needs error handling because the world is unpredictable. Users do unexpected things, networks fail, and files disappear.

## 

[​](https://python.datalumina.com/#types-of-errors)

Types of errors

**Syntax errors** happen when Python can’t understand your code:

```
# Missing colon
if x > 5  # SyntaxError
    print("Big number")
```

**Runtime errors** happen when your code runs:

```
# Division by zero
result = 10 / 0  # ZeroDivisionError

# Variable doesn't exist
print(score)  # NameError

# Wrong type
"hello" + 5  # TypeError
```

## 

[​](https://python.datalumina.com/#why-handle-errors)

Why handle errors?

Here’s a program that crashes:

```
# This will crash if the file doesn't exist
with open('data.txt', 'r') as f:
    content = f.read()
print("Done!")  # Never reaches here if file missing
```

Here’s a program that handles the error:

```
# This keeps running even if file doesn't exist
try:
    with open('data.txt', 'r') as f:
        content = f.read()
except FileNotFoundError:
    print("Could not find data.txt")
    content = "default data"
print("Done!")  # Always reaches here
```

## Try and except

Basic error handling syntax

## Common errors

Errors you’ll encounter often

[Suggest edits](https://github.com/daveebbelaar/python-course/edit/main/advanced/error-handling/index.mdx)

[Organizing code](https://python.datalumina.com/practical-python/organizing-code) [Try and except](https://python.datalumina.com/advanced/error-handling/try-except)

⌘I
# Source: https://python.datalumina.com/advanced/error-handling/common-errors

## 

[​](https://python.datalumina.com/#errors-you’ll-encounter)

Errors you’ll encounter

Here are the most common Python errors and how to fix them. Understanding these will save you hours of debugging.

## 

[​](https://python.datalumina.com/#filenotfounderror)

FileNotFoundError

Happens when a file doesn’t exist:

```
# This fails if file doesn't exist
with open('missing.txt', 'r') as f:
    content = f.read()
```

**Fix:**

```
import os

# Check first
if os.path.exists('data.txt'):
    with open('data.txt', 'r') as f:
        content = f.read()
else:
    print("File not found")

# Or use try-except
try:
    with open('data.txt', 'r') as f:
        content = f.read()
except FileNotFoundError:
    content = ""  # Default value
```

## 

[​](https://python.datalumina.com/#valueerror)

ValueError

Happens when a value is wrong type or format:

```
# These cause ValueError
int("hello")        # Can't convert to number
int("12.5")         # int() doesn't accept decimals
list.remove("x")    # Item not in list
```

**Fix:**

```
# Validate user input
try:
    age = int(input("Age: "))
except ValueError:
    print("Please enter a number")

# Convert carefully
float_str = "12.5"
number = int(float(float_str))  # Convert to float first
```

## 

[​](https://python.datalumina.com/#keyerror)

KeyError

Happens when a dictionary key doesn’t exist:

```
user = {"name": "Alice", "age": 25}
print(user["email"])  # KeyError - no email key
```

**Fix:**

```
# Check if key exists
if "email" in user:
    print(user["email"])

# Use get() with default
email = user.get("email", "no-email@example.com")

# Or handle the error
try:
    print(user["email"])
except KeyError:
    print("Email not found")
```

## 

[​](https://python.datalumina.com/#indexerror)

IndexError

Happens when accessing invalid list position:

```
numbers = [1, 2, 3]
print(numbers[5])  # IndexError - only 3 items
```

**Fix:**

```
# Check length first
if len(numbers) > 5:
    print(numbers[5])

# Use negative indexing carefully
last_item = numbers[-1] if numbers else None

# Handle the error
try:
    print(numbers[5])
except IndexError:
    print("List too short")
```

## 

[​](https://python.datalumina.com/#typeerror)

TypeError

Happens when operations use wrong types:

```
# These cause TypeError
"hello" + 5            # Can't add string and number
len(42)                # Numbers don't have length
int([1, 2, 3])         # Can't convert list to int
```

**Fix:**

```
# Convert types explicitly
"hello" + str(5)       # "hello5"
str(42)                # "42"

# Check type first
if isinstance(value, str):
    print(len(value))
```

## 

[​](https://python.datalumina.com/#attributeerror)

AttributeError

Happens when accessing non-existent attributes:

```
text = "hello"
text.append("!")  # AttributeError - strings don't have append
```

**Fix:**

```
# Use correct methods
text = "hello"
text = text + "!"  # Strings are immutable

# Check if attribute exists
if hasattr(obj, 'append'):
    obj.append(item)
```

Error messages are your friends! They tell you:

- What went wrong (error type)
- Where it happened (file and line number)
- Why it happened (error message)

Always read the full error message before trying to fix it.

## 

[​](https://python.datalumina.com/#reading-error-messages)

Reading error messages

Python error messages show a “traceback”:

```
Traceback (most recent call last):
  File "script.py", line 5, in <module>
    result = 10 / 0
ZeroDivisionError: division by zero
```

Read from bottom to top:

1. **Error type**: `ZeroDivisionError`
2. **Error message**: `division by zero`
3. **Location**: `script.py`, line 5
4. **Code that failed**: `result = 10 / 0`

## 

[​](https://python.datalumina.com/#common-mistake-patterns)

Common mistake patterns

Off-by-one errors

```
# Wrong - lists start at 0
items = ["a", "b", "c"]
third_item = items[3]  # IndexError

# Right
third_item = items[2]  # "c"
```
Modifying while iterating

```
# Wrong - changes list size during iteration
numbers = [1, 2, 3, 4, 5]
for num in numbers:
    if num % 2 == 0:
        numbers.remove(num)  # Dangerous!

# Right - create new list
odd_numbers = [n for n in numbers if n % 2 != 0]
```
Mutable default arguments

```
# Wrong - same list for all calls!
def add_item(item, items=[]):
    items.append(item)
    return items

# Right - create new list each time
def add_item(item, items=None):
    if items is None:
        items = []
    items.append(item)
    return items
```

## 

[​](https://python.datalumina.com/#what’s-next)

What’s next?

Now that you understand error handling, let’s learn about classes - Python’s way of organizing code and data together.

## Classes

Object-oriented programming

[Suggest edits](https://github.com/daveebbelaar/python-course/edit/main/advanced/error-handling/common-errors.mdx)

[Try and except](https://python.datalumina.com/advanced/error-handling/try-except) [Classes](https://python.datalumina.com/advanced/classes)

⌘I
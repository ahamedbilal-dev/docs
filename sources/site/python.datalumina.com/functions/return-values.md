# Source: https://python.datalumina.com/functions/return-values

## 

[​](https://python.datalumina.com/#getting-results-from-functions)

Getting results from functions

So far, our functions have printed output. But often you want functions to calculate something and give you the result to use elsewhere.

```
# This function only prints
def add_print(a, b):
    print(a + b)

# This function returns a value
def add_return(a, b):
    return a + b

# Now you can use the result
result = add_return(5, 3)
print(f"The result is {result}")  # The result is 8
```

## 

[​](https://python.datalumina.com/#the-return-statement)

The return statement

Use `return` to send a value back from a function:

```
def calculate_area(width, height):
    area = width * height
    return area

# Store the returned value
room_area = calculate_area(10, 12)
print(f"Room size: {room_area} sq ft")  # Room size: 120 sq ft
```

When Python hits a `return` statement, it immediately exits the function. Any code after `return` won’t run.

## 

[​](https://python.datalumina.com/#using-returned-values)

Using returned values

Returned values can be used in many ways:

```
def double(number):
    return number * 2

# Store in variable
result = double(5)

# Use in expressions
total = double(5) + double(3)  # 10 + 6 = 16

# Pass to other functions
print(double(10))  # 20

# Use in conditions
if double(7) > 10:
    print("Big number!")
```

## 

[​](https://python.datalumina.com/#returning-multiple-values)

Returning multiple values

Python can return multiple values as a tuple:

```
def get_min_max(numbers):
    return min(numbers), max(numbers)

# Get both values
minimum, maximum = get_min_max([5, 2, 8, 1, 9])
print(f"Min: {minimum}, Max: {maximum}")  # Min: 1, Max: 9

# Or as a tuple
result = get_min_max([5, 2, 8, 1, 9])
print(result)  # (1, 9)
```

## 

[​](https://python.datalumina.com/#return-vs-print)

Return vs print

Understanding the difference is crucial:

```
def get_greeting_print(name):
    print(f"Hello, {name}!")  # Just displays

def get_greeting_return(name):
    return f"Hello, {name}!"  # Gives back value

# Can't use print version's output
message = get_greeting_print("Alice")  # Prints but returns None
print(message)  # None

# Can use return version's output
message = get_greeting_return("Alice")  # Returns the string
print(message.upper())  # HELLO, ALICE!
```

Use `return` when you need to use the result elsewhere. Use `print` when you just want to display information.

## 

[​](https://python.datalumina.com/#functions-without-return)

Functions without return

Functions without explicit `return` statements return `None`:

```
def greet(name):
    print(f"Hello, {name}!")
    # No return statement

result = greet("Alice")  # Prints: Hello, Alice!
print(result)  # None
```

## 

[​](https://python.datalumina.com/#common-mistakes)

Common mistakes

Forgetting to return

```
# Wrong - calculates but doesn't return
def calculate_total(items):
    total = sum(items)
    # Forgot return!

# Right
def calculate_total(items):
    total = sum(items)
    return total
```
Code after return

```
# Wrong - code after return never runs
def get_status():
    return "Done"
    print("This never prints!")  # Unreachable

# Right - return last
def get_status():
    print("Checking status...")
    return "Done"
```
Printing instead of returning

```
# Wrong - prints instead of returning
def multiply(a, b):
    print(a * b)

result = multiply(3, 4)  # Prints 12
total = result + 10      # Error! result is None

# Right - return the value
def multiply(a, b):
    return a * b
```

## 

[​](https://python.datalumina.com/#what’s-next)

What’s next?

Now that you know functions, let’s learn how to use external libraries and APIs to extend Python’s capabilities!

[**External tools**\\ \\ Use libraries and APIs](https://python.datalumina.com/libraries-apis/index)

[Suggest edits](https://github.com/daveebbelaar/python-course/edit/main/functions/return-values.mdx)

[Parameters](https://python.datalumina.com/functions/parameters) [External tools](https://python.datalumina.com/libraries-apis)

Ctrl+I
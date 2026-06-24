# Source: https://python.datalumina.com/functions/defining-functions

## 

[​](https://python.datalumina.com/#your-first-function)

Your first function

A function is a named block of code that performs a specific task. You define it once, then call it whenever you need that task done.

```
def greet():
    print("Hello, world!")
    print("Welcome to Python!")

# Call the function
greet()
```

## 

[​](https://python.datalumina.com/#function-syntax)

Function syntax

Every function follows this pattern:

```
def function_name():
    # Code goes here
    # Must be indented
    pass
```

Key parts:

- `def` - keyword that creates a function
- Function name followed by parentheses `()`
- Colon `:` to start the function body
- Indented code block (the function body)

## 

[​](https://python.datalumina.com/#naming-functions)

Naming functions

Follow these rules for function names:

- Use lowercase letters
- Separate words with underscores
- Be descriptive about what it does

```
# Good names
def calculate_total():
    pass

def send_email():
    pass

def validate_password():
    pass

# Bad names
def func1():  # Not descriptive
    pass

def Calculate():  # Should be lowercase
    pass
```

## 

[​](https://python.datalumina.com/#calling-functions)

Calling functions

To use a function, call it by name with parentheses:

```
def say_goodbye():
    print("Goodbye!")
    print("See you later!")

# Call it multiple times
say_goodbye()
say_goodbye()
say_goodbye()
```

The power of functions: write once, use many times. The above code prints 6 lines with just 3 function calls!

## 

[​](https://python.datalumina.com/#functions-with-logic)

Functions with logic

Functions can contain any Python code:

```
def check_weather():
    temperature = 25
    if temperature > 30:
        print("It's hot!")
    else:
        print("Nice weather!")

# Use the function
check_weather()
```

## 

[​](https://python.datalumina.com/#variable-scope-local-vs-global)

Variable scope: Local vs Global

Variables in Python have a “scope” - where they can be accessed and used.

### 

[​](https://python.datalumina.com/#local-variables)

Local variables

Variables created inside a function only exist within that function:

```
def calculate_price():
    price = 100
    tax = price * 0.1
    print(f"Total: {price + tax}")

calculate_price()  # Total: 110

# This fails - price doesn't exist outside the function
print(price)  # NameError: name 'price' is not defined
```

### 

[​](https://python.datalumina.com/#global-variables)

Global variables

Variables created outside functions can be accessed anywhere:

```
discount_rate = 0.15  # Global variable

def apply_discount(price):
    discount = price * discount_rate  # Can read global variable
    return price - discount

result = apply_discount(100)
print(result)  # 85.0
```

### 

[​](https://python.datalumina.com/#modifying-global-variables)

Modifying global variables

To change a global variable inside a function, use the `global` keyword:

```
counter = 0  # Global variable

def increment():
    global counter  # Declare we want to modify the global variable
    counter += 1

increment()
increment()
print(counter)  # 2
```

Avoid using `global` when possible. It makes code harder to understand and debug. Instead, pass values as parameters and return results.

### 

[​](https://python.datalumina.com/#best-practice-use-parameters-and-returns)

Best practice: Use parameters and returns

```
# Bad - using global variable
total = 0

def add_to_total(amount):
    global total
    total += amount

# Good - using parameters and return
def add_amounts(current_total, amount):
    return current_total + amount

total = 0
total = add_amounts(total, 10)
total = add_amounts(total, 20)
print(total)  # 30
```

When a local and global variable have the same name, the local variable “shadows” the global one inside the function. Python always uses the local version first.

## 

[​](https://python.datalumina.com/#common-mistakes)

Common mistakes

Forgetting parentheses when calling

```
# Wrong - this doesn't call the function
greet

# Right - parentheses are required
greet()
```
Forgetting the colon

```
# Wrong
def greet()
    print("Hello")

# Right
def greet():
    print("Hello")
```
Bad indentation

```
# Wrong - not indented
def greet():
print("Hello")

# Right - must indent function body
def greet():
    print("Hello")
```

## 

[​](https://python.datalumina.com/#what’s-next)

What’s next?

Functions become powerful when they can accept input. Let’s learn about parameters!

## Parameters

Pass data to functions

[Suggest edits](https://github.com/daveebbelaar/python-course/edit/main/functions/defining-functions.mdx)

[Functions](https://python.datalumina.com/functions) [Parameters](https://python.datalumina.com/functions/parameters)

⌘I
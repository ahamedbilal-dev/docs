# Source: https://python.datalumina.com/functions/parameters

## 

[​](https://python.datalumina.com/#what-are-parameters)

What are parameters?

Parameters let you pass data into functions. Instead of hardcoding values, you make functions flexible to work with different inputs.

```
# Without parameters (inflexible)
def greet_alice():
    print("Hello, Alice!")

# With parameters (flexible)
def greet(name):
    print(f"Hello, {name}!")

# Now it works for anyone
greet("Alice")
greet("Bob")
greet("Charlie")
```

## 

[​](https://python.datalumina.com/#basic-parameters)

Basic parameters

Add parameters inside the parentheses when defining a function:

```
def introduce(name, age):
    print(f"My name is {name}")
    print(f"I am {age} years old")

# Call with values
introduce("Alice", 25)
introduce("Bob", 30)
```

The values you pass when calling a function are called “arguments”. The variables in the function definition are “parameters”. Many people use these terms interchangeably.

## 

[​](https://python.datalumina.com/#multiple-parameters)

Multiple parameters

Functions can have multiple parameters:

```
def calculate_total(price, tax_rate, discount):
    tax = price * tax_rate
    final_price = price + tax - discount
    print(f"Total: ${final_price}")

# Order matters!
calculate_total(100, 0.08, 10)  # $98
```

## 

[​](https://python.datalumina.com/#default-values)

Default values

Give parameters default values for optional arguments:

```
def greet(name, greeting="Hello"):
    print(f"{greeting}, {name}!")

# Use default
greet("Alice")           # Hello, Alice!

# Override default
greet("Bob", "Hi")       # Hi, Bob!
greet("Charlie", "Hey")  # Hey, Charlie!
```

Put parameters with defaults at the end. Required parameters come first, optional ones last.

## 

[​](https://python.datalumina.com/#keyword-arguments)

Keyword arguments

Call functions using parameter names for clarity:

```
def create_profile(name, age, city):
    print(f"{name}, {age}, from {city}")

# Positional arguments (order matters)
create_profile("Alice", 25, "NYC")

# Keyword arguments (order doesn't matter)
create_profile(city="NYC", age=25, name="Alice")
create_profile(name="Bob", city="LA", age=30)
```

## 

[​](https://python.datalumina.com/#common-mistakes)

Common mistakes

Wrong number of arguments

```
def greet(name, age):
    print(f"Hi {name}, you're {age}")

# Wrong - too few arguments
greet("Alice")  # TypeError!

# Wrong - too many arguments
greet("Alice", 25, "NYC")  # TypeError!

# Right
greet("Alice", 25)
```
Default values with mutable objects

```
# Wrong - don't use lists as defaults
def add_item(item, list=[]):
    list.append(item)
    return list

# Right - use None and create new list
def add_item(item, list=None):
    if list is None:
        list = []
    list.append(item)
    return list
```

## 

[​](https://python.datalumina.com/#what’s-next)

What’s next?

Functions become truly powerful when they can return values. Let’s learn how!

## Return values

Get results from functions

[Suggest edits](https://github.com/daveebbelaar/python-course/edit/main/functions/parameters.mdx)

[Defining functions](https://python.datalumina.com/functions/defining-functions) [Return values](https://python.datalumina.com/functions/return-values)

⌘I
# Source: https://python.datalumina.com/basics/string-manipulation

## 

[​](https://python.datalumina.com/#working-with-text)

Working with text

Now that you know what strings are, let’s learn how to manipulate them. Python gives you powerful tools to work with text.

## 

[​](https://python.datalumina.com/#string-operations)

String operations

### 

[​](https://python.datalumina.com/#concatenation-joining)

Concatenation (joining)

```
first_name = "Jane"
last_name = "Doe"

# Using +
full_name = first_name + " " + last_name  # "Jane Doe"

# Using f-strings (modern Python way!)
greeting = f"Hello, {first_name}!"  # "Hello, Jane!"

# Multiple variables
age = 25
intro = f"I'm {first_name} and I'm {age} years old"
```

### 

[​](https://python.datalumina.com/#repetition)

Repetition

```
star = "*"
stars = star * 10  # "**********"

separator = "-" * 20  # "--------------------"
```

## 

[​](https://python.datalumina.com/#string-methods)

String methods

Python strings come with many built-in methods - functions you can call directly on any string. These methods let you transform text, search for patterns, and clean up data. The best part? You can often guess what they do from their names - `upper()` makes text uppercase, `replace()` replaces text, and so on.

### 

[​](https://python.datalumina.com/#changing-case)

Changing case

```
text = "Python Programming"

print(text.lower())      # "python programming"
print(text.upper())      # "PYTHON PROGRAMMING"
print(text.title())      # "Python Programming"
```

### 

[​](https://python.datalumina.com/#cleaning-strings)

Cleaning strings

```
messy = "  hello world  "
print(messy.strip())     # "hello world" (removes whitespace)

price = "$19.99"
print(price.strip("$"))  # "19.99"
```

### 

[​](https://python.datalumina.com/#finding-and-replacing)

Finding and replacing

```
message = "I love Python programming with Python"

# Check if something exists
print("Python" in message)        # True
print(message.startswith("I"))   # True
print(message.endswith("Python")) # True

# Find position
print(message.find("Python"))     # 7 (first occurrence)
print(message.count("Python"))    # 2 (number of times)

# Replace
new_message = message.replace("Python", "JavaScript")
print(new_message)  # "I love JavaScript programming with JavaScript"
```

Python has over 40 string methods! We’ve covered the most common ones here. For a complete list, check the [official Python documentation](https://docs.python.org/3/library/stdtypes.html#string-methods).

## 

[​](https://python.datalumina.com/#common-mistakes)

Common mistakes

Forgetting the f in f-strings

```
# Wrong
name = "Alice"
message = "Hello {name}"  # Prints: "Hello {name}"

# Right
message = f"Hello {name}"  # Prints: "Hello Alice"
```
Wrong quotes in strings

```
# Wrong - mismatched quotes
text = 'It's Python'

# Right - escape or use different quotes
text = "It's Python"  # Double quotes outside
text = 'It\'s Python'  # Escape the apostrophe
```

## 

[​](https://python.datalumina.com/#what’s-next)

What’s next?

You’ve mastered working with data! Ready to make your programs smart with decision-making?

## Control flow

Learn if statements and loops

[Suggest edits](https://github.com/daveebbelaar/python-course/edit/main/basics/string-manipulation.mdx)

[Operators](https://python.datalumina.com/basics/operators) [Control flow](https://python.datalumina.com/control-flow)

⌘I
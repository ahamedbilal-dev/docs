# Source: https://python.datalumina.com/data-types

## 

[​](https://python.datalumina.com/#what-are-data-types)

What are data types?

Just like in real life, Python works with different kinds of information. You can’t add someone’s name to their age - they’re different types of data. Python has four main data types you’ll use constantly:

- **Numbers** for counting and calculations
- **Text** for words and messages
- **True/False** for decisions

Each type has its own rules and abilities. Let’s explore them.

## 

[​](https://python.datalumina.com/#the-main-types)

The main types

## Numbers

Integers and decimals for math

## Strings

Text, words, and characters

## Booleans

True or False values

## 

[​](https://python.datalumina.com/#why-we-need-data-types)

Why we need data types

Python needs to know what type of data you’re working with:

```
# Numbers can do math
total = 10 + 5  # 15

# Strings combine differently  
name = "Hello" + "World"  # "HelloWorld"

# Can't mix without converting
# age = "25" + 5  # Error!
age = int("25") + 5  # 30 (converted string to number)
```

## 

[​](https://python.datalumina.com/#checking-types)

Checking types

You can always check what type something is with `type()`:

```
# Check different types
print(type(42))          # <class 'int'>
print(type(3.14))        # <class 'float'>
print(type("Hello"))     # <class 'str'>
print(type(True))        # <class 'bool'>

# Check variables
age = 25
name = "Alice"
print(type(age))         # <class 'int'>
print(type(name))        # <class 'str'>
```

## 

[​](https://python.datalumina.com/#start-learning)

Start learning

Pick a data type to explore - numbers are a great place to start!

## Learn about numbers

Integers and floats

[Suggest edits](https://github.com/daveebbelaar/python-course/edit/main/data-types/index.mdx)

[Comments](https://python.datalumina.com/basics/comments) [Numbers](https://python.datalumina.com/data-types/numbers)

⌘I
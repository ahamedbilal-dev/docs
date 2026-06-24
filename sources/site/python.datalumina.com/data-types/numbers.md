# Source: https://python.datalumina.com/data-types/numbers

## 

[​](https://python.datalumina.com/#two-types-of-numbers)

Two types of numbers

Python has two ways to store numbers: **Integers** - Whole numbers without decimals

```
age = 25
score = -10
```

**Floats** - Numbers with decimal points

```
price = 19.99
temperature = -5.5
pi = 3.14159
```

Python uses a dot (.) for decimals, not a comma. Writing `3,14` creates a tuple, not the number 3.14!

## 

[​](https://python.datalumina.com/#why-two-types)

Why two types?

Python separates integers and floats for efficiency - computers can work with whole numbers faster and more precisely. But here’s the reassuring part: in practice, you rarely need to think about this. Python handles the conversion automatically when needed, and most of the time you’ll just use whatever makes sense - whole numbers for counting things, decimals for measurements and calculations.

## 

[​](https://python.datalumina.com/#basic-math-operations)

Basic math operations

Numbers work just like a calculator:

```
# Addition and subtraction
total = 10 + 5     # 15
change = 20 - 7    # 13

# Multiplication and division
area = 6 * 4       # 24
half = 10 / 2      # 5.0 (always returns float)

# Powers
squared = 5 ** 2   # 25
cubed = 2 ** 3     # 8
```

## 

[​](https://python.datalumina.com/#integer-vs-float-division)

Integer vs float division

Division has two forms:

```
# Regular division (always float)
result = 10 / 3    # 3.333...

# Integer division (rounds down)
result = 10 // 3   # 3
```

These are just the basics! Python can solve complex math problems too. When you need square roots, trigonometry, or advanced calculations, ask AI to help with the specific syntax - no need to memorize every math symbol right now.

## 

[​](https://python.datalumina.com/#common-mistakes)

Common mistakes

Division always returns float

```
# Even when dividing evenly
result = 10 / 2
print(result)       # 5.0 (not 5)
print(type(result)) # <class 'float'>

# Use // for integer result
result = 10 // 2    # 5
```
Can't use commas in numbers

```
# Wrong
million = 1,000,000  # Creates a tuple, not a number!

# Right
million = 1000000    # Hard to read
million = 1_000_000  # Python style
```

## 

[​](https://python.datalumina.com/#what’s-next)

What’s next?

Now let’s learn about working with text in Python!

## Strings

Text and characters

[Suggest edits](https://github.com/daveebbelaar/python-course/edit/main/data-types/numbers.mdx)

[Data types](https://python.datalumina.com/data-types) [Strings](https://python.datalumina.com/data-types/strings)

⌘I
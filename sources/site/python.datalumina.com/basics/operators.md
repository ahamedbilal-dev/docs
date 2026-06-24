# Source: https://python.datalumina.com/basics/operators

## 

[​](https://python.datalumina.com/#what-are-operators)

What are operators?

Operators are symbols that perform operations on values. Think of them as the “verbs” of programming - they make things happen! You already know most operators from math class:

- Calculate: `+`, `-`, `*`, `/`
- Compare: `>`, `<`, `==`
- Combine: `and`, `or`, `not`

## 

[​](https://python.datalumina.com/#arithmetic-operators)

Arithmetic operators

These work just like your calculator:

```
# Basic math
print(10 + 3)   # 13 - Addition
print(10 - 3)   # 7  - Subtraction
print(10 * 3)   # 30 - Multiplication
print(10 / 3)   # 3.333... - Division (always gives float)

# Special operators
print(10 // 3)  # 3  - Floor division (rounds down)
print(10 % 3)   # 1  - Modulo (remainder)
print(10 ** 3)  # 1000 - Exponent (power)
```

### 

[​](https://python.datalumina.com/#order-of-operations)

Order of operations

Python follows math rules (PEMDAS):

```
result = 2 + 3 * 4      # 14 (not 20!)
result = (2 + 3) * 4    # 20 (parentheses first)
```

## 

[​](https://python.datalumina.com/#comparison-operators)

Comparison operators

These compare values and return True or False:

```
age = 18

print(age == 18)    # True  - Equal to
print(age != 21)    # True  - Not equal to
print(age > 17)     # True  - Greater than
print(age < 20)     # True  - Less than
print(age >= 18)    # True  - Greater than or equal
print(age <= 18)    # True  - Less than or equal
```

Don’t confuse `=` (assignment) with `==` (comparison)!

- `age = 18` stores 18 in age
- `age == 18` checks if age equals 18

## 

[​](https://python.datalumina.com/#logical-operators)

Logical operators

These combine boolean values and conditions:

```
age = 25
has_license = True

# AND - both must be true
can_drive = age >= 16 and has_license
print(can_drive)  # True

# OR - at least one must be true
day = "Saturday"
is_weekend = day == "Saturday" or day == "Sunday"
print(is_weekend)  # True

# NOT - reverses the value
is_adult = age >= 18
is_child = not is_adult
print(is_child)  # False
```

### 

[​](https://python.datalumina.com/#truth-tables)

Truth tables

Understanding how `and`, `or`, and `not` work:

```
# AND: Both must be True
print(True and True)    # True
print(True and False)   # False
print(False and False)  # False

# OR: At least one must be True  
print(True or False)    # True
print(False or False)   # False

# NOT: Flips the value
print(not True)         # False
print(not False)        # True
```

## 

[​](https://python.datalumina.com/#assignment-shortcuts)

Assignment shortcuts

These shortcuts update variables in place:

```
# Instead of:
score = score + 10

# Write:
score += 10

# Works with all operators
x = 10
x += 5    # x is now 15
x *= 2    # x is now 30
```

## 

[​](https://python.datalumina.com/#common-mistakes)

Common mistakes

Division always returns float

```
# Regular division
result = 10 / 2    # 5.0 (not 5)

# Integer division
result = 10 // 2   # 5
```
Order of operations

```
# Wrong
average = 10 + 20 + 30 / 3  # 40.0

# Right
average = (10 + 20 + 30) / 3  # 20.0
```
Confusing = and ==

```
# = assigns a value
age = 18

# == compares values
if age == 18:
    print("Just turned adult!")
```

## 

[​](https://python.datalumina.com/#what’s-next)

What’s next?

You know operators! Let’s dive deeper into working with text strings.

## String manipulation

Advanced text operations

[Suggest edits](https://github.com/daveebbelaar/python-course/edit/main/basics/operators.mdx)

[Booleans](https://python.datalumina.com/data-types/booleans) [String manipulation](https://python.datalumina.com/basics/string-manipulation)

⌘I
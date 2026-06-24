# Source: https://python.datalumina.com/data-types/booleans

## 

[​](https://python.datalumina.com/#what-are-booleans)

What are booleans?

Booleans are the simplest data type - they can only be `True` or `False`. Think of them as yes/no answers.

```
is_logged_in = True
is_admin = False
has_permission = True
```

Boolean values are `True` and `False` with capital letters. Using `true` or `false` will cause an error!

## 

[​](https://python.datalumina.com/#creating-booleans)

Creating booleans

Booleans often come from comparisons:

```
# Direct assignment
is_ready = True

# From comparisons
age = 18
can_vote = age >= 18  # True

score = 75
passed = score > 60   # True
```

## 

[​](https://python.datalumina.com/#comparison-operators)

Comparison operators

These operators compare values and return `True` or `False`:

```
age = 25

# Equality
print(age == 25)     # True - equals
print(age != 30)     # True - not equals

# Greater/Less than
print(age > 20)      # True - greater than
print(age < 30)      # True - less than
print(age >= 25)     # True - greater or equal
print(age <= 25)     # True - less or equal
```

Remember: `=` assigns a value, while `==` compares values. This is a common source of bugs!

## 

[​](https://python.datalumina.com/#common-mistakes)

Common mistakes

Wrong capitalization

```
# Wrong
is_ready = true   # NameError!
is_done = TRUE    # NameError!

# Right
is_ready = True
is_done = False
```
Using = instead of ==

```
# Wrong - this assigns, not compares!
if is_logged_in = True:
    print("Welcome")

# Right - but redundant
if is_logged_in == True:
    print("Welcome")
    
# Best - booleans are already True/False
if is_logged_in:
    print("Welcome")
```

## 

[​](https://python.datalumina.com/#what’s-next)

What’s next?

Now that you understand data types, let’s learn how to work with them using operators!

[**Operators**\\ \\ Math, comparisons, and more](https://python.datalumina.com/basics/operators)

[Suggest edits](https://github.com/daveebbelaar/python-course/edit/main/data-types/booleans.mdx)

[Strings](https://python.datalumina.com/data-types/strings) [Operators](https://python.datalumina.com/basics/operators)

Ctrl+I
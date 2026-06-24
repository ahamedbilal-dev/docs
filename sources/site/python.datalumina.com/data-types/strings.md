# Source: https://python.datalumina.com/data-types/strings

## 

[​](https://python.datalumina.com/#what-are-strings)

What are strings?

Strings are text - any characters inside quotes. Python doesn’t care if you use single or double quotes, just be consistent.

```
name = "Alice"
message = 'Hello, World!'
```

## 

[​](https://python.datalumina.com/#creating-strings)

Creating strings

Three ways to make strings:

```
# Single quotes
first = 'Python'

# Double quotes  
second = "Python"

# Triple quotes for multiple lines
paragraph = """This is
a multi-line
string"""
```

Use double quotes when your text contains apostrophes: `"It's Python!"`

## 

[​](https://python.datalumina.com/#combining-strings)

Combining strings

Join strings together with `+`:

```
first_name = "John"
last_name = "Doe"

# Concatenation
full_name = first_name + " " + last_name
print(full_name)  # John Doe

# Repetition
stars = "*" * 5
print(stars)  # *****
```

## 

[​](https://python.datalumina.com/#string-length)

String length

Use `len()` to count characters:

```
message = "Hello"
print(len(message))  # 5

empty = ""
print(len(empty))    # 0
```

## 

[​](https://python.datalumina.com/#converting-to-string)

Converting to string

Turn other types into strings with `str()`:

```
age = 25
message = "I am " + str(age) + " years old"
print(message)  # I am 25 years old

# Or use f-strings (we'll learn more later)
message = f"I am {age} years old"
```

## 

[​](https://python.datalumina.com/#common-mistakes)

Common mistakes

Mixing quotes

```
# Wrong - mismatched quotes
text = "Hello'

# Right - matching quotes
text = "Hello"
text = 'Hello'
```
Can't add strings and numbers

```
# Wrong
result = "Age: " + 25  # TypeError!

# Right - convert number first
result = "Age: " + str(25)
```
Forgetting quotes entirely

```
# Wrong
name = Alice  # Python looks for variable Alice

# Right  
name = "Alice"  # String literal
```

## 

[​](https://python.datalumina.com/#what’s-next)

What’s next?

Let’s explore True/False values - essential for making decisions in your code!

## Booleans

True and False values

[Suggest edits](https://github.com/daveebbelaar/python-course/edit/main/data-types/strings.mdx)

[Numbers](https://python.datalumina.com/data-types/numbers) [Booleans](https://python.datalumina.com/data-types/booleans)

⌘I
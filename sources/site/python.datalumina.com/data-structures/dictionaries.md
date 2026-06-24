# Source: https://python.datalumina.com/data-structures/dictionaries

## 

[​](https://python.datalumina.com/#what-are-dictionaries)

What are dictionaries?

Dictionaries store data in key-value pairs. Think of them like a real dictionary where you look up a word (key) to find its definition (value). Real-world examples:

- Phone book: name > phone number
- Menu: dish > price
- User profile: username > user info

## 

[​](https://python.datalumina.com/#creating-dictionaries)

Creating dictionaries

```
# Empty dictionary
my_dict = {}

# Dictionary with data
person = {
    "name": "Alice",
    "age": 30,
    "city": "New York"
}

# Different ways to create
scores = dict(math=95, english=87, science=92)
```

Dictionaries use curly braces `{}` with key-value pairs separated by colons. Keys must be unique!

## 

[​](https://python.datalumina.com/#accessing-values)

Accessing values

```
person = {"name": "Alice", "age": 30, "city": "New York"}

# Get values by key
print(person["name"])       # "Alice"
print(person["age"])        # 30

# Safer with get()
print(person.get("job"))    # None (no error)
print(person.get("job", "Unknown"))  # "Unknown" (default)
```

## 

[​](https://python.datalumina.com/#changing-dictionaries)

Changing dictionaries

```
person = {"name": "Alice", "age": 30}

# Add or update
person["email"] = "alice@email.com"  # Add new
person["age"] = 31                   # Update existing

# Remove items
del person["email"]              # Remove by key
age = person.pop("age")          # Remove and return
person.clear()                   # Remove all items
```

## 

[​](https://python.datalumina.com/#dictionary-methods)

Dictionary methods

```
person = {"name": "Alice", "age": 30, "city": "New York"}

# Get all keys, values, or items
print(person.keys())    # dict_keys(['name', 'age', 'city'])
print(person.values())  # dict_values(['Alice', 30, 'New York'])
print(person.items())   # dict_items([('name', 'Alice'), ...])

# Check if key exists
if "name" in person:
    print("Name found!")

# Update multiple values
person.update({"age": 31, "job": "Engineer"})
```

### 

[​](https://python.datalumina.com/#nested-dictionaries)

Nested dictionaries

```
# Dictionary of dictionaries
students = {
    "alice": {"age": 20, "grade": "A"},
    "bob": {"age": 21, "grade": "B"},
    "charlie": {"age": 19, "grade": "A"}
}

# Access nested data
print(students["alice"]["grade"])  # "A"
```

## 

[​](https://python.datalumina.com/#common-mistakes)

Common mistakes

KeyError when key doesn't exist

```
# Wrong
person = {"name": "Alice"}
print(person["age"])  # KeyError!

# Right - use get()
print(person.get("age", 0))  # Returns 0 if missing
```
Using mutable keys

```
# Wrong - lists can't be keys
bad_dict = {[1, 2]: "value"}  # TypeError!

# Right - use immutable types
good_dict = {(1, 2): "value"}  # Tuple is OK
good_dict = {"1,2": "value"}   # String is OK
```

## 

[​](https://python.datalumina.com/#what’s-next)

What’s next?

Let’s explore tuples - like lists but unchangeable!

[**Tuples**\\ \\ Immutable sequences](https://python.datalumina.com/data-structures/tuples)

[Suggest edits](https://github.com/daveebbelaar/python-course/edit/main/data-structures/dictionaries.mdx)

[Lists](https://python.datalumina.com/data-structures/lists) [Tuples](https://python.datalumina.com/data-structures/tuples)

Ctrl+I
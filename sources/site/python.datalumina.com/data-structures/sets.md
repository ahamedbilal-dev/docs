# Source: https://python.datalumina.com/data-structures/sets

## 

[​](https://python.datalumina.com/#what-are-sets)

What are sets?

Sets are collections that only store unique values. They automatically remove duplicates. Think of sets like:

- A bag of unique marbles
- Guest list (each person once)
- Unique tags or categories

## 

[​](https://python.datalumina.com/#creating-sets)

Creating sets

You can create sets two ways: with `set()` or with curly braces `{}` (but only when it has values).

```
# Empty set (careful!)
empty_set = set()  # NOT {} - that's a dict!

# Set with values - both ways work
numbers = {1, 2, 3, 4, 5}
fruits = set(["apple", "banana", "orange"])

# From a list (removes duplicates)
scores = [85, 90, 85, 92, 90]
unique_scores = set(scores)  # {85, 90, 92}
```

Use `set()` for empty sets, not `{}`. Empty curly braces create a dictionary!

## 

[​](https://python.datalumina.com/#basic-operations)

Basic operations

```
colors = {"red", "blue"}

# Add items
colors.add("green")
print(colors)  # {'red', 'blue', 'green'}

# Remove items
colors.remove("blue")    # Error if not found
colors.discard("yellow") # No error if not found

# Check membership
if "red" in colors:
    print("Red is available")
```

## 

[​](https://python.datalumina.com/#common-uses)

Common uses

### 

[​](https://python.datalumina.com/#remove-duplicates)

Remove duplicates

```
names = ["Alice", "Bob", "Alice", "Charlie", "Bob"]
unique_names = list(set(names))
print(unique_names)  # ['Alice', 'Bob', 'Charlie']
```

### 

[​](https://python.datalumina.com/#fast-membership-testing)

Fast membership testing

```
allowed_users = {"alice", "bob", "charlie"}

if "alice" in allowed_users:  # Very fast!
    print("Access granted")
```

## 

[​](https://python.datalumina.com/#common-mistakes)

Common mistakes

Empty set syntax

```
# Wrong - creates empty dict
empty = {}

# Right - use set()
empty = set()
```
Sets are unordered

```
# Order is not guaranteed!
numbers = {3, 1, 4, 1, 5}
print(numbers)  # Could be any order

# Use list if order matters
ordered = [3, 1, 4, 1, 5]
```

## 

[​](https://python.datalumina.com/#what’s-next)

What’s next?

Congratulations! You’ve completed Python Basics. Ready to start building programs?

## Building Programs

Learn about functions

[Suggest edits](https://github.com/daveebbelaar/python-course/edit/main/data-structures/sets.mdx)

[Tuples](https://python.datalumina.com/data-structures/tuples)

⌘I
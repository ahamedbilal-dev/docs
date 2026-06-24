# Source: https://python.datalumina.com/data-structures/tuples

## 

[​](https://python.datalumina.com/#what-are-tuples)

What are tuples?

Tuples are like lists, but they can’t be changed once created. They’re immutable (unchangeable) sequences. Use tuples for data that shouldn’t change:

- Coordinates (x, y)
- RGB colors (255, 0, 0)
- Database records
- Function return values

## 

[​](https://python.datalumina.com/#creating-tuples)

Creating tuples

```
# Empty tuple
empty = ()

# Tuple with items
point = (3, 5)
colors = ("red", "green", "blue")

# Single item tuple needs comma!
single = (42,)  # Note the comma
not_tuple = (42)  # This is just 42 in parentheses

# Without parentheses (implicit)
coordinates = 10, 20
```

A single-item tuple needs a comma: `(42,)` not `(42)`. Without the comma, Python thinks it’s just parentheses around a number!

## 

[​](https://python.datalumina.com/#accessing-items)

Accessing items

Just like lists, tuples use indexing:

```
point = (3, 5)
colors = ("red", "green", "blue")

# Get items
print(point[0])      # 3
print(colors[-1])    # "blue"

# Slicing works too
print(colors[0:2])   # ("red", "green")
```

## 

[​](https://python.datalumina.com/#tuple-unpacking)

Tuple unpacking

Python’s coolest tuple feature:

```
# Unpack values
point = (3, 5)
x, y = point  # x = 3, y = 5

# Multiple assignment
a, b, c = 1, 2, 3  # Same as (1, 2, 3)

# Swap variables elegantly
x, y = y, x  # Swaps values!
```

## 

[​](https://python.datalumina.com/#common-mistakes)

Common mistakes

Forgetting comma in single tuple

```
# Wrong - not a tuple
single = (42)
print(type(single))  # <class 'int'>

# Right - include comma
single = (42,)
print(type(single))  # <class 'tuple'>
```
Trying to modify tuples

```
# Wrong - tuples are immutable
point = (3, 5)
point[0] = 4  # TypeError!

# Right - create a new tuple
point = (4, point[1])
# Or convert to list, modify, convert back
temp = list(point)
temp[0] = 4
point = tuple(temp)
```

## 

[​](https://python.datalumina.com/#what’s-next)

What’s next?

Finally, let’s explore sets - collections of unique items!

## Sets

Unique collections

[Suggest edits](https://github.com/daveebbelaar/python-course/edit/main/data-structures/tuples.mdx)

[Dictionaries](https://python.datalumina.com/data-structures/dictionaries) [Sets](https://python.datalumina.com/data-structures/sets)

⌘I
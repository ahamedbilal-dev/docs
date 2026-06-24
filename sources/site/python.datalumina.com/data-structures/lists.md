# Source: https://python.datalumina.com/data-structures/lists

## 

[​](https://python.datalumina.com/#what-are-lists)

What are lists?

Lists are Python’s most versatile data structure. They’re like containers that can hold multiple items in a specific order. Think of a list like:

- A shopping list (milk, eggs, bread)
- A to-do list (tasks in order)
- A playlist (songs in sequence)

## 

[​](https://python.datalumina.com/#creating-lists)

Creating lists

```
# Empty list
my_list = []

# List with items
fruits = ["apple", "banana", "orange"]
numbers = [1, 2, 3, 4, 5]
mixed = ["hello", 42, True, 3.14]  # Different types OK!
```

Lists use square brackets `[]` and items are separated by commas. You can mix different data types in the same list!

## 

[​](https://python.datalumina.com/#accessing-items)

Accessing items

Lists are indexed starting at 0:

```
fruits = ["apple", "banana", "orange"]

# Get items
print(fruits[0])    # "apple" (first item)
print(fruits[1])    # "banana"
print(fruits[-1])   # "orange" (last item)
print(fruits[-2])   # "banana" (second to last)

# Slicing
print(fruits[0:2])  # ["apple", "banana"]
print(fruits[1:])   # ["banana", "orange"]
```

## 

[​](https://python.datalumina.com/#changing-lists)

Changing lists

Lists are mutable - you can change them:

```
fruits = ["apple", "banana", "orange"]

# Change an item
fruits[0] = "mango"
print(fruits)  # ["mango", "banana", "orange"]

# Add items
fruits.append("grape")      # Add to end
fruits.insert(1, "kiwi")    # Insert at position

# Remove items
fruits.remove("banana")     # Remove by value
last = fruits.pop()        # Remove and return last
del fruits[0]              # Remove by index
```

## 

[​](https://python.datalumina.com/#list-methods)

List methods

```
numbers = [3, 1, 4, 1, 5, 9]

# Information
print(len(numbers))         # 6 (length)
print(numbers.count(1))     # 2 (count occurrences)
print(numbers.index(4))     # 2 (find position)

# Sorting
numbers.sort()              # Sort in place
print(numbers)              # [1, 1, 3, 4, 5, 9]

numbers.reverse()           # Reverse order
print(numbers)              # [9, 5, 4, 3, 1, 1]

# Copy
new_list = numbers.copy()   # Create a copy
```

## 

[​](https://python.datalumina.com/#checking-lists)

Checking lists

```
fruits = ["apple", "banana", "orange"]

# Check if item exists
if "apple" in fruits:
    print("Found apple!")

# Check if list is empty
if fruits:
    print("List has items")
else:
    print("List is empty")
```

## 

[​](https://python.datalumina.com/#common-mistakes)

Common mistakes

Index out of range

```
# Wrong
fruits = ["apple", "banana"]
print(fruits[2])  # IndexError!

# Right - check length first
if len(fruits) > 2:
    print(fruits[2])
```
Modifying while looping

```
# Wrong - changes list size during loop
numbers = [1, 2, 3, 4]
for num in numbers:
    if num == 2:
        numbers.remove(num)  # Dangerous!

# Right - use list comprehension
numbers = [num for num in numbers if num != 2]
```
Shallow copy issues

```
# Wrong - both variables point to same list
list1 = [1, 2, 3]
list2 = list1
list2.append(4)
print(list1)  # [1, 2, 3, 4] - changed!

# Right - make a copy
list1 = [1, 2, 3]
list2 = list1.copy()
list2.append(4)
print(list1)  # [1, 2, 3] - unchanged
```

## 

[​](https://python.datalumina.com/#what’s-next)

What’s next?

Now let’s learn about dictionaries - perfect for storing related information!

[**Dictionaries**\\ \\ Key-value pairs](https://python.datalumina.com/data-structures/dictionaries)

[Suggest edits](https://github.com/daveebbelaar/python-course/edit/main/data-structures/lists.mdx)

[Data structures](https://python.datalumina.com/data-structures) [Dictionaries](https://python.datalumina.com/data-structures/dictionaries)

Ctrl+I
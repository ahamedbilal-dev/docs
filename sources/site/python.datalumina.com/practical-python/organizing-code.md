# Source: https://python.datalumina.com/practical-python/organizing-code

## 

[​](https://python.datalumina.com/#why-organize-your-code)

Why organize your code?

As your scripts grow, they become harder to read and maintain. The solution? Split your code into functions and separate files. Benefits:

- **Reusable** - Write once, use many times
- **Readable** - Main script stays simple and clear
- **Testable** - Easy to test individual functions

## 

[​](https://python.datalumina.com/#creating-helper-functions)

Creating helper functions

Let’s create simple helper functions for our sales analysis. In your `sales-analysis` folder, create a new file called `helpers.py`:

```
# helpers.py

def calculate_total(quantity, price):
    """Calculate total for a single item"""
    return quantity * price

def format_currency(amount):
    """Format number as currency"""
    return f"${amount:,.2f}"
```

The `:.2f` in the format string rounds floating point numbers to 2 decimal places - perfect for displaying money!

That’s it! Two simple functions that do one thing each.

## 

[​](https://python.datalumina.com/#using-your-functions)

Using your functions

Now update `analyzer.py` to use these helpers:

```
# analyzer.py
import pandas as pd
from helpers import calculate_total, format_currency

# Read data
df = pd.read_csv('data/sales.csv')

# Calculate total for each row
totals = []
for index, row in df.iterrows():
    total = calculate_total(row['quantity'], row['price'])
    totals.append(total)

# Add totals to our data
df['total'] = totals

# Display with formatted totals
print("Sales Data:")
for index, row in df.iterrows():
    formatted_total = format_currency(row['total'])
    print(f"{row['product']}: {formatted_total}")

# Show grand total
grand_total = df['total'].sum()
formatted_grand_total = format_currency(grand_total)
print(f"\nGrand Total: {formatted_grand_total}")
```

## 

[​](https://python.datalumina.com/#how-imports-work)

How imports work

When you write `from helpers import calculate_total`:

1. Python looks for `helpers.py` in the same folder
2. It runs that file and makes the functions available
3. You can now use `calculate_total()` directly

The file must be in the same folder for this simple import to work. We covered more complex imports in the Python paths section.

## 

[​](https://python.datalumina.com/#what-you’ve-accomplished)

What you’ve accomplished

Look at what you’ve built! You started with a single Python file and now have:

- An organized project structure
- Understanding of how Python finds files
- Code that reads real data and saves results
- Reusable functions in separate files

This is how real Python projects work. You’re ready to build bigger things!

## Learn error handling

Handle errors gracefully in your code

[Suggest edits](https://github.com/daveebbelaar/python-course/edit/main/practical-python/organizing-code.mdx)

[Working with files](https://python.datalumina.com/practical-python/working-with-files) [Error handling](https://python.datalumina.com/advanced/error-handling)

⌘I
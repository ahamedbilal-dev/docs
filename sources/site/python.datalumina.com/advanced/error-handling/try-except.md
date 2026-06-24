# Source: https://python.datalumina.com/advanced/error-handling/try-except

## 

[​](https://python.datalumina.com/#basic-try-except-structure)

Basic try-except structure

The `try` block contains code that might fail. The `except` block runs if an error happens:

```
try:
    # Code that might cause an error
    risky_operation()
except:
    # Code that runs if there's an error
    print("Something went wrong")
```

## 

[​](https://python.datalumina.com/#catching-specific-errors)

Catching specific errors

Different errors need different handling. Catch specific error types:

```
try:
    age = int(input("Enter your age: "))
    print(f"In 10 years, you'll be {age + 10}")
except ValueError:
    print("Please enter a number")
```

## 

[​](https://python.datalumina.com/#multiple-error-types)

Multiple error types

Handle different errors differently:

```
try:
    # Read a number from a file
    with open('number.txt', 'r') as f:
        text = f.read()
    number = int(text)
    result = 100 / number
    print(f"Result: {result}")
except FileNotFoundError:
    print("Could not find number.txt")
except ValueError:
    print("File doesn't contain a valid number")
except ZeroDivisionError:
    print("Cannot divide by zero")
```

## 

[​](https://python.datalumina.com/#the-else-clause)

The else clause

Code in `else` runs only if no error happened:

```
try:
    with open('data.txt', 'r') as f:
        data = f.read()
except FileNotFoundError:
    print("File not found")
else:
    # This only runs if the file was opened successfully
    print(f"File has {len(data)} characters")
```

## 

[​](https://python.datalumina.com/#the-finally-clause)

The finally clause

Code in `finally` always runs, error or not:

```
try:
    file = open('data.txt', 'r')
    data = file.read()
except FileNotFoundError:
    print("File not found")
finally:
    # This always runs to clean up
    if 'file' in locals() and not file.closed:
        file.close()
    print("Cleanup complete")
```

Don’t catch all errors with a bare `except:`. It hides problems and makes debugging harder. Always catch specific error types when possible.

## 

[​](https://python.datalumina.com/#common-mistakes)

Common mistakes

Catching too broad exceptions

```
# Bad - catches everything
try:
    process_data()
except:
    pass  # Silent failure!

# Good - specific error
try:
    process_data()
except ValueError:
    print("Invalid data format")
```
Empty except blocks

```
# Bad - ignores the error
try:
    risky_operation()
except ValueError:
    pass

# Good - at least log it
try:
    risky_operation()
except ValueError:
    print("Warning: Invalid value encountered")
```
Not re-raising critical errors

```
# Bad - hides all errors
try:
    critical_operation()
except Exception as e:
    print(f"Error: {e}")

# Good - log and re-raise
try:
    critical_operation()
except Exception as e:
    print(f"Critical error: {e}")
    raise  # Let the error propagate
```

## 

[​](https://python.datalumina.com/#what’s-next)

What’s next?

Now let’s look at the most common errors you’ll encounter in Python.

## Common errors

Errors you’ll see often

[Suggest edits](https://github.com/daveebbelaar/python-course/edit/main/advanced/error-handling/try-except.mdx)

[Error handling](https://python.datalumina.com/advanced/error-handling) [Common errors](https://python.datalumina.com/advanced/error-handling/common-errors)

⌘I